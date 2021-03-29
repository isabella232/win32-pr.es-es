---
description: El método GetCommandDueFor recupera un comando diferido que está programado en un momento especificado.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Método CCmdQueue. GetCommandDueFor (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678963"
---
# <a name="ccmdqueuegetcommandduefor-method"></a>CCmdQueue. GetCommandDueFor, método

El `GetCommandDueFor` método recupera un comando diferido que se programa en un momento especificado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tStream* 
</dt> <dd>

Hora en la que se programa el comando.

</dd> <dt>

*ppCmd* 
</dt> <dd>

Dirección de un puntero al comando aplazado que se va a realizar en el momento especificado en el parámetro *tStream* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve VFW \_ E \_ no \_ encontrado si no hay ningún comando pendiente; de lo contrario, devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Esta función miembro toma un tiempo de secuencia y devuelve el comando diferido programado en ese momento. El desplazamiento real en tiempo de secuencia se calcula cuando se ejecuta la cola de comandos. Los comandos permanecen en la cola hasta que se ejecutan o se cancelan. Esta función miembro no se bloqueará.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




