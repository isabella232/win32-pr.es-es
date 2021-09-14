---
description: El método GetPinCount recupera el número de pines del filtro. Este método implementa el método CBaseFilter::GetPinCount virtual puro.
ms.assetid: 42000814-daee-4f7b-96d2-e09a21fde8cd
title: Método CSource.GetPinCount (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 724798d2b13e8e99bb11b50931be8f630413c24f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070033"
---
# <a name="csourcegetpincount-method"></a>Método CSource.GetPinCount

El `GetPinCount` método recupera el número de pines del filtro. Este método implementa el método [**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md) virtual puro.

## <a name="syntax"></a>Sintaxis


```C++
int GetPinCount();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el número de pines de este filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSource (clase)**](csource.md)
</dt> </dl>

 

 




