---
description: El método SetPopEvent especifica un evento que se señaliza cada vez que el objeto quita un ejemplo de la cola.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Método COutputQueue. SetPopEvent (Outputq. h)
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
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678971"
---
# <a name="coutputqueuesetpopevent-method"></a>COutputQueue. SetPopEvent, método

El `SetPopEvent` método especifica un evento que se señaliza cada vez que el objeto quita un ejemplo de la cola.

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

Identificador de un evento creado por el autor de la llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




