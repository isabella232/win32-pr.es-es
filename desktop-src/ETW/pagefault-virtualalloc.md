---
description: Esta clase es la clase de tipo de evento para los eventos de asignación virtual. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: PageFault_VirtualAlloc (clase)
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
ms.openlocfilehash: f9e754bc3dc09f492682d5a522a6489cfde27ceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360399"
---
# <a name="pagefault_virtualalloc-class"></a>Errores \_ VirtualAlloc (clase)

Esta clase es la clase de tipo de evento para los eventos de asignación virtual.

La siguiente sintaxis se simplifica desde el código MOF.

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

La clase **errores \_ VirtualAlloc** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **errores \_ VirtualAlloc** tiene estas propiedades.

<dl> <dt>

**BaseAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Dirección inicial en la que se ha asignado o liberado la memoria.

</dd> <dt>

**Marcas**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4), formato ("x")
</dt> </dl>

El tipo de asignación de memoria que se ha realizado. Para ver los valores posibles, vea el parámetro *flAllocationType* de la función [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) .

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

Proceso que poseía la memoria (puede ser diferente del subproceso que realizó la asignación).

</dd> <dt>

**Regiones**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), extensión ("Sizet")
</dt> </dl>

Tamaño, en bytes, de la memoria asignada o liberada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Errores \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 
