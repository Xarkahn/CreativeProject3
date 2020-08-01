<template>
  <div id="app">
    <div id="nav">
      <router-link tag="button" to="/">Home</router-link>
      <div class="dropdown">
        <button class="dropdown-toggle" type="button" data-toggle="dropdown">
          Characters <span class="caret"></span>
        </button>
        <ul class="dropdown-menu">
          <li>
            <router-link class="dropdown-option" to="/">
              <span>Grognak</span>
            </router-link>
          </li>
          <li>
            <router-link class="dropdown-option" to="/">
              <span>New Character </span>
              <img src="@/assets/Plus-square.svg" />
            </router-link>
          </li>
        </ul>
      </div>
      <div class="dropdown">
        <button class="dropdown-toggle" type="button" data-toggle="dropdown">
          Spells <span class="caret"></span>
        </button>
        <ul class="dropdown-menu">
          <li>
            <router-link class="dropdown-option" to="/">
              <span>D&D 5e</span>
            </router-link>
          </li>
        </ul>
      </div>
    </div>
    <div class="footer">
      <a href="https://github.com/Xarkahn/CreativeProject3">Repository</a>
    </div>
    <router-view />
  </div>
</template>

<style>
:root {
  --header-color: rgb(73, 38, 91);
  --header-active-color: rgb(120, 63, 142);
  --accent-color: rgb(81, 62, 67);
  --accent-color-pale: rgb(231, 216, 216);
}

body {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
}

#nav {
  background-color: var(--header-color);
  padding: 15px 30px;
  display: flex;
  flex-direction: row;
}

.router-link-exact-active {
  background-color: var(--header-active-color);
}

button {
  background-color: var(--header-color);
  color: white;
  padding: 0.5em 1em;
  border: none;
  border-radius: 0.5em;
  margin-right: 0.5em;
}

a {
  color: white;
}

a:hover {
  color: white;
  text-decoration: none;
}

.dropdown-option {
  background-color: transparent;
  color: black;
  padding-left: 1em;
}

.dropdown-option:hover {
  background-color: transparent;
  color: black;
}

.footer {
  position: absolute;
  bottom: 0;
  background-color: var(--header-color);
  width: 100%;
  text-align: center;
}
</style>
