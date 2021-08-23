---
description: El método IsIdle determina si el objeto está esperando datos.
ms.assetid: be1b5633-f9e9-497e-8b6f-5634eae91273
title: Método COutputQueue.IsIdle (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsIdle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c231e6e9dac3e05be6c01a2f3ebd87b5cdd69b8822a5ce26f930277c457206c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652125"
---
# <a name="coutputqueueisidle-method"></a>Método COutputQueue.IsIdle

El `IsIdle` método determina si el objeto está esperando datos.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsIdle();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** el subproceso está esperando y la matriz de ejemplo está vacía. De lo contrario, **devuelve FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




