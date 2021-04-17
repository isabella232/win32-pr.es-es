---
description: El método DeliverEndOfStream entrega una notificación de final de secuencia al pin de entrada conectado.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Método CBaseOutputPin. DeliverEndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 334101c9b61631a35c5da91bd398cb7742d39235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661164"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a>CBaseOutputPin. DeliverEndOfStream, método

El `DeliverEndOfStream` método entrega una notificación de final de secuencia al pin de entrada conectado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>              |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | El PIN no está conectado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método llama al método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el PIN de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




