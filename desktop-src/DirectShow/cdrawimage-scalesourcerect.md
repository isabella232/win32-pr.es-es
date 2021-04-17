---
description: El método ScaleSourceRect escala un rectángulo, si hay una diferencia entre el tamaño de vídeo nativo y el formato de tipo de medio.
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: Método CDrawImage. ScaleSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670532"
---
# <a name="cdrawimagescalesourcerect-method"></a>CDrawImage. ScaleSourceRect, método

El `ScaleSourceRect` método escala un rectángulo, si hay una diferencia entre el tamaño de vídeo nativo y el formato de tipo de medio.

## <a name="syntax"></a>Sintaxis


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSource* 
</dt> <dd>

Puntero a un rectángulo sin escala.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el rectángulo escalado.

## <a name="remarks"></a>Observaciones

En la clase **CDrawImage** , este método devuelve *pSource* sin ningún cambio. Puede invalidar este método si el filtro estira la imagen de vídeo entrante. Por ejemplo, el tamaño de vídeo nativo podría ser 320 240, pero el tipo de medio en el PIN de entrada podría ser 640 480. En ese caso, el filtro tendría que escalar el rectángulo de origen en un factor de 2.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




