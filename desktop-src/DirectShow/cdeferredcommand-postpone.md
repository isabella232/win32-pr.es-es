---
description: El método Postpone especifica un nuevo tiempo de presentación para un comando previamente en cola.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Método CDeferredCommand.Postpone (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 079b9f1a852ff0b9eb6e1c38cea6e24e3ee00107ac46ca15e738e1ef9e0eb8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074369"
---
# <a name="cdeferredcommandpostpone-method"></a>CDeferredCommand.Postpone (método)

El `Postpone` método especifica un nuevo tiempo de presentación para un comando previamente en cola.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newtime* 
</dt> <dd>

Nuevo tiempo de presentación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve VFW \_ E TIME ALREADY PASSED si ya se ha pasado \_ \_ \_ *newtime.* De lo contrario, devuelve un **HRESULT** resultante de una llamada a [**CCmdQueue::Remove**](ccmdqueue-remove.md) (al extraer de la lista) o [**CCmdQueue::Insert**](ccmdqueue-insert.md) (al volver a insertar con la hora cambiada).

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IDeferredCommand::P ostpone.**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDeferredCommand (clase)**](cdeferredcommand.md)
</dt> </dl>

 

 




