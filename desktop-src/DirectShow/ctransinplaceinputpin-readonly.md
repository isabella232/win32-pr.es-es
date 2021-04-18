---
description: El método ReadOnly indica si el flujo de entrada es de solo lectura.
ms.assetid: 25b8230d-be2b-4129-a1aa-f6b36e95199e
title: Método CTransInPlaceInputPin. ReadOnly (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.ReadOnly
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33e71f8fd0aa7bf37f76ed6446fb5132c1808fb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679251"
---
# <a name="ctransinplaceinputpinreadonly-method"></a>CTransInPlaceInputPin. ReadOnly (método)

El `ReadOnly` método indica si el flujo de entrada es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
const BOOL ReadOnly();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de la variable de miembro [**m \_ bReadOnly**](ctransinplaceinputpin-m-breadonly.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




