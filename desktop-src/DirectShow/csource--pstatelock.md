---
description: El método pStateLock recupera un puntero al objeto de sección crítica del filtro.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: Método CSource.pStateLock (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0705584a513d64dfd1cd17075d95617234f7f8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070045"
---
# <a name="csourcepstatelock-method"></a>Método CSource.pStateLock

El **método pStateLock** recupera un puntero al objeto de sección crítica del filtro.

> [!Note]  
> Aunque se denomina como una variable miembro, **pStateLock** es un método.

 

## <a name="syntax"></a>Sintaxis


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la variable [**miembro CSource::m \_ cStateLock.**](csource-m-cstatelock.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSource (clase)**](csource.md)
</dt> </dl>

 

 




