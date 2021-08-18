---
description: El método UsingDifferentAllocators determina si los pins de entrada y salida usan distintos asignadores.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: Método CTransInPlaceFilter.UsingDifferentAllocators (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0033c0f5ded1fe741d27397078367049d72061c40a993833f714686d9f8a96fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953424"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a>Método CTransInPlaceFilter.UsingDifferentAllocators

El `UsingDifferentAllocators` método determina si las clavijas de entrada y salida usan distintos asignadores.

## <a name="syntax"></a>Sintaxis


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si las clavijas de entrada y salida usan distintos asignadores, o **FALSE en caso** contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




