---
description: El método CopyPalette copia la paleta de cualquier estructura de videoinfo en cualquier estructura de videoinformación de paleta.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Método CImagePalette. CopyPalette (Winutil. h)
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
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671543"
---
# <a name="cimagepalettecopypalette-method"></a>CImagePalette. CopyPalette, método

El `CopyPalette` método copia la paleta de cualquier estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) en cualquier estructura de **videoinformación** de paleta.

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

Devuelve S \_ OK si se copió la paleta. Devuelve S \_ false si el tipo de medio de origen o de destino no tiene una paleta.

## <a name="remarks"></a>Observaciones

El tipo de medio *pDest* debe ser un formato de paleta con una profundidad de color de 8 bits o menos. El tipo de medio *pSrc* puede ser cualquier tipo de [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con una paleta, incluidos los formatos YUV y de color verdadero con entradas de paleta. El método copia las entradas de la paleta de *pSrc* en una nueva paleta y asocia la nueva paleta a *pDest*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




