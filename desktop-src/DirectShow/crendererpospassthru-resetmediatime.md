---
description: El método ResetMediaTime restablece las marcas de tiempo almacenadas en caché a cero.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Método CRendererPosPassThru. ResetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660450"
---
# <a name="crendererpospassthruresetmediatime-method"></a>CRendererPosPassThru. ResetMediaTime, método

El `ResetMediaTime` método restablece las marcas de tiempo almacenadas en caché a cero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El filtro debe llamar a este método siempre que las marcas de tiempo almacenadas en caché por el método [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) dejen de ser válidas. En concreto, debe llamar a este método en respuesta a los métodos [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) y [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

Después de llamar a este método, el método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) devuelve cero para las horas de inicio y finalización.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




