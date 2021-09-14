---
description: Marca que indica si hay una operación de desa confirmación en curso.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: CBaseAllocator::m_bDecommitInProgress miembro (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070158"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a>Miembro CBaseAllocator::m \_ bDecommitInProgress

Marca que indica si hay una operación de desa confirmación en curso. El valor es **TRUE después** de llamar al método [**CBaseAllocator::D ecommit,**](cbaseallocator-decommit.md) pero antes de que se hayan liberado todos los búferes. Si el valor es **TRUE**, se produce un error en el método [**CBaseAllocator::GetBuffer.**](cbaseallocator-getbuffer.md) Además, el asignador no debe eliminarse a sí mismo mientras el valor sea **TRUE.**

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




