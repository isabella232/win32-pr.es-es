---
description: La \_ variable miembro m bModifiesData indica si el filtro modifica los datos de ejemplo que se reciben. El valor se establece en el constructor CTransInPlaceFilter, pero el valor predeterminado es TRUE.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: CTransInPlaceFilter::m_bModifiesData miembro (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7461f7f62a6cbd1fea2ff18f6e8f2e4b73825ea04cb9e3b0a679ee7cf15fef90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654884"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a>Miembro CTransInPlaceFilter::m \_ bModifiesData

La `m_bModifiesData` variable miembro indica si el filtro modifica los datos de ejemplo que se reciben. El valor se establece en el constructor **CTransInPlaceFilter,** pero el valor predeterminado es **TRUE.**

## <a name="syntax"></a>Sintaxis


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a>Observaciones

Esta variable afecta a la forma en que el filtro negocia el asignador. Si el valor es **TRUE**, el filtro no puede usar un asignador de solo lectura para ambas conexiones de pin.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




