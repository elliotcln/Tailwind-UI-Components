<template>
  <div class="container py-6 px-4">
    <section>
      <h2 id="buttons" class="text-2xl font-semibold">
        Buttons <abbr title="Anchor" class="text-base text-gray-400">#</abbr>
      </h2>
      <div class="mt-4 grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-4">
        <KjButton model="success">Success button</KjButton>
        <KjButton model="warning">Warning button</KjButton>
        <KjButton model="error">Error button</KjButton>

        <KjButton class="kj-btn--blue">Basic button</KjButton>
        <KjButton class="kj-btn--indigo">Basic button</KjButton>
        <KjButton class="kj-btn--purple">Basic button</KjButton>
        <KjButton class="kj-btn--pink">Basic button</KjButton>
      </div>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
</style>