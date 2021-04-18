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
# <a name="cbasefilterjoinfiltergraph-method"></a><span data-ttu-id="5c34d-104">CBaseFilter. JoinFilterGraph, método</span><span class="sxs-lookup"><span data-stu-id="5c34d-104">CBaseFilter.JoinFilterGraph method</span></span>

<span data-ttu-id="5c34d-105">El `JoinFilterGraph` método notifica al filtro que se ha unido o ha dejado un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="5c34d-105">The `JoinFilterGraph` method notifies the filter that it has joined or left a filter graph.</span></span> <span data-ttu-id="5c34d-106">Este método implementa el método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .</span><span class="sxs-lookup"><span data-stu-id="5c34d-106">This method implements the [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c34d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c34d-107">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a><span data-ttu-id="5c34d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c34d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c34d-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="5c34d-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="5c34d-110">Puntero a la interfaz [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) del administrador de gráficos de filtro, o **null** si el filtro está saliendo del gráfico.</span><span class="sxs-lookup"><span data-stu-id="5c34d-110">Pointer to the filter graph manager's [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface, or **NULL** if the filter is leaving the graph.</span></span>

</dd> <dt>

<span data-ttu-id="5c34d-111">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5c34d-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c34d-112">Puntero a una cadena Unicode que contiene un nombre para el filtro.</span><span class="sxs-lookup"><span data-stu-id="5c34d-112">Pointer to a Unicode string containing a name for the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c34d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c34d-113">Return value</span></span>

<span data-ttu-id="5c34d-114">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5c34d-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c34d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c34d-115">Remarks</span></span>

<span data-ttu-id="5c34d-116">Este método establece la variable miembro [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md) igual al parámetro *pGraph* .</span><span class="sxs-lookup"><span data-stu-id="5c34d-116">This method sets the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable equal to the *pGraph* parameter.</span></span> <span data-ttu-id="5c34d-117">También consulta un puntero de interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) y lo almacena en la variable miembro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) .</span><span class="sxs-lookup"><span data-stu-id="5c34d-117">It also queries for an [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface pointer and stores it in the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="5c34d-118">Sin embargo, el filtro no mantiene un recuento de referencias en ninguna de estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="5c34d-118">However, the filter does not keep a reference count on either of these interfaces.</span></span> <span data-ttu-id="5c34d-119">Si lo hace, se creará un recuento de referencias circulares, ya que el administrador de gráficos de filtro mantiene un recuento de referencias en el filtro.</span><span class="sxs-lookup"><span data-stu-id="5c34d-119">Doing so would create a circular reference count, because the filter graph manager keeps a reference count on the filter.</span></span>

<span data-ttu-id="5c34d-120">El método copia la cadena especificada por *pName* en la variable miembro [**CBaseFilter:: m \_ pName**](cbasefilter-m-pname.md) .</span><span class="sxs-lookup"><span data-stu-id="5c34d-120">The method copies the string specified by *pName* into the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c34d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c34d-121">Requirements</span></span>



| <span data-ttu-id="5c34d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c34d-122">Requirement</span></span> | <span data-ttu-id="5c34d-123">Value</span><span class="sxs-lookup"><span data-stu-id="5c34d-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c34d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c34d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5c34d-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c34d-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5c34d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c34d-126">Library</span></span><br/> | <dl> <span data-ttu-id="5c34d-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5c34d-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c34d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c34d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c34d-129">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="5c34d-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




