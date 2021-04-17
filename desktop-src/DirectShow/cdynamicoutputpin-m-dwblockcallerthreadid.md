---
description: 'El identificador del subproceso que llamó por última vez al método IPinFlowControl:: Block en este pin. Esta variable miembro solo es válida mientras el PIN está bloqueado.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Miembro CDynamicOutputPin:: m_dwBlockCallerThreadID (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661354"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>Miembro dwBlockCallerThreadID CDynamicOutputPin:: m \_

El identificador del subproceso que llamó por última vez al método [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) en este pin. Esta variable miembro solo es válida mientras el PIN está bloqueado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>Observaciones

Antes de tener acceso a esta variable, conserve la sección crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




