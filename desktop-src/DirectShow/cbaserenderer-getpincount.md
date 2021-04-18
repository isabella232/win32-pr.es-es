---
description: El método GetPinCount recupera el número de clavijas.
ms.assetid: 518de15d-2ecf-425e-b4cd-14aaaf938417
title: Método CBaseRenderer. GetPinCount (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71b3703389019e2217a595884ac983e90835cdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670560"
---
# <a name="cbaserenderergetpincount-method"></a>CBaseRenderer. GetPinCount, método

El `GetPinCount` método recupera el número de clavijas.

## <a name="syntax"></a>Sintaxis


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 1.

## <a name="remarks"></a>Observaciones

Este método implementa el método [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md) , que es virtual puro en la clase **CBaseFilter** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




