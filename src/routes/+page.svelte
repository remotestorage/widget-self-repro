<script>
import RemoteStorage from 'remotestoragejs';
import Widget from 'remotestorage-widget';

const remoteStorage = new RemoteStorage();

remoteStorage.access.claim('myfavoritedrinks', 'rw');

const widget = new Widget(remoteStorage);
widget.attach();
</script>

<strong><a href="https://github.com/remotestorage/issue-145-repro">widget-self-error</a></strong>
<br>
<small>Reproduces issue <a href="https://github.com/remotestorage/remotestorage-widget/issues/145">#145</a></small>
<widget-wrapper></widget-wrapper>
