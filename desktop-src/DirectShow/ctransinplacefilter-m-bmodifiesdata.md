---
description: La \_ variable miembro m bModifiesData indica si el filtro modifica los datos de ejemplo que recibe. El valor se establece en el constructor CTransInPlaceFilter, pero su valor predeterminado es TRUE.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Miembro CTransInPlaceFilter:: m_bModifiesData (TRANSip. h)'
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
ms.openlocfilehash: 5bc0d630fd0eda6e9915f8c11f5b15d21b725ce8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660607"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a>Miembro bModifiesData CTransInPlaceFilter:: m \_

La `m_bModifiesData` variable miembro indica si el filtro modifica los datos de ejemplo que recibe. El valor se establece en el constructor **CTransInPlaceFilter** , pero su valor predeterminado es **true**.

## <a name="syntax"></a>Sintaxis


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a>Observaciones

Esta variable afecta a cómo el filtro negocia el asignador. Si el valor es **true**, el filtro no puede usar un asignador de solo lectura para ambas conexiones de PIN.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




