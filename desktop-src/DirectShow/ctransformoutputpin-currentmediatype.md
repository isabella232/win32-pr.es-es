---
description: 'Método CTransformOutputPin.CurrentMediaType: el método CurrentMediaType recupera el tipo de medio para la conexión de pin actual.'
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: Método CTransformOutputPin.CurrentMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cb40310afb1c22d00a5394c0a0667fc8d22eb03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094913"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a>Método CTransformOutputPin.CurrentMediaType

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
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




