---
description: El método ShouldSkipFrame determina si el filtro debe quitar una muestra especificada.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Método CVideoTransformFilter.ShouldSkipFrame (Vtrans.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266439"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a>CVideoTransformFilter.ShouldSkipFrame (método)

El `ShouldSkipFrame` método determina si el filtro debe quitar un ejemplo especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*anclar* 
</dt> <dd>

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el filtro debe quitar este ejemplo, o **FALSE** si el filtro debe procesar este ejemplo.

## <a name="remarks"></a>Observaciones

Este método devuelve **TRUE si** se cumplen las condiciones siguientes:

-   El ejemplo tiene marcas de tiempo.
-   El tiempo medio de lacodación es al menos el 25 % de la duración del fotograma.
-   Actualmente, el representador tiene al menos un fotograma de retraso, como se notifica a través de mensajes de calidad.
-   Omitir al siguiente fotograma clave no provocaría que el fotograma llegara más de un fotograma antes.

Para los fines de este cálculo, el filtro registra la siguiente información a medida que procesa los datos:

-   El tiempo medio de descodificación de los últimos 20 fotogramas **(m \_ itrAvgDecode)**
-   Número de fotogramas desde el último fotograma clave (**m \_ nFramesSinceKeyFrame**)
-   Una estimación de cuántos fotogramas hay entre fotogramas clave (**m \_ nKeyFramePeriod**)

Una vez que el filtro quita un marco, continúa quitando fotogramas hasta que alcanza el siguiente fotograma clave. Si este método devuelve **TRUE**, también envía un evento [**EC QUALITY \_ \_ CHANGE**](ec-quality-change.md) al Administrador de Graph Datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CVideoTransformFilter (clase)**](cvideotransformfilter.md)
</dt> </dl>

 

 




