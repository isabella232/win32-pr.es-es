---
description: El método IsQueued determina si el objeto está utilizando un subproceso de trabajo para proporcionar ejemplos.
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: Método COutputQueue. IsQueued (Outputq. h)
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
ms.openlocfilehash: 47093acedb3a28d633ea2c8b0bbdbba3c1493de7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670601"
---
# <a name="coutputqueueisqueued-method"></a>COutputQueue. IsQueued, método

El `IsQueued` método determina si el objeto está utilizando un subproceso de trabajo para proporcionar ejemplos.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsQueued();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el objeto está utilizando un subproceso de trabajo o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




