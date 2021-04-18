---
description: 'El método JoinFilterGraph notifica al filtro que se ha unido o ha dejado un gráfico de filtro. Este método implementa el método IBaseFilter:: JoinFilterGraph.'
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: Método CBaseFilter. JoinFilterGraph (Amfilter. h)
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
ms.openlocfilehash: 45453c6423b8fa9f68e5d8dff86d13b130d65f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661076"
---
# <a name="cbasefilterjoinfiltergraph-method"></a>CBaseFilter. JoinFilterGraph, método

El `JoinFilterGraph` método notifica al filtro que se ha unido o ha dejado un gráfico de filtro. Este método implementa el método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGraph* 
</dt> <dd>

Puntero a la interfaz [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) del administrador de gráficos de filtro, o **null** si el filtro está saliendo del gráfico.

</dd> <dt>

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode que contiene un nombre para el filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método establece la variable miembro [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md) igual al parámetro *pGraph* . También consulta un puntero de interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) y lo almacena en la variable miembro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) . Sin embargo, el filtro no mantiene un recuento de referencias en ninguna de estas interfaces. Si lo hace, se creará un recuento de referencias circulares, ya que el administrador de gráficos de filtro mantiene un recuento de referencias en el filtro.

El método copia la cadena especificada por *pName* en la variable miembro [**CBaseFilter:: m \_ pName**](cbasefilter-m-pname.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




