---
description: El método SetFilterGraph especifica el receptor de eventos para los eventos de control de flujo.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Método CBaseStreamControl. SetFilterGraph (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1cf8b571ee5d017acd056e00a06af54cd90b943a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660115"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a><span data-ttu-id="d18f2-103">CBaseStreamControl. SetFilterGraph, método</span><span class="sxs-lookup"><span data-stu-id="d18f2-103">CBaseStreamControl.SetFilterGraph method</span></span>

<span data-ttu-id="d18f2-104">El `SetFilterGraph` método especifica el receptor de eventos para los eventos de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="d18f2-104">The `SetFilterGraph` method specifies the event sink for stream control events.</span></span>

## <a name="syntax"></a><span data-ttu-id="d18f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d18f2-105">Syntax</span></span>


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="d18f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d18f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d18f2-107">*pSink*</span><span class="sxs-lookup"><span data-stu-id="d18f2-107">*pSink*</span></span> 
</dt> <dd>

<span data-ttu-id="d18f2-108">Puntero a la interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) del administrador de gráficos de filtro, o **null** cuando el filtro deja el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="d18f2-108">Pointer to the Filter Graph Manager's [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, or **NULL** when the filter leaves the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d18f2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d18f2-109">Return value</span></span>

<span data-ttu-id="d18f2-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d18f2-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d18f2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d18f2-111">Remarks</span></span>

<span data-ttu-id="d18f2-112">Llame a este método desde dentro del método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del filtro.</span><span class="sxs-lookup"><span data-stu-id="d18f2-112">Call this method from inside the filter's [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="d18f2-113">La clase **CBaseStreamControl** usa la interfaz **IMediaEventSink** para enviar eventos de detención de control de [**flujo de EC \_ \_ \_ iniciado**](ec-stream-control-started.md) y de [**\_ \_ control \_ de flujo de EC**](ec-stream-control-stopped.md) .</span><span class="sxs-lookup"><span data-stu-id="d18f2-113">The **CBaseStreamControl** class uses the **IMediaEventSink** interface to send [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) events.</span></span>

<span data-ttu-id="d18f2-114">Si el filtro se deriva de **CBaseFilter**, llame primero al método [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) , que establece la variable miembro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) .</span><span class="sxs-lookup"><span data-stu-id="d18f2-114">If your filter derives from **CBaseFilter**, first call the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, which sets the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="d18f2-115">Después, pase **m \_ pSink** al `SetFilterGraph` método.</span><span class="sxs-lookup"><span data-stu-id="d18f2-115">Then pass **m\_pSink** to the `SetFilterGraph` method.</span></span> <span data-ttu-id="d18f2-116">Tenga en cuenta que **m \_ PSink** es **null** cuando el filtro sale del gráfico, que es correcto.</span><span class="sxs-lookup"><span data-stu-id="d18f2-116">Note that **m\_pSink** is **NULL** when the filter leaves the graph, which is correct.</span></span>

## <a name="examples"></a><span data-ttu-id="d18f2-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d18f2-117">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::JoinFilterGraph(IFilterGraph * pGraph, LPCWSTR pName)
{
    // Note: It's OK if pGraph is NULL.

    HRESULT hr = CBaseFilter::JoinFilterGraph(pGraph, pName);
    if (SUCCEEDED(hr)) 
    {
        m_pMyPin->SetFilterGraph(m_pSink);
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="d18f2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d18f2-118">Requirements</span></span>



| <span data-ttu-id="d18f2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d18f2-119">Requirement</span></span> | <span data-ttu-id="d18f2-120">Value</span><span class="sxs-lookup"><span data-stu-id="d18f2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d18f2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d18f2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d18f2-122"><dt>Strmctl. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d18f2-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d18f2-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d18f2-123">Library</span></span><br/> | <dl> <span data-ttu-id="d18f2-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d18f2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d18f2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d18f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18f2-126">**Clase CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="d18f2-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




