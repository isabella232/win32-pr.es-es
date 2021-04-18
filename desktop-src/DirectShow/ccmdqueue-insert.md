---
description: El método Insert agrega un objeto CDeferredCommand a la cola.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Método CCmdQueue. Insert (Winutil. h)
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
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660169"
---
# <a name="ccmdqueueinsert-method"></a>CCmdQueue. Insert (método)

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

Puntero al objeto **CDeferredCommand** que se va a agregar a la cola.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK en la implementación predeterminada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




