# Dev-Tools
this is a script you can use for making development easier in scripting by adding new useful attributes


# Documentation

If you wanna use the dev tools make sure the script has
```csharp
using HuhMonke.DevTools;
```

if you want to use dev tools in scripts but want to know if they have it installed
```csharp
#if HUHMONKE_DEVTOOLS
using HuhMonke.DevTools;
#endif
```

## Attributes

### Editor Button
this will make a button at the bottom of the script to trigger a function
```csharp
[EditorButton("LabelName")]
public void Shoot()
{

}
```

### ReadOnly
this will make a field readonly so you can view it but not edit it
```csharp
[ReadOnly]
public string Password = "123";
```

### Dropdown
this will make a folder/dropdown for script fields use () to categorize
```csharp
[Dropdown("Health Settings")]
public float Health = 100;
[Dropdown("Health Settings")]
public float Regeneration = 1;
```

### Color
this will change a fields color
```csharp
[Color(255,0,0)] // make it red
public float Health = 100;
```

### Boolean Display
this will should a field if a bool is enabled or disabled :  how to use
```csharp
public bool UseFloat = true;
[BooleanDisplay(nameof(UseFloat), true)] // first part is name of field second part is if it should show if true or if it should show as false : this uses true so it will show if true
public float Number;
[BooleanDisplay(nameof(UseFloat), false)] // this is false so it will show if usefloat is false
public int IntNumber;
```

### Required
this will should a field if the field is filled
```csharp
public GameObject Bullet;
[Required(nameof(Bullet))] // shows if bullet is filled
public float BulletSpeed = 15f;
```
