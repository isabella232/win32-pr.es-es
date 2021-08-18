---
description: El método CopyPalette copia la paleta de cualquier estructura VIDEOINFO a cualquier estructura VIDEOINFO desenlaizada.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Método CImagePalette.CopyPalette (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5c6f645d134ccf5fa786ff59cf0bc6cd37211af0cb2571bbc9955e5bb6367a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055455"
---
# <a name="cimagepalettecopypalette-method"></a>Método CImagePalette.CopyPalette

El `CopyPalette` método copia la paleta de cualquier estructura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) en cualquier estructura **VIDEOINFO desenlaizada.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrc* 
</dt> <dd>

Puntero al tipo de medio de origen.

</dd> <dt>

*pDest* 
</dt> <dd>

Puntero al tipo de medio de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se copió la paleta. Devuelve S FALSE si el tipo de medio de origen \_ o de destino no tiene una paleta.

## <a name="remarks"></a>Comentarios

El tipo de medio *pDest* debe ser un formato con una profundidad de color de 8 bits o menos. El *tipo de medio pSrc* puede ser cualquier tipo [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con una paleta, incluidos YUV y formatos de color verdadero con entradas de paleta. El método copia las entradas de la paleta de *pSrc* en una nueva paleta y asocia la nueva paleta a *pDest.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImagePalette (clase)**](cimagepalette.md)
</dt> </dl>

 

 




