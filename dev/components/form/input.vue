<template>
  <div>
    <div class="layout-padding input-example" style="max-width: 600px;">
      <q-input v-model="text" />
      <q-input v-model="text" stack-label="Stack Label" />
      <q-input v-model="text" float-label="Float Label" placeholder="Gigi" />

      <q-input v-model="number" type="number" prefix="$" float-label="Number" />
      <q-input v-model="text" suffix="@gmail.com" float-label="Clearable" clearable />
      <q-input v-model="text" type="password" float-label="Password" />

      <q-input disable v-model="text" float-label="Float Label" placeholder="Gigi" />
      <q-input inverted disable v-model="text" float-label="Float Label" placeholder="Gigi" clearable />

      <q-input v-model="text" float-label="Colored" color="amber" />
      <q-input v-model="text" float-label="Colored" color="amber" error />

      <p class="caption">Solo Inputs</p>
      <q-input v-model="text" :error="error" inverted color="secondary" type="password" clearable placeholder="Some placeholder" :after="[{icon: 'warning', error: true, handler () {}}]" />
      <q-input v-model="text" inverted stack-label="Colored" color="amber" />
      <q-input v-model="text" inverted stack-label="Colored" :after="[{icon: 'arrow_forward', content: true, handler () {}}]"/>
      <q-input v-model="text" inverted type="textarea" stack-label="Colored" color="tertiary" :min-rows="5" />

      <p class="caption">On dark background</p>
      <div class="bg-grey-9" style="width: 500px; padding: 25px">
        <q-input v-model="text" float-label="Colored" dark prefix="$" suffix="TSP" />
        <q-input v-model="text" float-label="Colored" dark color="amber" prefix="$" suffix="TSP" />

        <q-field
          icon="wifi"
          label="Some Label"
          :count="10"
          helper="Some helper"
          :error="error"
          error-label="Some error"
        >
          <q-input
            v-model="text"
            dark
            color="yellow"
            float-label="Textfield"
          />
        </q-field>
      </div>

      <br><br>

      <q-field
        icon="wifi"
        label="Some Label"
        :count="10"
        helper="Some helper"
        error-label="Some error"
      >
        <q-input
          v-model="text"
          :error="error"
          float-label="Textfield"
        />
      </q-field>

      <q-field
        icon="wifi"
        label="Some Label"
        :count="10"
        helper="Some helper"
        :error="error"
        error-label="Some error"
      >
        <q-input v-model="text" inverted placeholder="On Field" :after="[{icon: 'arrow_forward', content: true, handler () {}}]"/>
      </q-field>

      <q-field
        icon="wifi"
        label="Some Label"
        :count="10"
        helper="Some helper"
        :error="error"
        error-label="Some error"
      >
        <q-input v-model="text" color="amber" inverted stack-label="Stack Label" :after="[{icon: 'arrow_forward', content: true, handler () {}}]"/>
      </q-field>

      <q-field
        icon="wifi"
        helper="Some helper"
        :error="error"
        error-label="Some error"
      >
        <q-input
          v-model="text"
          float-label="Textfield"
          :error="error"
        />
      </q-field>

      <br><br>

      <q-input v-model="area" type="textarea" float-label="Textarea" :max-height="100" :min-rows="3" />

      <q-label class="fixed" style="bottom: 16px; right: 16px;">
        <q-checkbox v-model="error" />
        <span>Error</span>
      </q-label>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      text: '',
      number: null,
      area: '',
      focus: false,
      error: false
    }
  },
  computed: {
    length () {
      return this.text.length
    }
  }
}
</script>

<style lang="stylus">
.q-field
  // border 1px solid black
.q-input
  // border 1px solid black
</style>
