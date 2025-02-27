<script>
    import { blur, fade } from 'svelte/transition';
    let badges = [
        {title: 'Share', cssClass: 'badge-secondary', delay: 0},
        {title: 'Borrow', cssClass: 'badge-primary', delay: 200},
        {title: 'Lend', cssClass: 'badge-accent', delay: 400},
    ]
</script>

<div transition:blur|global={{duration: 400, delay: 800}} class="card sm:w-96 bg-base-100 border-base-100">
    <div class="card-body">
        <h1 class="text-secondary text-3xl sm:text-5xl font-bold">LEMESOM</h1>
        <div class="join mx-auto">
            {#each badges as {title, cssClass, delay}}
                <div transition:blur|global={{duration: 800, delay: delay + 800}} class="join-item badge badge-dash {cssClass}">{title}</div>
            {/each}
        </div>
    </div>
</div>
