<template lang="pug">
q-page()
  div(class="q-gutter-y-md q-pa-md")
    q-select(
      borderless
      dense
      v-model="model"
      :options="options"
      dark
      class="select"
    )
      template(v-if="model?.image" v-slot:prepend)
        q-avatar(size="2.12rem")
          img(:src="model.image")
      template(v-slot:option="scope")
        q-item(
          v-bind="scope.itemProps"
          v-on="scope.itemEvents"
        )
          q-item-section(avatar)
            q-avatar(size="2.12rem")
              q-img(:src="scope.opt.image")
          q-item-section()
            q-item-label(v-html="scope.opt.label")
    q-input(
      square
      filled
      borderless
      v-model="text"
      label="Currency"
      dark
      color="white"
      class=""
    )
  div(class="q-gutter-y-md q-pa-md")
    q-select(
      borderless
      dense
      v-model="model"
      :options="options"
      dark
      class="select"
    )
      template(v-if="model?.image" v-slot:prepend)
        q-avatar(size="2.12rem")
          img(:src="model.image")
      template(v-slot:option="scope")
        q-item(
          v-bind="scope.itemProps"
          v-on="scope.itemEvents"
        )
          q-item-section(avatar)
            q-avatar(size="2.12rem")
              q-img(:src="scope.opt.image")
          q-item-section()
            q-item-label(v-html="scope.opt.label")
    q-input(
      square
      filled
      borderless
      v-model="text"
      label="Currency"
      dark
      color="white"
      class=""
    )
</template>

<script>
export default {
  name: 'PageIndex',

  data() {
    return {
      model: null,
      options: [
        {
          label: 'USD',
          value: 1,
          image: 'https://imagensemoldes.com.br/wp-content/uploads/2020/05/Bandeira-do-Brasil-PNG.png',
        },
        {
          label: 'Facebook',
          value: 2,
          image: 'https://imagensemoldes.com.br/wp-content/uploads/2020/05/Bandeira-do-Brasil-PNG.png',
        },
        {
          label: 'Twitter',
          value: 3,
          image: 'https://imagensemoldes.com.br/wp-content/uploads/2020/05/Bandeira-do-Brasil-PNG.png',
        },
        {
          label: 'Apple',
          value: 4,
          image: 'https://imagensemoldes.com.br/wp-content/uploads/2020/05/Bandeira-do-Brasil-PNG.png',
        },
        {
          label: 'Oracle',
          value: 5,
          image: 'https://imagensemoldes.com.br/wp-content/uploads/2020/05/Bandeira-do-Brasil-PNG.png',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.select {
  width: 140px;
  border: none;
  font-size: 17px;
}
</style>
