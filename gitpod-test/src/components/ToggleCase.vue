<template>
    <div class="toggle-smoggle">
        <input
            type="text"
            name="some-input"
            id="my-text-input"
            class="test-class"
            v-model="someTestText"
            placeholder="Type Something Here"
            />
        <h1>{{ someTestText | uppers }}</h1>
    </div>
</template>

<script>
export default {
    data: function() {
        return  {
            someTestText : ''
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
    *:focus {
        outline: none;
    }
    .toggle-smoggle{
        padding: 30px 60px;
    }
    .test-class{
        color: #f4a;
        font-size: 3em;
        border: none;
        background: transparent;
        border-bottom: 1px solid #666;
    }
    h1 {
        font-size: 4em;

    }
</style>
