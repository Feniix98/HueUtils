# CheckPointUtils
- CheckPointUtils permet de simplifier la création de points bleu & de points véhicules (point jaune)
- Comment l'utiliser ?
- Tout d'abord supposont que je veuille crée un point bleu donc :
**Points bleues**
```CS
public override void OnPlayerSpawnCharacter(Player player, NetworkConnection conn, Characters character)
{
    base.OnPlayerSpawnCharacter(player, conn, character);
    UnityEngine.Vector3 pointPos = new UnityEngine.Vector3(0.0f, 0.0f, 0.0f); // Changer par la position de votre point
    CheckPointUtils.CreateCheckPoint(player, pointPos, delegate
    {
        // Action
    });
    // Le point est crée automatiquement
}
```
**Points jaunes**
```CS
public override void OnPlayerSpawnCharacter(Player player, NetworkConnection conn, Characters character)
{
    base.OnPlayerSpawnCharacter(player, conn, character);
    UnityEngine.Vector3 pointPos = new UnityEngine.Vector3(0.0f, 0.0f, 0.0f);
    CheckPointUtils.CreateVehicleCheckPoint(player, pointPos, (VehicleAction, someUint) =>
    {
        // Action
    });
    // Le point est crée automatiquement
}
```
