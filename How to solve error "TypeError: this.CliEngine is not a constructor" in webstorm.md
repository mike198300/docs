If webstorm shows :    
       "ESLint: TypeError: this.CliEngine is not a constructor"    
You should find 
       "eslint-plugin.js" in folder"x:\program files\JetBrains\WebStorm 2018.2.5\plugins\JavaScriptLanguage\languageService\eslint\bin"    
Get the line:       
```javascript
this.CliEngine = require(this.basicPath + "lib/cli-engine");
```

and change it to:

```javascript
this.CliEngine = require(this.basicPath + "lib/cli-engine").CliEngine;
```

That's it!
