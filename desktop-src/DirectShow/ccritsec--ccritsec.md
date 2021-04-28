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
ms.openlocfilehash: 6f282bfe6ea6bca8cb8553572c18cfbc85db6c77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095813"
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
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Streams.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CCritSec (clase)**](ccritsec.md)
</dt> </dl>

 

