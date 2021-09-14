---
description: 'Constructor CCritSec.CCritSec: método constructor.'
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Constructor CCritSec.CCritSec (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de2b852ffc9a12622a4560ae834a3347b1e07552
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072280"
---
# <a name="ccritsecccritsec-constructor"></a>Constructor CCritSec.CCritSec

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec();
```



## <a name="parameters"></a>Parámetros

Este constructor no tiene parámetros.

## <a name="remarks"></a>Observaciones

Este método llama a la [**función InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) para inicializar la sección crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CCritSec (clase)**](ccritsec.md)
</dt> </dl>

 

