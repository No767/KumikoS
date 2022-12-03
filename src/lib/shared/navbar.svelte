<script lang="ts">
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Button, Input } from 'flowbite-svelte'
</script>

<Navbar let:hidden let:toggle>
    <NavBrand href="/">
      <img
        src="https://raw.githubusercontent.com/No767/Kumiko/dev/assets/kumiko-resized-round.svg"
        class="mr-3 h-6 sm:h-9"
        alt="Flowbite Logo"
      />
      <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">
        Kumiko
      </span>
    </NavBrand>
    <div class="flex md:order-2 gap-x-4">
      <Button color="light" size="sm">Log In</Button>
      <Button size="sm" outline gradient color="purpleToBlue">Get started</Button>
      <NavHamburger on:click={toggle} />
    </div>
    <NavUl {hidden} class="order-1">
      <NavLi href="/commands">Commands</NavLi>
      <NavLi href="https://github.com/No767/Kumiko">GitHub</NavLi>
    </NavUl>
  </Navbar>