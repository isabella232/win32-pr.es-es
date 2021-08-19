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
ms.openlocfilehash: 67d41c23e45ba65416a0f57336e51d2784b194ee556a778b7036e8dc5fd829ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016393"
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

## <a name="remarks"></a>Comentarios

La variable [**miembro CMediaSample::m \_ lActual**](cmediasample-m-lactual.md) especifica esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

