---
description: El método FastRender dibuja la imagen de vídeo mediante las funciones BitBlt o StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Método CDrawImage. FastRender (Winutil. h)
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
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670734"
---
# <a name="cdrawimagefastrender-method"></a>CDrawImage. FastRender, método

El `FastRender` método dibuja la imagen de vídeo mediante las funciones **bitblt** o **StretchBlt** .

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

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo que contiene la imagen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método [**CDrawImage::D rawimage**](cdrawimage-drawimage.md) llama a este método, pero solo si el asignador de la conexión es un objeto [**CImageAllocator**](cimageallocator.md) . En ese caso, se garantiza que el ejemplo multimedia es un objeto [**CImageSample**](cimagesample.md) . El objeto **CImageSample** usa la función **CreateDIBSection** para asignar la memoria compartida para el mapa de bits, lo que permite dibujar la imagen mediante **bitblt** o **StretchBlt**.

Este método llama a **bitblt** si los rectángulos de origen y destino coinciden exactamente, o **StretchBlt** en caso contrario.

Si el filtro no posee el asignador, el método **DrawImage** usa [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md) para dibujar la imagen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




