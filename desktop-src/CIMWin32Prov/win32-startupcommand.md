---
description: Win32 \_ StartupCommand&\# 8194; La clase WMI representa un comando que se ejecuta automáticamente cuando un usuario inicia sesión en el sistema del equipo.
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Win32_StartupCommand (clase)
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907456"
---
# <a name="win32_startupcommand-class"></a>\_Clase Win32 StartupCommand

La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ StartupCommand de Win32** representa un comando que se ejecuta automáticamente cuando un usuario inicia sesión en el sistema del equipo.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

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

## <a name="members"></a>Miembros

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

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**Comando**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")
</dt> </dl>

Comando ejecutado por el comando de inicio.

WMI obtiene estos datos de la clave del registro

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Run**

Ejemplo: "C: \\ Windows \\notepad.exe myfile.txt"

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

**Ubicación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CURRENTVERSION \\ \\ Windows")
</dt> </dl>

Ruta de acceso en la que el comando de inicio reside en el sistema de archivos de disco.

Por ejemplo: HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

**Startup** ("startup")


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

**Inicio común** ("Inicio común")


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices")


</dt> <dd></dd> </dl>

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| File Structures \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| cFileName")
</dt> </dl>

Nombre de archivo del comando de inicio.

Ejemplo: "búsqueda rápida"

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

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

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

Ejemplo: "midominio mi \\ nombre"

</dd> <dt>

**UserSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

La propiedad UserSID indica el SID del usuario para el que se ejecutará este comando de inicio. Esa propiedad de usuario puede estar vacía, pero UserSID todavía tiene un valor si no se puede resolver el nombre de usuario (por ejemplo, en el caso de un usuario eliminado). La propiedad es útil para distinguir entre los comandos asociados a dos usuarios distintos con nombres sin resolver. Puede ser NULL cuando el comando está asociado a elementos que no identifican realmente a un usuario como todos los usuarios.

Ejemplo: S-1-5-21-1579938362-1064596589-3161144252-1006

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ StartupCommand de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).

El inicio del equipo no termina después de que se haya cargado el sistema operativo. En su lugar, se puede configurar el sistema operativo Windows para que se ejecuten los comandos de inicio cada vez que se inicie Windows. Los comandos de inicio se almacenan en el registro o como parte del perfil de usuario y se usan para iniciar automáticamente las aplicaciones o los scripts especificados cada vez que se carga Windows.

En la mayoría de los casos, los programas de inicio automático son útiles. garantizan que ciertas aplicaciones, como las herramientas antivirus, se inician y ejecutan automáticamente cada vez que se carga Windows. Sin embargo, los programas de inicio automático también pueden ser responsables de problemas como los siguientes:

-   Equipos que tardan mucho tiempo en iniciarse. Esto puede ser el resultado de un gran número de aplicaciones que se deben iniciar cada vez que se inicia Windows.
-   Aplicaciones que se representan en la barra de tareas o en el administrador de tareas, aunque el usuario no las haya iniciado. Aunque estas aplicaciones no causan necesariamente problemas, pueden dar lugar a llamadas al Departamento de soporte técnico por parte de usuarios que se confunden en el lugar en el que provienen estos programas y por qué se ejecutan.
-   Equipos que experimentan problemas incluso cuando parecen inactivos. A menudo se realiza un seguimiento de estos problemas con los comandos de inicio que se ejecutan cuando nadie es consciente de que se están ejecutando.

La identificación de las aplicaciones y los scripts que se ejecutan automáticamente en el inicio es una tarea administrativa importante pero difícil, porque los comandos de inicio se pueden almacenar en muchas ubicaciones diferentes:

-   HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   HKU \\ ProgID \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   SystemDrive \\ documentos y configuración \\ todos los usuarios \\ menú Inicio \\ programas \\ Inicio
-   unidadDelSistema \\ documentos y configuración \\ nombre de usuario \\ Inicio menú \\ programas \\ Inicio

Puede usar la clase Win32 StartupCommand de WMI \_ para enumerar programas de inicio automático con independencia de dónde se almacene la información.

El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro. Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio. Para obtener más información, vea [ejecutar operaciones con privilegios](../wmisdk/executing-privileged-operations.md).

Puede cambiar los valores del registro donde **Win32 \_ StartupCommand** obtiene los datos mediante una llamada a los métodos del [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) WMI en el script o en C++. Para obtener más información, vea [modificar el registro del sistema](../wmisdk/modifying-the-system-registry.md).

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
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
