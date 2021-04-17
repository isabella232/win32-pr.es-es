---
description: El método check comprueba si el evento está establecido, sin bloqueos.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: Método CAMEvent. check (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670373"
---
# <a name="cameventcheck-method"></a>CAMEvent. check (método)

El `Check` método comprueba si el evento está establecido, sin bloqueos.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Check();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Observaciones

Devuelve **true** si se establece el evento o **false** en caso contrario. Este método llama al método [**CAMEvent:: wait**](camevent-wait.md) con un tiempo de espera de cero. Si el objeto es un evento de restablecimiento automático, este método restablece el evento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMEvent**](camevent.md)
</dt> </dl>

 

 




