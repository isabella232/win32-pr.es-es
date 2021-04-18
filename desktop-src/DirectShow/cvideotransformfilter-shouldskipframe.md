---
description: El método ShouldSkipFrame determina si el filtro debe quitar un ejemplo especificado.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Método CVideoTransformFilter. ShouldSkipFrame (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660275"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a>CVideoTransformFilter. ShouldSkipFrame, método

El `ShouldSkipFrame` método determina si el filtro debe quitar un ejemplo especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Agujas* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el filtro debe quitar este ejemplo o **false** si el filtro debe procesar este ejemplo.

## <a name="remarks"></a>Observaciones

Este método devuelve **true** si se cumplen las condiciones siguientes:

-   El ejemplo tiene marcas de tiempo.
-   El tiempo medio de descodificación es al menos el 25% de la duración del fotograma.
-   Actualmente, el representador tiene al menos un fotograma más tarde, como se muestra en los mensajes de calidad.
-   Omitir el fotograma clave siguiente no hará que el fotograma llegue a más de un fotograma al principio.

Para los fines de este cálculo, el filtro registra la siguiente información a medida que procesa los datos:

-   El tiempo medio de descodificación en los 20 últimos fotogramas (**m \_ itrAvgDecode**)
-   Número de fotogramas desde el último fotograma clave (**m \_ nFramesSinceKeyFrame**)
-   Una estimación del número de fotogramas que hay entre fotogramas clave (**m \_ nKeyFramePeriod**)

Una vez que el filtro quita un fotograma, sigue colocando fotogramas hasta que llega al siguiente fotograma clave. Si este método devuelve **true**, también envía un evento [**de \_ \_ cambio de calidad de EC**](ec-quality-change.md) al administrador de gráficos de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




