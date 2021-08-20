---
description: El método GetCurrentSample recupera el ejemplo actual.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Método CBaseRenderer.GetCurrentSample (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ffe3cdf95d5ab248956e670c04572140fa4621fff5b0cb5183f9a7cbd9b837e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822726"
---
# <a name="cbaserenderergetcurrentsample-method"></a>Método CBaseRenderer.GetCurrentSample

El `GetCurrentSample` método recupera el ejemplo actual.

## <a name="syntax"></a>Sintaxis


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo o **NULL** si no hay ninguna muestra disponible.

## <a name="remarks"></a>Comentarios

A menos que el método **devuelva NULL,** el método llama **a AddRef** en el [**puntero IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) antes de devolverlo. El autor de la llamada debe liberar el puntero. (Por implicación, debe asignar el valor devuelto a una variable para que pueda liberarlo más adelante).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




