<template>
    <div class="c-radio-group">
        <slot></slot>
    </div>
</template>
<script>
import Emitter from './../mixins/emitter'

export default {
    name: 'CRadioGroup',
    componentName: 'CRadioGroup',
    mixins:[Emitter],
    // model:{
    //     prop:'checkValue',
    //     event:'change',
    // },
    props: {
        value:{},
        disabled:{
            type:Boolean,
        },
        size:{
            type: String,
            validator: function (value) {
                return ['medium', 'small', 'mini','tiny'].indexOf(value) !== -1
            }
        }
    }
}
</script>
<style lang="scss">
.c-radio-group{

}

</style>


