---
description: El método GetCurrentSample recupera el ejemplo actual.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Método CBaseRenderer. GetCurrentSample (Renbase. h)
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
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660753"
---
# <a name="cbaserenderergetcurrentsample-method"></a>CBaseRenderer. GetCurrentSample, método

El `GetCurrentSample` método recupera el ejemplo actual.

## <a name="syntax"></a>Sintaxis


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo, o **null** si no hay ningún ejemplo disponible.

## <a name="remarks"></a>Observaciones

A menos que el método devuelva **null**, el método llama a **AddRef** en el puntero [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) antes de devolverlo. El llamador debe liberar el puntero. (Por implicación, debe asignar el valor devuelto a una variable para poder publicarlo más adelante).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




