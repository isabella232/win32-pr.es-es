---
description: El método wait se bloquea hasta que se señale el evento o hasta que se agote el tiempo de espera.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Método CAMEvent. Wait (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661053"
---
# <a name="cameventwait-method"></a>CAMEvent. Wait (método)

El `Wait` método se bloquea hasta que se señale el evento o hasta que se agote el tiempo de espera.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwTimeout* 
</dt> <dd>

Valor de tiempo de espera opcional, representado en milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el evento se señala. De lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

En el caso de los eventos de restablecimiento automático, el evento se restablece a un estado no señalizado cuando este método devuelve.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMEvent**](camevent.md)
</dt> </dl>

 

 




