---
description: El método DrawVideoImageHere dibuja una imagen de un ejemplo multimedia en un contexto de dispositivo especificado.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Método CDrawImage.DrawVideoImageHere (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8137c4e18708ce6a0402d1d34caf9560054f267d8de0280a6efb5c3dd36e6517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909815"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a>Método CDrawImage.DrawVideoImageHere

El `DrawVideoImageHere` método dibuja una imagen de un ejemplo multimedia en un contexto de dispositivo especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hdc* 
</dt> <dd>

Identificador de un contexto de dispositivo, donde se producirá el dibujo.

</dd> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo que contiene la imagen.

</dd> <dt>

*lprcSrc* 
</dt> <dd>

Puntero a un rectángulo de origen que se usará para dibujar. Si **es NULL,** se usa [**el rectángulo de CDrawImage::m \_ SourceRect.**](cdrawimage-m-sourcerect.md)

</dd> <dt>

*lprcDst* 
</dt> <dd>

Puntero a un rectángulo de destino que se usará para dibujar. Si **es NULL,** se usa [**el rectángulo de CDrawImage::m \_ TargetRect.**](cdrawimage-m-targetrect.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> </dl>

 

 




