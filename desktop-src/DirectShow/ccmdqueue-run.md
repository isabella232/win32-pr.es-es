---
description: El método Run cambia al modo de ejecución para que se puedan ejecutar los comandos diferidos por tiempo de secuencia.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: Método CCmdQueue. Run (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678957"
---
# <a name="ccmdqueuerun-method"></a>CCmdQueue. Run (método)

El `Run` método cambia al modo de ejecución para que se puedan ejecutar los comandos diferidos por tiempo de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tStreamTimeOffset* 
</dt> <dd>

Hora de desplazamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Durante el modo de ejecución, se conoce la asignación del tiempo de espera de la presentación de la secuencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




