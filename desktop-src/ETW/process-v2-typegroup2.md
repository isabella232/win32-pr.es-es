---
description: Esta clase es la clase de tipo de evento para los eventos de contador de procesos. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Process_V2_TypeGroup2 clase
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
ms.openlocfilehash: 51c24e12ed423b6240daeefee0b69a40f9b14b86813ca83cb09f74f807e24429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069955"
---
# <a name="process_v2_typegroup2-class"></a>Clase \_ \_ TypeGroup2 de Process V2

Esta clase es la clase de tipo de evento para los eventos de contador de procesos.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase Process \_ V2 \_ TypeGroup2** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Process \_ V2 \_ TypeGroup2** tiene estas propiedades.

<dl> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

Recuento de identificadores usados.

</dd> <dt>

**PageFaultCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2)
</dt> </dl>

Recuento de errores de página.

</dd> <dt>

**PagefileUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(12), Extension("SizeT")
</dt> </dl>

Uso actual del archivo de página.

</dd> <dt>

**PeakPagefileUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(7), Extension("SizeT")
</dt> </dl>

Tamaño de archivo de página más grande usado.

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(5), Extension("SizeT")
</dt> </dl>

Tamaño de página virtual más grande usado.

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(6), Extension("SizeT")
</dt> </dl>

Tamaño de conjunto de trabajo más grande usado.

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(15), Extension("SizeT")
</dt> </dl>

Recuento de páginas físicas privadas actuales.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Format("x")
</dt> </dl>

Identificador de proceso global que puede usar para identificar un proceso. El valor es válido desde el momento en que se crea un proceso hasta que finaliza.

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(14), Extension("SizeT")
</dt> </dl>

Uso de memoria no paginada confirmado actual.

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(13), Extension("SizeT")
</dt> </dl>

Uso de memoria paginada confirmado actual.

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(9), Extension("SizeT")
</dt> </dl>

Mayor memoria no paginada confirmada usada.

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(8), Extension("SizeT")
</dt> </dl>

Mayor memoria paginada confirmada usada.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4)
</dt> </dl>

Reservado.

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(10), Extension("SizeT")
</dt> </dl>

Tamaño de página virtual actual.

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(11), Extension("SizeT")
</dt> </dl>

Tamaño actual del conjunto de trabajo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Estos eventos se registran cuando finaliza el proceso. El evento indica cómo un proceso controló el uso de memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Proceso \_ V2**](process-v2.md)
</dt> </dl>

 

 




