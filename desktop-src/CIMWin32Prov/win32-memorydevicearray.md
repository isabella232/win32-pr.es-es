---
description: La \_ clase WMI MemoryDeviceArray Association de Win32 relaciona un dispositivo de memoria y la matriz de memoria en la que reside.
ms.assetid: 39ea6333-2352-488b-99e4-97594bea7dcd
ms.tgt_platform: multiple
title: Win32_MemoryDeviceArray (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceArray
- Win32_MemoryDeviceArray.GroupComponent
- Win32_MemoryDeviceArray.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e527f77183c3bdc09d464f6fed4808e45adefa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907014"
---
# <a name="win32_memorydevicearray-class"></a>\_Clase Win32 MemoryDeviceArray

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryDeviceArray** Association de Win32 relaciona un dispositivo de memoria y la matriz de memoria en la que reside.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF563-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryDeviceArray : CIM_Component
{
  Win32_MemoryArray  REF GroupComponent;
  Win32_MemoryDevice REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ MemoryDeviceArray de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ MemoryDeviceArray de Win32** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ MemoryArray**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")
</dt> </dl>

[**\_ MemoryArray de Win32**](win32-memoryarray.md) que representa la parte de la matriz de memoria de la \_ Asociación MemoryDeviceArray de Win32.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ MemoryDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")
</dt> </dl>

[**\_ MemoryDevice de Win32**](win32-memorydevice.md) que representa una parte del dispositivo de memoria de la \_ Asociación MemoryDeviceArray de Win32.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ MemoryDeviceArray de Win32** se deriva [**del \_ componente CIM**](cim-component.md).

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

[**\_Componente CIM**](cim-component.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

