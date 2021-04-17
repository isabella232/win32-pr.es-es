---
description: La clase CEnumMediaTypes implementa un enumerador para los tipos de medios preferidos.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: Clase CEnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671157"
---
# <a name="cenummediatypes-class"></a><span data-ttu-id="0aa23-103">Clase CEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="0aa23-103">CEnumMediaTypes class</span></span>

![jerarquía de clases cenummediatypes](images/filter04.png)

<span data-ttu-id="0aa23-105">La `CEnumMediaTypes` clase implementa un enumerador para los tipos de medios preferidos.</span><span class="sxs-lookup"><span data-stu-id="0aa23-105">The `CEnumMediaTypes` class implements an enumerator for preferred media types.</span></span>

<span data-ttu-id="0aa23-106">Esta clase implementa la interfaz [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="0aa23-106">This class implements the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span> <span data-ttu-id="0aa23-107">Llama a los siguientes métodos [**CBasePin**](cbasepin.md) :</span><span class="sxs-lookup"><span data-stu-id="0aa23-107">It calls the following [**CBasePin**](cbasepin.md) methods:</span></span>

-   <span data-ttu-id="0aa23-108">[**CBasePin:: GetMediaType**](cbasepin-getmediatype.md): recupera un tipo de medio, al que hace referencia un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="0aa23-108">[**CBasePin::GetMediaType**](cbasepin-getmediatype.md):Retrieves a media type, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="0aa23-109">[**CBasePin:: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): determina si ha cambiado el conjunto de tipos preferidos.</span><span class="sxs-lookup"><span data-stu-id="0aa23-109">[**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): Determines whether the set of preferred types has changed.</span></span>

<span data-ttu-id="0aa23-110">Cada vez que un PIN modifica su lista de tipos de medios preferidos, el PIN incrementa el número de versión del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="0aa23-110">Whenever a pin alters its list of preferred media types, the pin increments the media-type version number.</span></span> <span data-ttu-id="0aa23-111">Cuando esto sucede, el objeto de enumerador ya no se sincroniza con el PIN y los métodos de clase devuelven la \_ \_ enumeración VFW E enum \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0aa23-111">When this happens, the enumerator object is no longer synchronized with the pin, and the class methods return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="0aa23-112">Llame al método [**CEnumMediaTypes:: RESET**](cenummediatypes-reset.md) para volver a sincronizar el enumerador.</span><span class="sxs-lookup"><span data-stu-id="0aa23-112">Call the [**CEnumMediaTypes::Reset**](cenummediatypes-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="0aa23-113">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="0aa23-113">Public Methods</span></span>                                               | <span data-ttu-id="0aa23-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0aa23-114">Description</span></span>                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="0aa23-115">**CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="0aa23-115">**CEnumMediaTypes**</span></span>](cenummediatypes-cenummediatypes.md)   | <span data-ttu-id="0aa23-116">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="0aa23-116">Constructor method.</span></span>                                             |
| [<span data-ttu-id="0aa23-117">**~ CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="0aa23-117">**~CEnumMediaTypes**</span></span>](cenummediatypes--cenummediatypes.md) | <span data-ttu-id="0aa23-118">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="0aa23-118">Destructor method.</span></span> <span data-ttu-id="0aa23-119">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="0aa23-119">Virtual.</span></span>                                     |
| <span data-ttu-id="0aa23-120">Métodos IEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="0aa23-120">IEnumMediaTypes Methods</span></span>                                      | <span data-ttu-id="0aa23-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0aa23-121">Description</span></span>                                                     |
| [<span data-ttu-id="0aa23-122">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="0aa23-122">**Clone**</span></span>](cenummediatypes-clone.md)                       | <span data-ttu-id="0aa23-123">Realiza una copia del enumerador con el mismo estado de enumeración.</span><span class="sxs-lookup"><span data-stu-id="0aa23-123">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="0aa23-124">**Next**</span><span class="sxs-lookup"><span data-stu-id="0aa23-124">**Next**</span></span>](cenummediatypes-next.md)                         | <span data-ttu-id="0aa23-125">Recupera un número especificado de tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="0aa23-125">Retrieves a specified number of media types.</span></span>                    |
| [<span data-ttu-id="0aa23-126">**Reset**</span><span class="sxs-lookup"><span data-stu-id="0aa23-126">**Reset**</span></span>](cenummediatypes-reset.md)                       | <span data-ttu-id="0aa23-127">Restablece la secuencia de enumeración al principio.</span><span class="sxs-lookup"><span data-stu-id="0aa23-127">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="0aa23-128">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="0aa23-128">**Skip**</span></span>](cenummediatypes-skip.md)                         | <span data-ttu-id="0aa23-129">Omite un número especificado de tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="0aa23-129">Skips over a specified number of media types.</span></span>                   |



 

## <a name="requirements"></a><span data-ttu-id="0aa23-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aa23-130">Requirements</span></span>



| <span data-ttu-id="0aa23-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa23-131">Requirement</span></span> | <span data-ttu-id="0aa23-132">Value</span><span class="sxs-lookup"><span data-stu-id="0aa23-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa23-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0aa23-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0aa23-134"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aa23-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0aa23-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0aa23-135">Library</span></span><br/> | <dl> <span data-ttu-id="0aa23-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0aa23-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




