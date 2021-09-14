---
description: La clase WMI de asociación SystemLoadOrderGroups de Win32 relaciona \_ un sistema informático y un grupo de orden de carga.
ms.assetid: fb637300-0f70-465a-a72b-f0ab3f246790
ms.tgt_platform: multiple
title: Win32_SystemLoadOrderGroups clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemLoadOrderGroups
- Win32_SystemLoadOrderGroups.GroupComponent
- Win32_SystemLoadOrderGroups.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 510acfbde2f562493a454abe80a4f7788377e556
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061451"
---
# <a name="win32_systemloadordergroups-class"></a>Clase \_ SystemLoadOrderGroups de Win32

La clase WMI **de asociación \_ SystemLoadOrderGroups** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona un sistema informático y un grupo de orden de carga.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C503-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemLoadOrderGroups : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_LoadOrderGroup REF PartComponent;
};
```

## <a name="members"></a>Members

La **clase \_ SystemLoadOrderGroups de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemLoadOrderGroups de Win32** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Referencia a la instancia de que representa el sistema del equipo donde existe el grupo de pedidos de carga.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ LoadOrderGroup de Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LoadOrderGroup")
</dt> </dl>

Referencia a la instancia de que representa el grupo de pedidos de carga existente en el sistema del equipo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ SystemLoadOrderGroups de Win32** se deriva de [**CIM \_ SystemComponent**](cim-systemcomponent.md).

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

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
