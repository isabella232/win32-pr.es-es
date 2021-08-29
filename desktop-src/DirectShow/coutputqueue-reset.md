---
description: El método Reset restablece el objeto para que pueda recibir más datos.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: Método COutputQueue.Reset (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4129730ae3ce2f3a95db41d8bc65025c3195056cbd4a1afddbfeb83d9bb33ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073659"
---
# <a name="coutputqueuereset-method"></a>Método COutputQueue.Reset

El `Reset` método restablece el objeto para que pueda recibir más datos.

## <a name="syntax"></a>Sintaxis


```C++
void Reset();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método restablece la variable [**miembro COutputQueue::m \_ hr**](coutputqueue-m-hr.md) a S \_ OK. El objeto puede volver a recibir ejemplos multimedia; por ejemplo, después de una operación de vaciado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




