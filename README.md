# Text Resize

This creates buttons with title text for a user to reduce font size to 85%, reset font to 100%, or increase font to 115% of the font size on the website.

Add this to a .js file, or to test quickly in Drupal it can be added to the html.tpl.php file:

````
<script type="text/javascript">
$(document).ready(function() {
    $("#sizeUp").click(function() {
        $("body").css("font-size","115%");
    });
    $("#normal").click(function() {
        $("body").css("font-size","100%");
    })
    $("#sizeDown").click(function() {
        $("body").css("font-size","85%");
    })
});
</script>

````

This code can then be added to the page.tpl.php file in the region you would like it to appear.

````
<div id="sizeDown" title="Set font size to 85%"><img src="<?php print base_path() . path_to_theme() . '/images/down.png' ?>" </a></div>
<div id="normal" title="Set font size to 100%"><img src="<?php print base_path() . path_to_theme() . '/images/reset.png' ?>" </a></div>
<div id="sizeUp" title="Set font size to 115%"><img src="<?php print base_path() . path_to_theme() . '/images/up.png' ?>" </a></div>
````

The icon images will go into the /images folder within your theme.
