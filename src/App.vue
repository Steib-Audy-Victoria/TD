<template>
  <header>
    <Menu>
      <MenuButton> <MenuIcon class="h-5 w-5 fill-blue-300 stroke-blue-300" /> <span class="sr-only">Menu</span></MenuButton>
      <transition enter-active-class="motion-safe:animate-backInLeft" leave-active-class="motion-safe:animate-backOutRight">
        <MenuItems class="absolute flex w-40 flex-col border-2 bg-slate-400 p-2">
          <MenuItem v-slot="{ active }">
            <RouterLink to="/" :class="{ 'bg-blue-600 text-white': active }" class="text-blue-600 underline"> Accueil</RouterLink>
          </MenuItem>
          <MenuItem v-slot="{ active }">
            <RouterLink to="/" :class="{ 'bg-blue-600 text-white': active }" class="text-blue-600 underline"> Autre</RouterLink>
          </MenuItem>
          <MenuItem v-slot="{ active }">
            <RouterLink to="/" :class="{ 'bg-blue-600 text-white': active }" class="text-blue-600 underline"> Autre</RouterLink>
          </MenuItem>
          <MenuItem disabled>
            <span class="opacity-75">Invite a friend (coming soon!)</span>
          </MenuItem>
        </MenuItems>
      </transition>
    </Menu>
  </header>

  <RouterView />
</template>



<script>
import { Menu, MenuButton, MenuItems, MenuItem } from "@headlessui/vue";
import { MenuIcon } from "@heroicons/vue";

export default {
  components: { Menu, MenuButton, MenuItems, MenuItem, MenuIcon },
};
</script>