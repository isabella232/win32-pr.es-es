---
description: Valor booleano que especifica si se debe hacer un seguimiento de este bloqueo.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: CCritSec::m_fTrace miembro (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072278"
---
# <a name="ccritsecm_ftrace-member"></a>Miembro CCritSec::m \_ fTrace

Valor booleano que especifica si se debe hacer un seguimiento de este bloqueo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Observaciones

Esta variable miembro solo se define en la versión de depuración de la clase base. Si el valor es **TRUE**, se escribe un seguimiento del estado de bloqueo en el registro de depuración. (El registro de depuración de las secciones críticas debe estar activo). Para obtener más información, [**vea DbgLockTrace**](dbglocktrace.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CCritSec (clase)**](ccritsec.md)
</dt> </dl>

 

 




