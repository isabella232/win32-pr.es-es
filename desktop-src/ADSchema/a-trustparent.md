---
title: Trust-Parent atributo)
description: Elemento primario en la jerarquía de confianza de KERBEROS.
ms.assetid: 738cf509-42a2-40b6-a525-6df34c02d0f0
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Trust-Parent
- trustParent esquema de AD de atributos
topic_type:
- apiref
api_name:
- Trust-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8be971c7597b14daf7a694e41c9d67714e5f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804807"
---
# <a name="trust-parent-attribute"></a><span data-ttu-id="a3d49-105">Trust-Parent atributo)</span><span class="sxs-lookup"><span data-stu-id="a3d49-105">Trust-Parent attribute</span></span>

<span data-ttu-id="a3d49-106">Elemento primario en la jerarquía de confianza de KERBEROS.</span><span class="sxs-lookup"><span data-stu-id="a3d49-106">The parent in KERBEROS trust hierarchy.</span></span>



| <span data-ttu-id="a3d49-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3d49-107">Entry</span></span> | <span data-ttu-id="a3d49-108">Value</span><span class="sxs-lookup"><span data-stu-id="a3d49-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="a3d49-109">CN</span><span class="sxs-lookup"><span data-stu-id="a3d49-109">CN</span></span>                | <span data-ttu-id="a3d49-110">Trust-Parent</span><span class="sxs-lookup"><span data-stu-id="a3d49-110">Trust-Parent</span></span>                            |
| <span data-ttu-id="a3d49-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a3d49-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a3d49-112">trustParent</span><span class="sxs-lookup"><span data-stu-id="a3d49-112">trustParent</span></span>                             |
| <span data-ttu-id="a3d49-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a3d49-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="a3d49-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a3d49-114">Update Privilege</span></span>  | <span data-ttu-id="a3d49-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="a3d49-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="a3d49-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a3d49-116">Update Frequency</span></span>  | <span data-ttu-id="a3d49-117">Cuando se crea un dominio secundario.</span><span class="sxs-lookup"><span data-stu-id="a3d49-117">When a child domain is created.</span></span>         |
| <span data-ttu-id="a3d49-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a3d49-118">Attribute-Id</span></span>      | <span data-ttu-id="a3d49-119">1.2.840.113556.1.4.471</span><span class="sxs-lookup"><span data-stu-id="a3d49-119">1.2.840.113556.1.4.471</span></span>                  |
| <span data-ttu-id="a3d49-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a3d49-120">System-Id-Guid</span></span>    | <span data-ttu-id="a3d49-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="a3d49-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="a3d49-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3d49-122">Syntax</span></span>            | [<span data-ttu-id="a3d49-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a3d49-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="a3d49-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a3d49-124">Implementations</span></span>

-   [<span data-ttu-id="a3d49-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a3d49-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a3d49-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a3d49-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a3d49-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a3d49-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a3d49-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a3d49-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a3d49-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a3d49-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a3d49-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a3d49-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a3d49-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a3d49-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a3d49-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3d49-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a3d49-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3d49-133">Entry</span></span> | <span data-ttu-id="a3d49-134">Value</span><span class="sxs-lookup"><span data-stu-id="a3d49-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a3d49-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3d49-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3d49-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3d49-137">System-Only</span></span>            | <span data-ttu-id="a3d49-138">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-138">False</span></span>                                      |
| <span data-ttu-id="a3d49-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3d49-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a3d49-140">True</span><span class="sxs-lookup"><span data-stu-id="a3d49-140">True</span></span>                                       |
| <span data-ttu-id="a3d49-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3d49-141">Is Indexed</span></span>             | <span data-ttu-id="a3d49-142">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-142">False</span></span>                                      |
| <span data-ttu-id="a3d49-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3d49-143">In Global Catalog</span></span>      | <span data-ttu-id="a3d49-144">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-144">False</span></span>                                      |
| <span data-ttu-id="a3d49-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3d49-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3d49-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3d49-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a3d49-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3d49-147">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3d49-148">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-149">Search-Flags</span></span>           | <span data-ttu-id="a3d49-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3d49-150">0x00000000</span></span>                                 |
| <span data-ttu-id="a3d49-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-151">System-Flags</span></span>           | <span data-ttu-id="a3d49-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3d49-152">0x00000010</span></span>                                 |
| <span data-ttu-id="a3d49-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3d49-153">Classes used in</span></span>        | [<span data-ttu-id="a3d49-154">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a3d49-154">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a3d49-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3d49-155">Windows Server 2003</span></span>



| <span data-ttu-id="a3d49-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3d49-156">Entry</span></span> | <span data-ttu-id="a3d49-157">Value</span><span class="sxs-lookup"><span data-stu-id="a3d49-157">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a3d49-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3d49-158">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3d49-159">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3d49-160">System-Only</span></span>            | <span data-ttu-id="a3d49-161">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-161">False</span></span>                                      |
| <span data-ttu-id="a3d49-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3d49-162">Is-Single-Valued</span></span>       | <span data-ttu-id="a3d49-163">True</span><span class="sxs-lookup"><span data-stu-id="a3d49-163">True</span></span>                                       |
| <span data-ttu-id="a3d49-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3d49-164">Is Indexed</span></span>             | <span data-ttu-id="a3d49-165">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-165">False</span></span>                                      |
| <span data-ttu-id="a3d49-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3d49-166">In Global Catalog</span></span>      | <span data-ttu-id="a3d49-167">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-167">False</span></span>                                      |
| <span data-ttu-id="a3d49-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3d49-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3d49-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3d49-169">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a3d49-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3d49-170">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3d49-171">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-172">Search-Flags</span></span>           | <span data-ttu-id="a3d49-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3d49-173">0x00000000</span></span>                                 |
| <span data-ttu-id="a3d49-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-174">System-Flags</span></span>           | <span data-ttu-id="a3d49-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3d49-175">0x00000010</span></span>                                 |
| <span data-ttu-id="a3d49-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3d49-176">Classes used in</span></span>        | [<span data-ttu-id="a3d49-177">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a3d49-177">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a3d49-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="a3d49-178">ADAM</span></span>



| <span data-ttu-id="a3d49-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3d49-179">Entry</span></span> | <span data-ttu-id="a3d49-180">Value</span><span class="sxs-lookup"><span data-stu-id="a3d49-180">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a3d49-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3d49-181">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3d49-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3d49-183">System-Only</span></span>            | <span data-ttu-id="a3d49-184">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-184">False</span></span>                                      |
| <span data-ttu-id="a3d49-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3d49-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a3d49-186">True</span><span class="sxs-lookup"><span data-stu-id="a3d49-186">True</span></span>                                       |
| <span data-ttu-id="a3d49-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3d49-187">Is Indexed</span></span>             | <span data-ttu-id="a3d49-188">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-188">False</span></span>                                      |
| <span data-ttu-id="a3d49-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3d49-189">In Global Catalog</span></span>      | <span data-ttu-id="a3d49-190">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-190">False</span></span>                                      |
| <span data-ttu-id="a3d49-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3d49-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3d49-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3d49-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a3d49-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3d49-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3d49-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-195">Search-Flags</span></span>           | <span data-ttu-id="a3d49-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3d49-196">0x00000000</span></span>                                 |
| <span data-ttu-id="a3d49-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-197">System-Flags</span></span>           | <span data-ttu-id="a3d49-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3d49-198">0x00000010</span></span>                                 |
| <span data-ttu-id="a3d49-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3d49-199">Classes used in</span></span>        | [<span data-ttu-id="a3d49-200">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a3d49-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a3d49-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a3d49-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a3d49-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3d49-202">Entry</span></span> | <span data-ttu-id="a3d49-203">Value</span><span class="sxs-lookup"><span data-stu-id="a3d49-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a3d49-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3d49-204">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3d49-205">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3d49-206">System-Only</span></span>            | <span data-ttu-id="a3d49-207">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-207">False</span></span>                                      |
| <span data-ttu-id="a3d49-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3d49-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a3d49-209">True</span><span class="sxs-lookup"><span data-stu-id="a3d49-209">True</span></span>                                       |
| <span data-ttu-id="a3d49-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3d49-210">Is Indexed</span></span>             | <span data-ttu-id="a3d49-211">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-211">False</span></span>                                      |
| <span data-ttu-id="a3d49-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3d49-212">In Global Catalog</span></span>      | <span data-ttu-id="a3d49-213">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-213">False</span></span>                                      |
| <span data-ttu-id="a3d49-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3d49-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3d49-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3d49-215">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a3d49-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3d49-216">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3d49-217">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-218">Search-Flags</span></span>           | <span data-ttu-id="a3d49-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3d49-219">0x00000000</span></span>                                 |
| <span data-ttu-id="a3d49-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-220">System-Flags</span></span>           | <span data-ttu-id="a3d49-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3d49-221">0x00000010</span></span>                                 |
| <span data-ttu-id="a3d49-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3d49-222">Classes used in</span></span>        | [<span data-ttu-id="a3d49-223">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a3d49-223">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a3d49-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3d49-224">Windows Server 2008</span></span>



| <span data-ttu-id="a3d49-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3d49-225">Entry</span></span> | <span data-ttu-id="a3d49-226">Value</span><span class="sxs-lookup"><span data-stu-id="a3d49-226">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a3d49-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3d49-227">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3d49-228">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3d49-229">System-Only</span></span>            | <span data-ttu-id="a3d49-230">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-230">False</span></span>                                      |
| <span data-ttu-id="a3d49-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3d49-231">Is-Single-Valued</span></span>       | <span data-ttu-id="a3d49-232">True</span><span class="sxs-lookup"><span data-stu-id="a3d49-232">True</span></span>                                       |
| <span data-ttu-id="a3d49-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3d49-233">Is Indexed</span></span>             | <span data-ttu-id="a3d49-234">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-234">False</span></span>                                      |
| <span data-ttu-id="a3d49-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3d49-235">In Global Catalog</span></span>      | <span data-ttu-id="a3d49-236">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-236">False</span></span>                                      |
| <span data-ttu-id="a3d49-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3d49-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3d49-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3d49-238">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a3d49-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3d49-239">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3d49-240">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-241">Search-Flags</span></span>           | <span data-ttu-id="a3d49-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3d49-242">0x00000000</span></span>                                 |
| <span data-ttu-id="a3d49-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-243">System-Flags</span></span>           | <span data-ttu-id="a3d49-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3d49-244">0x00000010</span></span>                                 |
| <span data-ttu-id="a3d49-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3d49-245">Classes used in</span></span>        | [<span data-ttu-id="a3d49-246">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a3d49-246">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a3d49-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3d49-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a3d49-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3d49-248">Entry</span></span> | <span data-ttu-id="a3d49-249">Value</span><span class="sxs-lookup"><span data-stu-id="a3d49-249">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a3d49-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3d49-250">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3d49-251">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3d49-252">System-Only</span></span>            | <span data-ttu-id="a3d49-253">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-253">False</span></span>                                      |
| <span data-ttu-id="a3d49-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3d49-254">Is-Single-Valued</span></span>       | <span data-ttu-id="a3d49-255">True</span><span class="sxs-lookup"><span data-stu-id="a3d49-255">True</span></span>                                       |
| <span data-ttu-id="a3d49-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3d49-256">Is Indexed</span></span>             | <span data-ttu-id="a3d49-257">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-257">False</span></span>                                      |
| <span data-ttu-id="a3d49-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3d49-258">In Global Catalog</span></span>      | <span data-ttu-id="a3d49-259">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-259">False</span></span>                                      |
| <span data-ttu-id="a3d49-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3d49-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3d49-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3d49-261">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a3d49-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3d49-262">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3d49-263">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-264">Search-Flags</span></span>           | <span data-ttu-id="a3d49-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3d49-265">0x00000000</span></span>                                 |
| <span data-ttu-id="a3d49-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-266">System-Flags</span></span>           | <span data-ttu-id="a3d49-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3d49-267">0x00000010</span></span>                                 |
| <span data-ttu-id="a3d49-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3d49-268">Classes used in</span></span>        | [<span data-ttu-id="a3d49-269">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a3d49-269">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a3d49-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3d49-270">Windows Server 2012</span></span>



| <span data-ttu-id="a3d49-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3d49-271">Entry</span></span> | <span data-ttu-id="a3d49-272">Value</span><span class="sxs-lookup"><span data-stu-id="a3d49-272">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a3d49-273">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3d49-273">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3d49-274">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a3d49-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3d49-275">System-Only</span></span>            | <span data-ttu-id="a3d49-276">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-276">False</span></span>                                      |
| <span data-ttu-id="a3d49-277">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3d49-277">Is-Single-Valued</span></span>       | <span data-ttu-id="a3d49-278">True</span><span class="sxs-lookup"><span data-stu-id="a3d49-278">True</span></span>                                       |
| <span data-ttu-id="a3d49-279">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3d49-279">Is Indexed</span></span>             | <span data-ttu-id="a3d49-280">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-280">False</span></span>                                      |
| <span data-ttu-id="a3d49-281">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3d49-281">In Global Catalog</span></span>      | <span data-ttu-id="a3d49-282">False</span><span class="sxs-lookup"><span data-stu-id="a3d49-282">False</span></span>                                      |
| <span data-ttu-id="a3d49-283">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3d49-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3d49-284">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3d49-284">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a3d49-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3d49-285">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3d49-286">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a3d49-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-287">Search-Flags</span></span>           | <span data-ttu-id="a3d49-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3d49-288">0x00000000</span></span>                                 |
| <span data-ttu-id="a3d49-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3d49-289">System-Flags</span></span>           | <span data-ttu-id="a3d49-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3d49-290">0x00000010</span></span>                                 |
| <span data-ttu-id="a3d49-291">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3d49-291">Classes used in</span></span>        | [<span data-ttu-id="a3d49-292">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a3d49-292">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





