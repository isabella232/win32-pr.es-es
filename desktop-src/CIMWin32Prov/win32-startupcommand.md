---
description: El objeto StartupCommand de Win32 \_&\# 8194; La clase WMI representa un comando que se ejecuta automáticamente cuando un usuario inicia sesión en el sistema del equipo.
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Win32_StartupCommand clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061474"
---
# <a name="win32_startupcommand-class"></a>Clase StartupCommand de Win32 \_

La **clase WMI \_ StartupCommand** [de](../wmisdk/retrieving-a-class.md) Win32 representa un comando que se ejecuta automáticamente cuando un usuario inicia sesión en el sistema del equipo.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a>Members

La **clase \_ StartupCommand de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ StartupCommand de Win32** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**Comando**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE Microsoft Windows \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ Run")
</dt> </dl>

Comando ejecutado por el comando de inicio.

WMI obtiene estos datos de la clave del Registro

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Run**

Ejemplo: "C: \\ Windows \\notepad.exe myfile.txt"

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

**Ubicación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ SOFTWARE MICROSOFT \\ \\ WINDOWS \\ \\ \\ \\ CURRENTVERSION \\ \\ Windows")
</dt> </dl>

Ruta de acceso donde reside el comando de inicio en el sistema de archivos de disco.

Por ejemplo: HKLM \\ SOFTWARE \\ Microsoft Windows \\ \\ CurrentVersion \\ Run

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

**Inicio** ("Inicio")


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

**Inicio común** ("inicio común")


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

**HKLM \\ \\ SOFTWARE \\ \\ Microsoft Windows \\ \\ \\ \\ CurrentVersion \\ \\ Run** ("HKLM \\ \\ SOFTWARE Microsoft \\ \\ Windows \\ \\ \\ \\ CurrentVersion \\ \\ Run")


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

**HKLM \\ \\ SOFTWARE \\ \\ Microsoft Windows \\ \\ \\ \\ CurrentVersion \\ \\ RunServices** ("HKLM \\ \\ SOFTWARE Microsoft \\ \\ \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices")


</dt> <dd></dd> </dl>

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Structures \| [**WIN32 FIND \_ \_ DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| cFileName")
</dt> </dl>

Nombre de archivo del comando de inicio.

Ejemplo: "FindFast"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador por el que se conoce el objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**User**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Nombre de usuario para el que se ejecutará este comando de inicio.

Ejemplo: "mydomain \\ myname"

</dd> <dt>

**UserSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

La propiedad UserSID indica el SID del usuario para el que se ejecutará este comando de inicio. Esa propiedad User puede estar vacía, pero UserSID todavía tiene un valor si el nombre de usuario no se puede resolver (como en el caso de un usuario eliminado). La propiedad es útil para distinguir entre los comandos asociados con dos usuarios diferentes con nombres sin resolver. Puede ser NULL cuando el comando está asociado a elementos que no identifican realmente a un usuario como Todos los usuarios.

Ejemplo: S-1-5-21-1579938362-1064596589-3161144252-1006

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ StartupCommand de Win32** se deriva de [**cim \_ setting**](cim-setting.md).

El inicio del equipo no finaliza una vez cargado el sistema operativo. En su lugar, Windows sistema operativo se puede configurar para que los comandos de inicio se ejecuten cada vez Windows inicio. Los comandos de inicio se almacenan en el Registro o como parte del perfil de usuario y se usan para iniciar automáticamente los scripts o aplicaciones especificados cada vez que Windows carga.

En la mayoría de los casos, los programas de inicio automático son útiles; garantizan que determinadas aplicaciones, como las herramientas antivirus, se inician y ejecutan automáticamente cada vez Windows carga. Sin embargo, los programas de inicio automático también pueden ser responsables de problemas como:

-   Equipos que tardaron un tiempo excepcionalmente largo en iniciarse. Este podría ser el resultado de un gran número de aplicaciones que se deben iniciar cada vez que Windows inicio.
-   Las aplicaciones que se representan en la barra de tareas o en Administrador de tareas, aunque el usuario no las haya empezado. Aunque estas aplicaciones no provocan necesariamente problemas, pueden dar lugar a llamadas del servicio de asistencia de usuarios que están confusos sobre de dónde provenían estos programas y por qué se están ejecutando.
-   Equipos que experimentan problemas incluso cuando parecen inactivos. Estos problemas se suelen seguir hasta los comandos de inicio que se ejecutan cuando nadie es consciente de que se están ejecutando.

Identificar las aplicaciones y scripts que se ejecutan automáticamente en el inicio es una tarea administrativa importante pero difícil, ya que los comandos de inicio se pueden almacenar en muchas ubicaciones diferentes:

-   HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion \\ Run
-   HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion \\ RunOnce
-   HKCU \\ Software Microsoft Windows \\ \\ \\ CurrentVersion \\ Run
-   HKCU \\ Software Microsoft Windows \\ \\ \\ CurrentVersion \\ RunOnce
-   HKU \\ ProgID \\ Software Microsoft Windows \\ \\ \\ CurrentVersion \\ Run
-   systemdrive \\ Documents and Configuración All Users Start Menu Programs \\ \\ \\ \\ Startup
-   systemdrive \\ Documents and Configuración username Start Menu Programs \\ \\ \\ \\ Startup

Puede usar la clase StartupCommand win32 de WMI para enumerar los programas de inicio automático independientemente de dónde \_ se almacene la información.

El proceso de llamada que usa esta clase debe tener el **SE \_ restore \_ NAME** en el equipo en el que reside el Registro. Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio. Para obtener más información, vea [Ejecutar operaciones con privilegios.](../wmisdk/executing-privileged-operations.md)

Puede cambiar los valores del Registro donde **Win32 \_ StartupCommand** obtiene datos llamando a los métodos del proveedor del [Registro del](/previous-versions/windows/desktop/regprov/system-registry-provider) sistema WMI en script o en C++. Para obtener más información, [vea Modificar el Registro del sistema](../wmisdk/modifying-the-system-registry.md).

## <a name="examples"></a>Ejemplos

El siguiente VBScript enumera los comandos de inicio en un equipo.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
Next
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

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
