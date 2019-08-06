<template>
    <section class="section">
        <div class="container">
            <div class="columns">
                <div class="column">
                    <div class="box is-flex">
                        <input
                            type="text"
                            name="some-input"
                            id="my-text-input"
                            class="input is-large"
                            v-model="someTestText"
                            placeholder="Type Some Text Here" />
                        <a class="button is-primary " @click="clearText" style="margin:1em">
                            Clear
                        </a>
                    </div>
                </div>
                <div class="column">
                    <div class="box has-text-centered">
                        <p>Uses a custom made filter to make the text uppercase.</p>
                        <h1 class="has-text-danger is-size-1">{{ someTestText | uppers }}</h1>
                    </div>
                </div>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    data: function() {
        return  {
            someTestText : ''
        }
    },
    methods: {
        clearText: function() {
            this.someTestText = '';
        }
    },
    filters: {
        uppers : function(value) {
            if ( !value ) return '';
            value = value.toString();
            return value.toUpperCase();
        }
    }
}
</script>

<style scoped>

</style>
