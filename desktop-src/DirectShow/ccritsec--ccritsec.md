---
description: 'Destructor CCritSec.~CCritSec: método Destructor.'
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Destructor CCritSec.~CCritSec (Wxutil.h)
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
ms.openlocfilehash: 4d34665bb18a6ea9f6e76ad6332a5d7f344993067848c1b5e473893e702b62a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999615"
---
# <a name="ccritsecccritsec-destructor"></a>Destructor CCritSec.~CCritSec

Método destructor.

## <a name="syntax"></a>Sintaxis


```C++
~CCritSec();
```



## <a name="remarks"></a>Comentarios

Este método llama a [**la función DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) para eliminar la sección crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCritSec (clase)**](ccritsec.md)
</dt> </dl>

 

