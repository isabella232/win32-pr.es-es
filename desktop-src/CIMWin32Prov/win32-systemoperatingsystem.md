---
description: La clase WMI de asociación SystemOperatingSystem de Win32 relaciona \_ un sistema informático y su sistema operativo.
ms.assetid: dc71f80b-6fbd-4bc8-8783-3922d8050518
ms.tgt_platform: multiple
title: Win32_SystemOperatingSystem clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemOperatingSystem
- Win32_SystemOperatingSystem.PrimaryOS
- Win32_SystemOperatingSystem.GroupComponent
- Win32_SystemOperatingSystem.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 56c7a2781a690be5e2a1228140cec305da22469a5e0d43a1158c5aacd9307750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917465"
---
# <a name="win32_systemoperatingsystem-class"></a>Clase \_ SystemOperatingSystem de Win32

La **clase WMI de asociación \_ SystemOperatingSystem** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona un sistema informático y su sistema operativo.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemOperatingSystem : CIM_InstalledOS
{
  boolean                   PrimaryOS;
  Win32_ComputerSystem  REF GroupComponent;
  Win32_OperatingSystem REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SystemOperatingSystem de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemOperatingSystem de Win32** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Un [**equipo Win32 \_ ComputerSystem**](win32-computersystemprocessor.md) que describe las propiedades del sistema informático en el que está instalado el sistema operativo.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ OperatingSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")
</dt> </dl>

Un [**sistema operativo Win32 \_**](win32-operatingsystem.md) que describe las propiedades del sistema operativo que se ejecuta en este sistema informático.

</dd> <dt>

**PrimaryOS**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Sistema operativo DMTF \| \| 001.4")
</dt> </dl>

Si **es TRUE**, el sistema operativo instalado es el sistema operativo predeterminado para el sistema operativo del equipo.

Esta propiedad se hereda de [**CIM \_ InstalledOS.**](cim-installedos.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ SystemOperatingSystem de Win32** se deriva de [**CIM \_ InstalledOS.**](cim-installedos.md)

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

[**CIM \_ instalado OS**](cim-installedos.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
