# HueUtils
- Comment utiliser HueUtils sur un de mes plugins ?
- Tout d'abord placons les usings principaux

```CS
using Life;
using Life.Network;
using Life.UI;
using HueUtils;
```
- Votre class devra héritée de **HueUtils.HueUtils**
Exemple :
```CS
using Life;
using Life.Network;
using Life.UI;
using HueUtils;

namespace HueDevs98Test
{
    public class TestHueUtils : HueUtils.HueUtils
    {
        public TestHueUtils(IGameAPI gameAPI) : base(gameAPI) { }
    }
}
```

- Maintenant que la base de notre plugin supposont que nous voulons initialisée un plugin
```CS
public override void OnPluginInit()
{
    base.OnPluginInit();
    ConsoleUtils.WriteDarkGreenMessage("[TestHueUtils] success : Initialized");
}
```
