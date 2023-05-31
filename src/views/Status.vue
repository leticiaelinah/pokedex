<template>
    <div>
        <div v-if="!pokemon.status">
            Selecione um Pokémon
        </div>
        <div v-else>
            <span>Força:</span>
            <div class="progress mb-2">
                <div 
                    class="progress-bar" 
                    role="progressbar" 
                    :style="`width: ${pokemon.status.forca}%;`" 
                    :aria-valuenow="`${pokemon.status.forca}`"
                    aria-valuemin="0" 
                    aria-valuemax="100">
                        {{ pokemon.status.forca }}
                </div>
            </div>

            <span>Agilidade:</span>
            <div class="progress mb-2">
                <div 
                    class="progress-bar" 
                    role="progressbar" 
                    :style="`width: ${pokemon.status.agilidade}%;`"
                    :aria-valuenow="`${pokemon.agilidade}`" 
                    aria-valuemin="0"
                    aria-valuemax="100">
                        {{ pokemon.status.agilidade }}
                </div>
            </div>

            <span>Ataque:</span>
            <div class="progress mb-2">
                <div 
                    class="progress-bar" 
                    role="progressbar" 
                    :style="`width: ${pokemon.status.ataque}%;`"
                    :aria-valuenow="`${pokemon.ataque}`" 
                    aria-valuemin="0"
                    aria-valuemax="100">
                        {{ pokemon.status.ataque }}
                </div>
            </div>
        
            <span>Defesa:</span>
            <div class="progress mb-2">
                <div 
                    class="progress-bar" 
                    role="progressbar" 
                    :style="`width: ${pokemon.status.defesa}%;`"
                    :aria-valuenow="`${pokemon.defesa}`" 
                    aria-valuemin="0"
                    aria-valuemax="100">
                        {{ pokemon.status.defesa }}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Status',
    props: {
        pokemon: Object
    }
};
</script>