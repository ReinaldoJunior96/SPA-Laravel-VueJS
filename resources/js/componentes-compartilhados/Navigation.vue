<template>
  <div class="">
    <nav
      class="
        h-16
        bg-gradient-to-r
        from-blue-500
        to-purple-600
        flex
        items-center
        px-5
        w-full
        relative
        z-10
      "
    >
      <div class="flex gap-2 items-center text-white">
        <i class="fas fa-dragon text-2xl"></i>
        <h3 class="">Dragon Dev</h3>
      </div>

      <ul class="lg:flex flex-1 justify-end gap-3 hidden">
        <li class="text-white hover:bg-blue-400 hover:rounded-lg p-2">
          <Link href="/"> Home </Link>
        </li>
        <li class="text-white hover:bg-blue-400 hover:rounded-lg p-2">
          <Link href="/about"> About </Link>
        </li>
        <li class="text-white hover:bg-blue-400 hover:rounded-lg p-2">
          <Link href="/contact"> Contact </Link>
        </li>
        <li class="text-white hover:bg-blue-400 hover:rounded-lg p-2">
          <Link href="/contact"> My Account </Link>
        </li>
      </ul>
      <div class="flex flex-1 justify-end gap-3 lg:hidden">
        <i @click="responsiveMenu()" class="fas fa-bars text-white"></i>
      </div>
    </nav>

    <div
      id="menu-responsive"
      class="
        top-0
        z-30
        fixed
        h-screen
        bg-gradient-to-b
        from-blue-500
        to-purple-600
        w-3/12
        -left-full
        transition-all
        duration-500
        sidebar-mobile
      "
    >
      <div class="flex flex-col items-center pt-5 text-white">
        <i class="fas fa-dragon text-xl"></i>
        <h3 class="">Dragon Dev</h3>
      </div>
      <hr />
      <ul class="flex flex-col items-center pt-5 gap-3 text-white">
        <li class="border-b-2 border-blue-400">
          <Link href="/"> Home </Link>
        </li>
        <li class="border-b-2 border-blue-400">
          <Link href="/about"> About </Link>
        </li>
        <li class="border-b-2 border-blue-400">
          <Link href="/contact"> Contact </Link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import { Link } from "@inertiajs/inertia-vue3";
export default {
  components: {
    Link,
  },
  data() {
    return {};
  },
  methods: {
    responsiveMenu: function () {
      var menu = document.getElementById("menu-responsive");
      menu.classList.toggle("-left-full");
      menu.classList.toggle("left-0");
    },
  },
};
</script>

<style>
</style>