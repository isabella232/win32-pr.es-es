---
description: El método Notify recibe una notificación que indica que se ha solicitado un cambio de calidad.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Método CBaseVideoRenderer. Notify (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd2b894bf78163a7b2d2387e43ecb5cec76ffdf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660396"
---
# <a name="cbasevideorenderernotify-method"></a>CBaseVideoRenderer. Notify (método)

El `Notify` método recibe una notificación de que se solicita un cambio de calidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSelf* \[ de\]
</dt> <dd>

Puntero al filtro que está enviando la notificación de calidad.

</dd> <dt>

*preguntas y respuestas* \[\]
</dt> <dd>

Estructura de notificación de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) en el representador de vídeo. Esto se llama, normalmente por el administrador de gráficos de filtro, cuando se debe recortar la calidad. Esto puede ocurrir cuando se ha aumentado la calidad de la reproducción de audio hasta el punto en que se debe reducir la calidad de reproducción de vídeo.

`Notify` establece el miembro de datos **m \_ trThrottle** en un valor de retraso que se va a insertar entre los marcos de [**ThrottleWait**](cbasevideorenderer-throttlewait.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




