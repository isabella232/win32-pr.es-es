---
description: El método IsDiscontinuity determina si este ejemplo representa una interrupción en el flujo de datos. Este método implementa el método IMediaSample::IsDiscontinuity.
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: Método CMediaSample.IsDiscontinuity (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254427"
---
# <a name="cmediasampleisdiscontinuity-method"></a>Método CMediaSample.IsDiscontinuity

El `IsDiscontinuity` método determina si este ejemplo representa una interrupción en el flujo de datos. Este método implementa el [**método IMediaSample::IsDiscontinuity.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el ejemplo es una interrupción en el flujo de datos y S FALSE en caso \_ contrario.

## <a name="remarks"></a>Observaciones

La variable [**miembro CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) especifica esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




