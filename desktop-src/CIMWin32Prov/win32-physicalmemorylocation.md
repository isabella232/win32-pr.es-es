---
description: La \_ clase WMI PhysicalMemoryLocation Association de Win32 relaciona una matriz de memoria física y su memoria física.
ms.assetid: 40252428-77ca-4dfb-8048-c05096a114d8
ms.tgt_platform: multiple
title: Win32_PhysicalMemoryLocation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryLocation
- Win32_PhysicalMemoryLocation.LocationWithinContainer
- Win32_PhysicalMemoryLocation.PartComponent
- Win32_PhysicalMemoryLocation.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daa6d47b13cb5caa74a10f28ab5fcd6e66e1524f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000821"
---
# <a name="win32_physicalmemorylocation-class"></a>\_Clase Win32 PhysicalMemoryLocation

La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PhysicalMemoryLocation** Association de Win32 relaciona una matriz de memoria física y su memoria física.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ PhysicalMemoryLocation de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PhysicalMemoryLocation de Win32** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ PhysicalMemoryArray**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemoryArray")
</dt> </dl>

[**\_ PhysicalMemoryArray de Win32**](win32-physicalmemoryarray.md) que representa la matriz de memoria física que contiene la memoria física.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que representa la posición del elemento físico en el paquete físico. La información relativa a los elementos estacionarios del contenedor (por ejemplo, "segunda Bahía de unidad de la parte superior"), ángulos, altitudes y otros datos se puede grabar en esta propiedad. Esta cadena se puede complementar o utilizar en lugar de crear una instancia del objeto de [**\_ Ubicación CIM**](cim-location.md) .

Esta propiedad se hereda del [**\_ contenedor CIM**](cim-container.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ PhysicalMemory**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemory")
</dt> </dl>

[**\_ PhysicalMemory de Win32**](win32-physicalmemory.md) que representa la memoria física incluida en la matriz de memoria física.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ PhysicalMemoryLocation de Win32** se deriva de [**\_ PackagedComponent de CIM**](cim-packagedcomponent.md).

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

[**\_PACKAGEDCOMPONENT CIM**](cim-packagedcomponent.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
