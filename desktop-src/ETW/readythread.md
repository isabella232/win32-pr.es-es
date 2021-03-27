---
description: Esta clase es la clase de tipo de evento para eventos de subprocesos listos. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: Clase ReadyThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908104"
---
# <a name="readythread-class"></a>Clase ReadyThread

Esta clase es la clase de tipo de evento para eventos de subprocesos listos.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a>Miembros

La clase **ReadyThread** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **ReadyThread** tiene estas propiedades.

<dl> <dt>

AdjustIncrement
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

Valor por el que se va a ajustar la prioridad.

</dd> <dt>

AdjustReason
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2)
</dt> </dl>

Motivo del aumento de prioridad.



| Value                                                                        | Significado                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Omitir el incremento.<br/>                                                                                        |
| <dl> <dt>1</dt> </dl> | Aplique el incremento, que se detendrá de forma incremental al final de cada Quantum.<br/>                              |
| <dl> <dt>2</dt> </dl> | Aplique el incremento como aumento que determinará en su totalidad en cuanto a Quantum (normalmente para donaciones prioritarias).<br/> |



 

</dd> <dt>

Marca
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4)
</dt> </dl>

A continuación se indican las posibles marcas de estado:



| Value                                                                          | Significado                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0x1</dt> </dl> | El subproceso se ha prepararon de DPC (llamada a procedimiento diferida).<br/> |
| <dl> <dt>0X2</dt> </dl> | La pila de kernel está intercambiada actualmente.<br/>                      |
| <dl> <dt>0x4</dt> </dl> | El espacio de direcciones de proceso se intercambia.<br/>                       |



 

Tenga en cuenta que cuando se intercambia la pila de kernel o el espacio de direcciones de proceso, habrá un evento ReadyThread adicional después de que la pila de kernel o el espacio de direcciones de proceso se haya cambiado de nuevo en y el subproceso esté listo para enviarse.

</dd> <dt>

Reservado
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (5)
</dt> </dl>

Reservado.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), Format ("x")
</dt> </dl>

Identificador del subproceso del subproceso que se va prepararon para su ejecución.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Subproceso \_ V2**](thread-v2.md)
</dt> </dl>

 

 




