---
description: Esta clase es la clase de tipo de evento para los eventos de asignación virtuales. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: PageFault_VirtualAlloc clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: fa3dd8eb53e9c1a79cf38edde0d9c4dba93ea85b0994bfb316b97064f211f26e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927575"
---
# <a name="pagefault_virtualalloc-class"></a>PageFault \_ VirtualAlloc (clase)

Esta clase es la clase de tipo de evento para los eventos de asignación virtuales.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a>Miembros

La **clase PageFault \_ VirtualAlloc** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase PageFault \_ VirtualAlloc** tiene estas propiedades.

<dl> <dt>

**BaseAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Dirección inicial en la que se asignó o se libera la memoria.

</dd> <dt>

**Marcas**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4), Format("x")
</dt> </dl>

Tipo de asignación de memoria que se realizó. Para ver los valores posibles, *consulte el parámetro flAllocationType* de la [**función VirtualAllocEx.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

El proceso que posee la memoria (puede ser diferente del subproceso que realizó la asignación).

</dd> <dt>

**RegionSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Extension("SizeT")
</dt> </dl>

Tamaño, en bytes, de la memoria asignada o liberada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 
