<template>
  <div id="app" class="bg-black h-screen w-screen">
    <div
      id="nav"
      class="bg-black flex justify-between items-center m-0 border-b-2 border-gray-900"
    >
      <div class="flex items-center">
        <a href="#"> <img src="images/youtubelogo.png" alt="logo" /> </a>
      </div>
      <div class="flex">
        <nav class="flex mr-0 h-12 items-center">
          <router-link to="/">Home</router-link>
          <router-link to="/explore">Explore </router-link>
          <router-link to="/library">Library</router-link>
        </nav>
        <!-- Bring search icon from fontawesome -->
        <div class="items-center py-2 search cursor-pointer">
          <span class="flex items-center ">
            <div class="items-center">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="rgba(255, 255, 255, 0.5)"
                width="24px"
                height="24px"
              >
                <path d="M0 0h24v24H0z" fill="none" />
                <path
                  d="M15.5 14h-.79l-.28-.27C15.41 12.59 16 11.11 16 9.5 16 5.91 13.09 3 9.5 3S3 5.91 3 9.5 5.91 16 9.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"
                />
              </svg>
            </div>
            Search
          </span>
        </div>
      </div>
      <a class="flex lg:ml-4 items-center cursor-pointer">
        <img
          class=" rounded-full w-6 h-6 "
          src="images/user_profile_picture.jpg"
          alt="user_profile_picture"
        />
      </a>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,500;1,500&display=swap");
@import url("https://fonts.googleapis.com/css?family=YT+Sans:500,700");
#app {
  font-family: "Roboto", "YT Sans" sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
}

nav {
  font-size: 10px;
}

#nav {
  height: 64px;
  padding: 8px 0px;
  font-size: 20px;
  a {
    font-weight: bold;
    color: rgba(255, 255, 255, 0.5);
    font-size: 20px;
    line-height: 1.2;
    font-weight: 500;
    margin: 0 24px;
    justify-content: space-between;

    &.router-link-exact-active {
      color: #ffffff;
    }
    &:hover {
      color: #ffffff;
    }
  }
}

.search {
  font-weight: bold;
  color: rgba(255, 255, 255, 0.5);
  font-size: 20px;
  font-weight: 500;
  margin: 0 24px;

  &:hover {
    color: #ffffff;
  }
}
svg {
  font-weight: bold;
  color: rgba(255, 255, 255, 0.5);
  font-size: 20px;
  font-weight: 500;
  margin: 0 12px;
  &:hover {
    fill: #ffffff !important;
  }
}
</style>
