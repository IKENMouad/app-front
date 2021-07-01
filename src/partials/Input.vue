<template>
    <div class="form-group">
        <label :for="inputName">{{ label }} </label>
        <input
            class="form-control"
            :type="inputType"
            :name="inputName"
            :id="inputName"
            :autofocus="isAutofocus"
            :value="model"
            @input="onInput"
            @change="onChange"
        />
    </div>
</template>

<script>
export default {
    name: 'Input',
    props: {
        inputName: { type: String, required: false },
        inputType: { type: String, required: false, default: 'text' },
        label: { type: String, required: false },
        isAutofocus: { type: Boolean, required: false },
        model: { type: String, required: true }
    },
    data() {
        return {};
    },
    methods: {
        onInput(event) {
            this.$emit('input', event.target.value);
        },
        onchange(event) {
            this.$emit('change', event.target.value);
        }
    }
};
</script>

<style></style>
