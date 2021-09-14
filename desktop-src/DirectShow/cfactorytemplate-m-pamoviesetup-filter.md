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
ms.openlocfilehash: 087612acf99a41966ccd98d3b41d2b83255a86f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266567"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a>Miembro de filtro CFactoryTemplate::m \_ pAMovieSetup \_

Puntero a una [**estructura FILTER \_ de AMOVIESETUP.**](amoviesetup-filter.md)

## <a name="syntax"></a>Sintaxis


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a>Observaciones

Use esta estructura para hacer que un filtro se registre de forma independiente. Si el componente no es un filtro, esta variable miembro puede ser **NULL.** Para obtener más información, vea How to Register DirectShow Filters.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CFactoryTemplate (clase)**](cfactorytemplate.md)
</dt> </dl>

 

 




