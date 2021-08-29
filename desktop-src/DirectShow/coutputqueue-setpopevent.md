---
description: El método SetPopEvent especifica un evento que se señala cada vez que el objeto quita un ejemplo de la cola.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Método COutputQueue.SetPopEvent (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e499d756d983cbd5849f3178bc3ed26d0d4194bd15e1e220462f86d2f3e9a00e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909445"
---
# <a name="coutputqueuesetpopevent-method"></a>Método COutputQueue.SetPopEvent

El `SetPopEvent` método especifica un evento que se señala cada vez que el objeto quita un ejemplo de la cola.

## <a name="syntax"></a>Sintaxis


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hEvent* 
</dt> <dd>

Controlar un evento creado por el autor de la llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




