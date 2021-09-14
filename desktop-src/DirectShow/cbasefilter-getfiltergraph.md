---
description: El método GetFilterGraph recupera un puntero al administrador de gráficos de filtro.
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
ms.openlocfilehash: c0843c7789afc1500565d2737d863cbc8af114d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063360"
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




