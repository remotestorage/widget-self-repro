<script>
import RemoteStorage from 'remotestoragejs';
import Widget from 'remotestorage-widget';

const remoteStorage = new RemoteStorage();

remoteStorage.access.claim('myfavoritedrinks', 'rw');

import { onMount } from 'svelte';
onMount(() => {
  (new Widget(remoteStorage)).attach('widget-wrapper');
});
</script>

<strong><a href="https://github.com/remotestorage/widget-self-repro">widget-self-repro</a></strong>
<br>
<small>Reproduces issue <a href="https://github.com/remotestorage/remotestorage-widget/issues/145">#145</a></small>

<p>If the widget imports successfully, it should appear after this text.</p>

<div id="widget-wrapper"></div>
