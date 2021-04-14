---
description: La clase CTransformInputPin implementa un PIN de entrada usado por la clase CTransformFilter.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: Clase CTransformInputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cbfad0a33384249ab474d6376ffc110294bca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661315"
---
# <a name="ctransforminputpin-class"></a><span data-ttu-id="ab52e-103">Clase CTransformInputPin</span><span class="sxs-lookup"><span data-stu-id="ab52e-103">CTransformInputPin class</span></span>

![jerarquía de clases ctransforminputpin](images/tfrm01.png)

<span data-ttu-id="ab52e-105">La `CTransformInputPin` clase implementa un PIN de entrada usado por la clase [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="ab52e-105">The `CTransformInputPin` class implements an input pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="ab52e-106">Normalmente, no es necesario derivar de esta clase.</span><span class="sxs-lookup"><span data-stu-id="ab52e-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="ab52e-107">La mayoría de los métodos de esta clase llaman a los métodos correspondientes en la clase **CTransformFilter** , que puede invalidar.</span><span class="sxs-lookup"><span data-stu-id="ab52e-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="ab52e-108">Si deriva de esta clase, debe invalidar el método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) del filtro para crear instancias de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="ab52e-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="ab52e-109">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="ab52e-109">Protected Member Variables</span></span>                                           | <span data-ttu-id="ab52e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab52e-110">Description</span></span>                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab52e-111">**m \_ pTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="ab52e-111">**m\_pTransformFilter**</span></span>](ctransforminputpin-m-ptransformfilter.md) | <span data-ttu-id="ab52e-112">Puntero al filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="ab52e-112">Pointer to the owning filter.</span></span>                                                          |
| <span data-ttu-id="ab52e-113">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="ab52e-113">Public Methods</span></span>                                                       | <span data-ttu-id="ab52e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab52e-114">Description</span></span>                                                                            |
| [<span data-ttu-id="ab52e-115">**CTransformInputPin**</span><span class="sxs-lookup"><span data-stu-id="ab52e-115">**CTransformInputPin**</span></span>](ctransforminputpin-ctransforminputpin.md)  | <span data-ttu-id="ab52e-116">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="ab52e-116">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="ab52e-117">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="ab52e-117">**CheckConnect**</span></span>](ctransforminputpin-checkconnect.md)              | <span data-ttu-id="ab52e-118">Determina si una conexión de PIN es adecuada.</span><span class="sxs-lookup"><span data-stu-id="ab52e-118">Determines whether a pin connection is suitable.</span></span>                                       |
| [<span data-ttu-id="ab52e-119">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="ab52e-119">**BreakConnect**</span></span>](ctransforminputpin-breakconnect.md)              | <span data-ttu-id="ab52e-120">Libera el PIN de una conexión.</span><span class="sxs-lookup"><span data-stu-id="ab52e-120">Releases the pin from a connection.</span></span>                                                    |
| [<span data-ttu-id="ab52e-121">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="ab52e-121">**CompleteConnect**</span></span>](ctransforminputpin-completeconnect.md)        | <span data-ttu-id="ab52e-122">Completa una conexión a otro PIN.</span><span class="sxs-lookup"><span data-stu-id="ab52e-122">Completes a connection to another pin.</span></span>                                                 |
| [<span data-ttu-id="ab52e-123">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="ab52e-123">**CheckMediaType**</span></span>](ctransforminputpin-checkmediatype.md)          | <span data-ttu-id="ab52e-124">Determina si el PIN acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="ab52e-124">Determines if the pin accepts a specific media type.</span></span>                                   |
| [<span data-ttu-id="ab52e-125">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="ab52e-125">**SetMediaType**</span></span>](ctransforminputpin-setmediatype.md)              | <span data-ttu-id="ab52e-126">Establece el tipo de medio para la conexión.</span><span class="sxs-lookup"><span data-stu-id="ab52e-126">Sets the media type for the connection.</span></span>                                                |
| [<span data-ttu-id="ab52e-127">**CheckStreaming**</span><span class="sxs-lookup"><span data-stu-id="ab52e-127">**CheckStreaming**</span></span>](ctransforminputpin-checkstreaming.md)          | <span data-ttu-id="ab52e-128">Determina si el pin puede aceptar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="ab52e-128">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="ab52e-129">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="ab52e-129">Virtual.</span></span>                                |
| [<span data-ttu-id="ab52e-130">**CurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="ab52e-130">**CurrentMediaType**</span></span>](ctransforminputpin-currentmediatype.md)      | <span data-ttu-id="ab52e-131">Recupera el tipo de medio para la conexión del PIN actual.</span><span class="sxs-lookup"><span data-stu-id="ab52e-131">Retrieves the media type for the current pin connection.</span></span>                               |
| <span data-ttu-id="ab52e-132">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="ab52e-132">IPin Methods</span></span>                                                         | <span data-ttu-id="ab52e-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab52e-133">Description</span></span>                                                                            |
| [<span data-ttu-id="ab52e-134">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="ab52e-134">**QueryId**</span></span>](ctransforminputpin-queryid.md)                        | <span data-ttu-id="ab52e-135">Recupera un identificador para el código PIN.</span><span class="sxs-lookup"><span data-stu-id="ab52e-135">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="ab52e-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="ab52e-136">**EndOfStream**</span></span>](ctransforminputpin-endofstream.md)                | <span data-ttu-id="ab52e-137">Notifica al pin que no se espera ningún dato adicional.</span><span class="sxs-lookup"><span data-stu-id="ab52e-137">Notifies the pin that no additional data is expected.</span></span>                                  |
| [<span data-ttu-id="ab52e-138">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="ab52e-138">**BeginFlush**</span></span>](ctransforminputpin-beginflush.md)                  | <span data-ttu-id="ab52e-139">Comienza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="ab52e-139">Begins a flush operation.</span></span>                                                              |
| [<span data-ttu-id="ab52e-140">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="ab52e-140">**EndFlush**</span></span>](ctransforminputpin-endflush.md)                      | <span data-ttu-id="ab52e-141">Finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="ab52e-141">Ends a flush operation.</span></span>                                                                |
| [<span data-ttu-id="ab52e-142">**NewSegment**</span><span class="sxs-lookup"><span data-stu-id="ab52e-142">**NewSegment**</span></span>](ctransforminputpin-newsegment.md)                  | <span data-ttu-id="ab52e-143">Notifica al pin que los ejemplos de multimedia recibieron después de que esta llamada se agrupe como un segmento.</span><span class="sxs-lookup"><span data-stu-id="ab52e-143">Notifies the pin that media samples received after this call are grouped as a segment.</span></span> |
| <span data-ttu-id="ab52e-144">Métodos IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="ab52e-144">IMemInputPin Methods</span></span>                                                 | <span data-ttu-id="ab52e-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab52e-145">Description</span></span>                                                                            |
| [<span data-ttu-id="ab52e-146">**Aparecen**</span><span class="sxs-lookup"><span data-stu-id="ab52e-146">**Receive**</span></span>](ctransforminputpin-receive.md)                        | <span data-ttu-id="ab52e-147">Recibe el siguiente ejemplo multimedia en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ab52e-147">Receives the next media sample in the stream.</span></span>                                          |



 

## <a name="requirements"></a><span data-ttu-id="ab52e-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab52e-148">Requirements</span></span>



| <span data-ttu-id="ab52e-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab52e-149">Requirement</span></span> | <span data-ttu-id="ab52e-150">Value</span><span class="sxs-lookup"><span data-stu-id="ab52e-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab52e-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab52e-151">Header</span></span><br/>  | <dl> <span data-ttu-id="ab52e-152"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab52e-152"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ab52e-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab52e-153">Library</span></span><br/> | <dl> <span data-ttu-id="ab52e-154"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ab52e-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




