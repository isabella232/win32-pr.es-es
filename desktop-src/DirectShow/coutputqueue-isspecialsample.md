---
description: El método IsSpecialSample determina si los datos en cola son un mensaje de control.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Método COutputQueue.IsSpecialSample (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246765"
---
# <a name="coutputqueueisspecialsample-method"></a>Método COutputQueue.IsSpecialSample

El `IsSpecialSample` método determina si los datos en cola son un mensaje de control.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a un elemento de la cola.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** *pSample* es un mensaje de control o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

El [**método COutputQueue::QueueSample**](coutputqueue-queuesample.md) puede recibir mensajes de control además de ejemplos multimedia. Un mensaje de control es una constante definida (conversión a un tipo LONG PTR) que indica al subproceso \_ que realice una acción. Los mensajes de control no contienen datos multimedia. Para obtener más información, **vea COutputQueue::QueueSample**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




