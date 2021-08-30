---
description: La clase WMI de asociación MemoryDeviceArray de Win32 relaciona un dispositivo de memoria y la matriz de memoria \_ en la que reside.
ms.assetid: 39ea6333-2352-488b-99e4-97594bea7dcd
ms.tgt_platform: multiple
title: Win32_MemoryDeviceArray clase
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
ms.openlocfilehash: 2226e9adffa917a479078f9fb1fbcddfa4e1f74c3f481a294947dc8f832c4c7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973005"
---
# <a name="win32_memorydevicearray-class"></a>Clase MemoryDeviceArray de Win32 \_

La clase WMI **de asociación \_ MemoryDeviceArray** [de](/windows/desktop/WmiSdk/retrieving-a-class) Win32 relaciona un dispositivo de memoria y la matriz de memoria en la que reside.

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

Tipo de datos: **\_ MemoryArray de Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")
</dt> </dl>

MemoryArray [**de Win32 \_ que representa**](win32-memoryarray.md) la parte de la matriz de memoria de la asociación \_ MemoryDeviceArray de Win32.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ MemoryDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")
</dt> </dl>

Un [**dispositivo \_ MemoryDevice de Win32**](win32-memorydevice.md) que representa una parte del dispositivo de memoria de la asociación \_ MemoryDeviceArray de Win32.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ MemoryDeviceArray de Win32** se deriva del [**componente CIM \_**](cim-component.md).

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

[**Componente \_ CIM**](cim-component.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

