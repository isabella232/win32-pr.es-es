---
description: La clase CBaseRendererInputPin implementa un PIN de entrada para la clase CBaseRenderer. Excepto donde se indique, los métodos de esta clase delegan a los métodos correspondientes en la clase CBaseRenderer.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: Clase CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ec48b31170b2233f211e7e72de81d8792ae9160
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661283"
---
# <a name="crendererinputpin-class"></a><span data-ttu-id="3ab9c-104">Clase CRendererInputPin</span><span class="sxs-lookup"><span data-stu-id="3ab9c-104">CRendererInputPin class</span></span>

![jerarquía de clases crendererinput PIN](images/rbase01.png)

<span data-ttu-id="3ab9c-106">La clase **CBaseRendererInputPin** implementa un PIN de entrada para la clase [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="3ab9c-106">The **CBaseRendererInputPin** class implements an input pin for the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="3ab9c-107">Excepto donde se indique, los métodos de esta clase delegan a los métodos correspondientes en la clase **CBaseRenderer** .</span><span class="sxs-lookup"><span data-stu-id="3ab9c-107">Except where noted, the methods in this class delegate to corresponding methods on the **CBaseRenderer** class.</span></span>



| <span data-ttu-id="3ab9c-108">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="3ab9c-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="3ab9c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ab9c-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ab9c-110">**m \_ pRenderer**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-110">**m\_pRenderer**</span></span>](crendererinputpin-m-prenderer.md)            | <span data-ttu-id="3ab9c-111">Puntero al filtro.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-111">Pointer to the filter.</span></span>                                                                 |
| <span data-ttu-id="3ab9c-112">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="3ab9c-112">Public Methods</span></span>                                                   | <span data-ttu-id="3ab9c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ab9c-113">Description</span></span>                                                                            |
| [<span data-ttu-id="3ab9c-114">**CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-114">**CRendererInputPin**</span></span>](crendererinputpin-crendererinputpin.md) | <span data-ttu-id="3ab9c-115">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-115">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="3ab9c-116">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-116">**BreakConnect**</span></span>](crendererinputpin-breakconnect.md)           | <span data-ttu-id="3ab9c-117">Agrega código personalizado al interrumpir una conexión.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-117">Adds customized code upon breaking a connection.</span></span>                                       |
| [<span data-ttu-id="3ab9c-118">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-118">**CompleteConnect**</span></span>](crendererinputpin-completeconnect.md)     | <span data-ttu-id="3ab9c-119">Completa la conexión.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-119">Completes the connection.</span></span>                                                              |
| [<span data-ttu-id="3ab9c-120">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-120">**CheckMediaType**</span></span>](crendererinputpin-checkmediatype.md)       | <span data-ttu-id="3ab9c-121">Determina si el pin puede admitir un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-121">Determines if the pin can support a specific media type.</span></span>                               |
| [<span data-ttu-id="3ab9c-122">**Active**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-122">**Active**</span></span>](crendererinputpin-active.md)                       | <span data-ttu-id="3ab9c-123">Cambia el PIN al modo activo (en pausa o en ejecución).</span><span class="sxs-lookup"><span data-stu-id="3ab9c-123">Switches the pin to the active (paused or running) mode.</span></span>                               |
| [<span data-ttu-id="3ab9c-124">**Inactivo**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-124">**Inactive**</span></span>](crendererinputpin-inactive.md)                   | <span data-ttu-id="3ab9c-125">Cambia el PIN a un estado inactivo y libera la memoria del asignador.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-125">Switches the pin to an inactive state and releases the memory of the allocator.</span></span>        |
| [<span data-ttu-id="3ab9c-126">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-126">**SetMediaType**</span></span>](crendererinputpin-setmediatype.md)           | <span data-ttu-id="3ab9c-127">Establece el tipo de medio del PIN.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-127">Sets the media type of the pin.</span></span>                                                        |
| [<span data-ttu-id="3ab9c-128">**Asignador**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-128">**Allocator**</span></span>](crendererinputpin-allocator.md)                 | <span data-ttu-id="3ab9c-129">Recupera un puntero al asignador de memoria predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-129">Retrieves a pointer to the default memory allocator.</span></span>                                   |
| <span data-ttu-id="3ab9c-130">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="3ab9c-130">IPin Methods</span></span>                                                     | <span data-ttu-id="3ab9c-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ab9c-131">Description</span></span>                                                                            |
| [<span data-ttu-id="3ab9c-132">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-132">**QueryId**</span></span>](crendererinputpin-queryid.md)                     | <span data-ttu-id="3ab9c-133">Recupera un identificador para el código PIN.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-133">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="3ab9c-134">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-134">**EndOfStream**</span></span>](crendererinputpin-endofstream.md)             | <span data-ttu-id="3ab9c-135">Informa al pin de que no se esperan datos adicionales hasta que se emita un nuevo comando de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-135">Informs the pin that no additional data is expected until a new run command is issued.</span></span> |
| [<span data-ttu-id="3ab9c-136">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-136">**BeginFlush**</span></span>](crendererinputpin-beginflush.md)               | <span data-ttu-id="3ab9c-137">Informa al pin para iniciar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-137">Informs the pin to begin a flush operation.</span></span>                                            |
| [<span data-ttu-id="3ab9c-138">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-138">**EndFlush**</span></span>](crendererinputpin-endflush.md)                   | <span data-ttu-id="3ab9c-139">Informa al código PIN para finalizar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-139">Informs the pin to end a flush operation.</span></span>                                              |
| <span data-ttu-id="3ab9c-140">Métodos IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="3ab9c-140">IMemInputPin Methods</span></span>                                             | <span data-ttu-id="3ab9c-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ab9c-141">Description</span></span>                                                                            |
| [<span data-ttu-id="3ab9c-142">**Aparecen**</span><span class="sxs-lookup"><span data-stu-id="3ab9c-142">**Receive**</span></span>](crendererinputpin-receive.md)                     | <span data-ttu-id="3ab9c-143">Recupera el siguiente bloque de datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-143">Retrieves the next block of data from the stream.</span></span>                                      |



 

## <a name="requirements"></a><span data-ttu-id="3ab9c-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ab9c-144">Requirements</span></span>



| <span data-ttu-id="3ab9c-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ab9c-145">Requirement</span></span> | <span data-ttu-id="3ab9c-146">Value</span><span class="sxs-lookup"><span data-stu-id="3ab9c-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab9c-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ab9c-147">Header</span></span><br/>  | <dl> <span data-ttu-id="3ab9c-148"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ab9c-148"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3ab9c-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ab9c-149">Library</span></span><br/> | <dl> <span data-ttu-id="3ab9c-150"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3ab9c-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




