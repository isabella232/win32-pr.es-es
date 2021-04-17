---
description: El método Remove quita el objeto CDeferredCommand de la cola.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Método CCmdQueue. Remove (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661247"
---
# <a name="ccmdqueueremove-method"></a>CCmdQueue. Remove (método)

El `Remove` método quita el objeto [**CDeferredCommand**](cdeferredcommand.md) de la cola.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCmd* 
</dt> <dd>

Puntero al objeto **CDeferredCommand** que se va a quitar de la cola.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve VFW \_ E \_ no \_ encontrado si el objeto no se encuentra en la cola. De lo contrario, devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




