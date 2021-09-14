---
description: El método UsingDifferentAllocators determina si los pins de entrada y salida usan asignadores diferentes.
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
ms.openlocfilehash: f20802836adb665614e2bbfb8cb79bdccd5a36ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255314"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a>CTransInPlaceFilter.UsingDifferentAllocators (método)

El `UsingDifferentAllocators` método determina si los pins de entrada y salida usan asignadores diferentes.

## <a name="syntax"></a>Sintaxis


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si las patillas de entrada y salida usan asignadores diferentes o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




