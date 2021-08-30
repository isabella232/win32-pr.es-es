---
description: Crea una copia de memoria de una imagen.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Método CBaseControlVideo.CopyImage (Ctlutil.h)
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
ms.openlocfilehash: 20e427a9c8b146dc1398443df06cbb8a3fb58452e3bbabd0a6291428f960a79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057335"
---
# <a name="cbasecontrolvideocopyimage-method"></a>Método CBaseControlVideo.CopyImage

Crea una copia de memoria de una imagen.

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

Si el *parámetro pVideoImage* es **NULL,** el parámetro *pBufferSize* se rellena con el número de bytes que el búfer de salida necesita para almacenar la imagen. Si el búfer pasado es demasiado pequeño o la función miembro no puede asignar suficiente memoria, la función miembro devuelve E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

La función miembro recupera la imagen del ejemplo y la copia en el búfer de salida. La sección de vídeo copiada en el búfer de salida refleja el rectángulo de origen que se establece a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) (aunque no refleja el rectángulo de destino).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




