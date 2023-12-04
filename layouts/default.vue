<template>
  <div>
    <nav>
      <ul>
        <li>
          <Nuxt-link to="/"> Create Notes</Nuxt-link>
        </li>
        <li>
          <Nuxt-link to="/Notes"> My Notes</Nuxt-link>
        </li>
      </ul>
    </nav>
    <Nuxt />
  </div>
</template>

<style>
nav {
  width: 100%;
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(0, 0, 0, 0.589);
  overflow: hidden; /* Hide overflowing content */
}

nav ul {
  list-style: none;
  display: flex;
  transition: transform 0.3s ease; /* Add smooth transition for the list items */
}

nav ul li {
  margin: 0 10px;
  transform: translateY(0); /* Initial position for the list items */
  transition: transform 0.3s ease; /* Add smooth transition for the list items */
}

nav ul li:hover {
  transform: translateY(-5px); /* Move the list item up on hover */
}

nav ul li a {
  text-decoration: none;
  color: #fff;
  padding: 10px;
  border: 1px solid #fff;
  transition: background 0.3s ease; /* Add smooth transition for the background */
}

nav ul li a:hover {
  background: #000;
}

.nuxt-link-exact-active {
  background: #000;
}
</style>
