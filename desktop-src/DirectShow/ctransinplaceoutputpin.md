---
description: La clase CTransInPlaceOutputPin implementa un PIN de salida que se usa en la clase CTransInPlaceFilter.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Clase CTransInPlaceOutputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679238"
---
# <a name="ctransinplaceoutputpin-class"></a><span data-ttu-id="06f99-103">Clase CTransInPlaceOutputPin</span><span class="sxs-lookup"><span data-stu-id="06f99-103">CTransInPlaceOutputPin class</span></span>

![jerarquía de clases ctransinplaceoutputpin](images/tsip02.png)

<span data-ttu-id="06f99-105">La `CTransInPlaceOutputPin` clase implementa un PIN de salida que se usa en la clase [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="06f99-105">The `CTransInPlaceOutputPin` class implements an output pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="06f99-106">Normalmente, no es necesario derivar de esta clase.</span><span class="sxs-lookup"><span data-stu-id="06f99-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="06f99-107">Si lo hace, debe invalidar el método [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) del filtro para crear instancias de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="06f99-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="06f99-108">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="06f99-108">Protected Member Variables</span></span>                                                      | <span data-ttu-id="06f99-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="06f99-109">Description</span></span>                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="06f99-110">**m \_ pTIPFilter**</span><span class="sxs-lookup"><span data-stu-id="06f99-110">**m\_pTIPFilter**</span></span>](ctransinplaceoutputpin-m-ptipfilter.md)                    | <span data-ttu-id="06f99-111">Puntero al filtro que creó este pin.</span><span class="sxs-lookup"><span data-stu-id="06f99-111">Pointer to the filter that created this pin.</span></span>         |
| <span data-ttu-id="06f99-112">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="06f99-112">Public Methods</span></span>                                                                  | <span data-ttu-id="06f99-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="06f99-113">Description</span></span>                                          |
| [<span data-ttu-id="06f99-114">**CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="06f99-114">**CTransInPlaceOutputPin**</span></span>](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | <span data-ttu-id="06f99-115">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="06f99-115">Constructor method.</span></span>                                  |
| [<span data-ttu-id="06f99-116">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="06f99-116">**CheckMediaType**</span></span>](ctransinplaceoutputpin-checkmediatype.md)                 | <span data-ttu-id="06f99-117">Determina si el PIN acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="06f99-117">Determines if the pin accepts a specific media type.</span></span> |
| [<span data-ttu-id="06f99-118">**SetAllocator**</span><span class="sxs-lookup"><span data-stu-id="06f99-118">**SetAllocator**</span></span>](ctransinplaceoutputpin-setallocator.md)                     | <span data-ttu-id="06f99-119">Especifica un asignador para la conexión.</span><span class="sxs-lookup"><span data-stu-id="06f99-119">Specifies an allocator for the connection.</span></span>           |
| [<span data-ttu-id="06f99-120">**ConnectedIMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="06f99-120">**ConnectedIMemInputPin**</span></span>](ctransinplaceoutputpin-connectedimeminputpin.md)   | <span data-ttu-id="06f99-121">Recupera un puntero al pin de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="06f99-121">Retrieves a pointer to the downstream input pin.</span></span>     |
| [<span data-ttu-id="06f99-122">**PeekAllocator**</span><span class="sxs-lookup"><span data-stu-id="06f99-122">**PeekAllocator**</span></span>](ctransinplaceoutputpin-peekallocator.md)                   | <span data-ttu-id="06f99-123">Recupera un puntero al asignador del PIN.</span><span class="sxs-lookup"><span data-stu-id="06f99-123">Retrieves a pointer to the pin's allocator.</span></span>          |
| <span data-ttu-id="06f99-124">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="06f99-124">IPin Methods</span></span>                                                                    | <span data-ttu-id="06f99-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="06f99-125">Description</span></span>                                          |
| [<span data-ttu-id="06f99-126">**EnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="06f99-126">**EnumMediaTypes**</span></span>](ctransinplaceoutputpin-enummediatypes.md)                 | <span data-ttu-id="06f99-127">Enumera los tipos de medios preferidos del PIN.</span><span class="sxs-lookup"><span data-stu-id="06f99-127">Enumerates the pin's preferred media types.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="06f99-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06f99-128">Requirements</span></span>



| <span data-ttu-id="06f99-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="06f99-129">Requirement</span></span> | <span data-ttu-id="06f99-130">Value</span><span class="sxs-lookup"><span data-stu-id="06f99-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06f99-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06f99-131">Header</span></span><br/>  | <dl> <span data-ttu-id="06f99-132"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06f99-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="06f99-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06f99-133">Library</span></span><br/> | <dl> <span data-ttu-id="06f99-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="06f99-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




