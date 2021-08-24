---
description: 'Método CTransformInputPin.CurrentMediaType: el método CurrentMediaType recupera el tipo de medio para la conexión de pin actual.'
ms.assetid: d46f4d8e-9e9d-49d3-b823-f2f0fcf25383
title: Método CTransformInputPin.CurrentMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e313cc132f325b57a09e2b8609bc14f052aaaac69187ac4468ee1d5471d2442
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053585"
---
# <a name="ctransforminputpincurrentmediatype-method"></a>Método CTransformInputPin.CurrentMediaType

El `CurrentMediaType` método recupera el tipo de medio para la conexión de pin actual.

## <a name="syntax"></a>Sintaxis


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia a la variable [**miembro CBasePin::m \_ mt.**](cbasepin-m-mt.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




