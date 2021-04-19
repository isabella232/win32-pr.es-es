---
description: El método DrawVideoImageHere dibuja una imagen de un ejemplo multimedia en un contexto de dispositivo especificado.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Método CDrawImage. DrawVideoImageHere (Winutil. h)
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
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660457"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a>CDrawImage. DrawVideoImageHere, método

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

*cámaras* 
</dt> <dd>

Identificador de un contexto de dispositivo, donde se producirá el dibujo.

</dd> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo que contiene la imagen.

</dd> <dt>

*lprcSrc* 
</dt> <dd>

Puntero a un rectángulo de origen que se va a utilizar para dibujar. Si es **null**, se usa el rectángulo en [**CDrawImage:: m \_ SourceRect**](cdrawimage-m-sourcerect.md) .

</dd> <dt>

*lprcDst* 
</dt> <dd>

Puntero a un rectángulo de destino que se va a utilizar para dibujar. Si es **null**, se usa el rectángulo en [**CDrawImage:: m \_ TargetRect**](cdrawimage-m-targetrect.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true si es** correcto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




