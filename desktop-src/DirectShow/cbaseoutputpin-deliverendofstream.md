---
description: El método DeliverEndOfStream entrega una notificación de fin de flujo al pin de entrada conectado.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Método CBaseOutputPin.DeliverEndOfStream (Amfilter.h)
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
ms.openlocfilehash: c13463ae4effb9fee31ad7c9201ad5af6fd406099c5259c2e6fdff9dcbb62798
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814195"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a>Método CBaseOutputPin.DeliverEndOfStream

El `DeliverEndOfStream` método entrega una notificación de fin de flujo al pin de entrada conectado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>              |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin no está conectado.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método llama al [**método IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el pin de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




