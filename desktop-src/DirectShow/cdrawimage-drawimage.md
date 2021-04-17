---
description: El método DrawImage dibuja un fotograma de vídeo en la ventana de vídeo.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Método CDrawImage. DrawImage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660458"
---
# <a name="cdrawimagedrawimage-method"></a>CDrawImage. DrawImage (método)

El `DrawImage` método dibuja un fotograma de vídeo en la ventana de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL DrawImage(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo que contiene la imagen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Este método delega en [**CDrawImage:: FastRender**](cdrawimage-fastrender.md) o [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md), en función de si el filtro posee el asignador que proporcionó el ejemplo. Si el filtro posee el asignador, se garantiza que el ejemplo es un objeto [**CImageSample**](cimagesample.md) . En ese caso, el ejemplo utiliza la memoria compartida asignada por GDI y la imagen se puede dibujar mediante **bitblt** o **StretchBlt**. De lo contrario, las imágenes se deben dibujar con las funciones **SetDIBitsToDevice** o **StretchDIBits** más lentas.

En las compilaciones de depuración, este método llama a **DisplaySampleTimes** para dibujar las marcas de tiempo del ejemplo sobre la imagen de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




