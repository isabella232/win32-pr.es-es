---
description: Recupera información de las aplicaciones que se importan.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Colección FilesForImport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153259"
---
# <a name="filesforimport-collection"></a><span data-ttu-id="a1695-103">Colección FilesForImport</span><span class="sxs-lookup"><span data-stu-id="a1695-103">FilesForImport collection</span></span>

<span data-ttu-id="a1695-104">Recupera información de las aplicaciones que se importan.</span><span class="sxs-lookup"><span data-stu-id="a1695-104">Retrieves information for applications that are imported.</span></span>

<span data-ttu-id="a1695-105">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="a1695-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="a1695-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1695-106">Members</span></span>

<span data-ttu-id="a1695-107">La colección **FilesForImport** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="a1695-107">The **FilesForImport** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="a1695-108">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="a1695-108">Related Collections</span></span>

<span data-ttu-id="a1695-109">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="a1695-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="a1695-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a1695-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="a1695-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a1695-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="a1695-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="a1695-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="a1695-113">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a1695-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="a1695-114">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="a1695-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="a1695-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1695-115">Properties</span></span>

<span data-ttu-id="a1695-116">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="a1695-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="a1695-117">ApplicationFileName</span><span class="sxs-lookup"><span data-stu-id="a1695-117">ApplicationFileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="a1695-118">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a1695-118">ApplicationName</span></span>](#applicationname)
-   [<span data-ttu-id="a1695-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-119">Description</span></span>](#partitiondescription)
-   [<span data-ttu-id="a1695-120">FileName</span><span class="sxs-lookup"><span data-stu-id="a1695-120">FileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="a1695-121">HasUsers</span><span class="sxs-lookup"><span data-stu-id="a1695-121">HasUsers</span></span>](#hasusers)
-   [<span data-ttu-id="a1695-122">IsProxy</span><span class="sxs-lookup"><span data-stu-id="a1695-122">IsProxy</span></span>](#isproxy)
-   [<span data-ttu-id="a1695-123">IsService</span><span class="sxs-lookup"><span data-stu-id="a1695-123">IsService</span></span>](#isservice)
-   [<span data-ttu-id="a1695-124">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="a1695-124">PartitionDescription</span></span>](#partitiondescription)
-   [<span data-ttu-id="a1695-125">PartitionID</span><span class="sxs-lookup"><span data-stu-id="a1695-125">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="a1695-126">PartitionName</span><span class="sxs-lookup"><span data-stu-id="a1695-126">PartitionName</span></span>](#partitionname)

### <a name="applicationfilename"></a><span data-ttu-id="a1695-127">ApplicationFileName</span><span class="sxs-lookup"><span data-stu-id="a1695-127">ApplicationFileName</span></span>



| <span data-ttu-id="a1695-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1695-128">Entry</span></span> | <span data-ttu-id="a1695-129">Value</span><span class="sxs-lookup"><span data-stu-id="a1695-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a1695-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-130">Description</span></span>    | <span data-ttu-id="a1695-131">Nombre del archivo MSI que contiene la aplicación que se puede importar.</span><span class="sxs-lookup"><span data-stu-id="a1695-131">The name of the MSI file that contains the application that can be imported.</span></span> |
| <span data-ttu-id="a1695-132">Access</span><span class="sxs-lookup"><span data-stu-id="a1695-132">Access</span></span>         | <span data-ttu-id="a1695-133">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1695-133">ReadOnly</span></span>                                                                     |
| <span data-ttu-id="a1695-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1695-134">Type</span></span>           | <span data-ttu-id="a1695-135">String</span><span class="sxs-lookup"><span data-stu-id="a1695-135">String</span></span>                                                                       |
| <span data-ttu-id="a1695-136">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a1695-136">Default</span></span>        | <span data-ttu-id="a1695-137">N/D</span><span class="sxs-lookup"><span data-stu-id="a1695-137">N/A</span></span>                                                                          |
| <span data-ttu-id="a1695-138">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a1695-138">Minimum system</span></span> | <span data-ttu-id="a1695-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1695-139">Windows XP</span></span>                                                                   |



 

### <a name="applicationname"></a><span data-ttu-id="a1695-140">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a1695-140">ApplicationName</span></span>



| <span data-ttu-id="a1695-141">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1695-141">Entry</span></span> | <span data-ttu-id="a1695-142">Value</span><span class="sxs-lookup"><span data-stu-id="a1695-142">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="a1695-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-143">Description</span></span>    | <span data-ttu-id="a1695-144">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1695-144">The name of the application.</span></span> |
| <span data-ttu-id="a1695-145">Access</span><span class="sxs-lookup"><span data-stu-id="a1695-145">Access</span></span>         | <span data-ttu-id="a1695-146">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1695-146">ReadOnly</span></span>                     |
| <span data-ttu-id="a1695-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1695-147">Type</span></span>           | <span data-ttu-id="a1695-148">String</span><span class="sxs-lookup"><span data-stu-id="a1695-148">String</span></span>                       |
| <span data-ttu-id="a1695-149">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a1695-149">Default</span></span>        | <span data-ttu-id="a1695-150">""</span><span class="sxs-lookup"><span data-stu-id="a1695-150">""</span></span>                           |
| <span data-ttu-id="a1695-151">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a1695-151">Minimum system</span></span> | <span data-ttu-id="a1695-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1695-152">Windows XP</span></span>                   |



 

### <a name="description"></a><span data-ttu-id="a1695-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-153">Description</span></span>



| <span data-ttu-id="a1695-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1695-154">Entry</span></span> | <span data-ttu-id="a1695-155">Value</span><span class="sxs-lookup"><span data-stu-id="a1695-155">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="a1695-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-156">Description</span></span>    | <span data-ttu-id="a1695-157">Una descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1695-157">A description of the application.</span></span> |
| <span data-ttu-id="a1695-158">Access</span><span class="sxs-lookup"><span data-stu-id="a1695-158">Access</span></span>         | <span data-ttu-id="a1695-159">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1695-159">ReadOnly</span></span>                          |
| <span data-ttu-id="a1695-160">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1695-160">Type</span></span>           | <span data-ttu-id="a1695-161">String</span><span class="sxs-lookup"><span data-stu-id="a1695-161">String</span></span>                            |
| <span data-ttu-id="a1695-162">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a1695-162">Default</span></span>        | <span data-ttu-id="a1695-163">""</span><span class="sxs-lookup"><span data-stu-id="a1695-163">""</span></span>                                |
| <span data-ttu-id="a1695-164">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a1695-164">Minimum system</span></span> | <span data-ttu-id="a1695-165">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1695-165">Windows XP</span></span>                        |



 

### <a name="filename"></a><span data-ttu-id="a1695-166">FileName</span><span class="sxs-lookup"><span data-stu-id="a1695-166">FileName</span></span>



| <span data-ttu-id="a1695-167">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1695-167">Entry</span></span> | <span data-ttu-id="a1695-168">Value</span><span class="sxs-lookup"><span data-stu-id="a1695-168">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1695-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-169">Description</span></span>    | <span data-ttu-id="a1695-170">Nombre del archivo DLL o EXE que contiene la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1695-170">The name of the DLL or EXE file that contains the application.</span></span> <span data-ttu-id="a1695-171">Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="a1695-171">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a1695-172">Access</span><span class="sxs-lookup"><span data-stu-id="a1695-172">Access</span></span>         | <span data-ttu-id="a1695-173">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1695-173">ReadOnly</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="a1695-174">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1695-174">Type</span></span>           | <span data-ttu-id="a1695-175">String</span><span class="sxs-lookup"><span data-stu-id="a1695-175">String</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="a1695-176">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a1695-176">Default</span></span>        | <span data-ttu-id="a1695-177">""</span><span class="sxs-lookup"><span data-stu-id="a1695-177">""</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="a1695-178">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a1695-178">Minimum system</span></span> | <span data-ttu-id="a1695-179">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1695-179">Windows XP</span></span>                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a><span data-ttu-id="a1695-180">HasUsers</span><span class="sxs-lookup"><span data-stu-id="a1695-180">HasUsers</span></span>



| <span data-ttu-id="a1695-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1695-181">Entry</span></span> | <span data-ttu-id="a1695-182">Value</span><span class="sxs-lookup"><span data-stu-id="a1695-182">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="a1695-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-183">Description</span></span>    | <span data-ttu-id="a1695-184">Indica si la aplicación tiene algún usuario.</span><span class="sxs-lookup"><span data-stu-id="a1695-184">Indicates whether the application has any users.</span></span> |
| <span data-ttu-id="a1695-185">Access</span><span class="sxs-lookup"><span data-stu-id="a1695-185">Access</span></span>         | <span data-ttu-id="a1695-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1695-186">ReadOnly</span></span>                                         |
| <span data-ttu-id="a1695-187">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1695-187">Type</span></span>           | <span data-ttu-id="a1695-188">Bool</span><span class="sxs-lookup"><span data-stu-id="a1695-188">Bool</span></span>                                             |
| <span data-ttu-id="a1695-189">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="a1695-189">Default</span></span>        | <span data-ttu-id="a1695-190">False</span><span class="sxs-lookup"><span data-stu-id="a1695-190">False</span></span>                                            |
| <span data-ttu-id="a1695-191">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a1695-191">Minimum system</span></span> | <span data-ttu-id="a1695-192">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1695-192">Windows XP</span></span>                                       |



 

### <a name="isproxy"></a><span data-ttu-id="a1695-193">IsProxy</span><span class="sxs-lookup"><span data-stu-id="a1695-193">IsProxy</span></span>



| <span data-ttu-id="a1695-194">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1695-194">Entry</span></span> | <span data-ttu-id="a1695-195">Value</span><span class="sxs-lookup"><span data-stu-id="a1695-195">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="a1695-196">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-196">Description</span></span>    | <span data-ttu-id="a1695-197">Indica si la aplicación es un proxy.</span><span class="sxs-lookup"><span data-stu-id="a1695-197">Indicates whether the application is a proxy.</span></span> |
| <span data-ttu-id="a1695-198">Access</span><span class="sxs-lookup"><span data-stu-id="a1695-198">Access</span></span>         | <span data-ttu-id="a1695-199">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1695-199">ReadOnly</span></span>                                      |
| <span data-ttu-id="a1695-200">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1695-200">Type</span></span>           | <span data-ttu-id="a1695-201">Bool</span><span class="sxs-lookup"><span data-stu-id="a1695-201">Bool</span></span>                                          |
| <span data-ttu-id="a1695-202">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="a1695-202">Default</span></span>        | <span data-ttu-id="a1695-203">False</span><span class="sxs-lookup"><span data-stu-id="a1695-203">False</span></span>                                         |
| <span data-ttu-id="a1695-204">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a1695-204">Minimum system</span></span> | <span data-ttu-id="a1695-205">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1695-205">Windows XP</span></span>                                    |



 

### <a name="isservice"></a><span data-ttu-id="a1695-206">IsService</span><span class="sxs-lookup"><span data-stu-id="a1695-206">IsService</span></span>



| <span data-ttu-id="a1695-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1695-207">Entry</span></span> | <span data-ttu-id="a1695-208">Value</span><span class="sxs-lookup"><span data-stu-id="a1695-208">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="a1695-209">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-209">Description</span></span>    | <span data-ttu-id="a1695-210">Indica si la aplicación es un servicio.</span><span class="sxs-lookup"><span data-stu-id="a1695-210">Indicates whether the application is a service.</span></span> |
| <span data-ttu-id="a1695-211">Access</span><span class="sxs-lookup"><span data-stu-id="a1695-211">Access</span></span>         | <span data-ttu-id="a1695-212">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1695-212">ReadOnly</span></span>                                        |
| <span data-ttu-id="a1695-213">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1695-213">Type</span></span>           | <span data-ttu-id="a1695-214">Bool</span><span class="sxs-lookup"><span data-stu-id="a1695-214">Bool</span></span>                                            |
| <span data-ttu-id="a1695-215">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="a1695-215">Default</span></span>        | <span data-ttu-id="a1695-216">False</span><span class="sxs-lookup"><span data-stu-id="a1695-216">False</span></span>                                           |
| <span data-ttu-id="a1695-217">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a1695-217">Minimum system</span></span> | <span data-ttu-id="a1695-218">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1695-218">Windows XP</span></span>                                      |



 

### <a name="partitiondescription"></a><span data-ttu-id="a1695-219">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="a1695-219">PartitionDescription</span></span>



| <span data-ttu-id="a1695-220">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1695-220">Entry</span></span> | <span data-ttu-id="a1695-221">Value</span><span class="sxs-lookup"><span data-stu-id="a1695-221">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="a1695-222">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-222">Description</span></span>    | <span data-ttu-id="a1695-223">Una descripción de la partición de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1695-223">A description of the application's partition.</span></span> |
| <span data-ttu-id="a1695-224">Access</span><span class="sxs-lookup"><span data-stu-id="a1695-224">Access</span></span>         | <span data-ttu-id="a1695-225">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1695-225">ReadOnly</span></span>                                      |
| <span data-ttu-id="a1695-226">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1695-226">Type</span></span>           | <span data-ttu-id="a1695-227">String</span><span class="sxs-lookup"><span data-stu-id="a1695-227">String</span></span>                                        |
| <span data-ttu-id="a1695-228">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a1695-228">Default</span></span>        | <span data-ttu-id="a1695-229">""</span><span class="sxs-lookup"><span data-stu-id="a1695-229">""</span></span>                                            |
| <span data-ttu-id="a1695-230">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a1695-230">Minimum system</span></span> | <span data-ttu-id="a1695-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1695-231">Windows Server 2003</span></span>                           |



 

### <a name="partitionid"></a><span data-ttu-id="a1695-232">PartitionID</span><span class="sxs-lookup"><span data-stu-id="a1695-232">PartitionID</span></span>



| <span data-ttu-id="a1695-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1695-233">Entry</span></span> | <span data-ttu-id="a1695-234">Value</span><span class="sxs-lookup"><span data-stu-id="a1695-234">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="a1695-235">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-235">Description</span></span>    | <span data-ttu-id="a1695-236">GUID de la partición de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1695-236">The GUID of the application's partition.</span></span> |
| <span data-ttu-id="a1695-237">Access</span><span class="sxs-lookup"><span data-stu-id="a1695-237">Access</span></span>         | <span data-ttu-id="a1695-238">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1695-238">ReadOnly</span></span>                                 |
| <span data-ttu-id="a1695-239">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1695-239">Type</span></span>           | <span data-ttu-id="a1695-240">String</span><span class="sxs-lookup"><span data-stu-id="a1695-240">String</span></span>                                   |
| <span data-ttu-id="a1695-241">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a1695-241">Default</span></span>        | <span data-ttu-id="a1695-242">""</span><span class="sxs-lookup"><span data-stu-id="a1695-242">""</span></span>                                       |
| <span data-ttu-id="a1695-243">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a1695-243">Minimum system</span></span> | <span data-ttu-id="a1695-244">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1695-244">Windows Server 2003</span></span>                      |



 

### <a name="partitionname"></a><span data-ttu-id="a1695-245">PartitionName</span><span class="sxs-lookup"><span data-stu-id="a1695-245">PartitionName</span></span>



| <span data-ttu-id="a1695-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1695-246">Entry</span></span> | <span data-ttu-id="a1695-247">Value</span><span class="sxs-lookup"><span data-stu-id="a1695-247">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="a1695-248">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1695-248">Description</span></span>    | <span data-ttu-id="a1695-249">Nombre de la partición de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1695-249">The name of the application's partition.</span></span> |
| <span data-ttu-id="a1695-250">Access</span><span class="sxs-lookup"><span data-stu-id="a1695-250">Access</span></span>         | <span data-ttu-id="a1695-251">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1695-251">ReadOnly</span></span>                                 |
| <span data-ttu-id="a1695-252">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1695-252">Type</span></span>           | <span data-ttu-id="a1695-253">String</span><span class="sxs-lookup"><span data-stu-id="a1695-253">String</span></span>                                   |
| <span data-ttu-id="a1695-254">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a1695-254">Default</span></span>        | <span data-ttu-id="a1695-255">""</span><span class="sxs-lookup"><span data-stu-id="a1695-255">""</span></span>                                       |
| <span data-ttu-id="a1695-256">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a1695-256">Minimum system</span></span> | <span data-ttu-id="a1695-257">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1695-257">Windows Server 2003</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="a1695-258">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1695-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1695-259">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="a1695-259">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
