<template src="./template.html"></template>

<script>
export default {
  name: 'Sidebar'
};
</script>
<style lang="less">
#sidebar {
    min-width: 200px;
    padding-top: 20px;
    position: sticky;
    top: 0;
    height: 300px;

    ul {
        margin: 0;
        padding: 0;

        li {
            display: block;

            a {
                display: block;
                padding: 10px;
                border-radius: 4px;

                &.active {
                    background: #F3F6FA;
                }
            }
        }
    }
}
</style>
