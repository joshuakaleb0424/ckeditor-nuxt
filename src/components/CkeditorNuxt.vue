<template>
    <ckeditor
            :editor="editor"
            :value="value"
            :config="config"
            :tagName="tagName"
            :disabled="disabled"
            @input="event => $emit('input', event)"
    />
</template>
<script>

    // import FullFreeBuildEditor from '@blowstack/ckeditor5-full-free-build'

    // import FullFreeBuildEditor from '@engrjerickcmangalus/ckeditor5-build-custom-simpleuploader'
    // import FullFreeBuildEditor from '@engrjerickcmangalus/ckeditor5-build-custom-inlineuploader'
    // import FullFreeBuildEditor from '@engrjerickcmangalus/ckeditor5-build-custom-ck'
    // import FullFreeBuildEditor from '@engrjerickcmangalus/ckeditor5-build-custom-inline-project'

    import FullFreeBuildEditor from '@engrjerickcmangalus/ckeditor5-build-custom-simpleuploader'
    
    import CKEditor from '@ckeditor/ckeditor5-vue'

    export default {
        components: {
            ckeditor: CKEditor.component
        },
        props: {
            value: {
                type: String,
                required: false
            },
            tagName: {
                type: String,
                required: false,
                default: 'div'
            },
            disabled: {
                type: Boolean,
                required: false,
            },
            uploadUrl: {
                type: String,
                required: false
            },
            config: {
                type: Object,
                required: false,
                default: function () {
                }
            }
        },
        data() {
            return {
                editor: FullFreeBuildEditor,
            }
        },
    };
</script>
