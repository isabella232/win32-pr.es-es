---
description: El método GetActualDataLength recupera la longitud de los datos válidos en el búfer. Este método implementa el método IMediaSample::GetActualDataLength.
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Método CMediaSample.GetActualDataLength (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973864"
---
# <a name="cmediasamplegetactualdatalength-method"></a>Método CMediaSample.GetActualDataLength

El `GetActualDataLength` método recupera la longitud de los datos válidos en el búfer. Este método implementa el [**método IMediaSample::GetActualDataLength.**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength)

## <a name="syntax"></a>Sintaxis


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la longitud de los datos válidos, en bytes.

## <a name="remarks"></a>Observaciones

La variable [**miembro CMediaSample::m \_ lActual**](cmediasample-m-lactual.md) especifica esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

