---
description: Puntero a una estructura FILTER \_ de AMOVIESETUP.
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: CFactoryTemplate::m_pAMovieSetup_Filter miembro (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAMovieSetup_Filter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc4ee059eb47e08ae827392e8f29968463bb9bd4ca86e0c6b8a87a9f3bbd5667
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697715"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a>Miembro de filtro CFactoryTemplate::m \_ pAMovieSetup \_

Puntero a una [**estructura FILTER \_ de AMOVIESETUP.**](amoviesetup-filter.md)

## <a name="syntax"></a>Sintaxis


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a>Comentarios

Use esta estructura para crear un filtro de registro propio. Si el componente no es un filtro, esta variable miembro puede ser **NULL.** Para obtener más información, vea How to Register DirectShow Filters.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CFactoryTemplate (clase)**](cfactorytemplate.md)
</dt> </dl>

 

 




