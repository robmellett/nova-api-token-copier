<template>
    <modal
        @modal-close="handleClose"
        data-testid="ApiTokenCopier"
        tabindex="-1"
        role="dialogue"
    >
        <div class="bg-white rounded-lg shadow-lg overflow-hidden" style="width: 400px">
            <p class="text-80 px-8 my-8">{{ data.message }} </p>
            <p class="text-80 px-8 my-8">{{ data.token }} </p>
        </div>
        <div class="bg-white rounded-lg shadow-lg overflow-hidden" style="width: 400px">
            <button
                class="bg-primary text-white h-9 p-4" type="button"
                @click.prevent="handleClose()"
            >
                Close
            </button>
        </div>
    </modal>
</template>

<script>
export default {
    props: {
        data: {type: Object},
    },

    methods: {
        handleClose() {
            this.$emit('close')
        },
    },
}
</script>
