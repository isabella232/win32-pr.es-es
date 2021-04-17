---
title: atributo MS-DS-Additional-Sam-Account-Name
description: Este atributo se usa para almacenar los nombres de cuenta SAM que corresponden a los nombres de host DNS en MS-DS-Additional-DNS-host-name.
ms.assetid: eb69e1d4-42b7-42e1-aeae-77188db307ef
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de nombre de cuenta de MS-DS-Account-Sam
- Esquema de AD de atributo msDS-AdditionalSamAccountName
topic_type:
- apiref
api_name:
- ms-DS-Additional-Sam-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a437c30e6ddb0e551498480f7589791bce59feaf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659149"
---
# <a name="ms-ds-additional-sam-account-name-attribute"></a><span data-ttu-id="9aa83-105">atributo MS-DS-Additional-Sam-Account-Name</span><span class="sxs-lookup"><span data-stu-id="9aa83-105">ms-DS-Additional-Sam-Account-Name attribute</span></span>

<span data-ttu-id="9aa83-106">Este atributo se usa para almacenar los nombres de cuenta SAM que corresponden a los nombres de host DNS en MS-DS-Additional-DNS-host-name.</span><span class="sxs-lookup"><span data-stu-id="9aa83-106">This attribute is used to store the SAM account names that correspond to the DNS host names in ms-DS-Additional-Dns-Host-Name.</span></span>



| <span data-ttu-id="9aa83-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9aa83-107">Entry</span></span> | <span data-ttu-id="9aa83-108">Value</span><span class="sxs-lookup"><span data-stu-id="9aa83-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9aa83-109">CN</span><span class="sxs-lookup"><span data-stu-id="9aa83-109">CN</span></span>                | <span data-ttu-id="9aa83-110">Nombre de la cuenta de MS-DS-Additional-Sam</span><span class="sxs-lookup"><span data-stu-id="9aa83-110">ms-DS-Additional-Sam-Account-Name</span></span>           |
| <span data-ttu-id="9aa83-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="9aa83-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9aa83-112">msDS-AdditionalSamAccountName</span><span class="sxs-lookup"><span data-stu-id="9aa83-112">msDS-AdditionalSamAccountName</span></span>               |
| <span data-ttu-id="9aa83-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="9aa83-113">Size</span></span>              | <span data-ttu-id="9aa83-114">Menos de 20 bytes.</span><span class="sxs-lookup"><span data-stu-id="9aa83-114">Less than 20 bytes.</span></span>                         |
| <span data-ttu-id="9aa83-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="9aa83-115">Update Privilege</span></span>  | <span data-ttu-id="9aa83-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="9aa83-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="9aa83-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="9aa83-117">Update Frequency</span></span>  | <span data-ttu-id="9aa83-118">Cuando se cambia el nombre del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="9aa83-118">When the DC is renamed.</span></span>                     |
| <span data-ttu-id="9aa83-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9aa83-119">Attribute-Id</span></span>      | <span data-ttu-id="9aa83-120">1.2.840.113556.1.4.1718</span><span class="sxs-lookup"><span data-stu-id="9aa83-120">1.2.840.113556.1.4.1718</span></span>                     |
| <span data-ttu-id="9aa83-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9aa83-121">System-Id-Guid</span></span>    | <span data-ttu-id="9aa83-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span><span class="sxs-lookup"><span data-stu-id="9aa83-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span></span>        |
| <span data-ttu-id="9aa83-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9aa83-123">Syntax</span></span>            | [<span data-ttu-id="9aa83-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9aa83-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9aa83-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="9aa83-125">Implementations</span></span>

-   [<span data-ttu-id="9aa83-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9aa83-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9aa83-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9aa83-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9aa83-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9aa83-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9aa83-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9aa83-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9aa83-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9aa83-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9aa83-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9aa83-131">Windows Server 2003</span></span>



| <span data-ttu-id="9aa83-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="9aa83-132">Entry</span></span> | <span data-ttu-id="9aa83-133">Value</span><span class="sxs-lookup"><span data-stu-id="9aa83-133">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="9aa83-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9aa83-134">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="9aa83-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9aa83-135">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="9aa83-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9aa83-136">System-Only</span></span>            | <span data-ttu-id="9aa83-137">True</span><span class="sxs-lookup"><span data-stu-id="9aa83-137">True</span></span>                                      |
| <span data-ttu-id="9aa83-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9aa83-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9aa83-139">False</span><span class="sxs-lookup"><span data-stu-id="9aa83-139">False</span></span>                                     |
| <span data-ttu-id="9aa83-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9aa83-140">Is Indexed</span></span>             | <span data-ttu-id="9aa83-141">True</span><span class="sxs-lookup"><span data-stu-id="9aa83-141">True</span></span>                                      |
| <span data-ttu-id="9aa83-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9aa83-142">In Global Catalog</span></span>      | <span data-ttu-id="9aa83-143">False</span><span class="sxs-lookup"><span data-stu-id="9aa83-143">False</span></span>                                     |
| <span data-ttu-id="9aa83-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9aa83-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9aa83-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9aa83-145">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="9aa83-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9aa83-146">Range-Lower</span></span>            | <span data-ttu-id="9aa83-147">0</span><span class="sxs-lookup"><span data-stu-id="9aa83-147">0</span></span>                                         |
| <span data-ttu-id="9aa83-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9aa83-148">Range-Upper</span></span>            | <span data-ttu-id="9aa83-149">256</span><span class="sxs-lookup"><span data-stu-id="9aa83-149">256</span></span>                                       |
| <span data-ttu-id="9aa83-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa83-150">Search-Flags</span></span>           | <span data-ttu-id="9aa83-151">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="9aa83-151">0x0000000D</span></span>                                |
| <span data-ttu-id="9aa83-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa83-152">System-Flags</span></span>           | <span data-ttu-id="9aa83-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9aa83-153">0x00000010</span></span>                                |
| <span data-ttu-id="9aa83-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9aa83-154">Classes used in</span></span>        | [<span data-ttu-id="9aa83-155">**Computer**</span><span class="sxs-lookup"><span data-stu-id="9aa83-155">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9aa83-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9aa83-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9aa83-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="9aa83-157">Entry</span></span> | <span data-ttu-id="9aa83-158">Value</span><span class="sxs-lookup"><span data-stu-id="9aa83-158">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="9aa83-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9aa83-159">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="9aa83-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9aa83-160">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="9aa83-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="9aa83-161">System-Only</span></span>            | <span data-ttu-id="9aa83-162">True</span><span class="sxs-lookup"><span data-stu-id="9aa83-162">True</span></span>                                      |
| <span data-ttu-id="9aa83-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9aa83-163">Is-Single-Valued</span></span>       | <span data-ttu-id="9aa83-164">False</span><span class="sxs-lookup"><span data-stu-id="9aa83-164">False</span></span>                                     |
| <span data-ttu-id="9aa83-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9aa83-165">Is Indexed</span></span>             | <span data-ttu-id="9aa83-166">True</span><span class="sxs-lookup"><span data-stu-id="9aa83-166">True</span></span>                                      |
| <span data-ttu-id="9aa83-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9aa83-167">In Global Catalog</span></span>      | <span data-ttu-id="9aa83-168">False</span><span class="sxs-lookup"><span data-stu-id="9aa83-168">False</span></span>                                     |
| <span data-ttu-id="9aa83-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9aa83-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="9aa83-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9aa83-170">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="9aa83-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9aa83-171">Range-Lower</span></span>            | <span data-ttu-id="9aa83-172">0</span><span class="sxs-lookup"><span data-stu-id="9aa83-172">0</span></span>                                         |
| <span data-ttu-id="9aa83-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9aa83-173">Range-Upper</span></span>            | <span data-ttu-id="9aa83-174">256</span><span class="sxs-lookup"><span data-stu-id="9aa83-174">256</span></span>                                       |
| <span data-ttu-id="9aa83-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa83-175">Search-Flags</span></span>           | <span data-ttu-id="9aa83-176">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="9aa83-176">0x0000000D</span></span>                                |
| <span data-ttu-id="9aa83-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa83-177">System-Flags</span></span>           | <span data-ttu-id="9aa83-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9aa83-178">0x00000010</span></span>                                |
| <span data-ttu-id="9aa83-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9aa83-179">Classes used in</span></span>        | [<span data-ttu-id="9aa83-180">**Computer**</span><span class="sxs-lookup"><span data-stu-id="9aa83-180">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9aa83-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9aa83-181">Windows Server 2008</span></span>



| <span data-ttu-id="9aa83-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="9aa83-182">Entry</span></span> | <span data-ttu-id="9aa83-183">Value</span><span class="sxs-lookup"><span data-stu-id="9aa83-183">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="9aa83-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9aa83-184">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="9aa83-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9aa83-185">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="9aa83-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="9aa83-186">System-Only</span></span>            | <span data-ttu-id="9aa83-187">True</span><span class="sxs-lookup"><span data-stu-id="9aa83-187">True</span></span>                                      |
| <span data-ttu-id="9aa83-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9aa83-188">Is-Single-Valued</span></span>       | <span data-ttu-id="9aa83-189">False</span><span class="sxs-lookup"><span data-stu-id="9aa83-189">False</span></span>                                     |
| <span data-ttu-id="9aa83-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9aa83-190">Is Indexed</span></span>             | <span data-ttu-id="9aa83-191">True</span><span class="sxs-lookup"><span data-stu-id="9aa83-191">True</span></span>                                      |
| <span data-ttu-id="9aa83-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9aa83-192">In Global Catalog</span></span>      | <span data-ttu-id="9aa83-193">False</span><span class="sxs-lookup"><span data-stu-id="9aa83-193">False</span></span>                                     |
| <span data-ttu-id="9aa83-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9aa83-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="9aa83-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9aa83-195">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="9aa83-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9aa83-196">Range-Lower</span></span>            | <span data-ttu-id="9aa83-197">0</span><span class="sxs-lookup"><span data-stu-id="9aa83-197">0</span></span>                                         |
| <span data-ttu-id="9aa83-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9aa83-198">Range-Upper</span></span>            | <span data-ttu-id="9aa83-199">256</span><span class="sxs-lookup"><span data-stu-id="9aa83-199">256</span></span>                                       |
| <span data-ttu-id="9aa83-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa83-200">Search-Flags</span></span>           | <span data-ttu-id="9aa83-201">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="9aa83-201">0x0000000D</span></span>                                |
| <span data-ttu-id="9aa83-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa83-202">System-Flags</span></span>           | <span data-ttu-id="9aa83-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9aa83-203">0x00000010</span></span>                                |
| <span data-ttu-id="9aa83-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9aa83-204">Classes used in</span></span>        | [<span data-ttu-id="9aa83-205">**Computer**</span><span class="sxs-lookup"><span data-stu-id="9aa83-205">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9aa83-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9aa83-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9aa83-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="9aa83-207">Entry</span></span> | <span data-ttu-id="9aa83-208">Value</span><span class="sxs-lookup"><span data-stu-id="9aa83-208">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="9aa83-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9aa83-209">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="9aa83-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9aa83-210">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="9aa83-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="9aa83-211">System-Only</span></span>            | <span data-ttu-id="9aa83-212">True</span><span class="sxs-lookup"><span data-stu-id="9aa83-212">True</span></span>                                      |
| <span data-ttu-id="9aa83-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9aa83-213">Is-Single-Valued</span></span>       | <span data-ttu-id="9aa83-214">False</span><span class="sxs-lookup"><span data-stu-id="9aa83-214">False</span></span>                                     |
| <span data-ttu-id="9aa83-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9aa83-215">Is Indexed</span></span>             | <span data-ttu-id="9aa83-216">True</span><span class="sxs-lookup"><span data-stu-id="9aa83-216">True</span></span>                                      |
| <span data-ttu-id="9aa83-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9aa83-217">In Global Catalog</span></span>      | <span data-ttu-id="9aa83-218">False</span><span class="sxs-lookup"><span data-stu-id="9aa83-218">False</span></span>                                     |
| <span data-ttu-id="9aa83-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9aa83-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="9aa83-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9aa83-220">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="9aa83-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9aa83-221">Range-Lower</span></span>            | <span data-ttu-id="9aa83-222">0</span><span class="sxs-lookup"><span data-stu-id="9aa83-222">0</span></span>                                         |
| <span data-ttu-id="9aa83-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9aa83-223">Range-Upper</span></span>            | <span data-ttu-id="9aa83-224">256</span><span class="sxs-lookup"><span data-stu-id="9aa83-224">256</span></span>                                       |
| <span data-ttu-id="9aa83-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa83-225">Search-Flags</span></span>           | <span data-ttu-id="9aa83-226">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="9aa83-226">0x0000000D</span></span>                                |
| <span data-ttu-id="9aa83-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa83-227">System-Flags</span></span>           | <span data-ttu-id="9aa83-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9aa83-228">0x00000010</span></span>                                |
| <span data-ttu-id="9aa83-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9aa83-229">Classes used in</span></span>        | [<span data-ttu-id="9aa83-230">**Computer**</span><span class="sxs-lookup"><span data-stu-id="9aa83-230">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9aa83-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9aa83-231">Windows Server 2012</span></span>



| <span data-ttu-id="9aa83-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="9aa83-232">Entry</span></span> | <span data-ttu-id="9aa83-233">Value</span><span class="sxs-lookup"><span data-stu-id="9aa83-233">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="9aa83-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9aa83-234">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="9aa83-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9aa83-235">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="9aa83-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="9aa83-236">System-Only</span></span>            | <span data-ttu-id="9aa83-237">True</span><span class="sxs-lookup"><span data-stu-id="9aa83-237">True</span></span>                                      |
| <span data-ttu-id="9aa83-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9aa83-238">Is-Single-Valued</span></span>       | <span data-ttu-id="9aa83-239">False</span><span class="sxs-lookup"><span data-stu-id="9aa83-239">False</span></span>                                     |
| <span data-ttu-id="9aa83-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9aa83-240">Is Indexed</span></span>             | <span data-ttu-id="9aa83-241">True</span><span class="sxs-lookup"><span data-stu-id="9aa83-241">True</span></span>                                      |
| <span data-ttu-id="9aa83-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9aa83-242">In Global Catalog</span></span>      | <span data-ttu-id="9aa83-243">False</span><span class="sxs-lookup"><span data-stu-id="9aa83-243">False</span></span>                                     |
| <span data-ttu-id="9aa83-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9aa83-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="9aa83-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9aa83-245">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="9aa83-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9aa83-246">Range-Lower</span></span>            | <span data-ttu-id="9aa83-247">0</span><span class="sxs-lookup"><span data-stu-id="9aa83-247">0</span></span>                                         |
| <span data-ttu-id="9aa83-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9aa83-248">Range-Upper</span></span>            | <span data-ttu-id="9aa83-249">256</span><span class="sxs-lookup"><span data-stu-id="9aa83-249">256</span></span>                                       |
| <span data-ttu-id="9aa83-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa83-250">Search-Flags</span></span>           | <span data-ttu-id="9aa83-251">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="9aa83-251">0x0000000D</span></span>                                |
| <span data-ttu-id="9aa83-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9aa83-252">System-Flags</span></span>           | <span data-ttu-id="9aa83-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9aa83-253">0x00000010</span></span>                                |
| <span data-ttu-id="9aa83-254">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9aa83-254">Classes used in</span></span>        | [<span data-ttu-id="9aa83-255">**Computer**</span><span class="sxs-lookup"><span data-stu-id="9aa83-255">**Computer**</span></span>](c-computer.md)<br/> |



 

 





