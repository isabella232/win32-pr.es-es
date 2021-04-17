---
description: La clase CRendererPosPassThru controla los comandos de búsqueda para los filtros de representador, pasándolos al siguiente filtro.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: Clase CRendererPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670727"
---
# <a name="crendererpospassthru-class"></a><span data-ttu-id="f3ac2-103">Clase CRendererPosPassThru</span><span class="sxs-lookup"><span data-stu-id="f3ac2-103">CRendererPosPassThru class</span></span>

![jerarquía de clases crendererpospassthru](images/cutil14.png)

<span data-ttu-id="f3ac2-105">La `CRendererPosPassThru` clase controla los comandos de búsqueda para los filtros de representador, pasándolos al siguiente filtro.</span><span class="sxs-lookup"><span data-stu-id="f3ac2-105">The `CRendererPosPassThru` class handles seek commands for renderer filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="f3ac2-106">Esta clase se deriva de la clase [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="f3ac2-106">This class derives from the [**CPosPassThru**](cpospassthru.md) class.</span></span> <span data-ttu-id="f3ac2-107">Agrega compatibilidad para el almacenamiento en caché de las marcas de tiempo de los ejemplos a medida que llegan.</span><span class="sxs-lookup"><span data-stu-id="f3ac2-107">It adds support for caching the time stamps from samples as they arrive.</span></span> <span data-ttu-id="f3ac2-108">Utilice esta clase de la misma forma que la clase **CPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="f3ac2-108">Use this class in the same way as the **CPosPassThru** class.</span></span> <span data-ttu-id="f3ac2-109">Consulte la documentación de **CPosPassThru** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f3ac2-109">Refer to the **CPosPassThru** documentation for details.</span></span>

<span data-ttu-id="f3ac2-110">El filtro de representador debe actualizar las `CRendererPosPassThru` marcas de tiempo almacenadas en caché del objeto, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f3ac2-110">The renderer filter must update the `CRendererPosPassThru` object's cached time stamps, as follows:</span></span>

-   <span data-ttu-id="f3ac2-111">Para cada ejemplo que recibe el filtro, llame al método [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="f3ac2-111">For each sample the filter receives, call the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method.</span></span>
-   <span data-ttu-id="f3ac2-112">Cuando se detenga el filtro o reciba una llamada **EndFlush** , llame al método [**CRendererPosPassThru:: ResetMediaTime**](crendererpospassthru-resetmediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="f3ac2-112">When the filter is stopped or receives an **EndFlush** call, call the [**CRendererPosPassThru::ResetMediaTime**](crendererpospassthru-resetmediatime.md) method.</span></span>
-   <span data-ttu-id="f3ac2-113">Cuando el filtro recibe una notificación de final de secuencia, llame al método [**CRendererPosPassThru:: EOS**](crendererpospassthru-eos.md) .</span><span class="sxs-lookup"><span data-stu-id="f3ac2-113">When the filter receives an end-of-stream notification, call the [**CRendererPosPassThru::EOS**](crendererpospassthru-eos.md) method.</span></span>

<span data-ttu-id="f3ac2-114">Para obtener un ejemplo de cómo usar esta clase, consulte el código fuente de [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="f3ac2-114">For an example of how to use this class, refer to the [**CBaseRenderer**](cbaserenderer.md) source code.</span></span>



| <span data-ttu-id="f3ac2-115">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="f3ac2-115">Public Methods</span></span>                                                            | <span data-ttu-id="f3ac2-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3ac2-116">Description</span></span>                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="f3ac2-117">**CRendererPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="f3ac2-117">**CRendererPosPassThru**</span></span>](crendererpospassthru-crendererpospassthru.md) | <span data-ttu-id="f3ac2-118">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="f3ac2-118">Constructor method.</span></span>                                                 |
| [<span data-ttu-id="f3ac2-119">**GetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="f3ac2-119">**GetMediaTime**</span></span>](crendererpospassthru-getmediatime.md)                 | <span data-ttu-id="f3ac2-120">Recupera las marcas de tiempo en el ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="f3ac2-120">Retrieves the time stamps on the current sample.</span></span>                    |
| [<span data-ttu-id="f3ac2-121">**RegisterMediaTime**</span><span class="sxs-lookup"><span data-stu-id="f3ac2-121">**RegisterMediaTime**</span></span>](crendererpospassthru-registermediatime.md)       | <span data-ttu-id="f3ac2-122">Almacena en memoria caché las marcas de tiempo del ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="f3ac2-122">Caches the time stamps from the current sample.</span></span>                     |
| [<span data-ttu-id="f3ac2-123">**ResetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="f3ac2-123">**ResetMediaTime**</span></span>](crendererpospassthru-resetmediatime.md)             | <span data-ttu-id="f3ac2-124">Restablece el valor cero de las marcas de tiempo almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="f3ac2-124">Resets the cached time stamps to zero.</span></span>                              |
| [<span data-ttu-id="f3ac2-125">**OCASIONA**</span><span class="sxs-lookup"><span data-stu-id="f3ac2-125">**EOS**</span></span>](crendererpospassthru-eos.md)                                   | <span data-ttu-id="f3ac2-126">Actualiza las marcas de tiempo almacenadas en caché después de una notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="f3ac2-126">Updates the cached time stamps after an end-of-stream notification.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f3ac2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3ac2-127">Requirements</span></span>



| <span data-ttu-id="f3ac2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3ac2-128">Requirement</span></span> | <span data-ttu-id="f3ac2-129">Value</span><span class="sxs-lookup"><span data-stu-id="f3ac2-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ac2-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3ac2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f3ac2-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3ac2-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f3ac2-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3ac2-132">Library</span></span><br/> | <dl> <span data-ttu-id="f3ac2-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f3ac2-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




