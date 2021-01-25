<template>
<div>
    <div class="board-row">
        <Square :value="squares[0]" @clicked="$emit('squareClicked', 0) " />
        <Square :value="squares[1]" @clicked="$emit('squareClicked', 1) " />
        <Square :value="squares[2]" @clicked="$emit('squareClicked', 2) " />
    </div>
    <div class="board-row">
        <Square :value="squares[3]" @clicked="$emit('squareClicked', 3) " />
        <Square :value="squares[4]" @clicked="$emit('squareClicked', 4) " />
        <Square :value="squares[5]" @clicked="$emit('squareClicked', 5) " />
    </div>
    <div class="board-row">
        <Square :value="squares[6]" @clicked="$emit('squareClicked', 6) " />
        <Square :value="squares[7]" @clicked="$emit('squareClicked', 7) " />
        <Square :value="squares[8]" @clicked="$emit('squareClicked', 8) " />
    </div>
</div>
</template>

<script>
import Square from './Square.vue'

export default {
    name: 'Board',
    components: {
        Square
    },
    props: ['squares'],
}
</script>

<style scoped>
.status {
    margin-bottom: 10px;
}

.board-row:after {
    clear: both;
    content: "";
    display: table;
}
</style>
