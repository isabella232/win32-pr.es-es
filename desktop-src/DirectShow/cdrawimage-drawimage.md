---
description: El método DrawImage dibuja un fotograma de vídeo en la ventana de vídeo.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Método CDrawImage.DrawImage (Winutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061298"
---
# <a name="cdrawimagedrawimage-method"></a>Método CDrawImage.DrawImage

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

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo que contiene la imagen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="remarks"></a>Observaciones

Este método delega en [**CDrawImage::FastRender**](cdrawimage-fastrender.md) o [**CDrawImage::SlowRender**](cdrawimage-slowrender.md), en función de si el filtro posee el asignador que proporcionó el ejemplo. Si el filtro posee el asignador, se garantiza que el ejemplo es un [**objeto CImageSample.**](cimagesample.md) En ese caso, el ejemplo usa memoria compartida asignada por GDI y la imagen se puede dibujar mediante **BitBlt** o **StretchBlt**. De lo contrario, las imágenes se deben dibujar mediante las funciones **SetDIBitsToDevice** o **StretchDIBits más lentas.**

En las compilaciones de depuración, este método llama **a DisplaySampleTimes** para dibujar las marcas de tiempo del ejemplo en la imagen de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




