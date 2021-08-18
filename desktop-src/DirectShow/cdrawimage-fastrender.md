---
description: El método FastRender dibuja la imagen de vídeo mediante las funciones BitBlt o StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Método CDrawImage.FastRender (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146c3736f7aaa89fc9a724d9dd7e4bfb58160e21e2de57f40a8e855c8a3c1446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043615"
---
# <a name="cdrawimagefastrender-method"></a>Método CDrawImage.FastRender

El `FastRender` método dibuja la imagen de vídeo mediante las funciones **BitBlt** **o StretchBlt.**

## <a name="syntax"></a>Sintaxis


```C++
void FastRender(
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

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El [**método CDrawImage::D rawImage**](cdrawimage-drawimage.md) llama a este método, pero solo si el asignador de la conexión es un [**objeto CImageAllocator.**](cimageallocator.md) En ese caso, se garantiza que el ejemplo multimedia es un [**objeto CImageSample.**](cimagesample.md) El **objeto CImageSample** usa la función **CreateDIBSection** para asignar memoria compartida para el mapa de bits, lo que permite dibujar la imagen mediante **BitBlt** o **StretchBlt.**

Este método llama a **BitBlt si** los rectángulos de origen y targer coinciden exactamente, o **StretchBlt en caso** contrario.

Si el filtro no es propietario del asignador, el **método DrawImage** usa [**CDrawImage::SlowRender**](cdrawimage-slowrender.md) para dibujar la imagen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> </dl>

 

 




