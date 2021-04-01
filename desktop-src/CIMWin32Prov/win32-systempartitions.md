---
description: La \_ clase WMI SystemPartitions Association de Win32 relaciona un equipo y una partición de disco en ese sistema.
ms.assetid: e8f02cd0-9446-4258-b476-5dc6c72c80d4
ms.tgt_platform: multiple
title: Win32_SystemPartitions (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemPartitions
- Win32_SystemPartitions.GroupComponent
- Win32_SystemPartitions.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deae8129772e5d854f05b5b953ec66a12bd5bcaf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907247"
---
# <a name="win32_systempartitions-class"></a>\_Clase Win32 SystemPartitions

La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemPartitions** Association de Win32 relaciona un equipo y una partición de disco en ese sistema.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemPartitions : Win32_SystemDevices
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_DiskPartition  REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SystemPartitions de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemPartitions de Win32** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Referencia a la instancia de que representa las propiedades del sistema del equipo donde se encuentra la partición de disco.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ DiskPartition**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ DiskPartition")
</dt> </dl>

Referencia a la instancia de que representa las propiedades de una partición de disco que existe en el sistema del equipo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ SystemPartitions de Win32** se deriva de [**\_ SystemDevices de Win32**](win32-systemdevices.md).

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

[**Win32 \_ SystemDevices**](win32-systemdevices.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
