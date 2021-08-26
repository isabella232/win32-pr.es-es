---
description: OSRecoveryConfiguration de Win32 \_&\# 8194; La clase WMI representa los tipos de información que se recopilarán de la memoria cuando se produce un error en el sistema operativo. Esto incluye errores de arranque y bloqueos del sistema.
ms.assetid: 0c8a2aeb-2fd9-44b7-8f91-d19afb8d2de6
ms.tgt_platform: multiple
title: Win32_OSRecoveryConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OSRecoveryConfiguration
- Win32_OSRecoveryConfiguration.Caption
- Win32_OSRecoveryConfiguration.Description
- Win32_OSRecoveryConfiguration.SettingID
- Win32_OSRecoveryConfiguration.AutoReboot
- Win32_OSRecoveryConfiguration.DebugFilePath
- Win32_OSRecoveryConfiguration.DebugInfoType
- Win32_OSRecoveryConfiguration.ExpandedDebugFilePath
- Win32_OSRecoveryConfiguration.ExpandedMiniDumpDirectory
- Win32_OSRecoveryConfiguration.KernelDumpOnly
- Win32_OSRecoveryConfiguration.MiniDumpDirectory
- Win32_OSRecoveryConfiguration.Name
- Win32_OSRecoveryConfiguration.OverwriteExistingDebugFile
- Win32_OSRecoveryConfiguration.SendAdminAlert
- Win32_OSRecoveryConfiguration.WriteDebugInfo
- Win32_OSRecoveryConfiguration.WriteToSystemLog
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a780e0997ef3a56bc644adda2842b905aaf9744d28a2075fbc4726134c16aa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972295"
---
# <a name="win32_osrecoveryconfiguration-class"></a>Clase \_ OSRecoveryConfiguration de Win32

La clase  [WMI](../wmisdk/retrieving-a-class.md) **\_ OSRecoveryConfiguration de Win32** representa los tipos de información que se recopilarán de la memoria cuando se produce un error en el sistema operativo. Esto incluye errores de arranque y bloqueos del sistema.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4E8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OSRecoveryConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AutoReboot;
  string  DebugFilePath;
  uint32  DebugInfoType;
  string  ExpandedDebugFilePath;
  string  ExpandedMiniDumpDirectory;
  boolean KernelDumpOnly;
  string  MiniDumpDirectory;
  string  Name;
  boolean OverwriteExistingDebugFile;
  boolean SendAdminAlert;
  boolean WriteDebugInfo;
  boolean WriteToSystemLog;
};
```

## <a name="members"></a>Miembros

La **clase \_ OSRecoveryConfiguration de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ OSRecoveryConfiguration de Win32** tiene estas propiedades.

<dl> <dt>

**Arranque automático**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| AutoReboot")
</dt> </dl>

El sistema se reiniciará automáticamente durante una operación de recuperación.

</dd> <dt>

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

**DebugFilePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| DumpFile")
</dt> </dl>

Ruta de acceso completa al archivo de depuración. Se crea un archivo de depuración con el estado de memoria del equipo después de un error del equipo.

Ejemplo: "C: \\ Windows \\ Memory.dmp"

</dd> <dt>

**DebugInfoType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Tipo de información de depuración escrita en el archivo de registro.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (0)


</dt> <dd></dd> <dt>

<span id="Complete_memory_dump"></span><span id="complete_memory_dump"></span><span id="COMPLETE_MEMORY_DUMP"></span>

**Volcado de memoria completo** (1)


</dt> <dd></dd> <dt>

<span id="Kernel_memory_dump"></span><span id="kernel_memory_dump"></span><span id="KERNEL_MEMORY_DUMP"></span>

**Volcado de memoria del** kernel (2)


</dt> <dd></dd> <dt>

<span id="Small_memory_dump"></span><span id="small_memory_dump"></span><span id="SMALL_MEMORY_DUMP"></span>

**Volcado de memoria pequeño** (3)


</dt> <dd></dd> </dl>

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

**ExpandedDebugFilePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Versión expandida de la **propiedad DebugFilePath.**

Ejemplo: "C: \\ Windows \\ Memory.dmp"

</dd> <dt>

**ExpandedMiniDumpDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Versión expandida de la **propiedad MiniDumpDirectory.**

Ejemplo: "C: \\ Windows \\ MiniDump"

</dd> <dt>

**KernelDumpOnly**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| KernelDumpOnly")
</dt> </dl>

Solo se escribirá información de depuración del kernel en el archivo de registro de depuración. Si **es TRUE,** solo se escribe el estado del kernel en un archivo en caso de error del sistema. Si **es FALSE,** el sistema intentará registrar el estado de la memoria y los dispositivos que puedan proporcionar información sobre el sistema cuando se ha fallado.

</dd> <dt>

**MiniDumpDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| MiniDumpDir")
</dt> </dl>

Directorio donde se registrarán y acumularán archivos de volcado de memoria pequeños.

Ejemplo: "%systemRoot% \\ MiniDump"

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Identificar el nombre de esta instancia de la **clase \_ OSRecoveryConfiguration de Win32.**

</dd> <dt>

**OverwriteExistingDebugFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| Overwrite")
</dt> </dl>

El nuevo archivo de depuración sobrescribirá uno existente.

</dd> <dt>

**SendAdminAlert**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| SendAlert")
</dt> </dl>

El mensaje de alerta se enviará al administrador del sistema en caso de error del sistema operativo.

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

**WriteDebugInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| CrashDumpEnabled")
</dt> </dl>

La información de depuración se va a escribir en un archivo de registro.

</dd> <dt>

**WriteToSystemLog**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| LogEvent")
</dt> </dl>

Los eventos se escribirán en un registro del sistema.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ OSRecoveryConfiguration de Win32** se deriva de [**cim \_ setting**](cim-setting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
