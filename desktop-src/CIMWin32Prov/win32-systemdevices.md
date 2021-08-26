---
description: La clase WMI de asociación SystemDevices de Win32 relaciona un sistema informático y un dispositivo \_ lógico instalado en ese sistema.
ms.assetid: 84dfcb75-3b44-4b27-8eee-779be522eb1f
ms.tgt_platform: multiple
title: Win32_SystemDevices clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDevices
- Win32_SystemDevices.GroupComponent
- Win32_SystemDevices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 698b827e2dd3f9097f2348c83cbb52120186b0694a836fd2468396c542e535c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971475"
---
# <a name="win32_systemdevices-class"></a>Clase SystemDevices de Win32 \_

La clase WMI **de asociación \_ SystemDevices** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona un sistema informático y un dispositivo lógico instalado en ese sistema.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDevices : CIM_SystemDevice
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_LogicalDevice    REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SystemDevices de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemDevices de Win32** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Referencia a la instancia de que representa las propiedades del sistema informático donde existe el dispositivo lógico.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| \_ LogicalDevice")
</dt> </dl>

Referencia a la instancia de que representa las propiedades de un dispositivo lógico que existe en el sistema del equipo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ SystemDevices de Win32** se deriva de [**CIM \_ SystemDevice**](cim-systemdevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sistema \_ CIMDispositivo**](cim-systemdevice.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
