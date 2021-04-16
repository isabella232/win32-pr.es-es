---
description: El método Set señala el evento.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: Método CAMEvent. set (Wxutil. h)
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
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671424"
---
# <a name="cameventset-method"></a>CAMEvent. set (método)

El `Set` método señala el evento.

## <a name="syntax"></a>Sintaxis


```C++
void Set();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El comportamiento depende de si el objeto es un evento de restablecimiento automático o un evento de restablecimiento manual:

-   **Restablecimiento automático**: Si algún subproceso está esperando en este evento, se libera un subproceso y se restablece el evento. Si no hay ningún subproceso esperando en este evento, el evento permanece señalado.
-   **Restablecimiento manual**: se liberan todos los subprocesos que esperan en este evento. El evento permanece señalado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMEvent**](camevent.md)
</dt> </dl>

 

 




