---
title: Atributo MS-DS-All-Users-Trust-quota
description: Se usa para aplicar una cuota de usuarios combinados en el número total de objetos de Trusted-Domain creados mediante el derecho de acceso de control nuevo, crear-entrada-bosque-confianza.
ms.assetid: 77e70a26-99b4-4b49-a984-6809d02f6fb8
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DS-All-Users-Trust-quota
- Esquema de AD de atributo msDS-AllUsersTrustQuota
topic_type:
- apiref
api_name:
- MS-DS-All-Users-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0538ff38f1eb57f339a8e0e244a378a36dd92498
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805041"
---
# <a name="ms-ds-all-users-trust-quota-attribute"></a><span data-ttu-id="b75d9-105">Atributo MS-DS-All-Users-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="b75d9-105">MS-DS-All-Users-Trust-Quota attribute</span></span>

<span data-ttu-id="b75d9-106">Se usa para aplicar una cuota de usuarios combinados en el número total de objetos de Trusted-Domain creados mediante el derecho de acceso de control nuevo, crear-entrada-bosque-confianza.</span><span class="sxs-lookup"><span data-stu-id="b75d9-106">Used to enforce a combined users quota on the total number of Trusted-Domain objects created by using the new control access right, Create-Inbound-Forest-Trust.</span></span>



| <span data-ttu-id="b75d9-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b75d9-107">Entry</span></span> | <span data-ttu-id="b75d9-108">Value</span><span class="sxs-lookup"><span data-stu-id="b75d9-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="b75d9-109">CN</span><span class="sxs-lookup"><span data-stu-id="b75d9-109">CN</span></span>                | <span data-ttu-id="b75d9-110">MS-DS-All-Users-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="b75d9-110">MS-DS-All-Users-Trust-Quota</span></span>               |
| <span data-ttu-id="b75d9-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b75d9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b75d9-112">msDS-AllUsersTrustQuota</span><span class="sxs-lookup"><span data-stu-id="b75d9-112">msDS-AllUsersTrustQuota</span></span>                   |
| <span data-ttu-id="b75d9-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b75d9-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="b75d9-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b75d9-114">Update Privilege</span></span>  | <span data-ttu-id="b75d9-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="b75d9-115">Domain administrator</span></span>                      |
| <span data-ttu-id="b75d9-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b75d9-116">Update Frequency</span></span>  | <span data-ttu-id="b75d9-117">Al crear el bosque y raramente después.</span><span class="sxs-lookup"><span data-stu-id="b75d9-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="b75d9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b75d9-118">Attribute-Id</span></span>      | <span data-ttu-id="b75d9-119">1.2.840.113556.1.4.1789</span><span class="sxs-lookup"><span data-stu-id="b75d9-119">1.2.840.113556.1.4.1789</span></span>                   |
| <span data-ttu-id="b75d9-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b75d9-120">System-Id-Guid</span></span>    | <span data-ttu-id="b75d9-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span><span class="sxs-lookup"><span data-stu-id="b75d9-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span></span>      |
| <span data-ttu-id="b75d9-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b75d9-122">Syntax</span></span>            | [<span data-ttu-id="b75d9-123">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="b75d9-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="b75d9-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b75d9-124">Implementations</span></span>

-   [<span data-ttu-id="b75d9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b75d9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b75d9-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b75d9-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b75d9-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b75d9-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b75d9-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b75d9-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b75d9-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b75d9-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b75d9-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b75d9-130">Windows Server 2003</span></span>



| <span data-ttu-id="b75d9-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="b75d9-131">Entry</span></span> | <span data-ttu-id="b75d9-132">Value</span><span class="sxs-lookup"><span data-stu-id="b75d9-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b75d9-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b75d9-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b75d9-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b75d9-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b75d9-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b75d9-135">System-Only</span></span>            | <span data-ttu-id="b75d9-136">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-136">False</span></span>                                        |
| <span data-ttu-id="b75d9-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b75d9-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b75d9-138">True</span><span class="sxs-lookup"><span data-stu-id="b75d9-138">True</span></span>                                         |
| <span data-ttu-id="b75d9-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b75d9-139">Is Indexed</span></span>             | <span data-ttu-id="b75d9-140">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-140">False</span></span>                                        |
| <span data-ttu-id="b75d9-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b75d9-141">In Global Catalog</span></span>      | <span data-ttu-id="b75d9-142">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-142">False</span></span>                                        |
| <span data-ttu-id="b75d9-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b75d9-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b75d9-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b75d9-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b75d9-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b75d9-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b75d9-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b75d9-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b75d9-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b75d9-147">Search-Flags</span></span>           | <span data-ttu-id="b75d9-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b75d9-148">0x00000000</span></span>                                   |
| <span data-ttu-id="b75d9-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b75d9-149">System-Flags</span></span>           | <span data-ttu-id="b75d9-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b75d9-150">0x00000010</span></span>                                   |
| <span data-ttu-id="b75d9-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b75d9-151">Classes used in</span></span>        | [<span data-ttu-id="b75d9-152">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="b75d9-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b75d9-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b75d9-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b75d9-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="b75d9-154">Entry</span></span> | <span data-ttu-id="b75d9-155">Value</span><span class="sxs-lookup"><span data-stu-id="b75d9-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b75d9-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b75d9-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b75d9-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b75d9-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b75d9-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b75d9-158">System-Only</span></span>            | <span data-ttu-id="b75d9-159">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-159">False</span></span>                                        |
| <span data-ttu-id="b75d9-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b75d9-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b75d9-161">True</span><span class="sxs-lookup"><span data-stu-id="b75d9-161">True</span></span>                                         |
| <span data-ttu-id="b75d9-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b75d9-162">Is Indexed</span></span>             | <span data-ttu-id="b75d9-163">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-163">False</span></span>                                        |
| <span data-ttu-id="b75d9-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b75d9-164">In Global Catalog</span></span>      | <span data-ttu-id="b75d9-165">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-165">False</span></span>                                        |
| <span data-ttu-id="b75d9-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b75d9-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b75d9-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b75d9-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b75d9-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b75d9-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b75d9-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b75d9-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b75d9-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b75d9-170">Search-Flags</span></span>           | <span data-ttu-id="b75d9-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b75d9-171">0x00000000</span></span>                                   |
| <span data-ttu-id="b75d9-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b75d9-172">System-Flags</span></span>           | <span data-ttu-id="b75d9-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b75d9-173">0x00000010</span></span>                                   |
| <span data-ttu-id="b75d9-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b75d9-174">Classes used in</span></span>        | [<span data-ttu-id="b75d9-175">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="b75d9-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b75d9-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b75d9-176">Windows Server 2008</span></span>



| <span data-ttu-id="b75d9-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="b75d9-177">Entry</span></span> | <span data-ttu-id="b75d9-178">Value</span><span class="sxs-lookup"><span data-stu-id="b75d9-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b75d9-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b75d9-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b75d9-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b75d9-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b75d9-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b75d9-181">System-Only</span></span>            | <span data-ttu-id="b75d9-182">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-182">False</span></span>                                        |
| <span data-ttu-id="b75d9-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b75d9-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b75d9-184">True</span><span class="sxs-lookup"><span data-stu-id="b75d9-184">True</span></span>                                         |
| <span data-ttu-id="b75d9-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b75d9-185">Is Indexed</span></span>             | <span data-ttu-id="b75d9-186">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-186">False</span></span>                                        |
| <span data-ttu-id="b75d9-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b75d9-187">In Global Catalog</span></span>      | <span data-ttu-id="b75d9-188">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-188">False</span></span>                                        |
| <span data-ttu-id="b75d9-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b75d9-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b75d9-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b75d9-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b75d9-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b75d9-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b75d9-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b75d9-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b75d9-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b75d9-193">Search-Flags</span></span>           | <span data-ttu-id="b75d9-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b75d9-194">0x00000000</span></span>                                   |
| <span data-ttu-id="b75d9-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b75d9-195">System-Flags</span></span>           | <span data-ttu-id="b75d9-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b75d9-196">0x00000010</span></span>                                   |
| <span data-ttu-id="b75d9-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b75d9-197">Classes used in</span></span>        | [<span data-ttu-id="b75d9-198">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="b75d9-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b75d9-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b75d9-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b75d9-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="b75d9-200">Entry</span></span> | <span data-ttu-id="b75d9-201">Value</span><span class="sxs-lookup"><span data-stu-id="b75d9-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b75d9-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b75d9-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b75d9-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b75d9-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b75d9-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b75d9-204">System-Only</span></span>            | <span data-ttu-id="b75d9-205">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-205">False</span></span>                                        |
| <span data-ttu-id="b75d9-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b75d9-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b75d9-207">True</span><span class="sxs-lookup"><span data-stu-id="b75d9-207">True</span></span>                                         |
| <span data-ttu-id="b75d9-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b75d9-208">Is Indexed</span></span>             | <span data-ttu-id="b75d9-209">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-209">False</span></span>                                        |
| <span data-ttu-id="b75d9-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b75d9-210">In Global Catalog</span></span>      | <span data-ttu-id="b75d9-211">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-211">False</span></span>                                        |
| <span data-ttu-id="b75d9-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b75d9-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b75d9-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b75d9-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b75d9-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b75d9-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b75d9-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b75d9-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b75d9-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b75d9-216">Search-Flags</span></span>           | <span data-ttu-id="b75d9-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b75d9-217">0x00000000</span></span>                                   |
| <span data-ttu-id="b75d9-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b75d9-218">System-Flags</span></span>           | <span data-ttu-id="b75d9-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b75d9-219">0x00000010</span></span>                                   |
| <span data-ttu-id="b75d9-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b75d9-220">Classes used in</span></span>        | [<span data-ttu-id="b75d9-221">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="b75d9-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b75d9-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b75d9-222">Windows Server 2012</span></span>



| <span data-ttu-id="b75d9-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="b75d9-223">Entry</span></span> | <span data-ttu-id="b75d9-224">Value</span><span class="sxs-lookup"><span data-stu-id="b75d9-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b75d9-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b75d9-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b75d9-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b75d9-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b75d9-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b75d9-227">System-Only</span></span>            | <span data-ttu-id="b75d9-228">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-228">False</span></span>                                        |
| <span data-ttu-id="b75d9-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b75d9-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b75d9-230">True</span><span class="sxs-lookup"><span data-stu-id="b75d9-230">True</span></span>                                         |
| <span data-ttu-id="b75d9-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b75d9-231">Is Indexed</span></span>             | <span data-ttu-id="b75d9-232">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-232">False</span></span>                                        |
| <span data-ttu-id="b75d9-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b75d9-233">In Global Catalog</span></span>      | <span data-ttu-id="b75d9-234">False</span><span class="sxs-lookup"><span data-stu-id="b75d9-234">False</span></span>                                        |
| <span data-ttu-id="b75d9-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b75d9-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b75d9-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b75d9-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b75d9-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b75d9-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b75d9-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b75d9-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b75d9-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b75d9-239">Search-Flags</span></span>           | <span data-ttu-id="b75d9-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b75d9-240">0x00000000</span></span>                                   |
| <span data-ttu-id="b75d9-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b75d9-241">System-Flags</span></span>           | <span data-ttu-id="b75d9-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b75d9-242">0x00000010</span></span>                                   |
| <span data-ttu-id="b75d9-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b75d9-243">Classes used in</span></span>        | [<span data-ttu-id="b75d9-244">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="b75d9-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





