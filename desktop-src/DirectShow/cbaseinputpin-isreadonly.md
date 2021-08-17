---
description: Consulta si el asignador usa ejemplos multimedia de solo lectura.
ms.assetid: 2cb692da-f030-4265-afe4-b1608b51fd47
title: Método CBaseInputPin.IsReadOnly (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsReadOnly
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45a8fc563e9377f7308ad9ea702b16f48ea9723aa13902ef29d60e2da903ffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017043"
---
# <a name="cbaseinputpinisreadonly-method"></a>Método CBaseInputPin.IsReadOnly

Consulta si el asignador usa ejemplos multimedia de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsReadOnly();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de la variable [**miembro CBaseInputPin::m \_ bReadOnly.**](cbaseinputpin-m-breadonly.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 




