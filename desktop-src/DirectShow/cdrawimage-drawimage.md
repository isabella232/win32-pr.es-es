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
ms.openlocfilehash: c2791d20b906f2a2adce31ce99b9e7498854c8fca00ade4507db0207e04b2cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043614"
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

## <a name="remarks"></a>Comentarios

Este método delega en [**CDrawImage::FastRender**](cdrawimage-fastrender.md) o [**CDrawImage::SlowRender**](cdrawimage-slowrender.md), en función de si el filtro posee el asignador que proporcionó el ejemplo. Si el filtro posee el asignador, se garantiza que el ejemplo es un [**objeto CImageSample.**](cimagesample.md) En ese caso, el ejemplo usa memoria compartida asignada por GDI y la imagen se puede dibujar mediante **BitBlt** o **StretchBlt**. De lo contrario, las imágenes se deben dibujar mediante las funciones **SetDIBitsToDevice** o **StretchDIBits más lentas.**

En las compilaciones de depuración, este método llama **a DisplaySampleTimes** para dibujar las marcas de tiempo del ejemplo en la imagen de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




