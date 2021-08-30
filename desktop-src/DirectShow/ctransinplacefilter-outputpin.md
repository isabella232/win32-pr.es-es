---
description: El método OutputPin recupera un puntero al pin de salida del filtro.
ms.assetid: 8c8c125e-553d-43c5-bc63-a0c7d5b01260
title: Método CTransInPlaceFilter.OutputPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.OutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cccd1f6c47488f1330e97a3e5b95b1dbea3a3b5c43b6395dfe6246214109bdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907275"
---
# <a name="ctransinplacefilteroutputpin-method"></a>Método CTransInPlaceFilter.OutputPin

El `OutputPin` método recupera un puntero al pin de salida del filtro.

## <a name="syntax"></a>Sintaxis


```C++
CTransInPlaceOutputPin* OutputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la [**variable miembro CTransformFilter::m \_ pOutput.**](ctransformfilter-m-poutput.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




