---
description: Recupera el identificador del subproceso en el objeto CMsgThread.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: Método CMsgThread. GetThreadHandle (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61d7bfb11f78be3c1d23275589c8cb1c62259bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680347"
---
# <a name="cmsgthreadgetthreadhandle-method"></a>CMsgThread. GetThreadHandle, método

Recupera el identificador del subproceso en el objeto [**CMsgThread**](cmsgthread.md) .

## <a name="syntax"></a>Sintaxis


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del subproceso.

## <a name="remarks"></a>Observaciones

El identificador del subproceso se puede pasar a funciones de espera, como [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects). El identificador del subproceso se señala cuando el subproceso ha salido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMsgThread**](cmsgthread.md)
</dt> </dl>

 

