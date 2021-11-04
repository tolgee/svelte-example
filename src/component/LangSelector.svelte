<script lang="ts">
  import { useSetLanguage, useGetLanguage } from "@tolgee/svelte";

  const setLanguage = useSetLanguage();
  const getLanguage = useGetLanguage();

  let lang = getLanguage();
  $: setLanguage(lang);

</script>

<select bind:value={lang} class="lang-selector">
  <option value="en">🇬🇧 English</option>
  <option value="cs">🇨🇿 česky</option>
  <option value="fr">🇫🇷 français</option>
  <option value="de">🇩🇪 Deutsch</option>
</select>
