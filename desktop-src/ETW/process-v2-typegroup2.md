---
description: Esta clase es la clase de tipo de evento para procesar eventos de contador. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Process_V2_TypeGroup2 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 284b77da03b53f9c2662c8729a7bf6606c45630a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912325"
---
# <a name="process_v2_typegroup2-class"></a>\_ \_ Clase TypeGroup2 de proceso V2

Esta clase es la clase de tipo de evento para procesar eventos de contador.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ TypeGroup2 de Process V2** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ TypeGroup2 de proceso V2** tiene estas propiedades.

<dl> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

Recuento de identificadores usados.

</dd> <dt>

**PageFaultCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2)
</dt> </dl>

Recuento de errores de página.

</dd> <dt>

**PagefileUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (12), extensión ("Sizet")
</dt> </dl>

Uso del archivo de paginación actual.

</dd> <dt>

**PeakPagefileUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (7), extensión ("Sizet")
</dt> </dl>

Tamaño de archivo de página más grande usado.

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (5), extensión ("Sizet")
</dt> </dl>

Tamaño de página virtual más grande usado.

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (6), extensión ("Sizet")
</dt> </dl>

Mayor tamaño del espacio de trabajo usado.

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (15), extensión ("Sizet")
</dt> </dl>

Recuento de páginas físicas privadas actuales.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), Format ("x")
</dt> </dl>

Identificador de proceso global que puede usar para identificar un proceso. El valor es válido desde el momento en que se crea un proceso hasta que se termina.

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (14), extensión ("Sizet")
</dt> </dl>

Uso de memoria no paginada actual.

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (13), extensión ("Sizet")
</dt> </dl>

Uso de memoria paginada actual.

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (9), extensión ("Sizet")
</dt> </dl>

Mayor memoria no paginada confirmada utilizada.

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (8), extensión ("Sizet")
</dt> </dl>

Mayor memoria paginada confirmada utilizada.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4)
</dt> </dl>

Reservado.

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (10), extensión ("Sizet")
</dt> </dl>

Tamaño actual de la página virtual.

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (11), extensión ("Sizet")
</dt> </dl>

Tamaño del espacio de trabajo actual.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos eventos se registran cuando finaliza el proceso. El evento indica el modo en que un proceso controla el uso de memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Proceso \_ V2**](process-v2.md)
</dt> </dl>

 

 




