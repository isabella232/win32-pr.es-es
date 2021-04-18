---
description: Método de destructor.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: CCritSec. ~ CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21029e2d53fd03ded2be4faa98e8b3e27681600c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680754"
---
# <a name="ccritsecccritsec-destructor"></a>CCritSec. ~ CCritSec (destructor)

Método de destructor.

## <a name="syntax"></a>Sintaxis


```C++
~CCritSec();
```



## <a name="remarks"></a>Observaciones

Este método llama a la función [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) para eliminar la sección crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCritSec**](ccritsec.md)
</dt> </dl>

 

