---
title: atributo MS-DS-allowed-to-Delegate
description: Se trata de un atributo de objetos de cuenta de servicio (equipo o cuenta de usuario).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-allowed-to-Delegate
- Esquema de AD de atributo msDS-AllowedToDelegateTo
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9562442d20053848e48cd2b1d501e65611f7d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658901"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a><span data-ttu-id="a54fe-105">atributo MS-DS-allowed-to-Delegate</span><span class="sxs-lookup"><span data-stu-id="a54fe-105">ms-DS-Allowed-To-Delegate-To attribute</span></span>

<span data-ttu-id="a54fe-106">Se trata de un atributo de objetos de cuenta de servicio (equipo o cuenta de usuario).</span><span class="sxs-lookup"><span data-stu-id="a54fe-106">This is an attribute on service account (computer or user account) objects.</span></span> <span data-ttu-id="a54fe-107">Contiene una lista de nombres de entidad de seguridad de servicio (SPN).</span><span class="sxs-lookup"><span data-stu-id="a54fe-107">It contains a list of Service Principal Names (SPNs).</span></span> <span data-ttu-id="a54fe-108">Este atributo se utiliza para configurar un servicio de modo que pueda obtener vales de servicio que se pueden usar para la delegación restringida.</span><span class="sxs-lookup"><span data-stu-id="a54fe-108">This attribute is used to configure a service so that it can obtain service tickets that can be used for Constrained Delegation.</span></span>



| <span data-ttu-id="a54fe-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a54fe-109">Entry</span></span> | <span data-ttu-id="a54fe-110">Value</span><span class="sxs-lookup"><span data-stu-id="a54fe-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a54fe-111">CN</span><span class="sxs-lookup"><span data-stu-id="a54fe-111">CN</span></span>                | <span data-ttu-id="a54fe-112">MS-DS-permitido a delegado a</span><span class="sxs-lookup"><span data-stu-id="a54fe-112">ms-DS-Allowed-To-Delegate-To</span></span>                |
| <span data-ttu-id="a54fe-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a54fe-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a54fe-114">msDS-AllowedToDelegateTo</span><span class="sxs-lookup"><span data-stu-id="a54fe-114">msDS-AllowedToDelegateTo</span></span>                    |
| <span data-ttu-id="a54fe-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a54fe-115">Size</span></span>              | <span data-ttu-id="a54fe-116">de 0 a 64 k</span><span class="sxs-lookup"><span data-stu-id="a54fe-116">0 to 64K</span></span>                                    |
| <span data-ttu-id="a54fe-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a54fe-117">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="a54fe-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a54fe-118">Update Frequency</span></span>  | <span data-ttu-id="a54fe-119">Con poca frecuencia</span><span class="sxs-lookup"><span data-stu-id="a54fe-119">Infrequently</span></span>                                |
| <span data-ttu-id="a54fe-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a54fe-120">Attribute-Id</span></span>      | <span data-ttu-id="a54fe-121">1.2.840.113556.1.4.1787</span><span class="sxs-lookup"><span data-stu-id="a54fe-121">1.2.840.113556.1.4.1787</span></span>                     |
| <span data-ttu-id="a54fe-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a54fe-122">System-Id-Guid</span></span>    | <span data-ttu-id="a54fe-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span><span class="sxs-lookup"><span data-stu-id="a54fe-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span></span>        |
| <span data-ttu-id="a54fe-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a54fe-124">Syntax</span></span>            | [<span data-ttu-id="a54fe-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a54fe-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a54fe-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a54fe-126">Implementations</span></span>

-   [<span data-ttu-id="a54fe-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a54fe-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a54fe-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a54fe-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a54fe-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a54fe-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a54fe-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a54fe-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a54fe-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a54fe-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a54fe-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a54fe-132">Windows Server 2003</span></span>



| <span data-ttu-id="a54fe-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="a54fe-133">Entry</span></span> | <span data-ttu-id="a54fe-134">Value</span><span class="sxs-lookup"><span data-stu-id="a54fe-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a54fe-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a54fe-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a54fe-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a54fe-136">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a54fe-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a54fe-137">System-Only</span></span>            | <span data-ttu-id="a54fe-138">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-138">False</span></span>                                                              |
| <span data-ttu-id="a54fe-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a54fe-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a54fe-140">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-140">False</span></span>                                                              |
| <span data-ttu-id="a54fe-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a54fe-141">Is Indexed</span></span>             | <span data-ttu-id="a54fe-142">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-142">False</span></span>                                                              |
| <span data-ttu-id="a54fe-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a54fe-143">In Global Catalog</span></span>      | <span data-ttu-id="a54fe-144">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-144">False</span></span>                                                              |
| <span data-ttu-id="a54fe-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a54fe-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a54fe-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a54fe-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a54fe-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a54fe-147">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a54fe-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a54fe-148">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a54fe-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a54fe-149">Search-Flags</span></span>           | <span data-ttu-id="a54fe-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a54fe-150">0x00000000</span></span>                                                         |
| <span data-ttu-id="a54fe-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a54fe-151">System-Flags</span></span>           | <span data-ttu-id="a54fe-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a54fe-152">0x00000010</span></span>                                                         |
| <span data-ttu-id="a54fe-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a54fe-153">Classes used in</span></span>        | [<span data-ttu-id="a54fe-154">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="a54fe-154">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a54fe-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a54fe-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a54fe-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="a54fe-156">Entry</span></span> | <span data-ttu-id="a54fe-157">Value</span><span class="sxs-lookup"><span data-stu-id="a54fe-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a54fe-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a54fe-158">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a54fe-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a54fe-159">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a54fe-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="a54fe-160">System-Only</span></span>            | <span data-ttu-id="a54fe-161">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-161">False</span></span>                                                              |
| <span data-ttu-id="a54fe-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a54fe-162">Is-Single-Valued</span></span>       | <span data-ttu-id="a54fe-163">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-163">False</span></span>                                                              |
| <span data-ttu-id="a54fe-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a54fe-164">Is Indexed</span></span>             | <span data-ttu-id="a54fe-165">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-165">False</span></span>                                                              |
| <span data-ttu-id="a54fe-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a54fe-166">In Global Catalog</span></span>      | <span data-ttu-id="a54fe-167">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-167">False</span></span>                                                              |
| <span data-ttu-id="a54fe-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a54fe-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="a54fe-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a54fe-169">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a54fe-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a54fe-170">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a54fe-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a54fe-171">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a54fe-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a54fe-172">Search-Flags</span></span>           | <span data-ttu-id="a54fe-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a54fe-173">0x00000000</span></span>                                                         |
| <span data-ttu-id="a54fe-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a54fe-174">System-Flags</span></span>           | <span data-ttu-id="a54fe-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a54fe-175">0x00000010</span></span>                                                         |
| <span data-ttu-id="a54fe-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a54fe-176">Classes used in</span></span>        | [<span data-ttu-id="a54fe-177">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="a54fe-177">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a54fe-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a54fe-178">Windows Server 2008</span></span>



| <span data-ttu-id="a54fe-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="a54fe-179">Entry</span></span> | <span data-ttu-id="a54fe-180">Value</span><span class="sxs-lookup"><span data-stu-id="a54fe-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a54fe-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a54fe-181">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a54fe-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a54fe-182">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a54fe-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a54fe-183">System-Only</span></span>            | <span data-ttu-id="a54fe-184">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-184">False</span></span>                                                              |
| <span data-ttu-id="a54fe-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a54fe-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a54fe-186">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-186">False</span></span>                                                              |
| <span data-ttu-id="a54fe-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a54fe-187">Is Indexed</span></span>             | <span data-ttu-id="a54fe-188">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-188">False</span></span>                                                              |
| <span data-ttu-id="a54fe-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a54fe-189">In Global Catalog</span></span>      | <span data-ttu-id="a54fe-190">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-190">False</span></span>                                                              |
| <span data-ttu-id="a54fe-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a54fe-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a54fe-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a54fe-192">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a54fe-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a54fe-193">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a54fe-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a54fe-194">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a54fe-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a54fe-195">Search-Flags</span></span>           | <span data-ttu-id="a54fe-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a54fe-196">0x00000000</span></span>                                                         |
| <span data-ttu-id="a54fe-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a54fe-197">System-Flags</span></span>           | <span data-ttu-id="a54fe-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a54fe-198">0x00000010</span></span>                                                         |
| <span data-ttu-id="a54fe-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a54fe-199">Classes used in</span></span>        | [<span data-ttu-id="a54fe-200">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="a54fe-200">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a54fe-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a54fe-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a54fe-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="a54fe-202">Entry</span></span> | <span data-ttu-id="a54fe-203">Value</span><span class="sxs-lookup"><span data-stu-id="a54fe-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a54fe-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a54fe-204">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a54fe-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a54fe-205">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a54fe-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a54fe-206">System-Only</span></span>            | <span data-ttu-id="a54fe-207">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-207">False</span></span>                                                              |
| <span data-ttu-id="a54fe-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a54fe-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a54fe-209">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-209">False</span></span>                                                              |
| <span data-ttu-id="a54fe-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a54fe-210">Is Indexed</span></span>             | <span data-ttu-id="a54fe-211">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-211">False</span></span>                                                              |
| <span data-ttu-id="a54fe-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a54fe-212">In Global Catalog</span></span>      | <span data-ttu-id="a54fe-213">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-213">False</span></span>                                                              |
| <span data-ttu-id="a54fe-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a54fe-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a54fe-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a54fe-215">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a54fe-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a54fe-216">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a54fe-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a54fe-217">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a54fe-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a54fe-218">Search-Flags</span></span>           | <span data-ttu-id="a54fe-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a54fe-219">0x00000000</span></span>                                                         |
| <span data-ttu-id="a54fe-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a54fe-220">System-Flags</span></span>           | <span data-ttu-id="a54fe-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a54fe-221">0x00000010</span></span>                                                         |
| <span data-ttu-id="a54fe-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a54fe-222">Classes used in</span></span>        | [<span data-ttu-id="a54fe-223">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="a54fe-223">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a54fe-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a54fe-224">Windows Server 2012</span></span>



| <span data-ttu-id="a54fe-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="a54fe-225">Entry</span></span> | <span data-ttu-id="a54fe-226">Value</span><span class="sxs-lookup"><span data-stu-id="a54fe-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a54fe-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a54fe-227">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a54fe-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a54fe-228">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a54fe-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="a54fe-229">System-Only</span></span>            | <span data-ttu-id="a54fe-230">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-230">False</span></span>                                                              |
| <span data-ttu-id="a54fe-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a54fe-231">Is-Single-Valued</span></span>       | <span data-ttu-id="a54fe-232">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-232">False</span></span>                                                              |
| <span data-ttu-id="a54fe-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a54fe-233">Is Indexed</span></span>             | <span data-ttu-id="a54fe-234">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-234">False</span></span>                                                              |
| <span data-ttu-id="a54fe-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a54fe-235">In Global Catalog</span></span>      | <span data-ttu-id="a54fe-236">False</span><span class="sxs-lookup"><span data-stu-id="a54fe-236">False</span></span>                                                              |
| <span data-ttu-id="a54fe-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a54fe-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="a54fe-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a54fe-238">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a54fe-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a54fe-239">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a54fe-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a54fe-240">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a54fe-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a54fe-241">Search-Flags</span></span>           | <span data-ttu-id="a54fe-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a54fe-242">0x00000000</span></span>                                                         |
| <span data-ttu-id="a54fe-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a54fe-243">System-Flags</span></span>           | <span data-ttu-id="a54fe-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a54fe-244">0x00000010</span></span>                                                         |
| <span data-ttu-id="a54fe-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a54fe-245">Classes used in</span></span>        | [<span data-ttu-id="a54fe-246">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="a54fe-246">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





