---
description: Clase abstracta de la que se derivan todas las clases de seguimiento de eventos.
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: Clase Eventtracer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810454"
---
# <a name="eventtrace-class"></a>Clase Eventtracer

Clase abstracta de la que se derivan todas las clases de seguimiento de eventos.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a>Miembros

La clase **eventtracer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **eventtracer** tiene estas propiedades.

<dl> <dt>

**EventGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (8), **Max** (16)
</dt> </dl>

GUID de la clase de seguimiento de eventos de este evento.

</dd> <dt>

**Eventos**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1)
</dt> </dl>

Número total de bytes del evento.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3)
</dt> </dl>

Tipo de evento definido por el proveedor. Indica la clase de tipo de evento que se va a utilizar para descifrar los datos de eventos definidos por el proveedor (los datos a los que apunta **MofData**.

</dd> <dt>

**InstanceId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (11)
</dt> </dl>

Identificador de esta instancia de evento.

</dd> <dt>

**KernelTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (9)
</dt> </dl>

Tiempo de ejecución transcurrido para instrucciones en modo kernel, en TICs de CPU.

</dd> <dt>

**MofData**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (14), **puntero**
</dt> </dl>

Puntero a los datos de evento específicos del proveedor.

</dd> <dt>

**MofLength**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (15)
</dt> </dl>

Longitud de los datos de eventos específicos del proveedor.

</dd> <dt>

**ParentGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (12), **Max** (16)
</dt> </dl>

GUID de la clase de seguimiento de eventos de la instancia primaria.

</dd> <dt>

**ParentInstanceId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (13)
</dt> </dl>

Identificador de los datos de la instancia primaria.

</dd> <dt>

**ReservedHeaderField**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2)
</dt> </dl>

Reservado.

</dd> <dt>

**ThreadId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6), **puntero**
</dt> </dl>

Identifica el subproceso que ha generado el evento.

</dd> <dt>

**Indicaciones**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (7)
</dt> </dl>

Contiene la fecha y hora en que se produjo el evento.

</dd> <dt>

**TraceLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4)
</dt> </dl>

Valor definido por el proveedor que define el nivel de gravedad usado para generar el evento.

</dd> <dt>

**TraceVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5)
</dt> </dl>

Número de versión definido por el proveedor de la clase de seguimiento de eventos utilizada para generar el evento.

</dd> <dt>

**UserTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (10)
</dt> </dl>

Tiempo de ejecución transcurrido para instrucciones en modo de usuario, en TICs de CPU.

</dd> </dl>

## <a name="remarks"></a>Observaciones

No utilice estas propiedades.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| MOF<br/>                      | <dl> <dt>WMI. mof</dt> </dl> |



 

 




