---
description: El método posponer especifica un nuevo tiempo de presentación para un comando en cola previamente.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Método CDeferredCommand. posponer (Ctlutil. h)
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
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681265"
---
# <a name="cdeferredcommandpostpone-method"></a>CDeferredCommand. posponer (método)

El `Postpone` método especifica un nuevo tiempo de presentación para un comando en cola previamente.

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

Devuelve la \_ hora VFW E \_ \_ ya \_ pasada si *newtime* ya se ha pasado. De lo contrario, devuelve un **valor HRESULT** que es el resultado de una llamada a [**CCmdQueue:: Remove**](ccmdqueue-remove.md) (al extraer de la lista) o [**CCmdQueue:: Insert**](ccmdqueue-insert.md) (al volver a insertar con la hora modificada).

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IDeferredCommand::P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




