---
description: Es idéntico a la colección InprocServers, salvo que esta colección también incluye servidores locales.
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: Colección LegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2ea542fa539ea1eb1cceae0f4cb8ba8dc2012085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677211"
---
# <a name="legacyservers-collection"></a><span data-ttu-id="9fa48-103">Colección LegacyServers</span><span class="sxs-lookup"><span data-stu-id="9fa48-103">LegacyServers collection</span></span>

<span data-ttu-id="9fa48-104">Es idéntico a la colección [**InprocServers**](inprocservers.md) , salvo que esta colección también incluye servidores locales.</span><span class="sxs-lookup"><span data-stu-id="9fa48-104">Identical to the [**InprocServers**](inprocservers.md) collection except that this collection also includes local servers.</span></span>

<span data-ttu-id="9fa48-105">Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="9fa48-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="9fa48-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9fa48-106">Members</span></span>

<span data-ttu-id="9fa48-107">La colección **LegacyServers** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="9fa48-107">The **LegacyServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="9fa48-108">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="9fa48-108">Related Collections</span></span>

<span data-ttu-id="9fa48-109">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="9fa48-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="9fa48-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="9fa48-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="9fa48-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="9fa48-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="9fa48-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="9fa48-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="9fa48-113">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="9fa48-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="9fa48-114">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="9fa48-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="9fa48-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9fa48-115">Properties</span></span>

<span data-ttu-id="9fa48-116">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="9fa48-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="9fa48-117">ClassName</span><span class="sxs-lookup"><span data-stu-id="9fa48-117">ClassName</span></span>](#classname)
-   [<span data-ttu-id="9fa48-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="9fa48-118">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="9fa48-119">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="9fa48-119">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="9fa48-120">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="9fa48-120">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="9fa48-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="9fa48-121">ProgID</span></span>](#progid)

### <a name="classname"></a><span data-ttu-id="9fa48-122">ClassName</span><span class="sxs-lookup"><span data-stu-id="9fa48-122">ClassName</span></span>



| <span data-ttu-id="9fa48-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="9fa48-123">Entry</span></span> | <span data-ttu-id="9fa48-124">Value</span><span class="sxs-lookup"><span data-stu-id="9fa48-124">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="9fa48-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fa48-125">Description</span></span>    | <span data-ttu-id="9fa48-126">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="9fa48-126">The name of the class.</span></span> |
| <span data-ttu-id="9fa48-127">Access</span><span class="sxs-lookup"><span data-stu-id="9fa48-127">Access</span></span>         | <span data-ttu-id="9fa48-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9fa48-128">ReadOnly</span></span>               |
| <span data-ttu-id="9fa48-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fa48-129">Type</span></span>           | <span data-ttu-id="9fa48-130">String</span><span class="sxs-lookup"><span data-stu-id="9fa48-130">String</span></span>                 |
| <span data-ttu-id="9fa48-131">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="9fa48-131">Default</span></span>        | <span data-ttu-id="9fa48-132">N/D</span><span class="sxs-lookup"><span data-stu-id="9fa48-132">N/A</span></span>                    |
| <span data-ttu-id="9fa48-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="9fa48-133">Minimum system</span></span> | <span data-ttu-id="9fa48-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9fa48-134">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="9fa48-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="9fa48-135">CLSID</span></span>



| <span data-ttu-id="9fa48-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="9fa48-136">Entry</span></span> | <span data-ttu-id="9fa48-137">Value</span><span class="sxs-lookup"><span data-stu-id="9fa48-137">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa48-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fa48-138">Description</span></span>    | <span data-ttu-id="9fa48-139">GUID del componente.</span><span class="sxs-lookup"><span data-stu-id="9fa48-139">A GUID for the component.</span></span> <span data-ttu-id="9fa48-140">Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="9fa48-140">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="9fa48-141">Access</span><span class="sxs-lookup"><span data-stu-id="9fa48-141">Access</span></span>         | <span data-ttu-id="9fa48-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9fa48-142">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="9fa48-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fa48-143">Type</span></span>           | <span data-ttu-id="9fa48-144">String</span><span class="sxs-lookup"><span data-stu-id="9fa48-144">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="9fa48-145">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="9fa48-145">Default</span></span>        | <span data-ttu-id="9fa48-146">N/D</span><span class="sxs-lookup"><span data-stu-id="9fa48-146">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="9fa48-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="9fa48-147">Minimum system</span></span> | <span data-ttu-id="9fa48-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9fa48-148">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="9fa48-149">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="9fa48-149">InprocServer32</span></span>



| <span data-ttu-id="9fa48-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="9fa48-150">Entry</span></span> | <span data-ttu-id="9fa48-151">Value</span><span class="sxs-lookup"><span data-stu-id="9fa48-151">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="9fa48-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fa48-152">Description</span></span>    | <span data-ttu-id="9fa48-153">Ruta de acceso de archivo para el componente.</span><span class="sxs-lookup"><span data-stu-id="9fa48-153">The file path for the component.</span></span> |
| <span data-ttu-id="9fa48-154">Access</span><span class="sxs-lookup"><span data-stu-id="9fa48-154">Access</span></span>         | <span data-ttu-id="9fa48-155">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9fa48-155">ReadOnly</span></span>                         |
| <span data-ttu-id="9fa48-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fa48-156">Type</span></span>           | <span data-ttu-id="9fa48-157">String</span><span class="sxs-lookup"><span data-stu-id="9fa48-157">String</span></span>                           |
| <span data-ttu-id="9fa48-158">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="9fa48-158">Default</span></span>        | <span data-ttu-id="9fa48-159">N/D</span><span class="sxs-lookup"><span data-stu-id="9fa48-159">N/A</span></span>                              |
| <span data-ttu-id="9fa48-160">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="9fa48-160">Minimum system</span></span> | <span data-ttu-id="9fa48-161">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9fa48-161">Windows XP</span></span>                       |



 

### <a name="localserver32"></a><span data-ttu-id="9fa48-162">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="9fa48-162">LocalServer32</span></span>



| <span data-ttu-id="9fa48-163">Entrada</span><span class="sxs-lookup"><span data-stu-id="9fa48-163">Entry</span></span> | <span data-ttu-id="9fa48-164">Value</span><span class="sxs-lookup"><span data-stu-id="9fa48-164">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="9fa48-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fa48-165">Description</span></span>    | <span data-ttu-id="9fa48-166">Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9fa48-166">Specifies the full path to a 32-bit local server application.</span></span> |
| <span data-ttu-id="9fa48-167">Access</span><span class="sxs-lookup"><span data-stu-id="9fa48-167">Access</span></span>         | <span data-ttu-id="9fa48-168">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9fa48-168">ReadOnly</span></span>                                                      |
| <span data-ttu-id="9fa48-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fa48-169">Type</span></span>           | <span data-ttu-id="9fa48-170">String</span><span class="sxs-lookup"><span data-stu-id="9fa48-170">String</span></span>                                                        |
| <span data-ttu-id="9fa48-171">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="9fa48-171">Default</span></span>        | <span data-ttu-id="9fa48-172">N/D</span><span class="sxs-lookup"><span data-stu-id="9fa48-172">N/A</span></span>                                                           |
| <span data-ttu-id="9fa48-173">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="9fa48-173">Minimum system</span></span> | <span data-ttu-id="9fa48-174">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9fa48-174">Windows XP</span></span>                                                    |



 

### <a name="progid"></a><span data-ttu-id="9fa48-175">ProgID</span><span class="sxs-lookup"><span data-stu-id="9fa48-175">ProgID</span></span>



| <span data-ttu-id="9fa48-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="9fa48-176">Entry</span></span> | <span data-ttu-id="9fa48-177">Value</span><span class="sxs-lookup"><span data-stu-id="9fa48-177">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa48-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fa48-178">Description</span></span>    | <span data-ttu-id="9fa48-179">Nombre que identifica el componente.</span><span class="sxs-lookup"><span data-stu-id="9fa48-179">A name identifying the component.</span></span> <span data-ttu-id="9fa48-180">Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="9fa48-180">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="9fa48-181">Access</span><span class="sxs-lookup"><span data-stu-id="9fa48-181">Access</span></span>         | <span data-ttu-id="9fa48-182">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9fa48-182">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="9fa48-183">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fa48-183">Type</span></span>           | <span data-ttu-id="9fa48-184">String</span><span class="sxs-lookup"><span data-stu-id="9fa48-184">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="9fa48-185">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="9fa48-185">Default</span></span>        | <span data-ttu-id="9fa48-186">N/D</span><span class="sxs-lookup"><span data-stu-id="9fa48-186">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="9fa48-187">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="9fa48-187">Minimum system</span></span> | <span data-ttu-id="9fa48-188">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9fa48-188">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="9fa48-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fa48-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa48-190">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="9fa48-190">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
