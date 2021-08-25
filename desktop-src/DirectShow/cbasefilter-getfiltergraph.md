---
description: El método GetFilterGraph recupera un puntero al administrador de gráficos de filtros.
ms.assetid: 80b41272-2ca1-40db-8624-0d99d66f3c34
title: Método CBaseFilter.GetFilterGraph (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f35b40febff058d5bbd9f48c5ac6d10168d48d6e587b51ab2730704724e48c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056655"
---
# <a name="cbasefiltergetfiltergraph-method"></a>Método CBaseFilter.GetFilterGraph

El `GetFilterGraph` método recupera un puntero al administrador de gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
IFilterGraph* GetFilterGraph();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de [**CBaseFilter::m \_ pGraph**](cbasefilter-m-pgraph.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




