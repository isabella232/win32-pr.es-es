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
ms.openlocfilehash: 011f4eeda7f4a278baeceeadc7c21a822ae02b74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255464"
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



 

 




