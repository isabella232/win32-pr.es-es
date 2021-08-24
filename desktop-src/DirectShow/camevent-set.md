---
description: El método Set señala el evento.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: Método CAMEvent.Set (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 84059a66a77744b7ea570473474f6b773beae8005b7c4a68e73e59c76829f13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794285"
---
# <a name="cameventset-method"></a>Método CAMEvent.Set

El `Set` método señala el evento .

## <a name="syntax"></a>Sintaxis


```C++
void Set();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El comportamiento depende de si el objeto es un evento de restablecimiento automático o un evento de restablecimiento manual:

-   **Restablecimiento automático:** si algún subproceso está esperando este evento, se libera un subproceso y se restablece el evento. Si no hay subprocesos esperando a este evento, el evento permanece señalado.
-   **Restablecimiento manual:** se liberan todos los subprocesos que esperan este evento. El evento permanece señalado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMEvent**](camevent.md)
</dt> </dl>

 

 




