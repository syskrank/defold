<style type="text/css">
    body {
        background-color: #272b30;
    }
    #add_dependency {
        background-color: #232529;
        color: #8f9296;
        display: inline-block;
        cursor: pointer;
        padding: 6px 12px;
        text-decoration: none;
    }
    #add_dependency:hover {
        background-color: #45474b;
        border-radius: 4px;
    }
    .isDisabled {
      cursor: not-allowed !important;
      opacity: 0.5;
    }
    .isDisabled:hover {
      background-color: #232529 !important;
    }
    #checkmark {
        display: none;
        color: #6cff00;
    }
    .showCheckmark {
        display: inline-block !important;
    }
</style>
<script type="text/javascript">
    function showCheckmark(event)
    {
        var add_dependency_elem = document.getElementById('add_dependency');
        var checkmark_elem = document.getElementById('checkmark');

        add_dependency_elem.className = "isDisabled";
        add_dependency_elem.innerText = "Library added";
        // checkmark_elem.style = "display: inline-block";
        checkmark_elem.className = "showCheckmark";
    }
</script>
# WebView has been moved

We are in the process of moving a few of Defolds features from core
functionality into external native extensions. The goal is to keep the engine
as lean and minimal as possible, moving functionality that might only be
relevant for a select few of users. This also means that the extensions will be
available in full source code, enabling external developers to review and
contribute to them.

The `webview` module is the first step towards this goal, and with the 1.2.146
release of Defold it will no longer be part of the core functionality.



## Migrating to the external `webview` extension
If you previously were using the `webview` module, click the button below to add the
library to your project.

<a id="add_dependency" href="defold://add-dependency?url=https://github.com/defold/extension-webview/archive/master.zip" onclick="showCheckmark(event)">Add Library</a> <span id="checkmark">&#10004;</span>

### Adding Manually
You can also get the library manually by adding the following URL to your [game.project](defold://open?path=/game.project) dependencies:
```
https://github.com/defold/extension-webview/archive/master.zip
```

It has the same API and functionality as before.

The documentation is now available on GitHub:
[https://defold.github.io/extension-webview/](https://defold.github.io/extension-webview/)

The source code can be viewed on the public GitHub repository:
[https://github.com/defold/extension-webview](https://github.com/defold/extension-webview)
