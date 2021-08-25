---
description: El método IsQueued determina si el objeto usa un subproceso de trabajo para entregar ejemplos.
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: Método COutputQueue.IsQueued (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e261127e16cd1190fb711d81a9f5fd5606738b7f9a3f8697902170662b99f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813585"
---
# <a name="coutputqueueisqueued-method"></a>Método COutputQueue.IsQueued

El `IsQueued` método determina si el objeto usa un subproceso de trabajo para entregar ejemplos.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsQueued();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el objeto usa un subproceso de trabajo o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




