---
description: El método Check comprueba si el evento está establecido, sin bloquear.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: Método CAMEvent.Check (Wxutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161652"
---
# <a name="cameventcheck-method"></a>Método CAMEvent.Check

El `Check` método comprueba si el evento está establecido, sin bloquear.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Check();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Observaciones

Devuelve **TRUE** si se establece el evento o **FALSE** en caso contrario. Este método llama al [**método CAMEvent::Wait**](camevent-wait.md) con un tiempo de espera de cero. Si el objeto es un evento de restablecimiento automático, este método restablece el evento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMEvent**](camevent.md)
</dt> </dl>

 

 




