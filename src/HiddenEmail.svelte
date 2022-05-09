<script>
function handleMailLink(e) {
    e.preventDefault();
    let el = e.target;
    window.open('mailto:' + el.dataset.name + '@' + el.dataset.domain + '.' + el.dataset.tld);
}
export let to;
export let title = '';
let error = false;
let params = [];

// Kudos: https://stackoverflow.com/a/201378/11340761
if(!to.match(/(?:[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*|"(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21\x23-\x5b\x5d-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])*")@(?:(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?\.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?|\[(?:(?:(2(5[0-5]|[0-4][0-9])|1[0-9][0-9]|[1-9]?[0-9]))\.){3}(?:(2(5[0-5]|[0-4][0-9])|1[0-9][0-9]|[1-9]?[0-9])|[a-z0-9-]*[a-z0-9]:(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21-\x5a\x53-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])+)\])/)){
    error = true;
    console.error('HiddenEmail: Invalid "to" email address.')
} else {
    params = to.split(/[@\.]/);
}
</script>

<style>
a::after {
    content: attr(data-name) "@" attr(data-domain) "." attr(data-tld);
}
</style>

{#if !error}
<!-- svelte-ignore a11y-invalid-attribute -->
<a href="#" {title}
    data-name={params[0]}
    data-domain={params[1]}
    data-tld={params[2]}
    on:click={(e) => handleMailLink(e)}>&nbsp;</a>
{/if}