---
description: El método GetSampleSize recupera el tamaño de la muestra.
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: Método CMediaType. GetSampleSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.GetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc5b80e20ad2a16af9c25c68499348ffa744c0fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670318"
---
# <a name="cmediatypegetsamplesize-method"></a>CMediaType. GetSampleSize, método

El `GetSampleSize` método recupera el tamaño de la muestra.

## <a name="syntax"></a>Sintaxis


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el tamaño de la muestra es fijo, devuelve el tamaño de ejemplo en bytes. De lo contrario, devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 




