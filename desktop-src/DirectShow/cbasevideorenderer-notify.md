---
description: El método Notify recibe una notificación de que se solicita un cambio de calidad.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Método CBaseVideoRenderer.Notify (Renbase.h)
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
ms.openlocfilehash: 8674ecbf7951ca0c208f9ffb50c0e5d9591b16552fda266c7d641905edd09a4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052195"
---
# <a name="cbasevideorenderernotify-method"></a>CBaseVideoRenderer.Notify (método)

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

*pSelf* \[ En\]
</dt> <dd>

Puntero al filtro que envía la notificación de calidad.

</dd> <dt>

*q* \[ in\]
</dt> <dd>

Estructura de notificación de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) en el representador de vídeo. Esto se llama, normalmente mediante el administrador de gráficos de filtros, cuando se debe reducir la calidad. Esto puede ocurrir cuando se ha aumentado la calidad de la reproducción de audio hasta el punto de que se debe reducir la calidad de reproducción de vídeo.

`Notify`establece el **miembro de datos m \_ trThrottle** en un valor de retraso que throttleWait va a insertar [**entre fotogramas.**](cbasevideorenderer-throttlewait.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




