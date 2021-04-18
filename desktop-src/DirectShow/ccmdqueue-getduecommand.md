---
description: El método GetDueCommand recupera un puntero al siguiente comando que se debe a.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Método CCmdQueue. GetDueCommand (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660170"
---
# <a name="ccmdqueuegetduecommand-method"></a>CCmdQueue. GetDueCommand, método

El `GetDueCommand` método recupera un puntero al siguiente comando que se debe a.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppCmd* 
</dt> <dd>

Dirección de un puntero al comando aplazado.

</dd> <dt>

*msTimeout* 
</dt> <dd>

Cantidad de tiempo que hay que esperar antes de que se agote el tiempo de espera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ Abort si se agota el tiempo de espera. Devuelve \_ si es correcto; de lo contrario, devuelve un error. Devuelve un objeto que se ha incrementado mediante **IUnknown:: AddRef**.

## <a name="remarks"></a>Observaciones

Esta función miembro se bloquea hasta que se venza un comando pendiente. La función miembro se bloquea durante el tiempo, en milisegundos, especificado en el parámetro *msTimeout* . Los comandos de tiempo de secuencia solo se deben realizar entre las funciones miembro [**CCmdQueue:: Run**](ccmdqueue-run.md) y [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) . El comando permanece en cola hasta que se ejecuta o se cancela.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




