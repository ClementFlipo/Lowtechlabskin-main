Follow this tutorial to load the Lowtechlab skin into your wikifab site.

### 1. Download the LowtechlabSkin-extension

Download the LowtechlabSkin-extension and place the file(s) in a directory called LowtechlabSkin in your extensions/ folder.

### 2. Download the lowtechlab-skin files

Download the lowtechlab-skin and place the file(s) in a directory called lowtechlab-skin in your skins/ folder.

### 3. Update your LocalSettings.php

Add the following code at the bottom of your LocalSettings.php:

    require_once "$IP/extensions/LowtechlabSkin/LowtechlabSkin.php";
    $wgFavicon = "/skins/lowtechlab-skin/images/favicon.ico";

    $egChameleonExternalStyleModules = array(
    __DIR__ . '/skins/wikifabStyleModule/chameleon-wikifab.less' => $wgScriptPath . '/skins/wikifabStyleModule',
    __DIR__ . '/skins/wikifabStyleModule/font-awesome-4.4.0/less/font-awesome.less' => $wgScriptPath . '/skins/wikifabStyleModule/font-awesome-4.4.0/less/font-awesome.less',
    __DIR__ . '/skins/lowtechlab-skin/css/style.css' => $wgScriptPath . '/skins/lowtechlab-skin',);

### 4. Done!

Navigate to Special:Version on your wiki to verify that the extension is successfully installed.
