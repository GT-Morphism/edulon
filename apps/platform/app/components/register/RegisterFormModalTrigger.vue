<script setup lang="ts">
  import { RegisterFormModal } from "#components";
  const modal = useModal();

  defineShortcuts({
    ctrl_r: {
      usingInput: true,
      handler: () => {
        modal.open(RegisterFormModal);
      },
    },
  });
</script>

<template>
  <UTooltip
    text="Jetzt Account erstellen"
    :shortcuts="['Ctrl', 'R']"
    :popper="{ strategy: 'absolute' }"
  >
    <UButton
      type="button"
      class="smooth-rotation"
      icon="i-heroicons-user-plus"
      variant="ghost"
      color="white"
      :padded="false"
      @click="modal.open(RegisterFormModal)"
    >
      <span class="sr-only">Account erstellen</span>
    </UButton>
  </UTooltip>
</template>
