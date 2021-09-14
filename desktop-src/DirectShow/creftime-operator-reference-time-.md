---
description: El operador REFERENCE \_ TIME() convierte el objeto a un tipo de datos REFERENCE \_ TIME.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: Método REFERENCE_TIME CRefTime.operator (Reftime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061720"
---
# <a name="creftimeoperator-reference_time-method"></a>Método CRefTime.operator REFERENCE \_ TIME

El `REFERENCE_TIME()` operador convierte el objeto a un tipo de datos REFERENCE [**\_ TIME.**](reference-time.md)

## <a name="syntax"></a>Sintaxis


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de [**CRefTime::m \_ time**](creftime-m-time.md).

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra cómo usar este operador de conversión:


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Reftime.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




