---
title: Template-Roots atributo)
description: Este atributo se usa en el contenedor de configuración de Exchange para indicar dónde se almacenan los contenedores de la plantilla. Esta información la utiliza el proveedor de Active Directory MAPI.
ms.assetid: 1416ce4a-ca07-4ca9-8ea1-e1a6ad19e7ad
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Template-Roots
- templateRoots esquema de AD de atributos
topic_type:
- apiref
api_name:
- Template-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761c6d3d79bbf45e9a4d391b612956d6893cd314
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804825"
---
# <a name="template-roots-attribute"></a><span data-ttu-id="66a66-106">Template-Roots atributo)</span><span class="sxs-lookup"><span data-stu-id="66a66-106">Template-Roots attribute</span></span>

<span data-ttu-id="66a66-107">Este atributo se usa en el contenedor de configuración de Exchange para indicar dónde se almacenan los contenedores de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="66a66-107">This attribute is used on the Exchange config container to indicate where the template containers are stored.</span></span> <span data-ttu-id="66a66-108">Esta información la utiliza el proveedor de Active Directory MAPI.</span><span class="sxs-lookup"><span data-stu-id="66a66-108">This information is used by the Active Directory MAPI provider.</span></span>



| <span data-ttu-id="66a66-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="66a66-109">Entry</span></span> | <span data-ttu-id="66a66-110">Value</span><span class="sxs-lookup"><span data-stu-id="66a66-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="66a66-111">CN</span><span class="sxs-lookup"><span data-stu-id="66a66-111">CN</span></span>                | <span data-ttu-id="66a66-112">Template-Roots</span><span class="sxs-lookup"><span data-stu-id="66a66-112">Template-Roots</span></span>                          |
| <span data-ttu-id="66a66-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="66a66-113">Ldap-Display-Name</span></span> | <span data-ttu-id="66a66-114">templateRoots</span><span class="sxs-lookup"><span data-stu-id="66a66-114">templateRoots</span></span>                           |
| <span data-ttu-id="66a66-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="66a66-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="66a66-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="66a66-116">Update Privilege</span></span>  | <span data-ttu-id="66a66-117">Lo utiliza el sistema.</span><span class="sxs-lookup"><span data-stu-id="66a66-117">This is used by the system.</span></span>             |
| <span data-ttu-id="66a66-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="66a66-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="66a66-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="66a66-119">Attribute-Id</span></span>      | <span data-ttu-id="66a66-120">1.2.840.113556.1.4.1346</span><span class="sxs-lookup"><span data-stu-id="66a66-120">1.2.840.113556.1.4.1346</span></span>                 |
| <span data-ttu-id="66a66-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="66a66-121">System-Id-Guid</span></span>    | <span data-ttu-id="66a66-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="66a66-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span></span>    |
| <span data-ttu-id="66a66-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66a66-123">Syntax</span></span>            | [<span data-ttu-id="66a66-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="66a66-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="66a66-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="66a66-125">Implementations</span></span>

-   [<span data-ttu-id="66a66-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="66a66-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="66a66-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="66a66-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="66a66-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="66a66-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="66a66-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="66a66-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="66a66-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="66a66-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="66a66-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="66a66-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="66a66-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="66a66-132">Windows 2000 Server</span></span>



| <span data-ttu-id="66a66-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="66a66-133">Entry</span></span> | <span data-ttu-id="66a66-134">Value</span><span class="sxs-lookup"><span data-stu-id="66a66-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66a66-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66a66-135">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66a66-136">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="66a66-137">System-Only</span></span>            | <span data-ttu-id="66a66-138">False</span><span class="sxs-lookup"><span data-stu-id="66a66-138">False</span></span>                                                                                |
| <span data-ttu-id="66a66-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66a66-139">Is-Single-Valued</span></span>       | <span data-ttu-id="66a66-140">False</span><span class="sxs-lookup"><span data-stu-id="66a66-140">False</span></span>                                                                                |
| <span data-ttu-id="66a66-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66a66-141">Is Indexed</span></span>             | <span data-ttu-id="66a66-142">False</span><span class="sxs-lookup"><span data-stu-id="66a66-142">False</span></span>                                                                                |
| <span data-ttu-id="66a66-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66a66-143">In Global Catalog</span></span>      | <span data-ttu-id="66a66-144">False</span><span class="sxs-lookup"><span data-stu-id="66a66-144">False</span></span>                                                                                |
| <span data-ttu-id="66a66-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66a66-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="66a66-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66a66-146">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="66a66-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66a66-147">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66a66-148">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-149">Search-Flags</span></span>           | <span data-ttu-id="66a66-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66a66-150">0x00000000</span></span>                                                                           |
| <span data-ttu-id="66a66-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-151">System-Flags</span></span>           | <span data-ttu-id="66a66-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66a66-152">0x00000010</span></span>                                                                           |
| <span data-ttu-id="66a66-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66a66-153">Classes used in</span></span>        | [<span data-ttu-id="66a66-154">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="66a66-154">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="66a66-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="66a66-155">Windows Server 2003</span></span>



| <span data-ttu-id="66a66-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="66a66-156">Entry</span></span> | <span data-ttu-id="66a66-157">Value</span><span class="sxs-lookup"><span data-stu-id="66a66-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66a66-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66a66-158">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66a66-159">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="66a66-160">System-Only</span></span>            | <span data-ttu-id="66a66-161">False</span><span class="sxs-lookup"><span data-stu-id="66a66-161">False</span></span>                                                                                |
| <span data-ttu-id="66a66-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66a66-162">Is-Single-Valued</span></span>       | <span data-ttu-id="66a66-163">False</span><span class="sxs-lookup"><span data-stu-id="66a66-163">False</span></span>                                                                                |
| <span data-ttu-id="66a66-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66a66-164">Is Indexed</span></span>             | <span data-ttu-id="66a66-165">False</span><span class="sxs-lookup"><span data-stu-id="66a66-165">False</span></span>                                                                                |
| <span data-ttu-id="66a66-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66a66-166">In Global Catalog</span></span>      | <span data-ttu-id="66a66-167">False</span><span class="sxs-lookup"><span data-stu-id="66a66-167">False</span></span>                                                                                |
| <span data-ttu-id="66a66-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66a66-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="66a66-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66a66-169">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="66a66-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66a66-170">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66a66-171">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-172">Search-Flags</span></span>           | <span data-ttu-id="66a66-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66a66-173">0x00000000</span></span>                                                                           |
| <span data-ttu-id="66a66-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-174">System-Flags</span></span>           | <span data-ttu-id="66a66-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66a66-175">0x00000010</span></span>                                                                           |
| <span data-ttu-id="66a66-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66a66-176">Classes used in</span></span>        | [<span data-ttu-id="66a66-177">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="66a66-177">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="66a66-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="66a66-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="66a66-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="66a66-179">Entry</span></span> | <span data-ttu-id="66a66-180">Value</span><span class="sxs-lookup"><span data-stu-id="66a66-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66a66-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66a66-181">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66a66-182">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="66a66-183">System-Only</span></span>            | <span data-ttu-id="66a66-184">False</span><span class="sxs-lookup"><span data-stu-id="66a66-184">False</span></span>                                                                                |
| <span data-ttu-id="66a66-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66a66-185">Is-Single-Valued</span></span>       | <span data-ttu-id="66a66-186">False</span><span class="sxs-lookup"><span data-stu-id="66a66-186">False</span></span>                                                                                |
| <span data-ttu-id="66a66-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66a66-187">Is Indexed</span></span>             | <span data-ttu-id="66a66-188">False</span><span class="sxs-lookup"><span data-stu-id="66a66-188">False</span></span>                                                                                |
| <span data-ttu-id="66a66-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66a66-189">In Global Catalog</span></span>      | <span data-ttu-id="66a66-190">False</span><span class="sxs-lookup"><span data-stu-id="66a66-190">False</span></span>                                                                                |
| <span data-ttu-id="66a66-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66a66-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="66a66-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66a66-192">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="66a66-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66a66-193">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66a66-194">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-195">Search-Flags</span></span>           | <span data-ttu-id="66a66-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66a66-196">0x00000000</span></span>                                                                           |
| <span data-ttu-id="66a66-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-197">System-Flags</span></span>           | <span data-ttu-id="66a66-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66a66-198">0x00000010</span></span>                                                                           |
| <span data-ttu-id="66a66-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66a66-199">Classes used in</span></span>        | [<span data-ttu-id="66a66-200">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="66a66-200">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="66a66-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66a66-201">Windows Server 2008</span></span>



| <span data-ttu-id="66a66-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="66a66-202">Entry</span></span> | <span data-ttu-id="66a66-203">Value</span><span class="sxs-lookup"><span data-stu-id="66a66-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66a66-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66a66-204">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66a66-205">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="66a66-206">System-Only</span></span>            | <span data-ttu-id="66a66-207">False</span><span class="sxs-lookup"><span data-stu-id="66a66-207">False</span></span>                                                                                |
| <span data-ttu-id="66a66-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66a66-208">Is-Single-Valued</span></span>       | <span data-ttu-id="66a66-209">False</span><span class="sxs-lookup"><span data-stu-id="66a66-209">False</span></span>                                                                                |
| <span data-ttu-id="66a66-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66a66-210">Is Indexed</span></span>             | <span data-ttu-id="66a66-211">False</span><span class="sxs-lookup"><span data-stu-id="66a66-211">False</span></span>                                                                                |
| <span data-ttu-id="66a66-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66a66-212">In Global Catalog</span></span>      | <span data-ttu-id="66a66-213">False</span><span class="sxs-lookup"><span data-stu-id="66a66-213">False</span></span>                                                                                |
| <span data-ttu-id="66a66-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66a66-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="66a66-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66a66-215">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="66a66-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66a66-216">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66a66-217">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-218">Search-Flags</span></span>           | <span data-ttu-id="66a66-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66a66-219">0x00000000</span></span>                                                                           |
| <span data-ttu-id="66a66-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-220">System-Flags</span></span>           | <span data-ttu-id="66a66-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66a66-221">0x00000010</span></span>                                                                           |
| <span data-ttu-id="66a66-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66a66-222">Classes used in</span></span>        | [<span data-ttu-id="66a66-223">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="66a66-223">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="66a66-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="66a66-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="66a66-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="66a66-225">Entry</span></span> | <span data-ttu-id="66a66-226">Value</span><span class="sxs-lookup"><span data-stu-id="66a66-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66a66-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66a66-227">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66a66-228">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="66a66-229">System-Only</span></span>            | <span data-ttu-id="66a66-230">False</span><span class="sxs-lookup"><span data-stu-id="66a66-230">False</span></span>                                                                                |
| <span data-ttu-id="66a66-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66a66-231">Is-Single-Valued</span></span>       | <span data-ttu-id="66a66-232">False</span><span class="sxs-lookup"><span data-stu-id="66a66-232">False</span></span>                                                                                |
| <span data-ttu-id="66a66-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66a66-233">Is Indexed</span></span>             | <span data-ttu-id="66a66-234">False</span><span class="sxs-lookup"><span data-stu-id="66a66-234">False</span></span>                                                                                |
| <span data-ttu-id="66a66-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66a66-235">In Global Catalog</span></span>      | <span data-ttu-id="66a66-236">False</span><span class="sxs-lookup"><span data-stu-id="66a66-236">False</span></span>                                                                                |
| <span data-ttu-id="66a66-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66a66-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="66a66-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66a66-238">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="66a66-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66a66-239">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66a66-240">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-241">Search-Flags</span></span>           | <span data-ttu-id="66a66-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66a66-242">0x00000000</span></span>                                                                           |
| <span data-ttu-id="66a66-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-243">System-Flags</span></span>           | <span data-ttu-id="66a66-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66a66-244">0x00000010</span></span>                                                                           |
| <span data-ttu-id="66a66-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66a66-245">Classes used in</span></span>        | [<span data-ttu-id="66a66-246">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="66a66-246">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="66a66-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="66a66-247">Windows Server 2012</span></span>



| <span data-ttu-id="66a66-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="66a66-248">Entry</span></span> | <span data-ttu-id="66a66-249">Value</span><span class="sxs-lookup"><span data-stu-id="66a66-249">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66a66-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66a66-250">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66a66-251">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="66a66-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="66a66-252">System-Only</span></span>            | <span data-ttu-id="66a66-253">False</span><span class="sxs-lookup"><span data-stu-id="66a66-253">False</span></span>                                                                                |
| <span data-ttu-id="66a66-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66a66-254">Is-Single-Valued</span></span>       | <span data-ttu-id="66a66-255">False</span><span class="sxs-lookup"><span data-stu-id="66a66-255">False</span></span>                                                                                |
| <span data-ttu-id="66a66-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66a66-256">Is Indexed</span></span>             | <span data-ttu-id="66a66-257">False</span><span class="sxs-lookup"><span data-stu-id="66a66-257">False</span></span>                                                                                |
| <span data-ttu-id="66a66-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66a66-258">In Global Catalog</span></span>      | <span data-ttu-id="66a66-259">False</span><span class="sxs-lookup"><span data-stu-id="66a66-259">False</span></span>                                                                                |
| <span data-ttu-id="66a66-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66a66-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="66a66-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66a66-261">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="66a66-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66a66-262">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66a66-263">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="66a66-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-264">Search-Flags</span></span>           | <span data-ttu-id="66a66-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66a66-265">0x00000000</span></span>                                                                           |
| <span data-ttu-id="66a66-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66a66-266">System-Flags</span></span>           | <span data-ttu-id="66a66-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66a66-267">0x00000010</span></span>                                                                           |
| <span data-ttu-id="66a66-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66a66-268">Classes used in</span></span>        | [<span data-ttu-id="66a66-269">**MS-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="66a66-269">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





