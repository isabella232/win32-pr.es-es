---
title: atributo MS-DS-auxiliar-classes
description: Este atributo muestra las clases auxiliares que se han adjuntado dinámicamente a un objeto. Este atributo no está asociado con una clase. El sistema lo rellena automáticamente.
ms.assetid: bf41f15d-9af9-43de-8425-33d50880c3fa
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de clases MS-DS-auxiliar
- 'msDS-auxiliar: atributo de clases esquema de AD'
topic_type:
- apiref
api_name:
- ms-DS-Auxiliary-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24608d0626ae4bcd6adb70a646d95121615c29e5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906049"
---
# <a name="ms-ds-auxiliary-classes-attribute"></a><span data-ttu-id="d1582-107">atributo MS-DS-auxiliar-classes</span><span class="sxs-lookup"><span data-stu-id="d1582-107">ms-DS-Auxiliary-Classes attribute</span></span>

<span data-ttu-id="d1582-108">Este atributo muestra las clases auxiliares que se han adjuntado dinámicamente a un objeto.</span><span class="sxs-lookup"><span data-stu-id="d1582-108">This attribute lists the auxiliary classes that have been dynamically attached to an object.</span></span> <span data-ttu-id="d1582-109">Este atributo no está asociado con una clase.</span><span class="sxs-lookup"><span data-stu-id="d1582-109">This attribute is not associated with a class.</span></span> <span data-ttu-id="d1582-110">El sistema lo rellena automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d1582-110">It is automatically populated by the system.</span></span>



| <span data-ttu-id="d1582-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1582-111">Entry</span></span> | <span data-ttu-id="d1582-112">Value</span><span class="sxs-lookup"><span data-stu-id="d1582-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d1582-113">CN</span><span class="sxs-lookup"><span data-stu-id="d1582-113">CN</span></span>                | <span data-ttu-id="d1582-114">Clases de MS-DS-auxiliar</span><span class="sxs-lookup"><span data-stu-id="d1582-114">ms-DS-Auxiliary-Classes</span></span>                                         |
| <span data-ttu-id="d1582-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d1582-115">Ldap-Display-Name</span></span> | <span data-ttu-id="d1582-116">msDS-auxiliar-clases</span><span class="sxs-lookup"><span data-stu-id="d1582-116">msDS-Auxiliary-Classes</span></span>                                          |
| <span data-ttu-id="d1582-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d1582-117">Size</span></span>              | \-                                                              |
| <span data-ttu-id="d1582-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d1582-118">Update Privilege</span></span>  | <span data-ttu-id="d1582-119">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="d1582-119">This value is set by the system.</span></span>                                |
| <span data-ttu-id="d1582-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d1582-120">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="d1582-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d1582-121">Attribute-Id</span></span>      | <span data-ttu-id="d1582-122">1.2.840.113556.1.4.1458</span><span class="sxs-lookup"><span data-stu-id="d1582-122">1.2.840.113556.1.4.1458</span></span>                                         |
| <span data-ttu-id="d1582-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d1582-123">System-Id-Guid</span></span>    | <span data-ttu-id="d1582-124">c4af1073-ee50-4be0-b8c0-89a41fe99abe</span><span class="sxs-lookup"><span data-stu-id="d1582-124">c4af1073-ee50-4be0-b8c0-89a41fe99abe</span></span>                            |
| <span data-ttu-id="d1582-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1582-125">Syntax</span></span>            | [<span data-ttu-id="d1582-126">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="d1582-126">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="d1582-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d1582-127">Implementations</span></span>

-   [<span data-ttu-id="d1582-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d1582-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d1582-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d1582-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d1582-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d1582-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d1582-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d1582-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d1582-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d1582-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d1582-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d1582-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d1582-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d1582-134">Windows Server 2003</span></span>



| <span data-ttu-id="d1582-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1582-135">Entry</span></span> | <span data-ttu-id="d1582-136">Value</span><span class="sxs-lookup"><span data-stu-id="d1582-136">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d1582-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1582-137">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1582-138">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1582-139">System-Only</span></span>            | <span data-ttu-id="d1582-140">True</span><span class="sxs-lookup"><span data-stu-id="d1582-140">True</span></span>         |
| <span data-ttu-id="d1582-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1582-141">Is-Single-Valued</span></span>       | <span data-ttu-id="d1582-142">False</span><span class="sxs-lookup"><span data-stu-id="d1582-142">False</span></span>        |
| <span data-ttu-id="d1582-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1582-143">Is Indexed</span></span>             | <span data-ttu-id="d1582-144">False</span><span class="sxs-lookup"><span data-stu-id="d1582-144">False</span></span>        |
| <span data-ttu-id="d1582-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1582-145">In Global Catalog</span></span>      | <span data-ttu-id="d1582-146">False</span><span class="sxs-lookup"><span data-stu-id="d1582-146">False</span></span>        |
| <span data-ttu-id="d1582-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1582-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1582-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1582-148">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d1582-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1582-149">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d1582-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1582-150">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d1582-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-151">Search-Flags</span></span>           | <span data-ttu-id="d1582-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d1582-152">0x00000008</span></span>   |
| <span data-ttu-id="d1582-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-153">System-Flags</span></span>           | <span data-ttu-id="d1582-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d1582-154">0x00000014</span></span>   |
| <span data-ttu-id="d1582-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1582-155">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="d1582-156">ADAM</span><span class="sxs-lookup"><span data-stu-id="d1582-156">ADAM</span></span>



| <span data-ttu-id="d1582-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1582-157">Entry</span></span> | <span data-ttu-id="d1582-158">Value</span><span class="sxs-lookup"><span data-stu-id="d1582-158">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d1582-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1582-159">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1582-160">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1582-161">System-Only</span></span>            | <span data-ttu-id="d1582-162">True</span><span class="sxs-lookup"><span data-stu-id="d1582-162">True</span></span>         |
| <span data-ttu-id="d1582-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1582-163">Is-Single-Valued</span></span>       | <span data-ttu-id="d1582-164">False</span><span class="sxs-lookup"><span data-stu-id="d1582-164">False</span></span>        |
| <span data-ttu-id="d1582-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1582-165">Is Indexed</span></span>             | <span data-ttu-id="d1582-166">False</span><span class="sxs-lookup"><span data-stu-id="d1582-166">False</span></span>        |
| <span data-ttu-id="d1582-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1582-167">In Global Catalog</span></span>      | <span data-ttu-id="d1582-168">False</span><span class="sxs-lookup"><span data-stu-id="d1582-168">False</span></span>        |
| <span data-ttu-id="d1582-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1582-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1582-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1582-170">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d1582-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1582-171">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d1582-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1582-172">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d1582-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-173">Search-Flags</span></span>           | <span data-ttu-id="d1582-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d1582-174">0x00000008</span></span>   |
| <span data-ttu-id="d1582-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-175">System-Flags</span></span>           | <span data-ttu-id="d1582-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d1582-176">0x00000014</span></span>   |
| <span data-ttu-id="d1582-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1582-177">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d1582-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d1582-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d1582-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1582-179">Entry</span></span> | <span data-ttu-id="d1582-180">Value</span><span class="sxs-lookup"><span data-stu-id="d1582-180">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d1582-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1582-181">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1582-182">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1582-183">System-Only</span></span>            | <span data-ttu-id="d1582-184">True</span><span class="sxs-lookup"><span data-stu-id="d1582-184">True</span></span>         |
| <span data-ttu-id="d1582-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1582-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d1582-186">False</span><span class="sxs-lookup"><span data-stu-id="d1582-186">False</span></span>        |
| <span data-ttu-id="d1582-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1582-187">Is Indexed</span></span>             | <span data-ttu-id="d1582-188">False</span><span class="sxs-lookup"><span data-stu-id="d1582-188">False</span></span>        |
| <span data-ttu-id="d1582-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1582-189">In Global Catalog</span></span>      | <span data-ttu-id="d1582-190">False</span><span class="sxs-lookup"><span data-stu-id="d1582-190">False</span></span>        |
| <span data-ttu-id="d1582-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1582-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1582-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1582-192">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d1582-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1582-193">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d1582-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1582-194">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d1582-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-195">Search-Flags</span></span>           | <span data-ttu-id="d1582-196">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d1582-196">0x00000008</span></span>   |
| <span data-ttu-id="d1582-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-197">System-Flags</span></span>           | <span data-ttu-id="d1582-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d1582-198">0x00000014</span></span>   |
| <span data-ttu-id="d1582-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1582-199">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="d1582-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1582-200">Windows Server 2008</span></span>



| <span data-ttu-id="d1582-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1582-201">Entry</span></span> | <span data-ttu-id="d1582-202">Value</span><span class="sxs-lookup"><span data-stu-id="d1582-202">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d1582-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1582-203">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1582-204">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1582-205">System-Only</span></span>            | <span data-ttu-id="d1582-206">True</span><span class="sxs-lookup"><span data-stu-id="d1582-206">True</span></span>         |
| <span data-ttu-id="d1582-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1582-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d1582-208">False</span><span class="sxs-lookup"><span data-stu-id="d1582-208">False</span></span>        |
| <span data-ttu-id="d1582-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1582-209">Is Indexed</span></span>             | <span data-ttu-id="d1582-210">False</span><span class="sxs-lookup"><span data-stu-id="d1582-210">False</span></span>        |
| <span data-ttu-id="d1582-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1582-211">In Global Catalog</span></span>      | <span data-ttu-id="d1582-212">False</span><span class="sxs-lookup"><span data-stu-id="d1582-212">False</span></span>        |
| <span data-ttu-id="d1582-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1582-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1582-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1582-214">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d1582-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1582-215">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d1582-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1582-216">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d1582-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-217">Search-Flags</span></span>           | <span data-ttu-id="d1582-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d1582-218">0x00000008</span></span>   |
| <span data-ttu-id="d1582-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-219">System-Flags</span></span>           | <span data-ttu-id="d1582-220">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d1582-220">0x00000014</span></span>   |
| <span data-ttu-id="d1582-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1582-221">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d1582-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d1582-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d1582-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1582-223">Entry</span></span> | <span data-ttu-id="d1582-224">Value</span><span class="sxs-lookup"><span data-stu-id="d1582-224">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d1582-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1582-225">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1582-226">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1582-227">System-Only</span></span>            | <span data-ttu-id="d1582-228">True</span><span class="sxs-lookup"><span data-stu-id="d1582-228">True</span></span>         |
| <span data-ttu-id="d1582-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1582-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d1582-230">False</span><span class="sxs-lookup"><span data-stu-id="d1582-230">False</span></span>        |
| <span data-ttu-id="d1582-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1582-231">Is Indexed</span></span>             | <span data-ttu-id="d1582-232">False</span><span class="sxs-lookup"><span data-stu-id="d1582-232">False</span></span>        |
| <span data-ttu-id="d1582-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1582-233">In Global Catalog</span></span>      | <span data-ttu-id="d1582-234">False</span><span class="sxs-lookup"><span data-stu-id="d1582-234">False</span></span>        |
| <span data-ttu-id="d1582-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1582-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1582-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1582-236">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d1582-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1582-237">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d1582-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1582-238">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d1582-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-239">Search-Flags</span></span>           | <span data-ttu-id="d1582-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d1582-240">0x00000008</span></span>   |
| <span data-ttu-id="d1582-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-241">System-Flags</span></span>           | <span data-ttu-id="d1582-242">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d1582-242">0x00000014</span></span>   |
| <span data-ttu-id="d1582-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1582-243">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="d1582-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1582-244">Windows Server 2012</span></span>



| <span data-ttu-id="d1582-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1582-245">Entry</span></span> | <span data-ttu-id="d1582-246">Value</span><span class="sxs-lookup"><span data-stu-id="d1582-246">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="d1582-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1582-247">Link-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1582-248">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="d1582-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1582-249">System-Only</span></span>            | <span data-ttu-id="d1582-250">True</span><span class="sxs-lookup"><span data-stu-id="d1582-250">True</span></span>         |
| <span data-ttu-id="d1582-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1582-251">Is-Single-Valued</span></span>       | <span data-ttu-id="d1582-252">False</span><span class="sxs-lookup"><span data-stu-id="d1582-252">False</span></span>        |
| <span data-ttu-id="d1582-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1582-253">Is Indexed</span></span>             | <span data-ttu-id="d1582-254">False</span><span class="sxs-lookup"><span data-stu-id="d1582-254">False</span></span>        |
| <span data-ttu-id="d1582-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1582-255">In Global Catalog</span></span>      | <span data-ttu-id="d1582-256">False</span><span class="sxs-lookup"><span data-stu-id="d1582-256">False</span></span>        |
| <span data-ttu-id="d1582-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1582-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1582-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1582-258">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="d1582-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1582-259">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="d1582-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1582-260">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="d1582-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-261">Search-Flags</span></span>           | <span data-ttu-id="d1582-262">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d1582-262">0x00000008</span></span>   |
| <span data-ttu-id="d1582-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1582-263">System-Flags</span></span>           | <span data-ttu-id="d1582-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d1582-264">0x00000014</span></span>   |
| <span data-ttu-id="d1582-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1582-265">Classes used in</span></span>        | \-           |



 

 




