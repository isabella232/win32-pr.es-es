---
description: Esta clase es la clase de tipo de evento para los eventos de cambio de contexto. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: CSwitch (clase)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063150"
---
# <a name="cswitch-class"></a>CSwitch (clase)

Esta clase es la clase de tipo de evento para los eventos de cambio de contexto.

La sintaxis siguiente se simplifica a partir del código MOF.

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

## <a name="members"></a>Members

La **clase CSwitch** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CSwitch** tiene estas propiedades.

<dl> <dt>

**NewThreadId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Format("x")
</dt> </dl>

Nuevo identificador de subproceso después del modificador.

</dd> <dt>

**NewThreadPriority**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

Prioridad de subproceso del nuevo subproceso.

</dd> <dt>

**NewThreadWaitTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(11), Format("x")
</dt> </dl>

Tiempo de espera para el nuevo subproceso.

</dd> <dt>

**OldThreadId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Format("x")
</dt> </dl>

Identificador de subproceso anterior.

</dd> <dt>

**OldThreadPriority**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4)
</dt> </dl>

Prioridad del subproceso anterior.

</dd> <dt>

**OldThreadState**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(9)
</dt> </dl>

Estado del subproceso anterior. Estos son los valores de estado posibles:

| State | Descripción                                   |
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

Calificadores: WmiDataId(10), Format("x")
</dt> </dl>

Tiempo de espera ideal del subproceso anterior.

</dd> <dt>

**OldThreadWaitMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(8)
</dt> </dl>

Modo de espera para el subproceso anterior. Los posibles valores son los siguientes:

| State | Descripción |
|-------|-------------|
| 0     | KernelMode  |
| 1     | UserMode    |



 

</dd> <dt>

**OldThreadWaitReason**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(7)
</dt> </dl>

Motivo de espera del subproceso anterior. Los posibles valores son los siguientes:

| State | Descripción       |
|-------|-------------------|
| 0     | Ejecutivo         |
| 1     | FreePage          |
| 2     | PageIn            |
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

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(5)
</dt> </dl>

Índice del estado C que usó por última vez el procesador. Un valor de 0 representa el estado de inactividad más claro con valores más altos que representan estados C más profundos.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(12)
</dt> </dl>

Reservado.

</dd> <dt>

**SpareByte**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(6)
</dt> </dl>

No se usa.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos eventos generan un gran volumen de eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Thread**](thread.md)
</dt> <dt>

[**Subproceso \_ V2**](thread-v2.md)
</dt> </dl>

 

 




