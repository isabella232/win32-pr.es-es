---
description: Valor booleano que especifica si se va a realizar el seguimiento de este bloqueo.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Miembro CCritSec:: m_fTrace (Wxutil. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661239"
---
# <a name="ccritsecm_ftrace-member"></a>Miembro fTrace CCritSec:: m \_

Valor booleano que especifica si se va a realizar el seguimiento de este bloqueo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Observaciones

Esta variable miembro solo se define en la versión de depuración de la clase base. Si el valor es **true**, se escribe un seguimiento del estado de bloqueo en el registro de depuración. (El registro de depuración de las secciones críticas debe estar activo). Para obtener más información, vea [**DbgLockTrace**](dbglocktrace.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCritSec**](ccritsec.md)
</dt> </dl>

 

 




