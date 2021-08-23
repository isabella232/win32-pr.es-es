---
description: El método Remove quita el objeto CDeferredCommand de la cola.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Método CCmdQueue.Remove (Winutil.h)
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
ms.openlocfilehash: 6d0b0a4b416c5adb97b1a9efba1fbd5f6142b0e0fb761c6d4c0b277ac0cda7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954584"
---
# <a name="ccmdqueueremove-method"></a>Método CCmdQueue.Remove

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

Puntero al objeto **CDeferredCommand** que se quitará de la cola.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve VFW \_ E NOT FOUND si el objeto no se encuentra en la \_ \_ cola. De lo contrario, devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCmdQueue (clase)**](ccmdqueue.md)
</dt> </dl>

 

 




