<template>

    <div class="columns is-centered">
        <div class="column is-three-quarters">
            <vue-form-ss class="box animated fadeIn"
                         :route-params="[$route.name, $route.params.id, false]"
                         ref="form"
                         @loaded="pivotParams.events.id = $refs.form.field('event_id').value">
                <template slot="event_id" slot-scope="{ field, errors }">
                    <vue-select v-model="field.value"
                                :has-error="errors.has(field.name)"
                                @input="pivotParams.events.id=$event;errors.clear(field.name)"
                                :source="field.meta.source"/>
                </template>
            </vue-form-ss>
        </div>
    </div>

</template>

<script>
import VueFormSs from '../../components/enso/vueforms/VueFormSs.vue';
import VueSelect from '../../components/enso/select/VueSelect.vue';

export default {
    components: { VueFormSs, VueSelect },

    data() {
        return {
            pivotParams: { events: { id: null } },
        };
    },
};
</script>
