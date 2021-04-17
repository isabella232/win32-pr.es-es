---
description: La clase CTransformOutputPin implementa un PIN de salida que se usa en la clase CTransformFilter.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: Clase CTransformOutputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681107"
---
# <a name="ctransformoutputpin-class"></a><span data-ttu-id="bcb48-103">Clase CTransformOutputPin</span><span class="sxs-lookup"><span data-stu-id="bcb48-103">CTransformOutputPin class</span></span>

![jerarquía de clases ctransformoutputpin](images/tfrm02.png)

<span data-ttu-id="bcb48-105">La `CTransformOutputPin` clase implementa un PIN de salida que se usa en la clase [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="bcb48-105">The `CTransformOutputPin` class implements an output pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="bcb48-106">Normalmente, no es necesario derivar de esta clase.</span><span class="sxs-lookup"><span data-stu-id="bcb48-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="bcb48-107">La mayoría de los métodos de esta clase llaman a los métodos correspondientes en la clase **CTransformFilter** , que puede invalidar.</span><span class="sxs-lookup"><span data-stu-id="bcb48-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="bcb48-108">Si deriva de esta clase, debe invalidar el método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) del filtro para crear instancias de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="bcb48-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>

<span data-ttu-id="bcb48-109">Esta clase expone las interfaces **IMediaSeeking** y **IMediaPosition** a través del objeto [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="bcb48-109">This class exposes the **IMediaSeeking** and **IMediaPosition** interfaces through the [**CPosPassThru**](cpospassthru.md) object.</span></span> <span data-ttu-id="bcb48-110">Pasa todas las solicitudes de búsqueda al siguiente filtro ascendente.</span><span class="sxs-lookup"><span data-stu-id="bcb48-110">It passes all seek requests to the next filter upstream.</span></span>



| <span data-ttu-id="bcb48-111">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="bcb48-111">Protected Member Variables</span></span>                                               | <span data-ttu-id="bcb48-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcb48-112">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="bcb48-113">**m \_ pTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="bcb48-113">**m\_pTransformFilter**</span></span>](ctransformoutputpin-m-ptransformfilter.md)    | <span data-ttu-id="bcb48-114">Puntero al filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="bcb48-114">Pointer to the owning filter.</span></span>                            |
| <span data-ttu-id="bcb48-115">Variables de miembro público</span><span class="sxs-lookup"><span data-stu-id="bcb48-115">Public Member Variables</span></span>                                                  | <span data-ttu-id="bcb48-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcb48-116">Description</span></span>                                              |
| [<span data-ttu-id="bcb48-117">**m \_ pPosition**</span><span class="sxs-lookup"><span data-stu-id="bcb48-117">**m\_pPosition**</span></span>](ctransformoutputpin-m-pposition.md)                  | <span data-ttu-id="bcb48-118">Objeto auxiliar para pasar comandos de búsqueda ascendentes.</span><span class="sxs-lookup"><span data-stu-id="bcb48-118">Helper object to pass seek commands upstream.</span></span>            |
| <span data-ttu-id="bcb48-119">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="bcb48-119">Public Methods</span></span>                                                           | <span data-ttu-id="bcb48-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcb48-120">Description</span></span>                                              |
| [<span data-ttu-id="bcb48-121">**CTransformOutputPin**</span><span class="sxs-lookup"><span data-stu-id="bcb48-121">**CTransformOutputPin**</span></span>](ctransformoutputpin-ctransformoutputpin.md)   | <span data-ttu-id="bcb48-122">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="bcb48-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="bcb48-123">**~ CTransformOutputPin**</span><span class="sxs-lookup"><span data-stu-id="bcb48-123">**~CTransformOutputPin**</span></span>](ctransformoutputpin--ctransformoutputpin.md) | <span data-ttu-id="bcb48-124">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="bcb48-124">Destructor method.</span></span>                                       |
| [<span data-ttu-id="bcb48-125">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="bcb48-125">**CheckConnect**</span></span>](ctransformoutputpin-checkconnect.md)                 | <span data-ttu-id="bcb48-126">Determina si una conexión de PIN es adecuada.</span><span class="sxs-lookup"><span data-stu-id="bcb48-126">Determines whether a pin connection is suitable.</span></span>         |
| [<span data-ttu-id="bcb48-127">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="bcb48-127">**BreakConnect**</span></span>](ctransformoutputpin-breakconnect.md)                 | <span data-ttu-id="bcb48-128">Libera el PIN de una conexión.</span><span class="sxs-lookup"><span data-stu-id="bcb48-128">Releases the pin from a connection.</span></span>                      |
| [<span data-ttu-id="bcb48-129">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="bcb48-129">**CompleteConnect**</span></span>](ctransformoutputpin-completeconnect.md)           | <span data-ttu-id="bcb48-130">Completa una conexión a otro PIN.</span><span class="sxs-lookup"><span data-stu-id="bcb48-130">Completes a connection to another pin.</span></span>                   |
| [<span data-ttu-id="bcb48-131">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="bcb48-131">**CheckMediaType**</span></span>](ctransformoutputpin-checkmediatype.md)             | <span data-ttu-id="bcb48-132">Determina si el PIN acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="bcb48-132">Determines if the pin accepts a specific media type.</span></span>     |
| [<span data-ttu-id="bcb48-133">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="bcb48-133">**SetMediaType**</span></span>](ctransformoutputpin-setmediatype.md)                 | <span data-ttu-id="bcb48-134">Establece el tipo de medio para la conexión.</span><span class="sxs-lookup"><span data-stu-id="bcb48-134">Sets the media type for the connection.</span></span>                  |
| [<span data-ttu-id="bcb48-135">**DecideBufferSize**</span><span class="sxs-lookup"><span data-stu-id="bcb48-135">**DecideBufferSize**</span></span>](ctransformoutputpin-decidebuffersize.md)         | <span data-ttu-id="bcb48-136">Establece los requisitos de búfer.</span><span class="sxs-lookup"><span data-stu-id="bcb48-136">Sets the buffer requirements.</span></span>                            |
| [<span data-ttu-id="bcb48-137">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="bcb48-137">**GetMediaType**</span></span>](ctransformoutputpin-getmediatype.md)                 | <span data-ttu-id="bcb48-138">Recupera un tipo de medio preferido, por valor de índice.</span><span class="sxs-lookup"><span data-stu-id="bcb48-138">Retrieves a preferred media type, by index value.</span></span>        |
| [<span data-ttu-id="bcb48-139">**CurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="bcb48-139">**CurrentMediaType**</span></span>](ctransformoutputpin-currentmediatype.md)         | <span data-ttu-id="bcb48-140">Recupera el tipo de medio para la conexión del PIN actual.</span><span class="sxs-lookup"><span data-stu-id="bcb48-140">Retrieves the media type for the current pin connection.</span></span> |
| <span data-ttu-id="bcb48-141">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="bcb48-141">IPin Methods</span></span>                                                             | <span data-ttu-id="bcb48-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcb48-142">Description</span></span>                                              |
| [<span data-ttu-id="bcb48-143">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="bcb48-143">**QueryId**</span></span>](ctransformoutputpin-queryid.md)                           | <span data-ttu-id="bcb48-144">Recupera un identificador para el código PIN.</span><span class="sxs-lookup"><span data-stu-id="bcb48-144">Retrieves an identifier for the pin.</span></span>                     |
| <span data-ttu-id="bcb48-145">Métodos IQualityControl</span><span class="sxs-lookup"><span data-stu-id="bcb48-145">IQualityControl Methods</span></span>                                                  | <span data-ttu-id="bcb48-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcb48-146">Description</span></span>                                              |
| [<span data-ttu-id="bcb48-147">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="bcb48-147">**Notify**</span></span>](ctransformoutputpin-notify.md)                             | <span data-ttu-id="bcb48-148">Notifica al pin que se ha solicitado un cambio de calidad.</span><span class="sxs-lookup"><span data-stu-id="bcb48-148">Notifies the pin that a quality change is requested.</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="bcb48-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcb48-149">Requirements</span></span>



| <span data-ttu-id="bcb48-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcb48-150">Requirement</span></span> | <span data-ttu-id="bcb48-151">Value</span><span class="sxs-lookup"><span data-stu-id="bcb48-151">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb48-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcb48-152">Header</span></span><br/>  | <dl> <span data-ttu-id="bcb48-153"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb48-153"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bcb48-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bcb48-154">Library</span></span><br/> | <dl> <span data-ttu-id="bcb48-155"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb48-155"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




