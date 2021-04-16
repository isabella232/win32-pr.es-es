---
title: Token-Groups atributo)
description: Un atributo calculado que contiene la lista de SID debido a una operación de expansión de pertenencia a grupos transitiva en un usuario o equipo determinado. No se pueden recuperar grupos de tokens si no hay ningún catálogo global presente para recuperar las pertenencias inversas transitivas.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Token-Groups
- tokenGroups esquema de AD de atributos
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5342d1ff2bf549796340532b0514d5c5b060c2c1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658727"
---
# <a name="token-groups-attribute"></a><span data-ttu-id="18716-106">Token-Groups atributo)</span><span class="sxs-lookup"><span data-stu-id="18716-106">Token-Groups attribute</span></span>

<span data-ttu-id="18716-107">Un atributo calculado que contiene la lista de SID debido a una operación de expansión de pertenencia a grupos transitiva en un usuario o equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="18716-107">A computed attribute that contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="18716-108">No se pueden recuperar grupos de tokens si no hay ningún catálogo global presente para recuperar las pertenencias inversas transitivas.</span><span class="sxs-lookup"><span data-stu-id="18716-108">Token Groups cannot be retrieved if no Global Catalog is present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="18716-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="18716-109">Entry</span></span> | <span data-ttu-id="18716-110">Value</span><span class="sxs-lookup"><span data-stu-id="18716-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="18716-111">CN</span><span class="sxs-lookup"><span data-stu-id="18716-111">CN</span></span>                | <span data-ttu-id="18716-112">Token-Groups</span><span class="sxs-lookup"><span data-stu-id="18716-112">Token-Groups</span></span>                         |
| <span data-ttu-id="18716-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="18716-113">Ldap-Display-Name</span></span> | <span data-ttu-id="18716-114">tokenGroups</span><span class="sxs-lookup"><span data-stu-id="18716-114">tokenGroups</span></span>                          |
| <span data-ttu-id="18716-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="18716-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="18716-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="18716-116">Update Privilege</span></span>  | <span data-ttu-id="18716-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="18716-117">This value is set by the system.</span></span>     |
| <span data-ttu-id="18716-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="18716-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="18716-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18716-119">Attribute-Id</span></span>      | <span data-ttu-id="18716-120">1.2.840.113556.1.4.1301</span><span class="sxs-lookup"><span data-stu-id="18716-120">1.2.840.113556.1.4.1301</span></span>              |
| <span data-ttu-id="18716-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="18716-121">System-Id-Guid</span></span>    | <span data-ttu-id="18716-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="18716-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="18716-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18716-123">Syntax</span></span>            | [<span data-ttu-id="18716-124">**Cadena (SID)**</span><span class="sxs-lookup"><span data-stu-id="18716-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="18716-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="18716-125">Implementations</span></span>

-   [<span data-ttu-id="18716-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="18716-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="18716-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="18716-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="18716-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="18716-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="18716-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="18716-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="18716-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18716-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18716-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18716-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18716-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18716-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="18716-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="18716-133">Windows 2000 Server</span></span>



| <span data-ttu-id="18716-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="18716-134">Entry</span></span> | <span data-ttu-id="18716-135">Value</span><span class="sxs-lookup"><span data-stu-id="18716-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="18716-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="18716-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18716-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="18716-138">System-Only</span></span>            | <span data-ttu-id="18716-139">False</span><span class="sxs-lookup"><span data-stu-id="18716-139">False</span></span>                                                        |
| <span data-ttu-id="18716-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="18716-140">Is-Single-Valued</span></span>       | <span data-ttu-id="18716-141">False</span><span class="sxs-lookup"><span data-stu-id="18716-141">False</span></span>                                                        |
| <span data-ttu-id="18716-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="18716-142">Is Indexed</span></span>             | <span data-ttu-id="18716-143">False</span><span class="sxs-lookup"><span data-stu-id="18716-143">False</span></span>                                                        |
| <span data-ttu-id="18716-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="18716-144">In Global Catalog</span></span>      | <span data-ttu-id="18716-145">False</span><span class="sxs-lookup"><span data-stu-id="18716-145">False</span></span>                                                        |
| <span data-ttu-id="18716-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="18716-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="18716-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18716-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="18716-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18716-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="18716-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18716-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="18716-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-150">Search-Flags</span></span>           | <span data-ttu-id="18716-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18716-151">0x00000000</span></span>                                                   |
| <span data-ttu-id="18716-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-152">System-Flags</span></span>           | <span data-ttu-id="18716-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="18716-153">0x08000014</span></span>                                                   |
| <span data-ttu-id="18716-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="18716-154">Classes used in</span></span>        | [<span data-ttu-id="18716-155">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="18716-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="18716-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18716-156">Windows Server 2003</span></span>



| <span data-ttu-id="18716-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="18716-157">Entry</span></span> | <span data-ttu-id="18716-158">Value</span><span class="sxs-lookup"><span data-stu-id="18716-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="18716-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="18716-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18716-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="18716-161">System-Only</span></span>            | <span data-ttu-id="18716-162">False</span><span class="sxs-lookup"><span data-stu-id="18716-162">False</span></span>                                                        |
| <span data-ttu-id="18716-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="18716-163">Is-Single-Valued</span></span>       | <span data-ttu-id="18716-164">False</span><span class="sxs-lookup"><span data-stu-id="18716-164">False</span></span>                                                        |
| <span data-ttu-id="18716-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="18716-165">Is Indexed</span></span>             | <span data-ttu-id="18716-166">False</span><span class="sxs-lookup"><span data-stu-id="18716-166">False</span></span>                                                        |
| <span data-ttu-id="18716-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="18716-167">In Global Catalog</span></span>      | <span data-ttu-id="18716-168">False</span><span class="sxs-lookup"><span data-stu-id="18716-168">False</span></span>                                                        |
| <span data-ttu-id="18716-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="18716-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="18716-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18716-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="18716-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18716-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="18716-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18716-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="18716-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-173">Search-Flags</span></span>           | <span data-ttu-id="18716-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18716-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="18716-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-175">System-Flags</span></span>           | <span data-ttu-id="18716-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="18716-176">0x08000014</span></span>                                                   |
| <span data-ttu-id="18716-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="18716-177">Classes used in</span></span>        | [<span data-ttu-id="18716-178">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="18716-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="18716-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="18716-179">ADAM</span></span>



| <span data-ttu-id="18716-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="18716-180">Entry</span></span> | <span data-ttu-id="18716-181">Value</span><span class="sxs-lookup"><span data-stu-id="18716-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="18716-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="18716-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18716-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="18716-184">System-Only</span></span>            | <span data-ttu-id="18716-185">False</span><span class="sxs-lookup"><span data-stu-id="18716-185">False</span></span>                                                        |
| <span data-ttu-id="18716-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="18716-186">Is-Single-Valued</span></span>       | <span data-ttu-id="18716-187">False</span><span class="sxs-lookup"><span data-stu-id="18716-187">False</span></span>                                                        |
| <span data-ttu-id="18716-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="18716-188">Is Indexed</span></span>             | <span data-ttu-id="18716-189">False</span><span class="sxs-lookup"><span data-stu-id="18716-189">False</span></span>                                                        |
| <span data-ttu-id="18716-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="18716-190">In Global Catalog</span></span>      | <span data-ttu-id="18716-191">False</span><span class="sxs-lookup"><span data-stu-id="18716-191">False</span></span>                                                        |
| <span data-ttu-id="18716-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="18716-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="18716-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18716-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="18716-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18716-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="18716-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18716-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="18716-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-196">Search-Flags</span></span>           | <span data-ttu-id="18716-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18716-197">0x00000000</span></span>                                                   |
| <span data-ttu-id="18716-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-198">System-Flags</span></span>           | <span data-ttu-id="18716-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="18716-199">0x08000014</span></span>                                                   |
| <span data-ttu-id="18716-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="18716-200">Classes used in</span></span>        | [<span data-ttu-id="18716-201">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="18716-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="18716-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="18716-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="18716-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="18716-203">Entry</span></span> | <span data-ttu-id="18716-204">Value</span><span class="sxs-lookup"><span data-stu-id="18716-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="18716-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="18716-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18716-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="18716-207">System-Only</span></span>            | <span data-ttu-id="18716-208">False</span><span class="sxs-lookup"><span data-stu-id="18716-208">False</span></span>                                                        |
| <span data-ttu-id="18716-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="18716-209">Is-Single-Valued</span></span>       | <span data-ttu-id="18716-210">False</span><span class="sxs-lookup"><span data-stu-id="18716-210">False</span></span>                                                        |
| <span data-ttu-id="18716-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="18716-211">Is Indexed</span></span>             | <span data-ttu-id="18716-212">False</span><span class="sxs-lookup"><span data-stu-id="18716-212">False</span></span>                                                        |
| <span data-ttu-id="18716-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="18716-213">In Global Catalog</span></span>      | <span data-ttu-id="18716-214">False</span><span class="sxs-lookup"><span data-stu-id="18716-214">False</span></span>                                                        |
| <span data-ttu-id="18716-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="18716-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="18716-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18716-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="18716-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18716-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="18716-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18716-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="18716-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-219">Search-Flags</span></span>           | <span data-ttu-id="18716-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18716-220">0x00000000</span></span>                                                   |
| <span data-ttu-id="18716-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-221">System-Flags</span></span>           | <span data-ttu-id="18716-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="18716-222">0x08000014</span></span>                                                   |
| <span data-ttu-id="18716-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="18716-223">Classes used in</span></span>        | [<span data-ttu-id="18716-224">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="18716-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="18716-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18716-225">Windows Server 2008</span></span>



| <span data-ttu-id="18716-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="18716-226">Entry</span></span> | <span data-ttu-id="18716-227">Value</span><span class="sxs-lookup"><span data-stu-id="18716-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="18716-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="18716-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18716-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="18716-230">System-Only</span></span>            | <span data-ttu-id="18716-231">False</span><span class="sxs-lookup"><span data-stu-id="18716-231">False</span></span>                                                        |
| <span data-ttu-id="18716-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="18716-232">Is-Single-Valued</span></span>       | <span data-ttu-id="18716-233">False</span><span class="sxs-lookup"><span data-stu-id="18716-233">False</span></span>                                                        |
| <span data-ttu-id="18716-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="18716-234">Is Indexed</span></span>             | <span data-ttu-id="18716-235">False</span><span class="sxs-lookup"><span data-stu-id="18716-235">False</span></span>                                                        |
| <span data-ttu-id="18716-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="18716-236">In Global Catalog</span></span>      | <span data-ttu-id="18716-237">False</span><span class="sxs-lookup"><span data-stu-id="18716-237">False</span></span>                                                        |
| <span data-ttu-id="18716-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="18716-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="18716-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18716-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="18716-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18716-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="18716-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18716-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="18716-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-242">Search-Flags</span></span>           | <span data-ttu-id="18716-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18716-243">0x00000000</span></span>                                                   |
| <span data-ttu-id="18716-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-244">System-Flags</span></span>           | <span data-ttu-id="18716-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="18716-245">0x08000014</span></span>                                                   |
| <span data-ttu-id="18716-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="18716-246">Classes used in</span></span>        | [<span data-ttu-id="18716-247">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="18716-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18716-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18716-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18716-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="18716-249">Entry</span></span> | <span data-ttu-id="18716-250">Value</span><span class="sxs-lookup"><span data-stu-id="18716-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="18716-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="18716-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18716-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="18716-253">System-Only</span></span>            | <span data-ttu-id="18716-254">False</span><span class="sxs-lookup"><span data-stu-id="18716-254">False</span></span>                                                        |
| <span data-ttu-id="18716-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="18716-255">Is-Single-Valued</span></span>       | <span data-ttu-id="18716-256">False</span><span class="sxs-lookup"><span data-stu-id="18716-256">False</span></span>                                                        |
| <span data-ttu-id="18716-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="18716-257">Is Indexed</span></span>             | <span data-ttu-id="18716-258">False</span><span class="sxs-lookup"><span data-stu-id="18716-258">False</span></span>                                                        |
| <span data-ttu-id="18716-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="18716-259">In Global Catalog</span></span>      | <span data-ttu-id="18716-260">False</span><span class="sxs-lookup"><span data-stu-id="18716-260">False</span></span>                                                        |
| <span data-ttu-id="18716-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="18716-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="18716-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18716-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="18716-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18716-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="18716-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18716-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="18716-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-265">Search-Flags</span></span>           | <span data-ttu-id="18716-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18716-266">0x00000000</span></span>                                                   |
| <span data-ttu-id="18716-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-267">System-Flags</span></span>           | <span data-ttu-id="18716-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="18716-268">0x08000014</span></span>                                                   |
| <span data-ttu-id="18716-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="18716-269">Classes used in</span></span>        | [<span data-ttu-id="18716-270">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="18716-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18716-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18716-271">Windows Server 2012</span></span>



| <span data-ttu-id="18716-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="18716-272">Entry</span></span> | <span data-ttu-id="18716-273">Value</span><span class="sxs-lookup"><span data-stu-id="18716-273">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="18716-274">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="18716-274">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18716-275">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="18716-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="18716-276">System-Only</span></span>            | <span data-ttu-id="18716-277">False</span><span class="sxs-lookup"><span data-stu-id="18716-277">False</span></span>                                                        |
| <span data-ttu-id="18716-278">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="18716-278">Is-Single-Valued</span></span>       | <span data-ttu-id="18716-279">False</span><span class="sxs-lookup"><span data-stu-id="18716-279">False</span></span>                                                        |
| <span data-ttu-id="18716-280">Está indexado</span><span class="sxs-lookup"><span data-stu-id="18716-280">Is Indexed</span></span>             | <span data-ttu-id="18716-281">False</span><span class="sxs-lookup"><span data-stu-id="18716-281">False</span></span>                                                        |
| <span data-ttu-id="18716-282">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="18716-282">In Global Catalog</span></span>      | <span data-ttu-id="18716-283">False</span><span class="sxs-lookup"><span data-stu-id="18716-283">False</span></span>                                                        |
| <span data-ttu-id="18716-284">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="18716-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="18716-285">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18716-285">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="18716-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18716-286">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="18716-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18716-287">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="18716-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-288">Search-Flags</span></span>           | <span data-ttu-id="18716-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18716-289">0x00000000</span></span>                                                   |
| <span data-ttu-id="18716-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18716-290">System-Flags</span></span>           | <span data-ttu-id="18716-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="18716-291">0x08000014</span></span>                                                   |
| <span data-ttu-id="18716-292">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="18716-292">Classes used in</span></span>        | [<span data-ttu-id="18716-293">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="18716-293">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





