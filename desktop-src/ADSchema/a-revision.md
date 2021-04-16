---
title: Atributo de revisión
description: El nivel de revisión para un descriptor de seguridad u otro cambio. Solo se usa en los objetos Sam-Server y DS-UI-Settings.
ms.assetid: 480de80f-3e76-4a62-a4a7-29a67f910a62
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de revisión
- Esquema de AD de atributo de revisión
topic_type:
- apiref
api_name:
- Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8948bd865db776c52ac021d296792a6f7d0720dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535902"
---
# <a name="revision-attribute"></a><span data-ttu-id="a893c-106">Atributo de revisión</span><span class="sxs-lookup"><span data-stu-id="a893c-106">Revision attribute</span></span>

<span data-ttu-id="a893c-107">El nivel de revisión para un descriptor de seguridad u otro cambio.</span><span class="sxs-lookup"><span data-stu-id="a893c-107">The revision level for a security descriptor or other change.</span></span> <span data-ttu-id="a893c-108">Solo se usa en los objetos Sam-Server y DS-UI-Settings.</span><span class="sxs-lookup"><span data-stu-id="a893c-108">Only used in the sam-server and ds-ui-settings objects.</span></span>



| <span data-ttu-id="a893c-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a893c-109">Entry</span></span> | <span data-ttu-id="a893c-110">Value</span><span class="sxs-lookup"><span data-stu-id="a893c-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a893c-111">CN</span><span class="sxs-lookup"><span data-stu-id="a893c-111">CN</span></span>                | <span data-ttu-id="a893c-112">Revisión</span><span class="sxs-lookup"><span data-stu-id="a893c-112">Revision</span></span>                             |
| <span data-ttu-id="a893c-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a893c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a893c-114">revision</span><span class="sxs-lookup"><span data-stu-id="a893c-114">revision</span></span>                             |
| <span data-ttu-id="a893c-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a893c-115">Size</span></span>              | <span data-ttu-id="a893c-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="a893c-116">4 bytes</span></span>                              |
| <span data-ttu-id="a893c-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a893c-117">Update Privilege</span></span>  | <span data-ttu-id="a893c-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="a893c-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="a893c-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a893c-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a893c-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a893c-120">Attribute-Id</span></span>      | <span data-ttu-id="a893c-121">1.2.840.113556.1.4.145</span><span class="sxs-lookup"><span data-stu-id="a893c-121">1.2.840.113556.1.4.145</span></span>               |
| <span data-ttu-id="a893c-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a893c-122">System-Id-Guid</span></span>    | <span data-ttu-id="a893c-123">bf967a21-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a893c-123">bf967a21-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="a893c-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a893c-124">Syntax</span></span>            | [<span data-ttu-id="a893c-125">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="a893c-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="a893c-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a893c-126">Implementations</span></span>

-   [<span data-ttu-id="a893c-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a893c-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a893c-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a893c-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a893c-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a893c-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a893c-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a893c-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a893c-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a893c-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a893c-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a893c-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a893c-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a893c-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a893c-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a893c-134">Windows 2000 Server</span></span>



| <span data-ttu-id="a893c-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="a893c-135">Entry</span></span> | <span data-ttu-id="a893c-136">Value</span><span class="sxs-lookup"><span data-stu-id="a893c-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a893c-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a893c-137">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a893c-138">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="a893c-139">System-Only</span></span>            | <span data-ttu-id="a893c-140">False</span><span class="sxs-lookup"><span data-stu-id="a893c-140">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a893c-141">Is-Single-Valued</span></span>       | <span data-ttu-id="a893c-142">True</span><span class="sxs-lookup"><span data-stu-id="a893c-142">True</span></span>                                                                                  |
| <span data-ttu-id="a893c-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a893c-143">Is Indexed</span></span>             | <span data-ttu-id="a893c-144">False</span><span class="sxs-lookup"><span data-stu-id="a893c-144">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a893c-145">In Global Catalog</span></span>      | <span data-ttu-id="a893c-146">False</span><span class="sxs-lookup"><span data-stu-id="a893c-146">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a893c-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="a893c-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a893c-148">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="a893c-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a893c-149">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a893c-150">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-151">Search-Flags</span></span>           | <span data-ttu-id="a893c-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a893c-152">0x00000000</span></span>                                                                            |
| <span data-ttu-id="a893c-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-153">System-Flags</span></span>           | <span data-ttu-id="a893c-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a893c-154">0x00000010</span></span>                                                                            |
| <span data-ttu-id="a893c-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a893c-155">Classes used in</span></span>        | [<span data-ttu-id="a893c-156">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="a893c-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="a893c-157">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a893c-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a893c-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a893c-158">Windows Server 2003</span></span>



| <span data-ttu-id="a893c-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="a893c-159">Entry</span></span> | <span data-ttu-id="a893c-160">Value</span><span class="sxs-lookup"><span data-stu-id="a893c-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a893c-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a893c-161">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a893c-162">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="a893c-163">System-Only</span></span>            | <span data-ttu-id="a893c-164">False</span><span class="sxs-lookup"><span data-stu-id="a893c-164">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a893c-165">Is-Single-Valued</span></span>       | <span data-ttu-id="a893c-166">True</span><span class="sxs-lookup"><span data-stu-id="a893c-166">True</span></span>                                                                                  |
| <span data-ttu-id="a893c-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a893c-167">Is Indexed</span></span>             | <span data-ttu-id="a893c-168">False</span><span class="sxs-lookup"><span data-stu-id="a893c-168">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a893c-169">In Global Catalog</span></span>      | <span data-ttu-id="a893c-170">False</span><span class="sxs-lookup"><span data-stu-id="a893c-170">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a893c-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="a893c-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a893c-172">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="a893c-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a893c-173">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a893c-174">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-175">Search-Flags</span></span>           | <span data-ttu-id="a893c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a893c-176">0x00000000</span></span>                                                                            |
| <span data-ttu-id="a893c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-177">System-Flags</span></span>           | <span data-ttu-id="a893c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a893c-178">0x00000010</span></span>                                                                            |
| <span data-ttu-id="a893c-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a893c-179">Classes used in</span></span>        | [<span data-ttu-id="a893c-180">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="a893c-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="a893c-181">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a893c-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a893c-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="a893c-182">ADAM</span></span>



| <span data-ttu-id="a893c-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="a893c-183">Entry</span></span> | <span data-ttu-id="a893c-184">Value</span><span class="sxs-lookup"><span data-stu-id="a893c-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a893c-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a893c-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a893c-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a893c-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a893c-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="a893c-187">System-Only</span></span>            | <span data-ttu-id="a893c-188">False</span><span class="sxs-lookup"><span data-stu-id="a893c-188">False</span></span>                           |
| <span data-ttu-id="a893c-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a893c-189">Is-Single-Valued</span></span>       | <span data-ttu-id="a893c-190">True</span><span class="sxs-lookup"><span data-stu-id="a893c-190">True</span></span>                            |
| <span data-ttu-id="a893c-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a893c-191">Is Indexed</span></span>             | <span data-ttu-id="a893c-192">False</span><span class="sxs-lookup"><span data-stu-id="a893c-192">False</span></span>                           |
| <span data-ttu-id="a893c-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a893c-193">In Global Catalog</span></span>      | <span data-ttu-id="a893c-194">False</span><span class="sxs-lookup"><span data-stu-id="a893c-194">False</span></span>                           |
| <span data-ttu-id="a893c-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a893c-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="a893c-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a893c-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a893c-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a893c-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a893c-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a893c-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a893c-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-199">Search-Flags</span></span>           | <span data-ttu-id="a893c-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a893c-200">0x00000000</span></span>                      |
| <span data-ttu-id="a893c-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-201">System-Flags</span></span>           | <span data-ttu-id="a893c-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a893c-202">0x00000010</span></span>                      |
| <span data-ttu-id="a893c-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a893c-203">Classes used in</span></span>        | [<span data-ttu-id="a893c-204">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a893c-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a893c-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a893c-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a893c-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="a893c-206">Entry</span></span> | <span data-ttu-id="a893c-207">Value</span><span class="sxs-lookup"><span data-stu-id="a893c-207">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a893c-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a893c-208">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a893c-209">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="a893c-210">System-Only</span></span>            | <span data-ttu-id="a893c-211">False</span><span class="sxs-lookup"><span data-stu-id="a893c-211">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a893c-212">Is-Single-Valued</span></span>       | <span data-ttu-id="a893c-213">True</span><span class="sxs-lookup"><span data-stu-id="a893c-213">True</span></span>                                                                                  |
| <span data-ttu-id="a893c-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a893c-214">Is Indexed</span></span>             | <span data-ttu-id="a893c-215">False</span><span class="sxs-lookup"><span data-stu-id="a893c-215">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a893c-216">In Global Catalog</span></span>      | <span data-ttu-id="a893c-217">False</span><span class="sxs-lookup"><span data-stu-id="a893c-217">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a893c-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="a893c-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a893c-219">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="a893c-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a893c-220">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a893c-221">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-222">Search-Flags</span></span>           | <span data-ttu-id="a893c-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a893c-223">0x00000000</span></span>                                                                            |
| <span data-ttu-id="a893c-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-224">System-Flags</span></span>           | <span data-ttu-id="a893c-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a893c-225">0x00000010</span></span>                                                                            |
| <span data-ttu-id="a893c-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a893c-226">Classes used in</span></span>        | [<span data-ttu-id="a893c-227">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="a893c-227">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="a893c-228">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a893c-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a893c-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a893c-229">Windows Server 2008</span></span>



| <span data-ttu-id="a893c-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="a893c-230">Entry</span></span> | <span data-ttu-id="a893c-231">Value</span><span class="sxs-lookup"><span data-stu-id="a893c-231">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a893c-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a893c-232">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a893c-233">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="a893c-234">System-Only</span></span>            | <span data-ttu-id="a893c-235">False</span><span class="sxs-lookup"><span data-stu-id="a893c-235">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-236">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a893c-236">Is-Single-Valued</span></span>       | <span data-ttu-id="a893c-237">True</span><span class="sxs-lookup"><span data-stu-id="a893c-237">True</span></span>                                                                                  |
| <span data-ttu-id="a893c-238">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a893c-238">Is Indexed</span></span>             | <span data-ttu-id="a893c-239">False</span><span class="sxs-lookup"><span data-stu-id="a893c-239">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-240">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a893c-240">In Global Catalog</span></span>      | <span data-ttu-id="a893c-241">False</span><span class="sxs-lookup"><span data-stu-id="a893c-241">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-242">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a893c-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="a893c-243">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a893c-243">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="a893c-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a893c-244">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a893c-245">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-246">Search-Flags</span></span>           | <span data-ttu-id="a893c-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a893c-247">0x00000000</span></span>                                                                            |
| <span data-ttu-id="a893c-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-248">System-Flags</span></span>           | <span data-ttu-id="a893c-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a893c-249">0x00000010</span></span>                                                                            |
| <span data-ttu-id="a893c-250">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a893c-250">Classes used in</span></span>        | [<span data-ttu-id="a893c-251">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="a893c-251">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="a893c-252">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a893c-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a893c-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a893c-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a893c-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="a893c-254">Entry</span></span> | <span data-ttu-id="a893c-255">Value</span><span class="sxs-lookup"><span data-stu-id="a893c-255">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a893c-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a893c-256">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a893c-257">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="a893c-258">System-Only</span></span>            | <span data-ttu-id="a893c-259">False</span><span class="sxs-lookup"><span data-stu-id="a893c-259">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-260">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a893c-260">Is-Single-Valued</span></span>       | <span data-ttu-id="a893c-261">True</span><span class="sxs-lookup"><span data-stu-id="a893c-261">True</span></span>                                                                                  |
| <span data-ttu-id="a893c-262">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a893c-262">Is Indexed</span></span>             | <span data-ttu-id="a893c-263">False</span><span class="sxs-lookup"><span data-stu-id="a893c-263">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-264">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a893c-264">In Global Catalog</span></span>      | <span data-ttu-id="a893c-265">False</span><span class="sxs-lookup"><span data-stu-id="a893c-265">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-266">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a893c-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="a893c-267">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a893c-267">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="a893c-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a893c-268">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a893c-269">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-270">Search-Flags</span></span>           | <span data-ttu-id="a893c-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a893c-271">0x00000000</span></span>                                                                            |
| <span data-ttu-id="a893c-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-272">System-Flags</span></span>           | <span data-ttu-id="a893c-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a893c-273">0x00000010</span></span>                                                                            |
| <span data-ttu-id="a893c-274">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a893c-274">Classes used in</span></span>        | [<span data-ttu-id="a893c-275">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="a893c-275">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="a893c-276">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a893c-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a893c-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a893c-277">Windows Server 2012</span></span>



| <span data-ttu-id="a893c-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="a893c-278">Entry</span></span> | <span data-ttu-id="a893c-279">Value</span><span class="sxs-lookup"><span data-stu-id="a893c-279">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a893c-280">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a893c-280">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a893c-281">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="a893c-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="a893c-282">System-Only</span></span>            | <span data-ttu-id="a893c-283">False</span><span class="sxs-lookup"><span data-stu-id="a893c-283">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-284">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a893c-284">Is-Single-Valued</span></span>       | <span data-ttu-id="a893c-285">True</span><span class="sxs-lookup"><span data-stu-id="a893c-285">True</span></span>                                                                                  |
| <span data-ttu-id="a893c-286">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a893c-286">Is Indexed</span></span>             | <span data-ttu-id="a893c-287">False</span><span class="sxs-lookup"><span data-stu-id="a893c-287">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-288">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a893c-288">In Global Catalog</span></span>      | <span data-ttu-id="a893c-289">False</span><span class="sxs-lookup"><span data-stu-id="a893c-289">False</span></span>                                                                                 |
| <span data-ttu-id="a893c-290">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a893c-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="a893c-291">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a893c-291">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="a893c-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a893c-292">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a893c-293">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="a893c-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-294">Search-Flags</span></span>           | <span data-ttu-id="a893c-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a893c-295">0x00000000</span></span>                                                                            |
| <span data-ttu-id="a893c-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a893c-296">System-Flags</span></span>           | <span data-ttu-id="a893c-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a893c-297">0x00000010</span></span>                                                                            |
| <span data-ttu-id="a893c-298">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a893c-298">Classes used in</span></span>        | [<span data-ttu-id="a893c-299">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="a893c-299">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="a893c-300">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a893c-300">**Top**</span></span>](c-top.md)<br/> |



 

 





