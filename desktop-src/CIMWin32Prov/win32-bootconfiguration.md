---
description: La \_ clase WMI BootConfiguration de Win32 representa la configuración de arranque de un equipo que ejecuta Windows.
ms.assetid: c2db28dd-3feb-44bb-a532-c91cab980ba3
ms.tgt_platform: multiple
title: Win32_BootConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BootConfiguration
- Win32_BootConfiguration.Caption
- Win32_BootConfiguration.Description
- Win32_BootConfiguration.SettingID
- Win32_BootConfiguration.BootDirectory
- Win32_BootConfiguration.ConfigurationPath
- Win32_BootConfiguration.LastDrive
- Win32_BootConfiguration.Name
- Win32_BootConfiguration.ScratchDirectory
- Win32_BootConfiguration.TempDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 556688d7c80038f04dd5b94b7c61c5d6dfef3199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659710"
---
# <a name="win32_bootconfiguration-class"></a>\_Clase Win32 BootConfiguration

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ BootConfiguration de Win32** representa la configuración de arranque de un equipo que ejecuta Windows.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BootConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string BootDirectory;
  string ConfigurationPath;
  string LastDrive;
  string Name;
  string ScratchDirectory;
  string TempDirectory;
};
```

## <a name="members"></a>Miembros

La **clase \_ BootConfiguration de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ BootConfiguration de Win32** tiene estas propiedades.

<dl> <dt>

**BootDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Process and Thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")
</dt> </dl>

Ruta de acceso a los archivos del sistema necesarios para arrancar el sistema.

Ejemplo: "C: \\ Windows"

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

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**ConfigurationPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Process and Thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")
</dt> </dl>

Ruta de acceso a los archivos de configuración. Este valor puede ser similar al valor de la propiedad **BootDirectory** .

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**LastDrive**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| GetDriveType")
</dt> </dl>

Última letra de unidad a la que se asigna una unidad física.

Ejemplo: "E:"

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Nombre de la configuración de arranque. Es un identificador de la configuración de arranque.

</dd> <dt>

**ScratchDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| GetTempPath")
</dt> </dl>

Directorio en el que pueden residir los archivos temporales durante el arranque.

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

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**TempDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| GetTempPath")
</dt> </dl>

Directorio donde se almacenan los archivos temporales.

Ejemplo: "C: \\ Temp"

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ BootConfiguration de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).

## <a name="examples"></a>Ejemplos

La [lista de las propiedades de configuración de arranque de un ejemplo Perl de equipo](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) devuelve información de configuración de arranque para un equipo.

El siguiente ejemplo de VBScript devuelve información de configuración de arranque para un equipo.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BootConfiguration") 
 
For Each objItem in colItems 
    Wscript.Echo "Boot Directory: " & objItem.BootDirectory 
    Wscript.Echo "Configuration Path: " & objItem.ConfigurationPath 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Last Drive: " & objItem.LastDrive 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Scratch Directory: " & objItem.ScratchDirectory 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Temp Directory: " & objItem.TempDirectory 
Next 
```



En el siguiente ejemplo de código se muestra el uso de la clase WMI **\_ BootConfiguration de Win32** .


```PowerShell
# Get Boot configuration from WMI

$boot = Get-WMIObject Win32_BootConfiguration

# Display information

"Boot Directory     : {0}" -f $boot.bootdirectory
"Caption            : {0}" -f $boot.caption
"Description        : {0}" -f $boot.description
"Last Drive         : {0}" -f $boot.lastdrive
"Scratch Directory  : {0}" -f $boot.scratchdirectory
"Temp Directory     : {0}" -f $boot.tempdirectory

```



En el ejemplo de código anterior se crea el siguiente resultado:

``` syntax
Boot Directory     : \WINDOWS
Caption            : \Device\Harddisk0\Partition1
Description        : \Device\Harddisk0\Partition1
Last Drive         : K:
Scratch Directory  : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
Temp Directory     : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

