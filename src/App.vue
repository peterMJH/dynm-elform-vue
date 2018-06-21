<template>
    <div>
        <form-render :form-object="formObject"></form-render>
    </div>
</template>
<script>
import formRender from '@/components/form'
export default {
    components: { formRender },
    created () {
        this.setForm()
    },
    data () {
        return {
            formObject: {
                style: {},
                items: []
            }
        }
    },
    methods: {
        setForm () {
            this.formObject.items = [
                {
                    column: 'column1',
                    type: 'input',
                    label: 'input text',
                    value: '',
                    placeholder: '입력하세요',
                    width: '200px',
                    rules: {
                        required: true,
                        message: 'input text null message',
                        trigger: false
                    }
                },
                {
                    column: 'column2',
                    type: 'select',
                    label: 'select box',
                    value: '',
                    placeholder: '선택하세요',
                    width: '200px',
                    options: [
                        { label: 'option1', value: 'value1' },
                        { label: 'option2', value: 'value2' },
                        { label: 'option3', value: 'value3' }
                    ],
                    rules: {
                        required: true,
                        message: 'select box null message',
                        trigger: false
                    }
                },
                {
                    column: 'column3',
                    type: 'date-picker',
                    label: 'date picker',
                    value: '',
                    kinds: 'date',
                    placeholder: '날짜를 선택하세요',
                    width: '200px',
                    rules: {
                        required: true,
                        message: 'date null message',
                        trigger: false
                    }
                },
                {
                    column: 'column4',
                    type: 'switch',
                    label: 'switch',
                    value: '',
                    rules: {
                        required: false,
                        message: 'switch null message',
                        trigger: false
                    }
                },
                {
                    column: 'column5',
                    type: 'checkbox',
                    label: 'check box',
                    value: [],
                    group: [
                        { label: 'Online activities', value: 'checkVal1' },
                        { label: 'Promotion activities', value: 'checkVal2' },
                        { label: 'Offline activities', value: 'checkVal3' },
                        { label: 'Simple brand exposure', value: 'checkVal4' }
                    ],
                    rules: {
                    required: true,
                    message: 'checkbox null message',
                    trigger: false
                    }
                },
                {
                    column: 'column6',
                    type: 'radio',
                    label: 'radio',
                    value: '',
                    group: [{ label: 'Yes', value: 'Y' }, { label: 'No', value: 'N' }],
                    rules: {
                        required: true,
                        message: 'radio null message',
                        trigger: false
                    }
                },
                {
                    column: 'column7',
                    type: 'input',
                    label: 'text area',
                    kinds: 'textarea',
                    value: '',
                    placeholder: '입력하세요',
                    width: '700px',
                    rules: {
                        required: true,
                        message: 'textArea null message',
                        trigger: false
                    }
                }
            ]
        }
    }
}
</script>
