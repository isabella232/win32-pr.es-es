---
description: El método JoinFilterGraph notifica al filtro que se ha unido o ha dejado un gráfico de filtro. Este método implementa el método IBaseFilter::JoinFilterGraph.
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: Método CBaseFilter.JoinFilterGraph (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04dc47237ee7bd6f05ba4c187a0d643b478f6e98b74f7670e87df998998dcd03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076635"
---
# <a name="cbasefilterjoinfiltergraph-method"></a>Método CBaseFilter.JoinFilterGraph

El `JoinFilterGraph` método notifica al filtro que se ha unido o ha dejado un gráfico de filtro. Este método implementa el [**método IBaseFilter::JoinFilterGraph.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pgraph* 
</dt> <dd>

Puntero a la interfaz [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) del administrador del gráfico de filtros o **NULL** si el filtro sale del gráfico.

</dd> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode que contiene un nombre para el filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método establece la variable [**miembro CBaseFilter::m \_ pGraph**](cbasefilter-m-pgraph.md) igual al *parámetro pGraph.* También consulta un puntero de interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) y lo almacena en la variable miembro [**\_ PSink CBaseFilter::m.**](cbasefilter-m-psink.md) Sin embargo, el filtro no mantiene un recuento de referencias en ninguna de estas interfaces. Al hacerlo, se crearía un recuento circular de referencias, ya que el administrador de gráficos de filtros mantiene un recuento de referencias en el filtro.

El método copia la cadena especificada por *pName* en la variable miembro [**CBaseFilter::m \_ pName.**](cbasefilter-m-pname.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




