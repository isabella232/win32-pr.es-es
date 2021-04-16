---
description: La clase CMediaPosition controla los métodos IDispatch de la interfaz dual IMediaPosition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: Clase CMediaPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60d06a08badf3302ef4ddb352d840842a2605600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679298"
---
# <a name="cmediaposition-class"></a><span data-ttu-id="0b28a-103">Clase CMediaPosition</span><span class="sxs-lookup"><span data-stu-id="0b28a-103">CMediaPosition class</span></span>

![jerarquía de clases cmediaposition](images/cutil14.png)

<span data-ttu-id="0b28a-105">La clase **CMediaPosition** controla los métodos **IDispatch** de la interfaz dual [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .</span><span class="sxs-lookup"><span data-stu-id="0b28a-105">The **CMediaPosition** class handles the **IDispatch** methods of the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) dual interface.</span></span>

<span data-ttu-id="0b28a-106">Esta clase hereda la interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) , pero no la implementa.</span><span class="sxs-lookup"><span data-stu-id="0b28a-106">This class inherits the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface but does not implement it.</span></span> <span data-ttu-id="0b28a-107">Implementa **IDispatch** a través de la clase [**CBaseDispatch**](cbasedispatch.md) y la biblioteca de tipos de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0b28a-107">It implements **IDispatch** through the [**CBaseDispatch**](cbasedispatch.md) class and the DirectShow type library.</span></span> <span data-ttu-id="0b28a-108">No utilice esta clase directamente.</span><span class="sxs-lookup"><span data-stu-id="0b28a-108">Do not use this class directly.</span></span> <span data-ttu-id="0b28a-109">En su lugar, utilice una de las clases siguientes:</span><span class="sxs-lookup"><span data-stu-id="0b28a-109">Instead, use one of the following classes:</span></span>

-   <span data-ttu-id="0b28a-110">Filtros de origen: Use la clase base [**CSourceSeeking**](csourceseeking.md) para implementar operaciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0b28a-110">Source filters: Use the [**CSourceSeeking**](csourceseeking.md) base class to implement seeking.</span></span>
-   <span data-ttu-id="0b28a-111">Filtros de transformación: Use la clase [**CPosPassThru**](cpospassthru.md) para pasar los comandos de búsqueda ascendentes.</span><span class="sxs-lookup"><span data-stu-id="0b28a-111">Transform filters: Use the [**CPosPassThru**](cpospassthru.md) class to pass seeking commands upstream.</span></span>
-   <span data-ttu-id="0b28a-112">Representadores: Use la clase [**CRendererPosPassThru**](crendererpospassthru.md) para pasar comandos de búsqueda ascendentes.</span><span class="sxs-lookup"><span data-stu-id="0b28a-112">Renderers: Use the [**CRendererPosPassThru**](crendererpospassthru.md) class to pass seeking commands upstream.</span></span>



| <span data-ttu-id="0b28a-113">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="0b28a-113">Public Methods</span></span>                                              | <span data-ttu-id="0b28a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b28a-114">Description</span></span>                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b28a-115">**CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="0b28a-115">**CMediaPosition**</span></span>](cmediaposition-cmediaposition.md)     | <span data-ttu-id="0b28a-116">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="0b28a-116">Constructor method.</span></span>                                                                                                 |
| <span data-ttu-id="0b28a-117">Métodos IDispatch</span><span class="sxs-lookup"><span data-stu-id="0b28a-117">IDispatch Methods</span></span>                                           | <span data-ttu-id="0b28a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b28a-118">Description</span></span>                                                                                                         |
| [<span data-ttu-id="0b28a-119">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="0b28a-119">**GetIDsOfNames**</span></span>](cmediaposition-getidsofnames.md)       | <span data-ttu-id="0b28a-120">Asigna un conjunto de nombres a un conjunto correspondiente de DispId.</span><span class="sxs-lookup"><span data-stu-id="0b28a-120">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="0b28a-121">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="0b28a-121">**GetTypeInfo**</span></span>](cmediaposition-gettypeinfo.md)           | <span data-ttu-id="0b28a-122">Recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="0b28a-122">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="0b28a-123">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="0b28a-123">**GetTypeInfoCount**</span></span>](cmediaposition-gettypeinfocount.md) | <span data-ttu-id="0b28a-124">Recupera el número de interfaces de información de tipo que proporciona el objeto.</span><span class="sxs-lookup"><span data-stu-id="0b28a-124">Retrieves the number of type information interfaces the object provides.</span></span>                                            |
| [<span data-ttu-id="0b28a-125">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="0b28a-125">**Invoke**</span></span>](cmediaposition-invoke.md)                     | <span data-ttu-id="0b28a-126">Proporciona acceso a las propiedades y los métodos expuestos por el objeto.</span><span class="sxs-lookup"><span data-stu-id="0b28a-126">Provides access to properties and methods exposed by the object.</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="0b28a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b28a-127">Requirements</span></span>



| <span data-ttu-id="0b28a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b28a-128">Requirement</span></span> | <span data-ttu-id="0b28a-129">Value</span><span class="sxs-lookup"><span data-stu-id="0b28a-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b28a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b28a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0b28a-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b28a-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0b28a-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b28a-132">Library</span></span><br/> | <dl> <span data-ttu-id="0b28a-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0b28a-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b28a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b28a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b28a-135">Clases base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="0b28a-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




