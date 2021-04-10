---
description: Recupera información relacionada con las clases de eventos.
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: Colección EventClassesForIID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153025"
---
# <a name="eventclassesforiid-collection"></a><span data-ttu-id="46a8d-103">Colección EventClassesForIID</span><span class="sxs-lookup"><span data-stu-id="46a8d-103">EventClassesForIID collection</span></span>

<span data-ttu-id="46a8d-104">Recupera información relacionada con las clases de eventos.</span><span class="sxs-lookup"><span data-stu-id="46a8d-104">Retrieves information regarding event classes.</span></span>

<span data-ttu-id="46a8d-105">La conexión entre el publicador y el suscriptor se administra mediante un objeto [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) , que es un componente com+ que contiene las interfaces y los métodos utilizados por un publicador para activar los eventos.</span><span class="sxs-lookup"><span data-stu-id="46a8d-105">The connection between publisher and subscriber(s) is managed by an [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) object, which is a COM+ component that contains the interfaces and methods used by a publisher to fire events.</span></span>

<span data-ttu-id="46a8d-106">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="46a8d-106">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="46a8d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="46a8d-107">Members</span></span>

<span data-ttu-id="46a8d-108">La colección **EventClassesForIID** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="46a8d-108">The **EventClassesForIID** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="46a8d-109">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="46a8d-109">Related Collections</span></span>

<span data-ttu-id="46a8d-110">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="46a8d-110">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="46a8d-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="46a8d-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="46a8d-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="46a8d-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="46a8d-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="46a8d-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="46a8d-114">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="46a8d-114">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="46a8d-115">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="46a8d-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="46a8d-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46a8d-116">Properties</span></span>

<span data-ttu-id="46a8d-117">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="46a8d-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="46a8d-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="46a8d-118">Application</span></span>](#application)
-   [<span data-ttu-id="46a8d-119">Bits</span><span class="sxs-lookup"><span data-stu-id="46a8d-119">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="46a8d-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="46a8d-120">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="46a8d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="46a8d-121">Description</span></span>](#description)
-   [<span data-ttu-id="46a8d-122">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="46a8d-122">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="46a8d-123">ProgID</span><span class="sxs-lookup"><span data-stu-id="46a8d-123">ProgID</span></span>](#progid)

### <a name="application"></a><span data-ttu-id="46a8d-124">Application</span><span class="sxs-lookup"><span data-stu-id="46a8d-124">Application</span></span>



| <span data-ttu-id="46a8d-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="46a8d-125">Entry</span></span> | <span data-ttu-id="46a8d-126">Value</span><span class="sxs-lookup"><span data-stu-id="46a8d-126">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="46a8d-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="46a8d-127">Description</span></span>    | <span data-ttu-id="46a8d-128">GUID de la aplicación que contiene la clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="46a8d-128">The GUID for the application containing the event class.</span></span> |
| <span data-ttu-id="46a8d-129">Access</span><span class="sxs-lookup"><span data-stu-id="46a8d-129">Access</span></span>         | <span data-ttu-id="46a8d-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="46a8d-130">ReadOnly</span></span>                                                 |
| <span data-ttu-id="46a8d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="46a8d-131">Type</span></span>           | <span data-ttu-id="46a8d-132">String</span><span class="sxs-lookup"><span data-stu-id="46a8d-132">String</span></span>                                                   |
| <span data-ttu-id="46a8d-133">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="46a8d-133">Default</span></span>        | <span data-ttu-id="46a8d-134">N/D</span><span class="sxs-lookup"><span data-stu-id="46a8d-134">N/A</span></span>                                                      |
| <span data-ttu-id="46a8d-135">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="46a8d-135">Minimum system</span></span> | <span data-ttu-id="46a8d-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="46a8d-136">Windows XP</span></span>                                               |



 

### <a name="bitness"></a><span data-ttu-id="46a8d-137">Valor de bits</span><span class="sxs-lookup"><span data-stu-id="46a8d-137">Bitness</span></span>



| <span data-ttu-id="46a8d-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="46a8d-138">Entry</span></span> | <span data-ttu-id="46a8d-139">Value</span><span class="sxs-lookup"><span data-stu-id="46a8d-139">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a8d-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="46a8d-140">Description</span></span>    | <span data-ttu-id="46a8d-141">Representa el tipo de bits binario de la clase de evento.</span><span class="sxs-lookup"><span data-stu-id="46a8d-141">Represents the binary bitness type of the event class.</span></span> <span data-ttu-id="46a8d-142">En los sistemas que usan Windows de 64 bits, esta propiedad distingue entre los componentes de 64 bits y los componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="46a8d-142">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="46a8d-143">Access</span><span class="sxs-lookup"><span data-stu-id="46a8d-143">Access</span></span>         | <span data-ttu-id="46a8d-144">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="46a8d-144">ReadOnly</span></span>                                                                                                                                                                |
| <span data-ttu-id="46a8d-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="46a8d-145">Type</span></span>           | <span data-ttu-id="46a8d-146">Valores posibles largos: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)</span><span class="sxs-lookup"><span data-stu-id="46a8d-146">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                           |
| <span data-ttu-id="46a8d-147">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="46a8d-147">Default</span></span>        | <span data-ttu-id="46a8d-148">N/D</span><span class="sxs-lookup"><span data-stu-id="46a8d-148">N/A</span></span>                                                                                                                                                                     |
| <span data-ttu-id="46a8d-149">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="46a8d-149">Minimum system</span></span> | <span data-ttu-id="46a8d-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="46a8d-150">Windows XP</span></span>                                                                                                                                                              |



 

### <a name="clsid"></a><span data-ttu-id="46a8d-151">CLSID</span><span class="sxs-lookup"><span data-stu-id="46a8d-151">CLSID</span></span>



| <span data-ttu-id="46a8d-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="46a8d-152">Entry</span></span> | <span data-ttu-id="46a8d-153">Value</span><span class="sxs-lookup"><span data-stu-id="46a8d-153">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a8d-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="46a8d-154">Description</span></span>    | <span data-ttu-id="46a8d-155">GUID para la clase de evento.</span><span class="sxs-lookup"><span data-stu-id="46a8d-155">The GUID for the event class.</span></span> <span data-ttu-id="46a8d-156">Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="46a8d-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="46a8d-157">Access</span><span class="sxs-lookup"><span data-stu-id="46a8d-157">Access</span></span>         | <span data-ttu-id="46a8d-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="46a8d-158">ReadOnly</span></span>                                                                                                                                                      |
| <span data-ttu-id="46a8d-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="46a8d-159">Type</span></span>           | <span data-ttu-id="46a8d-160">String</span><span class="sxs-lookup"><span data-stu-id="46a8d-160">String</span></span>                                                                                                                                                        |
| <span data-ttu-id="46a8d-161">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="46a8d-161">Default</span></span>        | <span data-ttu-id="46a8d-162">N/D</span><span class="sxs-lookup"><span data-stu-id="46a8d-162">N/A</span></span>                                                                                                                                                           |
| <span data-ttu-id="46a8d-163">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="46a8d-163">Minimum system</span></span> | <span data-ttu-id="46a8d-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="46a8d-164">Windows XP</span></span>                                                                                                                                                    |



 

### <a name="description"></a><span data-ttu-id="46a8d-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="46a8d-165">Description</span></span>



| <span data-ttu-id="46a8d-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="46a8d-166">Entry</span></span> | <span data-ttu-id="46a8d-167">Value</span><span class="sxs-lookup"><span data-stu-id="46a8d-167">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="46a8d-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="46a8d-168">Description</span></span>    | <span data-ttu-id="46a8d-169">Describe la clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="46a8d-169">Describes the event class.</span></span> |
| <span data-ttu-id="46a8d-170">Access</span><span class="sxs-lookup"><span data-stu-id="46a8d-170">Access</span></span>         | <span data-ttu-id="46a8d-171">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="46a8d-171">ReadOnly</span></span>                   |
| <span data-ttu-id="46a8d-172">Tipo</span><span class="sxs-lookup"><span data-stu-id="46a8d-172">Type</span></span>           | <span data-ttu-id="46a8d-173">String</span><span class="sxs-lookup"><span data-stu-id="46a8d-173">String</span></span>                     |
| <span data-ttu-id="46a8d-174">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="46a8d-174">Default</span></span>        | <span data-ttu-id="46a8d-175">""</span><span class="sxs-lookup"><span data-stu-id="46a8d-175">""</span></span>                         |
| <span data-ttu-id="46a8d-176">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="46a8d-176">Minimum system</span></span> | <span data-ttu-id="46a8d-177">Windows XP</span><span class="sxs-lookup"><span data-stu-id="46a8d-177">Windows XP</span></span>                 |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="46a8d-178">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="46a8d-178">IsPrivateComponent</span></span>



| <span data-ttu-id="46a8d-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="46a8d-179">Entry</span></span> | <span data-ttu-id="46a8d-180">Value</span><span class="sxs-lookup"><span data-stu-id="46a8d-180">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="46a8d-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="46a8d-181">Description</span></span>    | <span data-ttu-id="46a8d-182">Indica si el componente de clase de eventos es privado.</span><span class="sxs-lookup"><span data-stu-id="46a8d-182">Indicates whether the event class component is private.</span></span> |
| <span data-ttu-id="46a8d-183">Access</span><span class="sxs-lookup"><span data-stu-id="46a8d-183">Access</span></span>         | <span data-ttu-id="46a8d-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="46a8d-184">ReadOnly</span></span>                                                |
| <span data-ttu-id="46a8d-185">Tipo</span><span class="sxs-lookup"><span data-stu-id="46a8d-185">Type</span></span>           | <span data-ttu-id="46a8d-186">Bool</span><span class="sxs-lookup"><span data-stu-id="46a8d-186">Bool</span></span>                                                    |
| <span data-ttu-id="46a8d-187">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="46a8d-187">Default</span></span>        | <span data-ttu-id="46a8d-188">False</span><span class="sxs-lookup"><span data-stu-id="46a8d-188">False</span></span>                                                   |
| <span data-ttu-id="46a8d-189">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="46a8d-189">Minimum system</span></span> | <span data-ttu-id="46a8d-190">Windows XP</span><span class="sxs-lookup"><span data-stu-id="46a8d-190">Windows XP</span></span>                                              |



 

### <a name="progid"></a><span data-ttu-id="46a8d-191">ProgID</span><span class="sxs-lookup"><span data-stu-id="46a8d-191">ProgID</span></span>



| <span data-ttu-id="46a8d-192">Entrada</span><span class="sxs-lookup"><span data-stu-id="46a8d-192">Entry</span></span> | <span data-ttu-id="46a8d-193">Value</span><span class="sxs-lookup"><span data-stu-id="46a8d-193">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a8d-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="46a8d-194">Description</span></span>    | <span data-ttu-id="46a8d-195">Nombre descriptivo que se usa para identificar la clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="46a8d-195">A friendly name used to identify the event class.</span></span> <span data-ttu-id="46a8d-196">Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="46a8d-196">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="46a8d-197">Access</span><span class="sxs-lookup"><span data-stu-id="46a8d-197">Access</span></span>         | <span data-ttu-id="46a8d-198">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="46a8d-198">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="46a8d-199">Tipo</span><span class="sxs-lookup"><span data-stu-id="46a8d-199">Type</span></span>           | <span data-ttu-id="46a8d-200">String</span><span class="sxs-lookup"><span data-stu-id="46a8d-200">String</span></span>                                                                                                                                                                              |
| <span data-ttu-id="46a8d-201">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="46a8d-201">Default</span></span>        | <span data-ttu-id="46a8d-202">""</span><span class="sxs-lookup"><span data-stu-id="46a8d-202">""</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="46a8d-203">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="46a8d-203">Minimum system</span></span> | <span data-ttu-id="46a8d-204">Windows XP</span><span class="sxs-lookup"><span data-stu-id="46a8d-204">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="46a8d-205">Vea también</span><span class="sxs-lookup"><span data-stu-id="46a8d-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a8d-206">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="46a8d-206">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
