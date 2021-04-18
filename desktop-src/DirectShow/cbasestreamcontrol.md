---
description: Esta clase implementa la interfaz IAMStreamControl para los terminales de entrada y salida.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: Clase CBaseStreamControl (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660432"
---
# <a name="cbasestreamcontrol-class"></a><span data-ttu-id="be567-103">Clase CBaseStreamControl</span><span class="sxs-lookup"><span data-stu-id="be567-103">CBaseStreamControl class</span></span>

![jerarquía de clases cbasestreamcontrol](images/strmctl1.png)

<span data-ttu-id="be567-105">Esta clase implementa la interfaz [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) para los terminales de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="be567-105">This class implements the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface for input and output pins.</span></span> <span data-ttu-id="be567-106">Proporciona control sobre el inicio y la detención de un PIN individual en el filtro.</span><span class="sxs-lookup"><span data-stu-id="be567-106">It provides control over starting and stopping an individual pin on the filter.</span></span> <span data-ttu-id="be567-107">Un PIN que admita **IAMStreamControl** debe heredar de esta clase base.</span><span class="sxs-lookup"><span data-stu-id="be567-107">A pin that supports **IAMStreamControl** should inherit from this base class.</span></span> <span data-ttu-id="be567-108">A continuación se proporciona una declaración típica para un PIN de entrada:</span><span class="sxs-lookup"><span data-stu-id="be567-108">The following is a typical declaration for an input pin:</span></span>

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

<span data-ttu-id="be567-109">Asegúrese de invalidar **NonDelegatingQueryInteface** para exponer **IAMStreamControl**.</span><span class="sxs-lookup"><span data-stu-id="be567-109">Be sure to override **NonDelegatingQueryInteface** to expose **IAMStreamControl**.</span></span> <span data-ttu-id="be567-110">Para obtener más información, vea [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="be567-110">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>



| <span data-ttu-id="be567-111">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="be567-111">Public Methods</span></span>                                                        | <span data-ttu-id="be567-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="be567-112">Description</span></span>                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be567-113">**CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="be567-113">**CBaseStreamControl**</span></span>](cbasestreamcontrol-cbasestreamcontrol.md)   | <span data-ttu-id="be567-114">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="be567-114">Constructor method.</span></span>                                                                                  |
| [<span data-ttu-id="be567-115">**~ CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="be567-115">**~CBaseStreamControl**</span></span>](cbasestreamcontrol--cbasestreamcontrol.md) | <span data-ttu-id="be567-116">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="be567-116">Destructor method.</span></span>                                                                                   |
| [<span data-ttu-id="be567-117">**CheckStreamState**</span><span class="sxs-lookup"><span data-stu-id="be567-117">**CheckStreamState**</span></span>](cbasestreamcontrol-checkstreamstate.md)       | <span data-ttu-id="be567-118">Determina si un ejemplo multimedia se debe entregar o descartar.</span><span class="sxs-lookup"><span data-stu-id="be567-118">Determines whether a media sample should be delivered or discarded.</span></span>                                  |
| [<span data-ttu-id="be567-119">**Vaciar**</span><span class="sxs-lookup"><span data-stu-id="be567-119">**Flushing**</span></span>](cbasestreamcontrol-flushing.md)                       | <span data-ttu-id="be567-120">Notifica a la clase base que el PIN se ha iniciado o detenido.</span><span class="sxs-lookup"><span data-stu-id="be567-120">Notifies the base class that the pin has started or stopped flushing.</span></span>                                |
| [<span data-ttu-id="be567-121">**NotifyFilterState**</span><span class="sxs-lookup"><span data-stu-id="be567-121">**NotifyFilterState**</span></span>](cbasestreamcontrol-notifyfilterstate.md)     | <span data-ttu-id="be567-122">Notifica al pin cuando cambia el estado del filtro.</span><span class="sxs-lookup"><span data-stu-id="be567-122">Notifies the pin when the filter's state changes.</span></span>                                                    |
| [<span data-ttu-id="be567-123">**SetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="be567-123">**SetFilterGraph**</span></span>](cbasestreamcontrol-setfiltergraph.md)           | <span data-ttu-id="be567-124">Especifica el receptor de eventos para los eventos de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="be567-124">Specifies the event sink for stream control events.</span></span>                                                  |
| [<span data-ttu-id="be567-125">**SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="be567-125">**SetSyncSource**</span></span>](cbasestreamcontrol-setsyncsource.md)             | <span data-ttu-id="be567-126">Notifica a la clase base del reloj de referencia actual.</span><span class="sxs-lookup"><span data-stu-id="be567-126">Notifies the base class of the current reference clock.</span></span>                                              |
| <span data-ttu-id="be567-127">Métodos IAMStreamControl</span><span class="sxs-lookup"><span data-stu-id="be567-127">IAMStreamControl Methods</span></span>                                              | <span data-ttu-id="be567-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="be567-128">Description</span></span>                                                                                          |
| [<span data-ttu-id="be567-129">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="be567-129">**GetInfo**</span></span>](cbasestreamcontrol-getinfo.md)                         | <span data-ttu-id="be567-130">Recupera información sobre la configuración actual del control de flujo, incluidas las horas de inicio y detención.</span><span class="sxs-lookup"><span data-stu-id="be567-130">Retrieves information about the current stream-control settings, including the start and stop times.</span></span> |
| [<span data-ttu-id="be567-131">**StartAt**</span><span class="sxs-lookup"><span data-stu-id="be567-131">**StartAt**</span></span>](cbasestreamcontrol-startat.md)                         | <span data-ttu-id="be567-132">Informa al pin Cuándo debe comenzar a entregar los datos.</span><span class="sxs-lookup"><span data-stu-id="be567-132">Informs the pin when to start delivering data.</span></span>                                                       |
| [<span data-ttu-id="be567-133">**StopAt**</span><span class="sxs-lookup"><span data-stu-id="be567-133">**StopAt**</span></span>](cbasestreamcontrol-stopat.md)                           | <span data-ttu-id="be567-134">Informa al pin Cuándo detener la entrega de datos.</span><span class="sxs-lookup"><span data-stu-id="be567-134">Informs the pin when to stop delivering data.</span></span>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="be567-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be567-135">Remarks</span></span>

<span data-ttu-id="be567-136">Esta clase requiere que el PIN y el filtro propietario notifiquen a la clase cuando se producen varios eventos, como el filtro que une el gráfico o la recepción de un nuevo reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="be567-136">This class requires the pin and the owning filter to notify the class when various events occur, such as the filter joining the graph or receiving a new reference clock.</span></span> <span data-ttu-id="be567-137">Debe llamar a los siguientes métodos de clase:</span><span class="sxs-lookup"><span data-stu-id="be567-137">You should call the following class methods:</span></span>

-   <span data-ttu-id="be567-138">En el método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) del filtro, llame al método [**CBaseStreamControl:: SetSyncSource**](cbasestreamcontrol-setsyncsource.md) .</span><span class="sxs-lookup"><span data-stu-id="be567-138">In the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method, call the [**CBaseStreamControl::SetSyncSource**](cbasestreamcontrol-setsyncsource.md) method.</span></span> <span data-ttu-id="be567-139">Este método notifica a la clase del reloj de referencia actual.</span><span class="sxs-lookup"><span data-stu-id="be567-139">This method notifies the class of the current reference clock.</span></span>
-   <span data-ttu-id="be567-140">En el método [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) del filtro, llame al método [**CBaseStreamControl:: SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="be567-140">In the filter's [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, call the [**CBaseStreamControl::SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) method.</span></span> <span data-ttu-id="be567-141">Este método proporciona a la clase un puntero al administrador de gráficos de filtro, de modo que la clase pueda enviar los eventos de control de flujo correctos.</span><span class="sxs-lookup"><span data-stu-id="be567-141">This method gives the class a pointer to the Filter Graph Manager, so that the class can send the right stream-control events.</span></span>
-   <span data-ttu-id="be567-142">Siempre que el filtro cambie de estado (a en ejecución, en pausa o detenido), llame al método [**CBaseStreamControl:: NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="be567-142">Whenever the filter changes state (to running, paused, or stopped), call the [**CBaseStreamControl::NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) method.</span></span>
-   <span data-ttu-id="be567-143">En los métodos IPin:: [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) y [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) del PIN, llame al método [**CBaseStreamControl:: Flushing**](cbasestreamcontrol-flushing.md) .</span><span class="sxs-lookup"><span data-stu-id="be567-143">In the pin's [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods, call the [**CBaseStreamControl::Flushing**](cbasestreamcontrol-flushing.md) method.</span></span>

<span data-ttu-id="be567-144">La `CBaseStreamControl` clase usa el reloj de referencia del gráfico de filtro para determinar qué muestras debe enviar el filtro y cuáles deben descartarse.</span><span class="sxs-lookup"><span data-stu-id="be567-144">The `CBaseStreamControl` class uses the filter graph's reference clock to determine which samples the filter should be deliver, and which it should discard.</span></span> <span data-ttu-id="be567-145">En el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del PIN, llame al método [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) con un puntero al ejemplo de multimedia entrante.</span><span class="sxs-lookup"><span data-stu-id="be567-145">In your pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, call the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method with a pointer to the incoming media sample.</span></span> <span data-ttu-id="be567-146">Si el método devuelve el flujo de valor que \_ fluye, entregue el ejemplo de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="be567-146">If the method returns the value STREAM\_FLOWING, deliver the sample downstream.</span></span> <span data-ttu-id="be567-147">De lo contrario, descartarlo.</span><span class="sxs-lookup"><span data-stu-id="be567-147">Otherwise, discard it.</span></span>

## <a name="requirements"></a><span data-ttu-id="be567-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be567-148">Requirements</span></span>



| <span data-ttu-id="be567-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="be567-149">Requirement</span></span> | <span data-ttu-id="be567-150">Value</span><span class="sxs-lookup"><span data-stu-id="be567-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be567-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be567-151">Header</span></span><br/>  | <dl> <span data-ttu-id="be567-152"><dt>Strmctl. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be567-152"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be567-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be567-153">Library</span></span><br/> | <dl> <span data-ttu-id="be567-154"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="be567-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




