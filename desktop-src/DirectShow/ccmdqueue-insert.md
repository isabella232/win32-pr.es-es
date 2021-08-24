---
description: El método Insert agrega un objeto CDeferredCommand a la cola.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Método CCmdQueue.Insert (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90e2bab4a3545e8a02315155ad4a477511ecf961c93a511ccba268b7fde7dd0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757325"
---
# <a name="ccmdqueueinsert-method"></a>Método CCmdQueue.Insert

El `Insert` método agrega un objeto [**CDeferredCommand**](cdeferredcommand.md) a la cola.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCmd* 
</dt> <dd>

Puntero al **objeto CDeferredCommand** que se agrega a la cola.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK en la implementación predeterminada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCmdQueue (clase)**](ccmdqueue.md)
</dt> </dl>

 

 




