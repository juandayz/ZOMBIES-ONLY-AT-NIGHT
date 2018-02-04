# ZOMBIES-ONLY-AT-NIGHT

1.Open your custom compiles.sqf and into !isDedicated  section paste:

```ruby
//needed to remove zeds during daytime
player_spawnCheck = compile preprocessFileLineNumbers "dayz_code\compile\player_spawnCheck.sqf";
building_spawnZombies = compile preprocessFileLineNumbers "dayz_code\compile\building_spawnZombies.sqf";
zombie_generate = compile preprocessFileLineNumbers "dayz_code\compile\zombie_generate.sqf";
//needed to remove zeds during daytime
```

2.Open your zombie_Wildgenerate.sqf located in : dayz_server.pbo\compile\  and at very top paste: 

```ruby
if (sunOrMoon == 1) exitWith {};
```

3. Place dayz_code folder into mpmissions\your instance map\

