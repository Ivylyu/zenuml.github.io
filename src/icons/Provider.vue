<template>
  <div class="icon-provider" :class="'icon-provider--' + classState">
    <icon-sync-off v-if="!classState"></icon-sync-off>
  </div>
</template>

<script>
export default {
  props: ['providerId'],
  computed: {
    classState() {
      switch (this.providerId) {
        case 'googleDrive':
        case 'googleDriveAppData':
        case 'googleDriveWorkspace':
          return 'google-drive';
        case 'googlePhotos':
          return 'google-photos';
        case 'dropboxRestricted':
          return 'dropbox';
        case 'gist':
          return 'github';
        case 'bloggerPage':
          return 'blogger';
        default:
          return this.providerId;
      }
    },
  },
};
</script>

<style lang="scss">
.icon-provider {
  width: 100%;
  height: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
}

.icon-provider--zenuml {
  background-image: url(../assets/iconZenUML.png);
}

.icon-provider--chrome {
  background-image: url(../assets/iconGoogleChrome.svg);
}

.icon-provider--coffee {
  background-image: url(../assets/cuplogo.svg);
}

.icon-provider--stackedit {
  background-image: url(../assets/iconStackedit.svg);
}

.icon-provider--google-drive {
  background-image: url(../assets/iconGoogleDrive.svg);
}

.icon-provider--google-photos {
  background-image: url(../assets/iconGooglePhotos.svg);
}

.icon-provider--github {
  background-image: url(../assets/iconGithub.svg);
}

.icon-provider--dropbox {
  background-image: url(../assets/iconDropbox.svg);
}

.icon-provider--wordpress {
  background-image: url(../assets/iconWordpress.svg);
}

.icon-provider--blogger {
  background-image: url(../assets/iconBlogger.svg);
}

.icon-provider--zendesk {
  background-image: url(../assets/iconZendesk.svg);
}
</style>
