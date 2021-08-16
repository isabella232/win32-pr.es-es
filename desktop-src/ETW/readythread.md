---
description: Esta clase es la clase de tipo de evento para los eventos de subproceso listos. La sintaxis siguiente se simplifica a partir del código MOF.
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
ms.openlocfilehash: 1b4b3d63b63e4deb9c48f9e117122f021e9d63791292e60da3cc919a6e4535e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069815"
---
# <a name="readythread-class"></a>Clase ReadyThread

Esta clase es la clase de tipo de evento para los eventos de subproceso listos.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase ReadyThread** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase ReadyThread** tiene estas propiedades.

<dl> <dt>

AdjustIncrement
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

Valor por el que se ajusta la prioridad.

</dd> <dt>

AdjustReason
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2)
</dt> </dl>

El motivo del aumento de prioridad.



| Valor                                                                        | Significado                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Omitir el incremento.<br/>                                                                                        |
| <dl> <dt>1</dt> </dl> | Aplique el incremento, que se desintegrará incrementalmente al final de cada cuántico.<br/>                              |
| <dl> <dt>2</dt> </dl> | Aplique el incremento como un aumento que decaerá en su totalidad en lo cuántico (normalmente para la prioridad de la prioridad).<br/> |



 

</dd> <dt>

Marca
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4)
</dt> </dl>

Estas son las posibles marcas de estado:



| Valor                                                                          | Significado                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0x1</dt> </dl> | El subproceso se ha leído de DPC (llamada a procedimiento diferido).<br/> |
| <dl> <dt>0x2</dt> </dl> | La pila de kernel se intercambia actualmente.<br/>                      |
| <dl> <dt>0x4</dt> </dl> | El espacio de direcciones del proceso se intercambia.<br/>                       |



 

Tenga en cuenta que cuando se intercambia la pila del kernel o el espacio de direcciones del proceso, habrá un evento ReadyThread adicional después de que la pila del kernel o el espacio de direcciones del proceso se hayan intercambiado de nuevo y el subproceso esté listo para enviarse.

</dd> <dt>

Reservada
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(5)
</dt> </dl>

Reservado.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Format("x")
</dt> </dl>

Identificador de subproceso del subproceso que se lee para su ejecución.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Subproceso \_ V2**](thread-v2.md)
</dt> </dl>

 

 




