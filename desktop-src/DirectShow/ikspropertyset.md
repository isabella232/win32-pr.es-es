---
description: 'La interfaz IKsPropertySet se diseñó originalmente como una forma eficaz de establecer y recuperar las propiedades del dispositivo en los controladores WDM, mediante KSProxy para traducir las llamadas a métodos COM en modo de usuario en los conjuntos de propiedades de modo kernel utilizados por los controladores de clase de transmisión por secuencias WDM. Esta interfaz se usa ahora también para pasar información de forma estricta entre los componentes de software. En algunos casos, los componentes de software deben implementar esta interfaz, o bien la interfaz IKsControl (documentada en el DDK de DirectShow). Por ejemplo, si está escribiendo un descodificador MPEG-2 de software para usarlo con el navegador de DVD, debe implementar una de estas interfaces y también admitir los conjuntos de propiedades relacionados con el DVD que el navegador enviará al descodificador. Los pin pueden admitir una de estas interfaces para permitir que otros PIN o filtros establezcan o recuperen sus propiedades. Nota: existe otra interfaz con este nombre en el archivo de encabezado dsound. h. Las dos interfaces no son compatibles. La interfaz IKsControl, documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre controladores WDM y componentes de modo de usuario. .'
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: Interfaz IKsPropertySet (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494332"
---
# <a name="ikspropertyset-interface"></a><span data-ttu-id="173e3-109">Interfaz IKsPropertySet</span><span class="sxs-lookup"><span data-stu-id="173e3-109">IKsPropertySet interface</span></span>

<span data-ttu-id="173e3-110">La `IKsPropertySet` interfaz se diseñó originalmente como una forma eficaz de establecer y recuperar las propiedades del dispositivo en los controladores WDM, mediante KSProxy para traducir las llamadas a métodos com en modo de usuario en los conjuntos de propiedades de modo kernel usados por los controladores de clase de transmisión por secuencias WDM.</span><span class="sxs-lookup"><span data-stu-id="173e3-110">The `IKsPropertySet` interface was originally designed as an efficient way to set and retrieve device properties on WDM drivers, using KSProxy to translate the user-mode COM method calls into the kernel-mode property sets used by WDM streaming class drivers.</span></span> <span data-ttu-id="173e3-111">Esta interfaz se usa ahora también para pasar información de forma estricta entre los componentes de software.</span><span class="sxs-lookup"><span data-stu-id="173e3-111">This interface is now also used to pass information strictly between software components.</span></span>

<span data-ttu-id="173e3-112">En algunos casos, los componentes de software deben implementar esta interfaz, o bien la interfaz **IKsControl** (documentada en el DDK de DirectShow).</span><span class="sxs-lookup"><span data-stu-id="173e3-112">In some cases, software components must implement either this interface, or else the **IKsControl** interface (documented in the DirectShow DDK).</span></span> <span data-ttu-id="173e3-113">Por ejemplo, si está escribiendo un descodificador MPEG-2 de software para usarlo con el [navegador de DVD](dvd-navigator-filter.md), debe implementar una de estas interfaces y también admitir los conjuntos de propiedades relacionados con el DVD que el navegador enviará al descodificador.</span><span class="sxs-lookup"><span data-stu-id="173e3-113">For example, if you are writing a software MPEG-2 decoder for use with the [DVD Navigator](dvd-navigator-filter.md), you must implement one of these interfaces and also support the DVD-related property sets that the Navigator will send to the decoder.</span></span> <span data-ttu-id="173e3-114">Los pin pueden admitir una de estas interfaces para permitir que otros PIN o filtros establezcan o recuperen sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="173e3-114">Pins may support one of these interfaces to allow other pins or filters to set or retrieve their properties.</span></span>

> [!Note]  
> <span data-ttu-id="173e3-115">Existe otra interfaz con este nombre en el archivo de encabezado dsound. h.</span><span class="sxs-lookup"><span data-stu-id="173e3-115">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="173e3-116">Las dos interfaces no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="173e3-116">The two interfaces are not compatible.</span></span> <span data-ttu-id="173e3-117">La interfaz **IKsControl** , documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre controladores WDM y componentes de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="173e3-117">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

## <a name="members"></a><span data-ttu-id="173e3-118">Miembros</span><span class="sxs-lookup"><span data-stu-id="173e3-118">Members</span></span>

<span data-ttu-id="173e3-119">La interfaz **IKsPropertySet** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="173e3-119">The **IKsPropertySet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="173e3-120">**IKsPropertySet** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="173e3-120">**IKsPropertySet** also has these types of members:</span></span>

-   [<span data-ttu-id="173e3-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="173e3-121">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="173e3-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="173e3-122">Methods</span></span>

<span data-ttu-id="173e3-123">La interfaz **IKsPropertySet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="173e3-123">The **IKsPropertySet** interface has these methods.</span></span>



| <span data-ttu-id="173e3-124">Método</span><span class="sxs-lookup"><span data-stu-id="173e3-124">Method</span></span>                                                  | <span data-ttu-id="173e3-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="173e3-125">Description</span></span>                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="173e3-126">**Obtener**</span><span class="sxs-lookup"><span data-stu-id="173e3-126">**Get**</span></span>](ikspropertyset-get.md)                       | <span data-ttu-id="173e3-127">Recupera una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="173e3-127">Retrieves a property identified by a property set GUID and a property ID.</span></span><br/> |
| [<span data-ttu-id="173e3-128">**QuerySupported**</span><span class="sxs-lookup"><span data-stu-id="173e3-128">**QuerySupported**</span></span>](ikspropertyset-querysupported.md) | <span data-ttu-id="173e3-129">Determina si un objeto admite un conjunto de propiedades especificado.</span><span class="sxs-lookup"><span data-stu-id="173e3-129">Determines whether an object supports a specified property set.</span></span><br/>           |
| [<span data-ttu-id="173e3-130">**Conjunto**</span><span class="sxs-lookup"><span data-stu-id="173e3-130">**Set**</span></span>](ikspropertyset-set.md)                       | <span data-ttu-id="173e3-131">Establece una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="173e3-131">Sets a property identified by a property set GUID and a property ID.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="173e3-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="173e3-132">Remarks</span></span>

<span data-ttu-id="173e3-133">Debe incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="173e3-133">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="173e3-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="173e3-134">Requirements</span></span>



| <span data-ttu-id="173e3-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="173e3-135">Requirement</span></span> | <span data-ttu-id="173e3-136">Value</span><span class="sxs-lookup"><span data-stu-id="173e3-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="173e3-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="173e3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="173e3-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="173e3-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="173e3-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="173e3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="173e3-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="173e3-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="173e3-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="173e3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="173e3-142"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="173e3-142"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="173e3-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="173e3-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="173e3-144"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="173e3-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="173e3-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="173e3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="173e3-146">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="173e3-146">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
