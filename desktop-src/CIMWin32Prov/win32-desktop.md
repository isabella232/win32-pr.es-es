---
description: La clase Win32 \_ DesktopWMI representa las características comunes del escritorio de un usuario. El usuario puede modificar las propiedades de esta clase para personalizar el escritorio.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Win32_Desktop clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d005104cb663a680bac080b7ff9b6529fd9b7a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970232"
---
# <a name="win32_desktop-class"></a>Clase de escritorio Win32 \_

La **clase \_ WMI de escritorio Win32** representa las características comunes del escritorio de un usuario.[](/windows/desktop/WmiSdk/retrieving-a-class) El usuario puede modificar las propiedades de esta clase para personalizar el escritorio.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a>Members

La **clase Win32 \_ Desktop** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Win32 \_ Desktop** tiene estas propiedades.

<dl> <dt>

**BorderWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control Desktop \\ \\ \\ \\ WindowMetrics \| BorderWidth")
</dt> </dl>

Ancho de los bordes alrededor de todas las ventanas con bordes ajustables.

Ejemplo: 3

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**CoolSwitch**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Panel de control Desktop \\ \\ \| CoolSwitch")
</dt> </dl>

La conmutación rápida de tareas está activada. El cambio rápido de tareas permite al usuario cambiar entre ventanas mediante la **combinación de teclado ALT+TAB.**

</dd> <dt>

**CursorBlinkRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Panel de control Desktop \\ \\ \| CursorBlinkRate"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")
</dt> </dl>

Período de tiempo entre parpadeos sucesivos del cursor.

Ejemplo: 530

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**DragFullWindows**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Panel de control Desktop \\ \\ \| DragFullWindows")
</dt> </dl>

El contenido de una ventana se muestra cuando un usuario mueve la ventana.

</dd> <dt>

**GridGranularity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Panel de control Desktop \\ \\ \| GridGranularity"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 píxeles")
</dt> </dl>

Espaciado de la cuadrícula a la que están enlazadas las ventanas en el escritorio. Esto facilita la organización de ventanas. El espaciado suele ser lo suficientemente bueno como para que el usuario no lo observe.

Ejemplo: 1

</dd> <dt>

**IconoSpacing**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control \\ \\ Desktop \\ \\ \| IconSpacing"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")
</dt> </dl>

Espaciado entre iconos.

Ejemplo: 75

</dd> <dt>

**IconTitleFaceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control Desktop \\ \\ \\ \\ IconMetricsFont") \|
</dt> </dl>

Fuente utilizada para los nombres de los iconos.

Ejemplo: "MS San Serif"

</dd> <dt>

**IconTitleSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Font and Text Structures \| [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")
</dt> </dl>

Tamaño de fuente del icono.

Ejemplo: 9

</dd> <dt>

**IconTitleWrap**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control Desktop \\ \\ \\ \\ IconMetricsTitleWrap") \|
</dt> </dl>

El texto del título del icono se ajusta a la línea siguiente.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Nombre que identifica el perfil de escritorio actual.

Ejemplo: "MainProf"

</dd> <dt>

**Patrón**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control desktop \\ \\ \| pattern")
</dt> </dl>

Nombre del patrón que se usa como fondo para el escritorio.

</dd> <dt>

**ScreenSaverActive**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control Desktop \\ \\ \| ScreenSaveActive")
</dt> </dl>

El protector de pantalla está activo.

</dd> <dt>

**ScreenSaverExecutable**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control Desktop \\ \\ \|SCRNSAVE.EXE")
</dt> </dl>

Nombre del archivo ejecutable del protector de pantalla actual.

Ejemplo: "LOGON. SCR"

</dd> <dt>

**ScreenSaverSecure**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control \\ \\ Desktop \| ScreenSaverIsSecure")
</dt> </dl>

La contraseña está habilitada para el protector de pantalla.

</dd> <dt>

**ScreenSaverTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control Desktop \\ \\ \| ScreenSaveTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")
</dt> </dl>

Cantidad de tiempo que pasa antes de que se inicie el protector de pantalla.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador por el que se conoce el objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**Fondo de pantalla**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control \\ \\ Desktop \| Wallpaper")
</dt> </dl>

Nombre de archivo para el diseño del papel tapiz en el fondo del escritorio.

Ejemplo: "WINNT.BMP"

</dd> <dt>

**WallpaperStretched**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control Desktop \\ \\ \| WallpaperStyle")
</dt> </dl>

El papel tapiz se extiende para rellenar toda la pantalla. Microsoft Plus! debe instalarse antes de que esta opción esté disponible. Si **es FALSE,** el papel tapiz conserva sus dimensiones originales en el fondo del escritorio.

</dd> <dt>

**WallpaperTiled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . DEFAULT \\ \\ Panel de control Desktop \\ \\ \| TileWallpaper")
</dt> </dl>

El papel tapiz está en mosaico o centrado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase Win32 \_ Desktop** se deriva de [**cim \_ setting**](cim-setting.md).

El proceso de llamada que usa esta clase debe tener el **SE \_ restore \_ NAME** en el equipo en el que reside el Registro. Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio. Para obtener más información, [vea Ejecutar operaciones con privilegios.](/windows/desktop/WmiSdk/executing-privileged-operations)

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se describe cómo recuperar información de escritorio.


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

