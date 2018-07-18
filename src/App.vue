<template>
  <div>
    <h1>Hello Vue!</h1>

    <div>
      <label>Every day</label>
      <input type='radio' value='everyDay' v-model='frequency' />
    </div>
    <div>
      <label>Every week</label>
      <input type='radio' value='oncePerWeek' v-model='frequency' />
    </div>
    <div>
      <label>Every month</label>
      <input type='radio' value='oncePerMonth' v-model='frequency' />
    </div>
    {{frequency}}

    <div>
      <select v-model='selectedCountry'>
        <option v-for='country in countries'>
          {{country}}
        </option>
      </select>
      {{selectedCountry}}
    </div>
  </div>

</template>

<script>
export default {
  data () {
    return {
      frequency: 'oncePerMonth',
      countries: [
        'Austria',
        'Sweden',
        'Australia',
        'Canada',
        'Germany'
      ],
      selectedCountry: 'Germany'
    }
  }
}
</script>
