---
description: La clase CRenderedInputPin es una clase base para implementar un PIN de entrada en un representador.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: Clase CRenderedInputPin (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fc00b4aa0ce1fc6c8a93fb2fbda2118ad6bb40e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670984"
---
# <a name="crenderedinputpin-class"></a><span data-ttu-id="2d2d0-103">Clase CRenderedInputPin</span><span class="sxs-lookup"><span data-stu-id="2d2d0-103">CRenderedInputPin class</span></span>

![jerarquía de clases crenderedinputpin](images/rbase04.png)

<span data-ttu-id="2d2d0-105">La clase **CRenderedInputPin** es una clase base para implementar un PIN de entrada en un representador.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-105">The **CRenderedInputPin** class is a base class for implementing an input pin on a renderer.</span></span> <span data-ttu-id="2d2d0-106">Esta clase está diseñada para los filtros de representador que no derivan de la clase [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="2d2d0-106">This class is designed for renderer filters that do not derive from the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="2d2d0-107">(Los filtros que derivan de **CBaseRenderer** deben usar la clase [**CRendererInputPin**](crendererinputpin.md) para el PIN de entrada).</span><span class="sxs-lookup"><span data-stu-id="2d2d0-107">(Filters that derive from **CBaseRenderer** should use the [**CRendererInputPin**](crendererinputpin.md) class for the input pin.)</span></span>

<span data-ttu-id="2d2d0-108">Para usar esta clase, debe realizar al menos lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2d2d0-108">To use this class, you must do at least the following:</span></span>

-   <span data-ttu-id="2d2d0-109">Declare una nueva clase de PIN que herede **CRenderedInputPin**.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-109">Declare a new pin class that inherits **CRenderedInputPin**.</span></span>
-   <span data-ttu-id="2d2d0-110">En la clase PIN, declare un objeto de sección crítica para que contenga el bloqueo de streaming.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-110">In your pin class, declare a critical section object to hold the streaming lock.</span></span> <span data-ttu-id="2d2d0-111">Puede usar la clase [**CCritSec**](ccritsec.md) para este propósito.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-111">You can use the [**CCritSec**](ccritsec.md) class for this purpose.</span></span> <span data-ttu-id="2d2d0-112">Para obtener más información, vea [subprocesos y secciones críticas](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="2d2d0-112">For more information, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>
-   <span data-ttu-id="2d2d0-113">Invalide [**CRenderedInputPin:: EndOfStream**](crenderedinputpin-endofstream.md) para contener el bloqueo de streaming.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-113">Override [**CRenderedInputPin::EndOfStream**](crenderedinputpin-endofstream.md) to hold the streaming lock.</span></span>
-   <span data-ttu-id="2d2d0-114">Implemente los métodos [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md)y [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="2d2d0-114">Implement the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md), and [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) methods.</span></span>
-   <span data-ttu-id="2d2d0-115">En el filtro, implemente [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) para devolver una instancia de la clase de PIN.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-115">In your filter, implement [**CBaseFilter::GetPin**](cbasefilter-getpin.md) to return an instance of your pin class.</span></span>

<span data-ttu-id="2d2d0-116">Puede usar esta clase en un representador que tenga más de un PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-116">You can use this class in a renderer that has more than one input pin.</span></span> <span data-ttu-id="2d2d0-117">Esta clase hereda la clase [**CBaseInputPin**](cbaseinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="2d2d0-117">This class inherits the [**CBaseInputPin**](cbaseinputpin.md) class.</span></span>



| <span data-ttu-id="2d2d0-118">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="2d2d0-118">Protected Member Variables</span></span>                                            | <span data-ttu-id="2d2d0-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d2d0-119">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d2d0-120">**m \_ bAtEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="2d2d0-120">**m\_bAtEndOfStream**</span></span>](crenderedinputpin-m-batendofstream.md)       | <span data-ttu-id="2d2d0-121">Indica si se ha alcanzado el final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-121">Indicates whether the end of the stream was reached.</span></span>                                                         |
| [<span data-ttu-id="2d2d0-122">**m \_ bCompleteNotified**</span><span class="sxs-lookup"><span data-stu-id="2d2d0-122">**m\_bCompleteNotified**</span></span>](crenderedinputpin-m-bcompletenotified.md) | <span data-ttu-id="2d2d0-123">Indica si el PIN ha enviado un evento de [**\_ finalización de EC**](ec-complete.md) al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-123">Indicates whether the pin has sent an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> |
| <span data-ttu-id="2d2d0-124">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="2d2d0-124">Public Methods</span></span>                                                        | <span data-ttu-id="2d2d0-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d2d0-125">Description</span></span>                                                                                                  |
| [<span data-ttu-id="2d2d0-126">**Activo**</span><span class="sxs-lookup"><span data-stu-id="2d2d0-126">**Active**</span></span>](crenderedinputpin-active.md)                            | <span data-ttu-id="2d2d0-127">Notifica al pin que el filtro está activo ahora.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-127">Notifies the pin that the filter is now active.</span></span>                                                              |
| [<span data-ttu-id="2d2d0-128">**CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="2d2d0-128">**CRenderedInputPin**</span></span>](crenderedinputpin-crenderedinputpin.md)      | <span data-ttu-id="2d2d0-129">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-129">Constructor method.</span></span>                                                                                          |
| [<span data-ttu-id="2d2d0-130">**Ejecutar**</span><span class="sxs-lookup"><span data-stu-id="2d2d0-130">**Run**</span></span>](crenderedinputpin-run.md)                                  | <span data-ttu-id="2d2d0-131">Notifica al pin que el filtro se está ejecutando ahora.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-131">Notifies the pin that the filter is now running.</span></span>                                                             |
| <span data-ttu-id="2d2d0-132">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="2d2d0-132">IPin Methods</span></span>                                                          | <span data-ttu-id="2d2d0-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d2d0-133">Description</span></span>                                                                                                  |
| [<span data-ttu-id="2d2d0-134">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="2d2d0-134">**EndFlush**</span></span>](crenderedinputpin-endflush.md)                        | <span data-ttu-id="2d2d0-135">Finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-135">Ends a flush operation.</span></span>                                                                                      |
| [<span data-ttu-id="2d2d0-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="2d2d0-136">**EndOfStream**</span></span>](crenderedinputpin-endofstream.md)                  | <span data-ttu-id="2d2d0-137">Notifica al pin que no se espera ningún dato adicional hasta que el filtro recibe un nuevo comando de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2d2d0-137">Notifies the pin that no additional data is expected until the filter receives a new run command.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="2d2d0-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d2d0-138">Requirements</span></span>



| <span data-ttu-id="2d2d0-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d2d0-139">Requirement</span></span> | <span data-ttu-id="2d2d0-140">Value</span><span class="sxs-lookup"><span data-stu-id="2d2d0-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d2d0-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d2d0-141">Header</span></span><br/>  | <dl> <span data-ttu-id="2d2d0-142"><dt>Amextra. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d2d0-142"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2d2d0-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d2d0-143">Library</span></span><br/> | <dl> <span data-ttu-id="2d2d0-144"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2d2d0-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




