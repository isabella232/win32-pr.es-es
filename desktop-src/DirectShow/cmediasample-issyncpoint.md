---
description: El método IsSyncPoint determina si el principio del ejemplo es un punto de sincronización. Este método implementa el método IMediaSample::IsSyncPoint.
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Método CMediaSample.IsSyncPoint (Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255507"
---
# <a name="cmediasampleissyncpoint-method"></a>Método CMediaSample.IsSyncPoint

El `IsSyncPoint` método determina si el principio del ejemplo es un punto de sincronización. Este método implementa el [**método IMediaSample::IsSyncPoint.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S OK si el ejemplo es un punto de sincronización o S FALSE en \_ \_ caso contrario.

## <a name="remarks"></a>Observaciones

La variable [**miembro CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) especifica esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




