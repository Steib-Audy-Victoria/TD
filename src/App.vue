<template>
  <header>
    <Menu>
      <MenuButton> <MenuIcon class="h-5 w-5 fill-blue-300 stroke-blue-600" /> <span class="sr-only">Menu</span></MenuButton>
      <transition
        enter-active-class="transition duration-300 ease-out"
        enter-from-class=" transform scale-95 opacity-0"
        enter-to-class=" transform scale-100 opacity-100"
        leave-active-class=" transform duration-[3s] ease-out"
        leave-from-class="transform scale-100 opacity-100"
        leave-to-class="transform  scale-95 opacity-0"
      ></transition>

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
    </Menu>
  </header>
</template>

<script>
import { Menu, MenuButton, MenuItems, MenuItem } from "@headlessui/vue";
import { MenuIcon } from "@heroicons/vue";

export default {
  components: { Menu, MenuButton, MenuItems, MenuItem, MenuIcon },
};
</script>