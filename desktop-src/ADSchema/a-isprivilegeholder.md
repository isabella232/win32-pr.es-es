---
title: Atributo is-privileged
description: Vínculo hacia atrás a los privilegios mantenidos por una entidad de seguridad determinada.
ms.assetid: 94355fbc-f7d8-460b-a516-1576629ca63e
ms.tgt_platform: multiple
keywords:
- Atributo is-Privilege-contenedor AD Schema
- isPrivilegeHolder esquema de AD de atributos
topic_type:
- apiref
api_name:
- Is-Privilege-Holder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895a0202f6ca51ffe7982f33c1fc9f02d021d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658936"
---
# <a name="is-privilege-holder-attribute"></a><span data-ttu-id="b81f1-105">Atributo is-privileged</span><span class="sxs-lookup"><span data-stu-id="b81f1-105">Is-Privilege-Holder attribute</span></span>

<span data-ttu-id="b81f1-106">Vínculo hacia atrás a los privilegios mantenidos por una entidad de seguridad determinada.</span><span class="sxs-lookup"><span data-stu-id="b81f1-106">Backward link to privileges held by a given principal.</span></span>



| <span data-ttu-id="b81f1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b81f1-107">Entry</span></span> | <span data-ttu-id="b81f1-108">Value</span><span class="sxs-lookup"><span data-stu-id="b81f1-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="b81f1-109">CN</span><span class="sxs-lookup"><span data-stu-id="b81f1-109">CN</span></span>                | <span data-ttu-id="b81f1-110">Es-titular de privilegios</span><span class="sxs-lookup"><span data-stu-id="b81f1-110">Is-Privilege-Holder</span></span>                     |
| <span data-ttu-id="b81f1-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b81f1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b81f1-112">isPrivilegeHolder</span><span class="sxs-lookup"><span data-stu-id="b81f1-112">isPrivilegeHolder</span></span>                       |
| <span data-ttu-id="b81f1-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b81f1-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="b81f1-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b81f1-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="b81f1-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b81f1-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="b81f1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b81f1-116">Attribute-Id</span></span>      | <span data-ttu-id="b81f1-117">1.2.840.113556.1.4.638</span><span class="sxs-lookup"><span data-stu-id="b81f1-117">1.2.840.113556.1.4.638</span></span>                  |
| <span data-ttu-id="b81f1-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b81f1-118">System-Id-Guid</span></span>    | <span data-ttu-id="b81f1-119">19405b9c-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b81f1-119">19405b9c-3cfa-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="b81f1-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b81f1-120">Syntax</span></span>            | [<span data-ttu-id="b81f1-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b81f1-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="b81f1-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b81f1-122">Implementations</span></span>

-   [<span data-ttu-id="b81f1-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b81f1-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b81f1-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b81f1-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b81f1-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b81f1-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b81f1-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b81f1-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b81f1-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b81f1-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b81f1-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b81f1-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b81f1-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b81f1-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b81f1-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="b81f1-130">Entry</span></span> | <span data-ttu-id="b81f1-131">Value</span><span class="sxs-lookup"><span data-stu-id="b81f1-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b81f1-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b81f1-132">Link-Id</span></span>                | <span data-ttu-id="b81f1-133">71</span><span class="sxs-lookup"><span data-stu-id="b81f1-133">71</span></span>                              |
| <span data-ttu-id="b81f1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b81f1-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b81f1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b81f1-135">System-Only</span></span>            | <span data-ttu-id="b81f1-136">True</span><span class="sxs-lookup"><span data-stu-id="b81f1-136">True</span></span>                            |
| <span data-ttu-id="b81f1-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b81f1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b81f1-138">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-138">False</span></span>                           |
| <span data-ttu-id="b81f1-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b81f1-139">Is Indexed</span></span>             | <span data-ttu-id="b81f1-140">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-140">False</span></span>                           |
| <span data-ttu-id="b81f1-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b81f1-141">In Global Catalog</span></span>      | <span data-ttu-id="b81f1-142">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-142">False</span></span>                           |
| <span data-ttu-id="b81f1-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b81f1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b81f1-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b81f1-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b81f1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b81f1-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b81f1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b81f1-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b81f1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-147">Search-Flags</span></span>           | <span data-ttu-id="b81f1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b81f1-148">0x00000000</span></span>                      |
| <span data-ttu-id="b81f1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-149">System-Flags</span></span>           | <span data-ttu-id="b81f1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b81f1-150">0x00000010</span></span>                      |
| <span data-ttu-id="b81f1-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b81f1-151">Classes used in</span></span>        | [<span data-ttu-id="b81f1-152">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="b81f1-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b81f1-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b81f1-153">Windows Server 2003</span></span>



| <span data-ttu-id="b81f1-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="b81f1-154">Entry</span></span> | <span data-ttu-id="b81f1-155">Value</span><span class="sxs-lookup"><span data-stu-id="b81f1-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b81f1-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b81f1-156">Link-Id</span></span>                | <span data-ttu-id="b81f1-157">71</span><span class="sxs-lookup"><span data-stu-id="b81f1-157">71</span></span>                              |
| <span data-ttu-id="b81f1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b81f1-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b81f1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b81f1-159">System-Only</span></span>            | <span data-ttu-id="b81f1-160">True</span><span class="sxs-lookup"><span data-stu-id="b81f1-160">True</span></span>                            |
| <span data-ttu-id="b81f1-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b81f1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b81f1-162">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-162">False</span></span>                           |
| <span data-ttu-id="b81f1-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b81f1-163">Is Indexed</span></span>             | <span data-ttu-id="b81f1-164">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-164">False</span></span>                           |
| <span data-ttu-id="b81f1-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b81f1-165">In Global Catalog</span></span>      | <span data-ttu-id="b81f1-166">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-166">False</span></span>                           |
| <span data-ttu-id="b81f1-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b81f1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b81f1-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b81f1-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b81f1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b81f1-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b81f1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b81f1-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b81f1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-171">Search-Flags</span></span>           | <span data-ttu-id="b81f1-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b81f1-172">0x00000000</span></span>                      |
| <span data-ttu-id="b81f1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-173">System-Flags</span></span>           | <span data-ttu-id="b81f1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b81f1-174">0x00000010</span></span>                      |
| <span data-ttu-id="b81f1-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b81f1-175">Classes used in</span></span>        | [<span data-ttu-id="b81f1-176">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="b81f1-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b81f1-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b81f1-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b81f1-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="b81f1-178">Entry</span></span> | <span data-ttu-id="b81f1-179">Value</span><span class="sxs-lookup"><span data-stu-id="b81f1-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b81f1-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b81f1-180">Link-Id</span></span>                | <span data-ttu-id="b81f1-181">71</span><span class="sxs-lookup"><span data-stu-id="b81f1-181">71</span></span>                              |
| <span data-ttu-id="b81f1-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b81f1-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b81f1-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b81f1-183">System-Only</span></span>            | <span data-ttu-id="b81f1-184">True</span><span class="sxs-lookup"><span data-stu-id="b81f1-184">True</span></span>                            |
| <span data-ttu-id="b81f1-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b81f1-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b81f1-186">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-186">False</span></span>                           |
| <span data-ttu-id="b81f1-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b81f1-187">Is Indexed</span></span>             | <span data-ttu-id="b81f1-188">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-188">False</span></span>                           |
| <span data-ttu-id="b81f1-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b81f1-189">In Global Catalog</span></span>      | <span data-ttu-id="b81f1-190">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-190">False</span></span>                           |
| <span data-ttu-id="b81f1-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b81f1-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b81f1-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b81f1-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b81f1-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b81f1-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b81f1-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b81f1-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b81f1-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-195">Search-Flags</span></span>           | <span data-ttu-id="b81f1-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b81f1-196">0x00000000</span></span>                      |
| <span data-ttu-id="b81f1-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-197">System-Flags</span></span>           | <span data-ttu-id="b81f1-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b81f1-198">0x00000010</span></span>                      |
| <span data-ttu-id="b81f1-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b81f1-199">Classes used in</span></span>        | [<span data-ttu-id="b81f1-200">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="b81f1-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b81f1-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b81f1-201">Windows Server 2008</span></span>



| <span data-ttu-id="b81f1-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="b81f1-202">Entry</span></span> | <span data-ttu-id="b81f1-203">Value</span><span class="sxs-lookup"><span data-stu-id="b81f1-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b81f1-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b81f1-204">Link-Id</span></span>                | <span data-ttu-id="b81f1-205">71</span><span class="sxs-lookup"><span data-stu-id="b81f1-205">71</span></span>                              |
| <span data-ttu-id="b81f1-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b81f1-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b81f1-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="b81f1-207">System-Only</span></span>            | <span data-ttu-id="b81f1-208">True</span><span class="sxs-lookup"><span data-stu-id="b81f1-208">True</span></span>                            |
| <span data-ttu-id="b81f1-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b81f1-209">Is-Single-Valued</span></span>       | <span data-ttu-id="b81f1-210">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-210">False</span></span>                           |
| <span data-ttu-id="b81f1-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b81f1-211">Is Indexed</span></span>             | <span data-ttu-id="b81f1-212">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-212">False</span></span>                           |
| <span data-ttu-id="b81f1-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b81f1-213">In Global Catalog</span></span>      | <span data-ttu-id="b81f1-214">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-214">False</span></span>                           |
| <span data-ttu-id="b81f1-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b81f1-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="b81f1-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b81f1-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b81f1-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b81f1-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b81f1-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b81f1-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b81f1-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-219">Search-Flags</span></span>           | <span data-ttu-id="b81f1-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b81f1-220">0x00000000</span></span>                      |
| <span data-ttu-id="b81f1-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-221">System-Flags</span></span>           | <span data-ttu-id="b81f1-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b81f1-222">0x00000010</span></span>                      |
| <span data-ttu-id="b81f1-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b81f1-223">Classes used in</span></span>        | [<span data-ttu-id="b81f1-224">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="b81f1-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b81f1-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b81f1-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b81f1-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="b81f1-226">Entry</span></span> | <span data-ttu-id="b81f1-227">Value</span><span class="sxs-lookup"><span data-stu-id="b81f1-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b81f1-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b81f1-228">Link-Id</span></span>                | <span data-ttu-id="b81f1-229">71</span><span class="sxs-lookup"><span data-stu-id="b81f1-229">71</span></span>                              |
| <span data-ttu-id="b81f1-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b81f1-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b81f1-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="b81f1-231">System-Only</span></span>            | <span data-ttu-id="b81f1-232">True</span><span class="sxs-lookup"><span data-stu-id="b81f1-232">True</span></span>                            |
| <span data-ttu-id="b81f1-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b81f1-233">Is-Single-Valued</span></span>       | <span data-ttu-id="b81f1-234">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-234">False</span></span>                           |
| <span data-ttu-id="b81f1-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b81f1-235">Is Indexed</span></span>             | <span data-ttu-id="b81f1-236">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-236">False</span></span>                           |
| <span data-ttu-id="b81f1-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b81f1-237">In Global Catalog</span></span>      | <span data-ttu-id="b81f1-238">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-238">False</span></span>                           |
| <span data-ttu-id="b81f1-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b81f1-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="b81f1-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b81f1-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b81f1-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b81f1-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b81f1-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b81f1-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b81f1-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-243">Search-Flags</span></span>           | <span data-ttu-id="b81f1-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b81f1-244">0x00000000</span></span>                      |
| <span data-ttu-id="b81f1-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-245">System-Flags</span></span>           | <span data-ttu-id="b81f1-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b81f1-246">0x00000010</span></span>                      |
| <span data-ttu-id="b81f1-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b81f1-247">Classes used in</span></span>        | [<span data-ttu-id="b81f1-248">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="b81f1-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b81f1-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b81f1-249">Windows Server 2012</span></span>



| <span data-ttu-id="b81f1-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="b81f1-250">Entry</span></span> | <span data-ttu-id="b81f1-251">Value</span><span class="sxs-lookup"><span data-stu-id="b81f1-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b81f1-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b81f1-252">Link-Id</span></span>                | <span data-ttu-id="b81f1-253">71</span><span class="sxs-lookup"><span data-stu-id="b81f1-253">71</span></span>                              |
| <span data-ttu-id="b81f1-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b81f1-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b81f1-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="b81f1-255">System-Only</span></span>            | <span data-ttu-id="b81f1-256">True</span><span class="sxs-lookup"><span data-stu-id="b81f1-256">True</span></span>                            |
| <span data-ttu-id="b81f1-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b81f1-257">Is-Single-Valued</span></span>       | <span data-ttu-id="b81f1-258">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-258">False</span></span>                           |
| <span data-ttu-id="b81f1-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b81f1-259">Is Indexed</span></span>             | <span data-ttu-id="b81f1-260">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-260">False</span></span>                           |
| <span data-ttu-id="b81f1-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b81f1-261">In Global Catalog</span></span>      | <span data-ttu-id="b81f1-262">False</span><span class="sxs-lookup"><span data-stu-id="b81f1-262">False</span></span>                           |
| <span data-ttu-id="b81f1-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b81f1-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="b81f1-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b81f1-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b81f1-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b81f1-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b81f1-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b81f1-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b81f1-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-267">Search-Flags</span></span>           | <span data-ttu-id="b81f1-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b81f1-268">0x00000000</span></span>                      |
| <span data-ttu-id="b81f1-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b81f1-269">System-Flags</span></span>           | <span data-ttu-id="b81f1-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b81f1-270">0x00000010</span></span>                      |
| <span data-ttu-id="b81f1-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b81f1-271">Classes used in</span></span>        | [<span data-ttu-id="b81f1-272">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="b81f1-272">**Top**</span></span>](c-top.md)<br/> |



 

 





