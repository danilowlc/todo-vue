<script setup>
    const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocaFiltro', 'editaTarefaTemp'])
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
            <div class="col-md-8">
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required
                    class="form-control" type="text" placeholder="Digite a descrição da tarefa">
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-primary">Cadastrar</button>
            </div>
            <div class="col-md-2">
                <select @change="props.trocaFiltro" class="form-control">
                    <option value="todas">Todas tarefas</option>
                    <option value="pedentes">Pedentes</option>
                    <option value="finalizadas">Finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>