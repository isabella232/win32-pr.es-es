---
description: El método SlowRender dibuja la imagen de vídeo con las funciones SetDIBitsToDevice o StretchDIBits.
ms.assetid: e1d8b189-b588-48eb-988a-3e5dedb38dbd
title: Método CDrawImage. SlowRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SlowRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b736bf6c44d4ada6e0a28408c449c9f8b2f1e1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660454"
---
# <a name="cdrawimageslowrender-method"></a>CDrawImage. SlowRender, método

El `SlowRender` método dibuja la imagen de vídeo mediante las funciones **SetDIBitsToDevice** o **StretchDIBits** .

## <a name="syntax"></a>Sintaxis


```C++
void SlowRender(
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

Si [**CDrawImage:: UsingImageAllocator**](cdrawimage-usingimageallocator.md) devuelve **false**, el método [**CDrawImage::D rawimage**](cdrawimage-drawimage.md) usa `SlowRender` para dibujar la imagen de vídeo. De lo contrario, DrawImage usa el método **FastRender** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::FastRender**](cdrawimage-fastrender.md)
</dt> </dl>

 

 




