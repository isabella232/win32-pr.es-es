---
description: Estado de bloqueo.
ms.assetid: 55afd314-efd3-47bf-80e3-e17c1332a4cf
title: CDynamicOutputPin::m_BlockState miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockState
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f02a59854b381db5e7b13a85ccca0754cc38f51d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061728"
---
# <a name="cdynamicoutputpinm_blockstate-member"></a>Miembro CDynamicOutputPin::m \_ BlockState

Estado de bloqueo.

## <a name="syntax"></a>Sintaxis


```C++
BLOCK_STATE m_BlockState;
```



## <a name="remarks"></a>Observaciones

Se definen los estados siguientes:

-   NO \_ BLOQUEADO
-   PENDING
-   BLOQUEADO

Antes de acceder a esta variable, mantenga presionada la [**sección crítica CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




