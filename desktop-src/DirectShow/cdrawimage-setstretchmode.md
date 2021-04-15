---
description: El método SetStretchMode calcula si se debe ajustar la imagen de vídeo.
ms.assetid: ffdcaf9c-e157-4557-9193-8430c1c451bf
title: Método CDrawImage. SetStretchMode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetStretchMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a4b3a6b104b9e2888776cc59183835f412fdcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661396"
---
# <a name="cdrawimagesetstretchmode-method"></a>CDrawImage. SetStretchMode, método

El `SetStretchMode` método calcula si se debe ajustar la imagen de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
void SetStretchMode();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La clase **CDrawImage** llama automáticamente a este método cada vez que cambia el rectángulo de origen o de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




