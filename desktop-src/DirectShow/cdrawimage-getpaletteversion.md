---
description: El método GetPaletteVersion recupera la versión actual de la paleta.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: Método CDrawImage.GetPaletteVersion (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14cc4df95507a0c28bd61ec6db405f01353f9228419d0da84c4fc9fc35ca6b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537295"
---
# <a name="cdrawimagegetpaletteversion-method"></a>Método CDrawImage.GetPaletteVersion

El `GetPaletteVersion` método recupera la versión actual de la paleta.

## <a name="syntax"></a>Sintaxis


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de la variable **miembro m \_ PaletteVersion.**

## <a name="remarks"></a>Comentarios

El valor devuelto por este método solo se aplica cuando el asignador es un [**objeto CImageAllocator.**](cimageallocator.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[**CDrawImage::ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




