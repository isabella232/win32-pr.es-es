---
description: Identificador del subproceso que llamó por última vez al método IPinFlowControl::Block en este pin. Esta variable miembro solo es válida mientras el pin está bloqueado.
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: CDynamicOutputPin::m_dwBlockCallerThreadID miembro (Amfilter.h)
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
ms.openlocfilehash: b52bd7f718798ea9dd2cf9d227f6d22e069d2c1a59bb8591f6126c20599af9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539755"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>Miembro CDynamicOutputPin::m \_ dwBlockCallerThreadID

Identificador del subproceso que llamó por última vez al [**método IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) en este pin. Esta variable miembro solo es válida mientras el pin está bloqueado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>Comentarios

Antes de acceder a esta variable, mantenga presionada la sección [**crítica CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




