---
title: Atributo ACS-Identity-Name
description: Este atributo contiene el DN de un usuario o una unidad organizativa y es la identidad de un usuario o un grupo de usuarios a los que se aplica esta directiva de QoS.
ms.assetid: 00e6e2bd-aec8-426f-b89e-0661c15cfd46
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ACS-Identity-Name
- aCSIdentityName esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-Identity-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33ef1db92b908ef8474dfb125aca678d3c22d09f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151903"
---
# <a name="acs-identity-name-attribute"></a><span data-ttu-id="cc021-105">Atributo ACS-Identity-Name</span><span class="sxs-lookup"><span data-stu-id="cc021-105">ACS-Identity-Name attribute</span></span>

<span data-ttu-id="cc021-106">Este atributo contiene el DN de un usuario o una unidad organizativa y es la identidad de un usuario o un grupo de usuarios a los que se aplica esta directiva de QoS.</span><span class="sxs-lookup"><span data-stu-id="cc021-106">This attribute contains the DN of a user or OU and is the identity of a user or a group of users to which this QoS policy applies.</span></span>



| <span data-ttu-id="cc021-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc021-107">Entry</span></span> | <span data-ttu-id="cc021-108">Value</span><span class="sxs-lookup"><span data-stu-id="cc021-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="cc021-109">CN</span><span class="sxs-lookup"><span data-stu-id="cc021-109">CN</span></span>                | <span data-ttu-id="cc021-110">Nombre de identidad de ACS</span><span class="sxs-lookup"><span data-stu-id="cc021-110">ACS-Identity-Name</span></span>                           |
| <span data-ttu-id="cc021-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="cc021-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cc021-112">aCSIdentityName</span><span class="sxs-lookup"><span data-stu-id="cc021-112">aCSIdentityName</span></span>                             |
| <span data-ttu-id="cc021-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="cc021-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="cc021-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="cc021-114">Update Privilege</span></span>  | <span data-ttu-id="cc021-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="cc021-115">Domain administrator</span></span>                        |
| <span data-ttu-id="cc021-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="cc021-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="cc021-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cc021-117">Attribute-Id</span></span>      | <span data-ttu-id="cc021-118">1.2.840.113556.1.4.784</span><span class="sxs-lookup"><span data-stu-id="cc021-118">1.2.840.113556.1.4.784</span></span>                      |
| <span data-ttu-id="cc021-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cc021-119">System-Id-Guid</span></span>    | <span data-ttu-id="cc021-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="cc021-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span></span>        |
| <span data-ttu-id="cc021-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc021-121">Syntax</span></span>            | [<span data-ttu-id="cc021-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cc021-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="cc021-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="cc021-123">Implementations</span></span>

-   [<span data-ttu-id="cc021-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cc021-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cc021-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cc021-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cc021-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cc021-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cc021-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cc021-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cc021-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cc021-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cc021-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cc021-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cc021-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc021-130">Windows 2000 Server</span></span>



| <span data-ttu-id="cc021-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc021-131">Entry</span></span> | <span data-ttu-id="cc021-132">Value</span><span class="sxs-lookup"><span data-stu-id="cc021-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cc021-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cc021-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc021-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc021-135">System-Only</span></span>            | <span data-ttu-id="cc021-136">False</span><span class="sxs-lookup"><span data-stu-id="cc021-136">False</span></span>                                        |
| <span data-ttu-id="cc021-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cc021-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cc021-138">False</span><span class="sxs-lookup"><span data-stu-id="cc021-138">False</span></span>                                        |
| <span data-ttu-id="cc021-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cc021-139">Is Indexed</span></span>             | <span data-ttu-id="cc021-140">False</span><span class="sxs-lookup"><span data-stu-id="cc021-140">False</span></span>                                        |
| <span data-ttu-id="cc021-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc021-141">In Global Catalog</span></span>      | <span data-ttu-id="cc021-142">False</span><span class="sxs-lookup"><span data-stu-id="cc021-142">False</span></span>                                        |
| <span data-ttu-id="cc021-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cc021-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc021-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc021-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cc021-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc021-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cc021-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc021-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cc021-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-147">Search-Flags</span></span>           | <span data-ttu-id="cc021-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc021-148">0x00000000</span></span>                                   |
| <span data-ttu-id="cc021-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-149">System-Flags</span></span>           | <span data-ttu-id="cc021-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc021-150">0x00000010</span></span>                                   |
| <span data-ttu-id="cc021-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cc021-151">Classes used in</span></span>        | [<span data-ttu-id="cc021-152">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="cc021-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cc021-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc021-153">Windows Server 2003</span></span>



| <span data-ttu-id="cc021-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc021-154">Entry</span></span> | <span data-ttu-id="cc021-155">Value</span><span class="sxs-lookup"><span data-stu-id="cc021-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cc021-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cc021-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc021-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc021-158">System-Only</span></span>            | <span data-ttu-id="cc021-159">False</span><span class="sxs-lookup"><span data-stu-id="cc021-159">False</span></span>                                        |
| <span data-ttu-id="cc021-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cc021-160">Is-Single-Valued</span></span>       | <span data-ttu-id="cc021-161">False</span><span class="sxs-lookup"><span data-stu-id="cc021-161">False</span></span>                                        |
| <span data-ttu-id="cc021-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cc021-162">Is Indexed</span></span>             | <span data-ttu-id="cc021-163">False</span><span class="sxs-lookup"><span data-stu-id="cc021-163">False</span></span>                                        |
| <span data-ttu-id="cc021-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc021-164">In Global Catalog</span></span>      | <span data-ttu-id="cc021-165">False</span><span class="sxs-lookup"><span data-stu-id="cc021-165">False</span></span>                                        |
| <span data-ttu-id="cc021-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cc021-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc021-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc021-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cc021-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc021-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cc021-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc021-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cc021-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-170">Search-Flags</span></span>           | <span data-ttu-id="cc021-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc021-171">0x00000000</span></span>                                   |
| <span data-ttu-id="cc021-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-172">System-Flags</span></span>           | <span data-ttu-id="cc021-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc021-173">0x00000010</span></span>                                   |
| <span data-ttu-id="cc021-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cc021-174">Classes used in</span></span>        | [<span data-ttu-id="cc021-175">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="cc021-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cc021-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cc021-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cc021-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc021-177">Entry</span></span> | <span data-ttu-id="cc021-178">Value</span><span class="sxs-lookup"><span data-stu-id="cc021-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cc021-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cc021-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc021-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc021-181">System-Only</span></span>            | <span data-ttu-id="cc021-182">False</span><span class="sxs-lookup"><span data-stu-id="cc021-182">False</span></span>                                        |
| <span data-ttu-id="cc021-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cc021-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cc021-184">False</span><span class="sxs-lookup"><span data-stu-id="cc021-184">False</span></span>                                        |
| <span data-ttu-id="cc021-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cc021-185">Is Indexed</span></span>             | <span data-ttu-id="cc021-186">False</span><span class="sxs-lookup"><span data-stu-id="cc021-186">False</span></span>                                        |
| <span data-ttu-id="cc021-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc021-187">In Global Catalog</span></span>      | <span data-ttu-id="cc021-188">False</span><span class="sxs-lookup"><span data-stu-id="cc021-188">False</span></span>                                        |
| <span data-ttu-id="cc021-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cc021-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc021-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc021-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cc021-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc021-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cc021-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc021-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cc021-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-193">Search-Flags</span></span>           | <span data-ttu-id="cc021-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc021-194">0x00000000</span></span>                                   |
| <span data-ttu-id="cc021-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-195">System-Flags</span></span>           | <span data-ttu-id="cc021-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc021-196">0x00000010</span></span>                                   |
| <span data-ttu-id="cc021-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cc021-197">Classes used in</span></span>        | [<span data-ttu-id="cc021-198">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="cc021-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cc021-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc021-199">Windows Server 2008</span></span>



| <span data-ttu-id="cc021-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc021-200">Entry</span></span> | <span data-ttu-id="cc021-201">Value</span><span class="sxs-lookup"><span data-stu-id="cc021-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cc021-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cc021-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc021-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc021-204">System-Only</span></span>            | <span data-ttu-id="cc021-205">False</span><span class="sxs-lookup"><span data-stu-id="cc021-205">False</span></span>                                        |
| <span data-ttu-id="cc021-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cc021-206">Is-Single-Valued</span></span>       | <span data-ttu-id="cc021-207">False</span><span class="sxs-lookup"><span data-stu-id="cc021-207">False</span></span>                                        |
| <span data-ttu-id="cc021-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cc021-208">Is Indexed</span></span>             | <span data-ttu-id="cc021-209">False</span><span class="sxs-lookup"><span data-stu-id="cc021-209">False</span></span>                                        |
| <span data-ttu-id="cc021-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc021-210">In Global Catalog</span></span>      | <span data-ttu-id="cc021-211">False</span><span class="sxs-lookup"><span data-stu-id="cc021-211">False</span></span>                                        |
| <span data-ttu-id="cc021-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cc021-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc021-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc021-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cc021-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc021-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cc021-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc021-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cc021-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-216">Search-Flags</span></span>           | <span data-ttu-id="cc021-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc021-217">0x00000000</span></span>                                   |
| <span data-ttu-id="cc021-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-218">System-Flags</span></span>           | <span data-ttu-id="cc021-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc021-219">0x00000010</span></span>                                   |
| <span data-ttu-id="cc021-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cc021-220">Classes used in</span></span>        | [<span data-ttu-id="cc021-221">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="cc021-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cc021-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cc021-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cc021-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc021-223">Entry</span></span> | <span data-ttu-id="cc021-224">Value</span><span class="sxs-lookup"><span data-stu-id="cc021-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cc021-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cc021-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc021-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc021-227">System-Only</span></span>            | <span data-ttu-id="cc021-228">False</span><span class="sxs-lookup"><span data-stu-id="cc021-228">False</span></span>                                        |
| <span data-ttu-id="cc021-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cc021-229">Is-Single-Valued</span></span>       | <span data-ttu-id="cc021-230">False</span><span class="sxs-lookup"><span data-stu-id="cc021-230">False</span></span>                                        |
| <span data-ttu-id="cc021-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cc021-231">Is Indexed</span></span>             | <span data-ttu-id="cc021-232">False</span><span class="sxs-lookup"><span data-stu-id="cc021-232">False</span></span>                                        |
| <span data-ttu-id="cc021-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc021-233">In Global Catalog</span></span>      | <span data-ttu-id="cc021-234">False</span><span class="sxs-lookup"><span data-stu-id="cc021-234">False</span></span>                                        |
| <span data-ttu-id="cc021-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cc021-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc021-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc021-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cc021-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc021-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cc021-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc021-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cc021-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-239">Search-Flags</span></span>           | <span data-ttu-id="cc021-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc021-240">0x00000000</span></span>                                   |
| <span data-ttu-id="cc021-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-241">System-Flags</span></span>           | <span data-ttu-id="cc021-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc021-242">0x00000010</span></span>                                   |
| <span data-ttu-id="cc021-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cc021-243">Classes used in</span></span>        | [<span data-ttu-id="cc021-244">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="cc021-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cc021-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc021-245">Windows Server 2012</span></span>



| <span data-ttu-id="cc021-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc021-246">Entry</span></span> | <span data-ttu-id="cc021-247">Value</span><span class="sxs-lookup"><span data-stu-id="cc021-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="cc021-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cc021-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc021-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="cc021-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc021-250">System-Only</span></span>            | <span data-ttu-id="cc021-251">False</span><span class="sxs-lookup"><span data-stu-id="cc021-251">False</span></span>                                        |
| <span data-ttu-id="cc021-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cc021-252">Is-Single-Valued</span></span>       | <span data-ttu-id="cc021-253">False</span><span class="sxs-lookup"><span data-stu-id="cc021-253">False</span></span>                                        |
| <span data-ttu-id="cc021-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cc021-254">Is Indexed</span></span>             | <span data-ttu-id="cc021-255">False</span><span class="sxs-lookup"><span data-stu-id="cc021-255">False</span></span>                                        |
| <span data-ttu-id="cc021-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc021-256">In Global Catalog</span></span>      | <span data-ttu-id="cc021-257">False</span><span class="sxs-lookup"><span data-stu-id="cc021-257">False</span></span>                                        |
| <span data-ttu-id="cc021-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cc021-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc021-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc021-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="cc021-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc021-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="cc021-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc021-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="cc021-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-262">Search-Flags</span></span>           | <span data-ttu-id="cc021-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc021-263">0x00000000</span></span>                                   |
| <span data-ttu-id="cc021-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc021-264">System-Flags</span></span>           | <span data-ttu-id="cc021-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc021-265">0x00000010</span></span>                                   |
| <span data-ttu-id="cc021-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cc021-266">Classes used in</span></span>        | [<span data-ttu-id="cc021-267">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="cc021-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





