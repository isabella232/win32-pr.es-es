---
description: El método JoinFilterGraph envía la \_ \_ notificación de eventos de la ventana de EC destruido cuando se quita un filtro del gráfico de filtros.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Método CBaseVideoRenderer. JoinFilterGraph (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680589"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a><span data-ttu-id="0e51a-103">CBaseVideoRenderer. JoinFilterGraph, método</span><span class="sxs-lookup"><span data-stu-id="0e51a-103">CBaseVideoRenderer.JoinFilterGraph method</span></span>

<span data-ttu-id="0e51a-104">El `JoinFilterGraph` método envía la notificación de eventos de la [**ventana de EC \_ \_ destruido**](ec-window-destroyed.md) cuando se quita un filtro del gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="0e51a-104">The `JoinFilterGraph` method sends [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification when a filter is removed from the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e51a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e51a-105">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="0e51a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e51a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e51a-107">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="0e51a-107">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="0e51a-108">Puntero al gráfico de filtro que se va a combinar.</span><span class="sxs-lookup"><span data-stu-id="0e51a-108">Pointer to the filter graph to join.</span></span>

</dd> <dt>

<span data-ttu-id="0e51a-109">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0e51a-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e51a-110">Puntero al nombre del filtro que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="0e51a-110">Pointer to the name of the filter being added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e51a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e51a-111">Return value</span></span>

<span data-ttu-id="0e51a-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0e51a-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e51a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e51a-113">Remarks</span></span>

<span data-ttu-id="0e51a-114">Esta función miembro invalida la función miembro [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="0e51a-114">This member function overrides the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) member function.</span></span> <span data-ttu-id="0e51a-115">Si el filtro deja el gráfico de filtro (*pGraph* es **null**), envía una notificación de eventos de [**ventana de EC \_ \_ destruido**](ec-window-destroyed.md) para que el administrador de recursos no mantenga el representador como un objeto de foco.</span><span class="sxs-lookup"><span data-stu-id="0e51a-115">If the filter is leaving the filter graph (*pGraph* is **NULL**), it sends an [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification so that the resource manager does not hold on to the renderer as a focus object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e51a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e51a-116">Requirements</span></span>



| <span data-ttu-id="0e51a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e51a-117">Requirement</span></span> | <span data-ttu-id="0e51a-118">Value</span><span class="sxs-lookup"><span data-stu-id="0e51a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e51a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e51a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0e51a-120"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e51a-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0e51a-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e51a-121">Library</span></span><br/> | <dl> <span data-ttu-id="0e51a-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0e51a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e51a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e51a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e51a-124">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="0e51a-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




