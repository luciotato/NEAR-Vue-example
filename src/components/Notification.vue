<template>
    <div class="notification">
        <aside>
            <a target="_blank" rel="noreferrer" v-bind:href="urlPrefix + '/' + accountId">
                {{ accountId }}
            </a>
            {{ msg }}
            in contract: <a target="_blank" rel="noreferrer" v-bind:href="urlPrefix + '/' + contractId">
                {{ contractId }}
            </a>
            <footer>
                <div>✔ Succeeded</div>
                <div>Just now</div>
            </footer>
        </aside>
    </div>
</template>

<script>
export default {
    name: 'Notification',
    props: {
        accountId: String,
        contractId: String,
        msg: String,
    },
    computed: {
        urlPrefix: () => "https://explorer." + window.networkId + ".near.org/accounts"
    }
}
</script>
