---
description: Valor booleano que especifica si se debe hacer un seguimiento de este bloqueo.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: Miembro CCritSec::m_fTrace (Wxutil.h)
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
ms.openlocfilehash: f5a47437e4f9ab475b64979ec970604ac7a621d2ab53ea7a3c87742fa81a8aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074399"
---
# <a name="ccritsecm_ftrace-member"></a>Miembro CCritSec::m \_ fTrace

Valor booleano que especifica si se debe hacer un seguimiento de este bloqueo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Comentarios

Esta variable miembro solo se define en la versión de depuración de la clase base. Si el valor es **TRUE**, se escribe un seguimiento del estado de bloqueo en el registro de depuración. (El registro de depuración de las secciones críticas debe estar activo). Para obtener más información, [**vea DbgLockTrace.**](dbglocktrace.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCritSec (clase)**](ccritsec.md)
</dt> </dl>

 

 




