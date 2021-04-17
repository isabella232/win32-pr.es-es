---
description: 'El método IsSyncPoint determina si el principio del ejemplo es un punto de sincronización. Este método implementa el método IMediaSample:: IsSyncPoint.'
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Método CMediaSample. IsSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8cc93c03ce3b864e1c1b0a5794d711b1b0c3d68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670472"
---
# <a name="cmediasampleissyncpoint-method"></a>CMediaSample. IsSyncPoint, método

El `IsSyncPoint` método determina si el principio del ejemplo es un punto de sincronización. Este método implementa el método [**IMediaSample:: IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el ejemplo es un punto de sincronización o S \_ false en caso contrario.

## <a name="remarks"></a>Observaciones

La variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




