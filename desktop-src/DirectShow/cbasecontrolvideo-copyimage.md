---
description: Crea una copia de la memoria de una imagen.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Método CBaseControlVideo. CopyImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660528"
---
# <a name="cbasecontrolvideocopyimage-method"></a>CBaseControlVideo. CopyImage, método

Crea una copia de la memoria de una imagen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero al ejemplo que contiene la imagen de vídeo.

</dd> <dt>

*pVideoInfo* 
</dt> <dd>

Puntero al formato que representa la imagen de vídeo.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Puntero al tamaño del búfer de salida.

</dd> <dt>

*pVideoImage* 
</dt> <dd>

Puntero al búfer de salida.

</dd> <dt>

*pSourceRect* 
</dt> <dd>

Puntero al rectángulo de vídeo de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el parámetro *pVideoImage* es **null**, el parámetro *pBufferSize* se rellena con el número de bytes que necesita el búfer de salida para almacenar la imagen. Si el búfer pasado es demasiado pequeño o la función miembro no puede asignar memoria suficiente, la función miembro devuelve E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La función miembro recupera la imagen de la muestra y la copia en el búfer de salida. La sección de vídeo copiada en el búfer de salida refleja el rectángulo de origen que se establece a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) (aunque no refleja el rectángulo de destino).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




