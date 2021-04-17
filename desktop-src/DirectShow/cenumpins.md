---
description: La clase CEnumPins implementa un enumerador para los pin.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: Clase CEnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660856"
---
# <a name="cenumpins-class"></a><span data-ttu-id="8f77e-103">Clase CEnumPins</span><span class="sxs-lookup"><span data-stu-id="8f77e-103">CEnumPins class</span></span>

![jerarquía de clases cenumpins](images/filter03.png)

<span data-ttu-id="8f77e-105">La `CEnumPins` clase implementa un enumerador para los pin.</span><span class="sxs-lookup"><span data-stu-id="8f77e-105">The `CEnumPins` class implements an enumerator for pins.</span></span>

<span data-ttu-id="8f77e-106">Esta clase implementa la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="8f77e-106">This class implements the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="8f77e-107">Llama a los siguientes métodos [**CBaseFilter**](cbasefilter.md) :</span><span class="sxs-lookup"><span data-stu-id="8f77e-107">It calls the following [**CBaseFilter**](cbasefilter.md) methods:</span></span>

-   <span data-ttu-id="8f77e-108">[**CBaseFilter:: GetPin**](cbasefilter-getpin.md): recupera un PIN en el filtro, al que hace referencia un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="8f77e-108">[**CBaseFilter::GetPin**](cbasefilter-getpin.md): Retrieves a pin on the filter, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="8f77e-109">[**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md): recupera el número total de clavijas del filtro.</span><span class="sxs-lookup"><span data-stu-id="8f77e-109">[**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md): Retrieves the total number of pins on the filter.</span></span>
-   <span data-ttu-id="8f77e-110">[**CBaseFilter:: GetPinVersion**](cbasefilter-getpinversion.md): determina si los pin han cambiado.</span><span class="sxs-lookup"><span data-stu-id="8f77e-110">[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md): Determines whether the pins have changed.</span></span>

<span data-ttu-id="8f77e-111">Si el filtro crea o destruye dinámicamente los pin, incrementa la versión del PIN cada vez que cambian los pin.</span><span class="sxs-lookup"><span data-stu-id="8f77e-111">If the filter dynamically creates or destroys pins, it increments the pin version whenever the pins change.</span></span> <span data-ttu-id="8f77e-112">Si el número de versión cambia, el objeto de enumerador ya no se sincroniza con el filtro.</span><span class="sxs-lookup"><span data-stu-id="8f77e-112">If the version number changes, the enumerator object is no longer synchronized with the filter.</span></span> <span data-ttu-id="8f77e-113">Una vez que el enumerador no está sincronizado, los métodos de `CEnumPins` devuelven la \_ enumeración VFW E no \_ \_ \_ \_ sincronizada.</span><span class="sxs-lookup"><span data-stu-id="8f77e-113">Once the enumerator is out of sync, the methods in `CEnumPins` return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="8f77e-114">Llame al método [**CEnumPins:: RESET**](cenumpins-reset.md) para volver a sincronizar el enumerador.</span><span class="sxs-lookup"><span data-stu-id="8f77e-114">Call the [**CEnumPins::Reset**](cenumpins-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="8f77e-115">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="8f77e-115">Public Methods</span></span>                             | <span data-ttu-id="8f77e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f77e-116">Description</span></span>                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="8f77e-117">**CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="8f77e-117">**CEnumPins**</span></span>](cenumpins-cenumpins.md)   | <span data-ttu-id="8f77e-118">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="8f77e-118">Constructor method.</span></span>                                             |
| [<span data-ttu-id="8f77e-119">**~ CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="8f77e-119">**~CEnumPins**</span></span>](cenumpins--cenumpins.md) | <span data-ttu-id="8f77e-120">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="8f77e-120">Destructor method.</span></span> <span data-ttu-id="8f77e-121">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="8f77e-121">Virtual.</span></span>                                     |
| <span data-ttu-id="8f77e-122">Métodos IEnumPins</span><span class="sxs-lookup"><span data-stu-id="8f77e-122">IEnumPins Methods</span></span>                          | <span data-ttu-id="8f77e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f77e-123">Description</span></span>                                                     |
| [<span data-ttu-id="8f77e-124">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="8f77e-124">**Clone**</span></span>](cenumpins-clone.md)           | <span data-ttu-id="8f77e-125">Realiza una copia del enumerador con el mismo estado de enumeración.</span><span class="sxs-lookup"><span data-stu-id="8f77e-125">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="8f77e-126">**Next**</span><span class="sxs-lookup"><span data-stu-id="8f77e-126">**Next**</span></span>](cenumpins-next.md)             | <span data-ttu-id="8f77e-127">Recupera un número especificado de clavijas.</span><span class="sxs-lookup"><span data-stu-id="8f77e-127">Retrieves a specified number of pins.</span></span>                           |
| [<span data-ttu-id="8f77e-128">**Reset**</span><span class="sxs-lookup"><span data-stu-id="8f77e-128">**Reset**</span></span>](cenumpins-reset.md)           | <span data-ttu-id="8f77e-129">Restablece la secuencia de enumeración al principio.</span><span class="sxs-lookup"><span data-stu-id="8f77e-129">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="8f77e-130">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="8f77e-130">**Skip**</span></span>](cenumpins-skip.md)             | <span data-ttu-id="8f77e-131">Omite un número especificado de clavijas.</span><span class="sxs-lookup"><span data-stu-id="8f77e-131">Skips over a specified number of pins.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="8f77e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f77e-132">Requirements</span></span>



| <span data-ttu-id="8f77e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f77e-133">Requirement</span></span> | <span data-ttu-id="8f77e-134">Value</span><span class="sxs-lookup"><span data-stu-id="8f77e-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f77e-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f77e-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8f77e-136"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f77e-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8f77e-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f77e-137">Library</span></span><br/> | <dl> <span data-ttu-id="8f77e-138"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8f77e-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




