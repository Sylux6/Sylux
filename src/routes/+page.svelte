<script>
  import { base } from "$app/paths";
  import ProfileImage from "$lib/images/profile.jpg"

  let showMenu = false;
</script>

<main class="main">
  <section class="profile">
    <div class="header">
      <img src={ProfileImage} alt="profile">

      <button class="btn" on:click={() => showMenu = !showMenu}>
        <i
          class="fa-solid fa-2xl"
          class:fa-bars={!showMenu}
          class:fa-xmark={showMenu}
        ></i>
      </button>
    </div>

    <div class="name">Sylux</div>

    <div class="title">Illustration</div>
  </section>

  <section class="content"></section>
</main>

<style>
  .main {
    height: 100%;
  }

  .header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-content: flex-start;
  }

  .btn {
    cursor: pointer;
    background: unset;
    border: unset;
    height: fit-content;
  }

  .profile {
    padding: 20px;
    display: flex;
    flex-direction: column;
    gap: 5px;
  }

  .name {
    position: relative;
    left: 20px;
    font-size: 24px;
  }

  .title {
    position: relative;
    left: 20px;
  }

  img {
    border-radius: 50%;
    border: 5px solid pink;
  }

  img:hover {
    filter: brightness(50%);
  }

  .content {
    flex: 1;
  }

  @media screen and (max-width: 1440px) {
    .main {
      display: flex;
      flex-direction: column;
    }
  }

  @media screen and (min-width: 1440px) {
    .main {
      display: flex;
      flex-direction: row;
    }

    .btn {
      display: none;
    }
  }
</style>