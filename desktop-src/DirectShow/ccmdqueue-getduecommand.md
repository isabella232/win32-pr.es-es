---
description: El método GetDueCommand recupera un puntero al siguiente comando que se debe.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Método CCmdQueue.GetDueCommand (Winutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973901"
---
# <a name="ccmdqueuegetduecommand-method"></a>Método CCmdQueue.GetDueCommand

El `GetDueCommand` método recupera un puntero al siguiente comando que se debe.

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

Dirección de un puntero al comando diferido.

</dd> <dt>

*msTimeout* 
</dt> <dd>

Cantidad de tiempo de espera antes de llevar a cabo el tiempo de espera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ ABORT si se produce un tiempo de espera. Devuelve S \_ OK si se realiza correctamente; de lo contrario, devuelve un error. Devuelve un objeto que se ha incrementado mediante **IUnknown::AddRef**.

## <a name="remarks"></a>Observaciones

Esta función miembro se bloquea hasta que se debe un comando pendiente. La función miembro se bloquea durante la cantidad de tiempo, en milisegundos, especificada en el *parámetro msTimeout.* Los comandos en tiempo de secuencia solo se deben entre las funciones miembro [**CCmdQueue::Run**](ccmdqueue-run.md) y [**CCmdQueue::EndRun.**](ccmdqueue-endrun.md) El comando permanece en cola hasta que se ejecuta o se cancela.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CCmdQueue (clase)**](ccmdqueue.md)
</dt> </dl>

 

 




