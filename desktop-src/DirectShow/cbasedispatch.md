---
description: La clase CBaseDispatch es una clase base para implementar la interfaz IDispatch en un filtro DirectShow.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: Clase CBaseDispatch (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660578"
---
# <a name="cbasedispatch-class"></a><span data-ttu-id="9eb02-103">Clase CBaseDispatch</span><span class="sxs-lookup"><span data-stu-id="9eb02-103">CBaseDispatch class</span></span>

![jerarquía de clases cbasedispatch](images/cutil01.png)

<span data-ttu-id="9eb02-105">La clase **CBaseDispatch** es una clase base para implementar la interfaz **IDispatch** en un filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9eb02-105">The **CBaseDispatch** class is a base class for implementing the **IDispatch** interface in a DirectShow filter.</span></span>

<span data-ttu-id="9eb02-106">Esta clase se limita a admitir las interfaces compatibles con automatización exportadas por la biblioteca de tipos de DirectShow, QuartzTypeLib.</span><span class="sxs-lookup"><span data-stu-id="9eb02-106">This class is limited to supporting the Automation-compatible interfaces exported by the DirectShow type library, QuartzTypeLib.</span></span> <span data-ttu-id="9eb02-107">Por ejemplo, las clases [**CMediaControl**](cmediacontrol.md) y [**CMediaPosition**](cmediaposition.md) usan **CBaseDispatch** para implementar [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) y [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9eb02-107">For example, the [**CMediaControl**](cmediacontrol.md) and [**CMediaPosition**](cmediaposition.md) classes use **CBaseDispatch** to implement [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectively.</span></span> <span data-ttu-id="9eb02-108">Debido a esta limitación, probablemente no haya ningún motivo para usar **CBaseDispatch** directamente en sus propios filtros.</span><span class="sxs-lookup"><span data-stu-id="9eb02-108">Because of this limitation, there is probably no reason to use **CBaseDispatch** directly in your own filters.</span></span>

<span data-ttu-id="9eb02-109">Para usar esta clase, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9eb02-109">To use this class, do the following:</span></span>

-   <span data-ttu-id="9eb02-110">Declare una nueva clase que admita **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="9eb02-110">Declare a new class that supports **IDispatch**.</span></span>
-   <span data-ttu-id="9eb02-111">Asigne a la nueva clase una variable miembro privada de tipo **CBaseDispatch**.</span><span class="sxs-lookup"><span data-stu-id="9eb02-111">Give your new class a private member variable of type **CBaseDispatch**.</span></span>
-   <span data-ttu-id="9eb02-112">Implemente los métodos **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="9eb02-112">Implement the **IDispatch** methods.</span></span>
-   <span data-ttu-id="9eb02-113">En los métodos **IDispatch** , llame a los métodos **CBaseDispatch** .</span><span class="sxs-lookup"><span data-stu-id="9eb02-113">In your **IDispatch** methods, call the **CBaseDispatch** methods.</span></span>

<span data-ttu-id="9eb02-114">Para obtener más información, consulte el código fuente de cualquiera de las clases de ejemplo declaradas en Ctlutil. h.</span><span class="sxs-lookup"><span data-stu-id="9eb02-114">For more details, refer to the source code for any of the sample classes declared in Ctlutil.h.</span></span>



| <span data-ttu-id="9eb02-115">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="9eb02-115">Public Methods</span></span>                                             | <span data-ttu-id="9eb02-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="9eb02-116">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eb02-117">**CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="9eb02-117">**CBaseDispatch**</span></span>](cbasedispatch-cbasedispatch.md)       | <span data-ttu-id="9eb02-118">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="9eb02-118">Constructor method.</span></span>                                                                                                 |
| [<span data-ttu-id="9eb02-119">**~ CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="9eb02-119">**~CBaseDispatch**</span></span>](cbasedispatch--cbasedispatch.md)     | <span data-ttu-id="9eb02-120">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="9eb02-120">Destructor method.</span></span>                                                                                                  |
| [<span data-ttu-id="9eb02-121">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="9eb02-121">**GetIDsOfNames**</span></span>](cbasedispatch-getidsofnames.md)       | <span data-ttu-id="9eb02-122">Asigna un conjunto de nombres a un conjunto correspondiente de DispId.</span><span class="sxs-lookup"><span data-stu-id="9eb02-122">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="9eb02-123">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="9eb02-123">**GetTypeInfo**</span></span>](cbasedispatch-gettypeinfo.md)           | <span data-ttu-id="9eb02-124">Recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="9eb02-124">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="9eb02-125">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="9eb02-125">**GetTypeInfoCount**</span></span>](cbasedispatch-gettypeinfocount.md) | <span data-ttu-id="9eb02-126">Recupera el número de interfaces de información de tipo que proporciona el objeto.</span><span class="sxs-lookup"><span data-stu-id="9eb02-126">Retrieves the number of type information interfaces the object provides.</span></span>                                            |



 

## <a name="requirements"></a><span data-ttu-id="9eb02-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eb02-127">Requirements</span></span>



| <span data-ttu-id="9eb02-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb02-128">Requirement</span></span> | <span data-ttu-id="9eb02-129">Value</span><span class="sxs-lookup"><span data-stu-id="9eb02-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb02-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9eb02-130">Header</span></span><br/>  | <dl> <span data-ttu-id="9eb02-131"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9eb02-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9eb02-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9eb02-132">Library</span></span><br/> | <dl> <span data-ttu-id="9eb02-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9eb02-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eb02-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9eb02-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb02-135">Clases base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="9eb02-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




