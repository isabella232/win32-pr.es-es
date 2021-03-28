---
description: Esta clase es la clase de tipo de evento para los eventos de cambio de contexto. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: Clase CSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 91004ca276140271e8d73c3fc226e83c4e03d1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275673"
---
# <a name="cswitch-class"></a>Clase CSwitch

Esta clase es la clase de tipo de evento para los eventos de cambio de contexto.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a>Miembros

La clase **CSwitch** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CSwitch** tiene estas propiedades.

<dl> <dt>

**NewThreadId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), Format ("x")
</dt> </dl>

Nuevo identificador de subproceso después del modificador.

</dd> <dt>

**NewThreadPriority**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

Prioridad del subproceso nuevo.

</dd> <dt>

**NewThreadWaitTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (11), formato ("x")
</dt> </dl>

Tiempo de espera para el nuevo subproceso.

</dd> <dt>

**OldThreadId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), Format ("x")
</dt> </dl>

IDENTIFICADOR de subproceso anterior.

</dd> <dt>

**OldThreadPriority**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4)
</dt> </dl>

Prioridad de subproceso del subproceso anterior.

</dd> <dt>

**OldThreadState**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (9)
</dt> </dl>

Estado del subproceso anterior. A continuación se muestran los posibles valores de estado:

| Estado | Descripción                                   |
|-------|-----------------------------------------------|
| 0     | Inicializado                                   |
| 1     | Ready                                         |
| 2     | En ejecución                                       |
| 3     | Standby                                       |
| 4     | Finalizado                                    |
| 5     | En espera                                       |
| 6     | Transición                                    |
| 7     | DeferredReady (agregado para Windows Server 2003) |



 

</dd> <dt>

**OldThreadWaitIdealProcessor**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (10), formato ("x")
</dt> </dl>

Tiempo de espera ideal del subproceso anterior.

</dd> <dt>

**OldThreadWaitMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (8)
</dt> </dl>

Modo de espera del subproceso anterior. Los posibles valores son los siguientes:

| Estado | Descripción |
|-------|-------------|
| 0     | KernelMode  |
| 1     | En modo usuario    |



 

</dd> <dt>

**OldThreadWaitReason**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (7)
</dt> </dl>

Razón de espera del subproceso anterior. Los posibles valores son los siguientes:

| Estado | Descripción       |
|-------|-------------------|
| 0     | Ejecutivo         |
| 1     | FreePage          |
| 2     | Pagein.            |
| 3     | PoolAllocation    |
| 4     | DelayExecution    |
| 5     | Suspended         |
| 6     | UserRequest       |
| 7     | WrExecutive       |
| 8     | WrFreePage        |
| 9     | WrPageIn          |
| 10    | WrPoolAllocation  |
| 11    | WrDelayExecution  |
| 12    | WrSuspended       |
| 13    | WrUserRequest     |
| 14    | WrEventPair       |
| 15    | WrQueue           |
| 16    | WrLpcReceive      |
| 17    | WrLpcReply        |
| 18    | WrVirtualMemory   |
| 19    | WrPageOut         |
| 20    | WrRendezvous      |
| 21    | WrKeyedEvent      |
| 22    | WrTerminated      |
| 23    | WrProcessInSwap   |
| 24    | WrCpuRateControl  |
| 25    | WrCalloutStack    |
| 26    | WrKernel          |
| 27    | WrResource        |
| 28    | WrPushLock        |
| 29    | WrMutex           |
| 30    | WrQuantumEnd      |
| 31    | WrDispatchInt     |
| 32    | WrPreempted       |
| 33    | WrYieldExecution  |
| 34    | WrFastMutex       |
| 35    | WrGuardedMutex    |
| 36    | WrRundown         |
| 37    | MaximumWaitReason |



 

</dd> <dt>

**PreviousCState**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (5)
</dt> </dl>

Índice del estado de C que el procesador utilizó por última vez. Un valor de 0 representa el estado de inactividad más claro con valores más altos que representan los Estados C más profundos.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (12)
</dt> </dl>

Reservado.

</dd> <dt>

**SpareByte**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (6)
</dt> </dl>

No se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos eventos producen un gran volumen de eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Conversaciones**](thread.md)
</dt> <dt>

[**Subproceso \_ V2**](thread-v2.md)
</dt> </dl>

 

 




