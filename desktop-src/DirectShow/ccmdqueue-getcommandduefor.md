---
description: El método GetCommandDueFor recupera un comando aplazado que se programa en un momento especificado.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Método CCmdQueue.GetCommandDueFor (Winutil.h)
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
ms.openlocfilehash: c290c5fac2bdf5fd0591a0b088189182638f6b796506361a288fadffe695a85d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757345"
---
# <a name="ccmdqueuegetcommandduefor-method"></a>Método CCmdQueue.GetCommandDueFor

El `GetCommandDueFor` método recupera un comando aplazado que se programa a la hora especificada.

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

Hora para la que se programa el comando.

</dd> <dt>

*ppCmd* 
</dt> <dd>

Dirección de un puntero al comando diferido que se va a llevar a cabo en el momento especificado en el *parámetro tStream.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve VFW \_ E NOT FOUND si no hay ningún comando \_ \_ debido; de lo contrario, devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Esta función miembro toma un tiempo de secuencia y devuelve el comando aplazado programado en ese momento. El desplazamiento real del tiempo de transmisión se calcula cuando se ejecuta la cola de comandos. Los comandos permanecen en cola hasta que se ejecutan o se cancelan. Esta función miembro no se bloqueará.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCmdQueue (clase)**](ccmdqueue.md)
</dt> </dl>

 

 




