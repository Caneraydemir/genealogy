<template>
    <div class="container">
        <div class="error-container has-text-grey">
            <div class="error-title">
                {{ __('Page Not Found') }}
                <fa class="has-text-warning"
                    icon="exclamation-triangle"/>
            </div>
        </div>
    </div>
</template>

<script>
import fontawesome from '@fortawesome/fontawesome';
import { faExclamationTriangle } from '@fortawesome/fontawesome-free-solid/shakable.es';

fontawesome.library.add([faExclamationTriangle]);

export default {
    name: 'NotFound',
};
</script>

<style>
.error-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 50%;
    font-weight: 100;
}

.error-title {
    font-size: 3rem;
}
</style>
