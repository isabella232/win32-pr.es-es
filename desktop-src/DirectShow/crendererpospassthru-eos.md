---
description: El método EOS actualiza las marcas de tiempo almacenadas en caché después de una notificación de final de secuencia.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: Método CRendererPosPassThru. EOS (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9e6990d946f32b441f0a33ceba8c0a59fdae488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661284"
---
# <a name="crendererpospassthrueos-method"></a>CRendererPosPassThru. EOS, método

El `EOS` método actualiza las marcas de tiempo almacenadas en caché después de una notificación de final de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EOS();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                            | Descripción                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Error. Posiblemente el filtro no se transmite por secuencias.<br/> |



 

## <a name="remarks"></a>Observaciones

El filtro debe llamar a este método cuando recibe una notificación de final de secuencia ([**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)). El método establece las marcas de tiempo almacenadas en caché igual a la posición de detención, asegurándose de que el método [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) devuelva los valores correctos al final de la secuencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




