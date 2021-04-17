---
description: 'El método EndFlush finaliza una operación de vaciado. Este método invalida el método CTransformFilter:: EndFlush.'
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Método CVideoTransformFilter. EndFlush (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca160bd2e3e66df3bcf6f293abe6f828309172c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660929"
---
# <a name="cvideotransformfilterendflush-method"></a>CVideoTransformFilter. EndFlush, método

El `EndFlush` método finaliza una operación de vaciado. Este método invalida el método [**CTransformFilter:: EndFlush**](ctransformfilter-endflush.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o un código de error.

## <a name="remarks"></a>Observaciones

Este método restablece todas las medidas de rendimiento internas del filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




