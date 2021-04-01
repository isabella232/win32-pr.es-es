---
title: Atributo FSMO-role-Owner
description: Operación flexible de Single-Master el nombre distintivo del controlador de dominio en el que se puede modificar el esquema.
ms.assetid: 8eb28524-4bbf-453c-89ab-864ef94b0781
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos FSMO-role-Owner
- Esquema de AD de atributos de fSMORoleOwner
topic_type:
- apiref
api_name:
- FSMO-Role-Owner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d4439e5ee10fba11db831024d6b1958b75cd81
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906086"
---
# <a name="fsmo-role-owner-attribute"></a><span data-ttu-id="1d945-105">Atributo FSMO-role-Owner</span><span class="sxs-lookup"><span data-stu-id="1d945-105">FSMO-Role-Owner attribute</span></span>

<span data-ttu-id="1d945-106">Operación de Single-Master flexible: nombre distintivo del controlador de dominio en el que se puede modificar el esquema.</span><span class="sxs-lookup"><span data-stu-id="1d945-106">Flexible Single-Master Operation: The distinguished name of the DC where the schema can be modified.</span></span>



| <span data-ttu-id="1d945-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d945-107">Entry</span></span> | <span data-ttu-id="1d945-108">Value</span><span class="sxs-lookup"><span data-stu-id="1d945-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="1d945-109">CN</span><span class="sxs-lookup"><span data-stu-id="1d945-109">CN</span></span>                | <span data-ttu-id="1d945-110">FSMO: rol-Propietario</span><span class="sxs-lookup"><span data-stu-id="1d945-110">FSMO-Role-Owner</span></span>                         |
| <span data-ttu-id="1d945-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1d945-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1d945-112">fSMORoleOwner</span><span class="sxs-lookup"><span data-stu-id="1d945-112">fSMORoleOwner</span></span>                           |
| <span data-ttu-id="1d945-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1d945-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="1d945-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1d945-114">Update Privilege</span></span>  | <span data-ttu-id="1d945-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="1d945-115">Schema administrator</span></span>                    |
| <span data-ttu-id="1d945-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1d945-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="1d945-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1d945-117">Attribute-Id</span></span>      | <span data-ttu-id="1d945-118">1.2.840.113556.1.4.369</span><span class="sxs-lookup"><span data-stu-id="1d945-118">1.2.840.113556.1.4.369</span></span>                  |
| <span data-ttu-id="1d945-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1d945-119">System-Id-Guid</span></span>    | <span data-ttu-id="1d945-120">66171887-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="1d945-120">66171887-8f3c-11d0-afda-00c04fd930c9</span></span>    |
| <span data-ttu-id="1d945-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d945-121">Syntax</span></span>            | [<span data-ttu-id="1d945-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1d945-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="1d945-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1d945-123">Implementations</span></span>

-   [<span data-ttu-id="1d945-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1d945-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1d945-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1d945-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1d945-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1d945-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1d945-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1d945-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1d945-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1d945-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1d945-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1d945-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1d945-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1d945-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1d945-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d945-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1d945-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d945-132">Entry</span></span> | <span data-ttu-id="1d945-133">Value</span><span class="sxs-lookup"><span data-stu-id="1d945-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d945-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d945-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d945-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d945-136">System-Only</span></span>            | <span data-ttu-id="1d945-137">False</span><span class="sxs-lookup"><span data-stu-id="1d945-137">False</span></span>                           |
| <span data-ttu-id="1d945-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d945-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1d945-139">True</span><span class="sxs-lookup"><span data-stu-id="1d945-139">True</span></span>                            |
| <span data-ttu-id="1d945-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d945-140">Is Indexed</span></span>             | <span data-ttu-id="1d945-141">True</span><span class="sxs-lookup"><span data-stu-id="1d945-141">True</span></span>                            |
| <span data-ttu-id="1d945-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d945-142">In Global Catalog</span></span>      | <span data-ttu-id="1d945-143">False</span><span class="sxs-lookup"><span data-stu-id="1d945-143">False</span></span>                           |
| <span data-ttu-id="1d945-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d945-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d945-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d945-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d945-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d945-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d945-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d945-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d945-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-148">Search-Flags</span></span>           | <span data-ttu-id="1d945-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1d945-149">0x00000001</span></span>                      |
| <span data-ttu-id="1d945-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-150">System-Flags</span></span>           | <span data-ttu-id="1d945-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d945-151">0x00000010</span></span>                      |
| <span data-ttu-id="1d945-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d945-152">Classes used in</span></span>        | [<span data-ttu-id="1d945-153">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1d945-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1d945-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1d945-154">Windows Server 2003</span></span>



| <span data-ttu-id="1d945-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d945-155">Entry</span></span> | <span data-ttu-id="1d945-156">Value</span><span class="sxs-lookup"><span data-stu-id="1d945-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d945-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d945-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d945-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d945-159">System-Only</span></span>            | <span data-ttu-id="1d945-160">False</span><span class="sxs-lookup"><span data-stu-id="1d945-160">False</span></span>                           |
| <span data-ttu-id="1d945-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d945-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1d945-162">True</span><span class="sxs-lookup"><span data-stu-id="1d945-162">True</span></span>                            |
| <span data-ttu-id="1d945-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d945-163">Is Indexed</span></span>             | <span data-ttu-id="1d945-164">True</span><span class="sxs-lookup"><span data-stu-id="1d945-164">True</span></span>                            |
| <span data-ttu-id="1d945-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d945-165">In Global Catalog</span></span>      | <span data-ttu-id="1d945-166">False</span><span class="sxs-lookup"><span data-stu-id="1d945-166">False</span></span>                           |
| <span data-ttu-id="1d945-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d945-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d945-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d945-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d945-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d945-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d945-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d945-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d945-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-171">Search-Flags</span></span>           | <span data-ttu-id="1d945-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1d945-172">0x00000001</span></span>                      |
| <span data-ttu-id="1d945-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-173">System-Flags</span></span>           | <span data-ttu-id="1d945-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d945-174">0x00000010</span></span>                      |
| <span data-ttu-id="1d945-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d945-175">Classes used in</span></span>        | [<span data-ttu-id="1d945-176">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1d945-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1d945-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="1d945-177">ADAM</span></span>



| <span data-ttu-id="1d945-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d945-178">Entry</span></span> | <span data-ttu-id="1d945-179">Value</span><span class="sxs-lookup"><span data-stu-id="1d945-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d945-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d945-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d945-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d945-182">System-Only</span></span>            | <span data-ttu-id="1d945-183">False</span><span class="sxs-lookup"><span data-stu-id="1d945-183">False</span></span>                           |
| <span data-ttu-id="1d945-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d945-184">Is-Single-Valued</span></span>       | <span data-ttu-id="1d945-185">True</span><span class="sxs-lookup"><span data-stu-id="1d945-185">True</span></span>                            |
| <span data-ttu-id="1d945-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d945-186">Is Indexed</span></span>             | <span data-ttu-id="1d945-187">True</span><span class="sxs-lookup"><span data-stu-id="1d945-187">True</span></span>                            |
| <span data-ttu-id="1d945-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d945-188">In Global Catalog</span></span>      | <span data-ttu-id="1d945-189">False</span><span class="sxs-lookup"><span data-stu-id="1d945-189">False</span></span>                           |
| <span data-ttu-id="1d945-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d945-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d945-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d945-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d945-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d945-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d945-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d945-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d945-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-194">Search-Flags</span></span>           | <span data-ttu-id="1d945-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1d945-195">0x00000001</span></span>                      |
| <span data-ttu-id="1d945-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-196">System-Flags</span></span>           | <span data-ttu-id="1d945-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d945-197">0x00000010</span></span>                      |
| <span data-ttu-id="1d945-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d945-198">Classes used in</span></span>        | [<span data-ttu-id="1d945-199">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1d945-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1d945-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1d945-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1d945-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d945-201">Entry</span></span> | <span data-ttu-id="1d945-202">Value</span><span class="sxs-lookup"><span data-stu-id="1d945-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d945-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d945-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d945-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d945-205">System-Only</span></span>            | <span data-ttu-id="1d945-206">False</span><span class="sxs-lookup"><span data-stu-id="1d945-206">False</span></span>                           |
| <span data-ttu-id="1d945-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d945-207">Is-Single-Valued</span></span>       | <span data-ttu-id="1d945-208">True</span><span class="sxs-lookup"><span data-stu-id="1d945-208">True</span></span>                            |
| <span data-ttu-id="1d945-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d945-209">Is Indexed</span></span>             | <span data-ttu-id="1d945-210">True</span><span class="sxs-lookup"><span data-stu-id="1d945-210">True</span></span>                            |
| <span data-ttu-id="1d945-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d945-211">In Global Catalog</span></span>      | <span data-ttu-id="1d945-212">False</span><span class="sxs-lookup"><span data-stu-id="1d945-212">False</span></span>                           |
| <span data-ttu-id="1d945-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d945-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d945-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d945-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d945-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d945-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d945-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d945-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d945-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-217">Search-Flags</span></span>           | <span data-ttu-id="1d945-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1d945-218">0x00000001</span></span>                      |
| <span data-ttu-id="1d945-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-219">System-Flags</span></span>           | <span data-ttu-id="1d945-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d945-220">0x00000010</span></span>                      |
| <span data-ttu-id="1d945-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d945-221">Classes used in</span></span>        | [<span data-ttu-id="1d945-222">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1d945-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1d945-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d945-223">Windows Server 2008</span></span>



| <span data-ttu-id="1d945-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d945-224">Entry</span></span> | <span data-ttu-id="1d945-225">Value</span><span class="sxs-lookup"><span data-stu-id="1d945-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d945-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d945-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d945-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d945-228">System-Only</span></span>            | <span data-ttu-id="1d945-229">False</span><span class="sxs-lookup"><span data-stu-id="1d945-229">False</span></span>                           |
| <span data-ttu-id="1d945-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d945-230">Is-Single-Valued</span></span>       | <span data-ttu-id="1d945-231">True</span><span class="sxs-lookup"><span data-stu-id="1d945-231">True</span></span>                            |
| <span data-ttu-id="1d945-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d945-232">Is Indexed</span></span>             | <span data-ttu-id="1d945-233">True</span><span class="sxs-lookup"><span data-stu-id="1d945-233">True</span></span>                            |
| <span data-ttu-id="1d945-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d945-234">In Global Catalog</span></span>      | <span data-ttu-id="1d945-235">False</span><span class="sxs-lookup"><span data-stu-id="1d945-235">False</span></span>                           |
| <span data-ttu-id="1d945-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d945-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d945-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d945-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d945-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d945-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d945-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d945-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d945-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-240">Search-Flags</span></span>           | <span data-ttu-id="1d945-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1d945-241">0x00000001</span></span>                      |
| <span data-ttu-id="1d945-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-242">System-Flags</span></span>           | <span data-ttu-id="1d945-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d945-243">0x00000010</span></span>                      |
| <span data-ttu-id="1d945-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d945-244">Classes used in</span></span>        | [<span data-ttu-id="1d945-245">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1d945-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1d945-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1d945-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1d945-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d945-247">Entry</span></span> | <span data-ttu-id="1d945-248">Value</span><span class="sxs-lookup"><span data-stu-id="1d945-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d945-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d945-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d945-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d945-251">System-Only</span></span>            | <span data-ttu-id="1d945-252">False</span><span class="sxs-lookup"><span data-stu-id="1d945-252">False</span></span>                           |
| <span data-ttu-id="1d945-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d945-253">Is-Single-Valued</span></span>       | <span data-ttu-id="1d945-254">True</span><span class="sxs-lookup"><span data-stu-id="1d945-254">True</span></span>                            |
| <span data-ttu-id="1d945-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d945-255">Is Indexed</span></span>             | <span data-ttu-id="1d945-256">True</span><span class="sxs-lookup"><span data-stu-id="1d945-256">True</span></span>                            |
| <span data-ttu-id="1d945-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d945-257">In Global Catalog</span></span>      | <span data-ttu-id="1d945-258">False</span><span class="sxs-lookup"><span data-stu-id="1d945-258">False</span></span>                           |
| <span data-ttu-id="1d945-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d945-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d945-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d945-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d945-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d945-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d945-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d945-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d945-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-263">Search-Flags</span></span>           | <span data-ttu-id="1d945-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1d945-264">0x00000001</span></span>                      |
| <span data-ttu-id="1d945-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-265">System-Flags</span></span>           | <span data-ttu-id="1d945-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d945-266">0x00000010</span></span>                      |
| <span data-ttu-id="1d945-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d945-267">Classes used in</span></span>        | [<span data-ttu-id="1d945-268">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1d945-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1d945-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d945-269">Windows Server 2012</span></span>



| <span data-ttu-id="1d945-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d945-270">Entry</span></span> | <span data-ttu-id="1d945-271">Value</span><span class="sxs-lookup"><span data-stu-id="1d945-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d945-272">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1d945-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d945-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d945-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d945-274">System-Only</span></span>            | <span data-ttu-id="1d945-275">False</span><span class="sxs-lookup"><span data-stu-id="1d945-275">False</span></span>                           |
| <span data-ttu-id="1d945-276">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1d945-276">Is-Single-Valued</span></span>       | <span data-ttu-id="1d945-277">True</span><span class="sxs-lookup"><span data-stu-id="1d945-277">True</span></span>                            |
| <span data-ttu-id="1d945-278">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1d945-278">Is Indexed</span></span>             | <span data-ttu-id="1d945-279">True</span><span class="sxs-lookup"><span data-stu-id="1d945-279">True</span></span>                            |
| <span data-ttu-id="1d945-280">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d945-280">In Global Catalog</span></span>      | <span data-ttu-id="1d945-281">False</span><span class="sxs-lookup"><span data-stu-id="1d945-281">False</span></span>                           |
| <span data-ttu-id="1d945-282">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1d945-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d945-283">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d945-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d945-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d945-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d945-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d945-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d945-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-286">Search-Flags</span></span>           | <span data-ttu-id="1d945-287">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1d945-287">0x00000001</span></span>                      |
| <span data-ttu-id="1d945-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d945-288">System-Flags</span></span>           | <span data-ttu-id="1d945-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d945-289">0x00000010</span></span>                      |
| <span data-ttu-id="1d945-290">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1d945-290">Classes used in</span></span>        | [<span data-ttu-id="1d945-291">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1d945-291">**Top**</span></span>](c-top.md)<br/> |



 

 





