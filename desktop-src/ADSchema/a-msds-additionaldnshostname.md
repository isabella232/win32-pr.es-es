---
title: atributo MS-DS-Additional-DNS-host-name
description: El atributo se utiliza para almacenar el nombre de host DNS adicional de un objeto de equipo. Este atributo se usa en el momento en que se cambia el nombre de un controlador de dominio.
ms.assetid: ea06f756-d9b6-409d-a008-0e3a1874ad94
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de nombre de host/DNS de MS-DS-Additional
- Esquema de AD de atributo msDS-AdditionalDnsHostName
topic_type:
- apiref
api_name:
- ms-DS-Additional-Dns-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dea3212a19bf743e608f356170adf7a03c06d0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997447"
---
# <a name="ms-ds-additional-dns-host-name-attribute"></a><span data-ttu-id="c3bee-106">atributo MS-DS-Additional-DNS-host-name</span><span class="sxs-lookup"><span data-stu-id="c3bee-106">ms-DS-Additional-Dns-Host-Name attribute</span></span>

<span data-ttu-id="c3bee-107">El atributo se utiliza para almacenar el nombre de host DNS adicional de un objeto de equipo.</span><span class="sxs-lookup"><span data-stu-id="c3bee-107">The attribute is used to store the additional DNS host name of a computer object.</span></span> <span data-ttu-id="c3bee-108">Este atributo se utiliza en el momento en que se cambia el nombre de un equipo o los nombres se administran con "netdom computername".</span><span class="sxs-lookup"><span data-stu-id="c3bee-108">This attribute is used at the time a computer is renamed, or names are managed with "netdom computername".</span></span>



| <span data-ttu-id="c3bee-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3bee-109">Entry</span></span> | <span data-ttu-id="c3bee-110">Value</span><span class="sxs-lookup"><span data-stu-id="c3bee-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="c3bee-111">CN</span><span class="sxs-lookup"><span data-stu-id="c3bee-111">CN</span></span>                | <span data-ttu-id="c3bee-112">MS-DS-Additional-DNS-host-name</span><span class="sxs-lookup"><span data-stu-id="c3bee-112">ms-DS-Additional-Dns-Host-Name</span></span>                                              |
| <span data-ttu-id="c3bee-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c3bee-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c3bee-114">msDS-AdditionalDnsHostName</span><span class="sxs-lookup"><span data-stu-id="c3bee-114">msDS-AdditionalDnsHostName</span></span>                                                  |
| <span data-ttu-id="c3bee-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c3bee-115">Size</span></span>              | <span data-ttu-id="c3bee-116">Cada valor puede tener 2048 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c3bee-116">Each value can be 2048 characters.</span></span> <span data-ttu-id="c3bee-117">El número de valor es el límite de la base de datos de aproximadamente 1200 valores.</span><span class="sxs-lookup"><span data-stu-id="c3bee-117">The number of value is the database limit of about 1200 values.</span></span> |
| <span data-ttu-id="c3bee-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c3bee-118">Update Privilege</span></span>  | <span data-ttu-id="c3bee-119">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="c3bee-119">This value is set by the system.</span></span>                                            |
| <span data-ttu-id="c3bee-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c3bee-120">Update Frequency</span></span>  | <span data-ttu-id="c3bee-121">Cuando se cambia el nombre de un equipo.</span><span class="sxs-lookup"><span data-stu-id="c3bee-121">When a computer is renamed.</span></span>                                                 |
| <span data-ttu-id="c3bee-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c3bee-122">Attribute-Id</span></span>      | <span data-ttu-id="c3bee-123">1.2.840.113556.1.4.1717</span><span class="sxs-lookup"><span data-stu-id="c3bee-123">1.2.840.113556.1.4.1717</span></span>                                                     |
| <span data-ttu-id="c3bee-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c3bee-124">System-Id-Guid</span></span>    | <span data-ttu-id="c3bee-125">80863791-dbe9-4eb8-837e-7f0ab55d9ac7</span><span class="sxs-lookup"><span data-stu-id="c3bee-125">80863791-dbe9-4eb8-837e-7f0ab55d9ac7</span></span>                                        |
| <span data-ttu-id="c3bee-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3bee-126">Syntax</span></span>            | [<span data-ttu-id="c3bee-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c3bee-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                 |



## <a name="implementations"></a><span data-ttu-id="c3bee-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c3bee-128">Implementations</span></span>

-   [<span data-ttu-id="c3bee-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c3bee-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c3bee-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c3bee-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c3bee-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c3bee-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c3bee-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c3bee-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c3bee-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c3bee-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c3bee-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3bee-134">Windows Server 2003</span></span>



| <span data-ttu-id="c3bee-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3bee-135">Entry</span></span> | <span data-ttu-id="c3bee-136">Value</span><span class="sxs-lookup"><span data-stu-id="c3bee-136">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c3bee-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c3bee-137">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c3bee-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3bee-138">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c3bee-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3bee-139">System-Only</span></span>            | <span data-ttu-id="c3bee-140">True</span><span class="sxs-lookup"><span data-stu-id="c3bee-140">True</span></span>                                      |
| <span data-ttu-id="c3bee-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c3bee-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c3bee-142">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-142">False</span></span>                                     |
| <span data-ttu-id="c3bee-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c3bee-143">Is Indexed</span></span>             | <span data-ttu-id="c3bee-144">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-144">False</span></span>                                     |
| <span data-ttu-id="c3bee-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c3bee-145">In Global Catalog</span></span>      | <span data-ttu-id="c3bee-146">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-146">False</span></span>                                     |
| <span data-ttu-id="c3bee-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c3bee-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3bee-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c3bee-148">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c3bee-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3bee-149">Range-Lower</span></span>            | <span data-ttu-id="c3bee-150">0</span><span class="sxs-lookup"><span data-stu-id="c3bee-150">0</span></span>                                         |
| <span data-ttu-id="c3bee-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3bee-151">Range-Upper</span></span>            | <span data-ttu-id="c3bee-152">2048</span><span class="sxs-lookup"><span data-stu-id="c3bee-152">2048</span></span>                                      |
| <span data-ttu-id="c3bee-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3bee-153">Search-Flags</span></span>           | <span data-ttu-id="c3bee-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3bee-154">0x00000000</span></span>                                |
| <span data-ttu-id="c3bee-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3bee-155">System-Flags</span></span>           | <span data-ttu-id="c3bee-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3bee-156">0x00000010</span></span>                                |
| <span data-ttu-id="c3bee-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c3bee-157">Classes used in</span></span>        | [<span data-ttu-id="c3bee-158">**Computer**</span><span class="sxs-lookup"><span data-stu-id="c3bee-158">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c3bee-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c3bee-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c3bee-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3bee-160">Entry</span></span> | <span data-ttu-id="c3bee-161">Value</span><span class="sxs-lookup"><span data-stu-id="c3bee-161">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c3bee-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c3bee-162">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c3bee-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3bee-163">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c3bee-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3bee-164">System-Only</span></span>            | <span data-ttu-id="c3bee-165">True</span><span class="sxs-lookup"><span data-stu-id="c3bee-165">True</span></span>                                      |
| <span data-ttu-id="c3bee-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c3bee-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c3bee-167">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-167">False</span></span>                                     |
| <span data-ttu-id="c3bee-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c3bee-168">Is Indexed</span></span>             | <span data-ttu-id="c3bee-169">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-169">False</span></span>                                     |
| <span data-ttu-id="c3bee-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c3bee-170">In Global Catalog</span></span>      | <span data-ttu-id="c3bee-171">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-171">False</span></span>                                     |
| <span data-ttu-id="c3bee-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c3bee-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3bee-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c3bee-173">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c3bee-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3bee-174">Range-Lower</span></span>            | <span data-ttu-id="c3bee-175">0</span><span class="sxs-lookup"><span data-stu-id="c3bee-175">0</span></span>                                         |
| <span data-ttu-id="c3bee-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3bee-176">Range-Upper</span></span>            | <span data-ttu-id="c3bee-177">2048</span><span class="sxs-lookup"><span data-stu-id="c3bee-177">2048</span></span>                                      |
| <span data-ttu-id="c3bee-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3bee-178">Search-Flags</span></span>           | <span data-ttu-id="c3bee-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3bee-179">0x00000000</span></span>                                |
| <span data-ttu-id="c3bee-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3bee-180">System-Flags</span></span>           | <span data-ttu-id="c3bee-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3bee-181">0x00000010</span></span>                                |
| <span data-ttu-id="c3bee-182">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c3bee-182">Classes used in</span></span>        | [<span data-ttu-id="c3bee-183">**Computer**</span><span class="sxs-lookup"><span data-stu-id="c3bee-183">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c3bee-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3bee-184">Windows Server 2008</span></span>



| <span data-ttu-id="c3bee-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3bee-185">Entry</span></span> | <span data-ttu-id="c3bee-186">Value</span><span class="sxs-lookup"><span data-stu-id="c3bee-186">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c3bee-187">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c3bee-187">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c3bee-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3bee-188">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c3bee-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3bee-189">System-Only</span></span>            | <span data-ttu-id="c3bee-190">True</span><span class="sxs-lookup"><span data-stu-id="c3bee-190">True</span></span>                                      |
| <span data-ttu-id="c3bee-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c3bee-191">Is-Single-Valued</span></span>       | <span data-ttu-id="c3bee-192">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-192">False</span></span>                                     |
| <span data-ttu-id="c3bee-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c3bee-193">Is Indexed</span></span>             | <span data-ttu-id="c3bee-194">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-194">False</span></span>                                     |
| <span data-ttu-id="c3bee-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c3bee-195">In Global Catalog</span></span>      | <span data-ttu-id="c3bee-196">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-196">False</span></span>                                     |
| <span data-ttu-id="c3bee-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c3bee-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3bee-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c3bee-198">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c3bee-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3bee-199">Range-Lower</span></span>            | <span data-ttu-id="c3bee-200">0</span><span class="sxs-lookup"><span data-stu-id="c3bee-200">0</span></span>                                         |
| <span data-ttu-id="c3bee-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3bee-201">Range-Upper</span></span>            | <span data-ttu-id="c3bee-202">2048</span><span class="sxs-lookup"><span data-stu-id="c3bee-202">2048</span></span>                                      |
| <span data-ttu-id="c3bee-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3bee-203">Search-Flags</span></span>           | <span data-ttu-id="c3bee-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3bee-204">0x00000000</span></span>                                |
| <span data-ttu-id="c3bee-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3bee-205">System-Flags</span></span>           | <span data-ttu-id="c3bee-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3bee-206">0x00000010</span></span>                                |
| <span data-ttu-id="c3bee-207">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c3bee-207">Classes used in</span></span>        | [<span data-ttu-id="c3bee-208">**Computer**</span><span class="sxs-lookup"><span data-stu-id="c3bee-208">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c3bee-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3bee-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c3bee-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3bee-210">Entry</span></span> | <span data-ttu-id="c3bee-211">Value</span><span class="sxs-lookup"><span data-stu-id="c3bee-211">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c3bee-212">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c3bee-212">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c3bee-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3bee-213">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c3bee-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3bee-214">System-Only</span></span>            | <span data-ttu-id="c3bee-215">True</span><span class="sxs-lookup"><span data-stu-id="c3bee-215">True</span></span>                                      |
| <span data-ttu-id="c3bee-216">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c3bee-216">Is-Single-Valued</span></span>       | <span data-ttu-id="c3bee-217">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-217">False</span></span>                                     |
| <span data-ttu-id="c3bee-218">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c3bee-218">Is Indexed</span></span>             | <span data-ttu-id="c3bee-219">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-219">False</span></span>                                     |
| <span data-ttu-id="c3bee-220">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c3bee-220">In Global Catalog</span></span>      | <span data-ttu-id="c3bee-221">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-221">False</span></span>                                     |
| <span data-ttu-id="c3bee-222">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c3bee-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3bee-223">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c3bee-223">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c3bee-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3bee-224">Range-Lower</span></span>            | <span data-ttu-id="c3bee-225">0</span><span class="sxs-lookup"><span data-stu-id="c3bee-225">0</span></span>                                         |
| <span data-ttu-id="c3bee-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3bee-226">Range-Upper</span></span>            | <span data-ttu-id="c3bee-227">2048</span><span class="sxs-lookup"><span data-stu-id="c3bee-227">2048</span></span>                                      |
| <span data-ttu-id="c3bee-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3bee-228">Search-Flags</span></span>           | <span data-ttu-id="c3bee-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3bee-229">0x00000000</span></span>                                |
| <span data-ttu-id="c3bee-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3bee-230">System-Flags</span></span>           | <span data-ttu-id="c3bee-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3bee-231">0x00000010</span></span>                                |
| <span data-ttu-id="c3bee-232">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c3bee-232">Classes used in</span></span>        | [<span data-ttu-id="c3bee-233">**Computer**</span><span class="sxs-lookup"><span data-stu-id="c3bee-233">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c3bee-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3bee-234">Windows Server 2012</span></span>



| <span data-ttu-id="c3bee-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3bee-235">Entry</span></span> | <span data-ttu-id="c3bee-236">Value</span><span class="sxs-lookup"><span data-stu-id="c3bee-236">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c3bee-237">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c3bee-237">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c3bee-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3bee-238">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c3bee-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3bee-239">System-Only</span></span>            | <span data-ttu-id="c3bee-240">True</span><span class="sxs-lookup"><span data-stu-id="c3bee-240">True</span></span>                                      |
| <span data-ttu-id="c3bee-241">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c3bee-241">Is-Single-Valued</span></span>       | <span data-ttu-id="c3bee-242">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-242">False</span></span>                                     |
| <span data-ttu-id="c3bee-243">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c3bee-243">Is Indexed</span></span>             | <span data-ttu-id="c3bee-244">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-244">False</span></span>                                     |
| <span data-ttu-id="c3bee-245">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c3bee-245">In Global Catalog</span></span>      | <span data-ttu-id="c3bee-246">False</span><span class="sxs-lookup"><span data-stu-id="c3bee-246">False</span></span>                                     |
| <span data-ttu-id="c3bee-247">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c3bee-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3bee-248">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c3bee-248">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c3bee-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3bee-249">Range-Lower</span></span>            | <span data-ttu-id="c3bee-250">0</span><span class="sxs-lookup"><span data-stu-id="c3bee-250">0</span></span>                                         |
| <span data-ttu-id="c3bee-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3bee-251">Range-Upper</span></span>            | <span data-ttu-id="c3bee-252">2048</span><span class="sxs-lookup"><span data-stu-id="c3bee-252">2048</span></span>                                      |
| <span data-ttu-id="c3bee-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3bee-253">Search-Flags</span></span>           | <span data-ttu-id="c3bee-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3bee-254">0x00000000</span></span>                                |
| <span data-ttu-id="c3bee-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3bee-255">System-Flags</span></span>           | <span data-ttu-id="c3bee-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3bee-256">0x00000010</span></span>                                |
| <span data-ttu-id="c3bee-257">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c3bee-257">Classes used in</span></span>        | [<span data-ttu-id="c3bee-258">**Computer**</span><span class="sxs-lookup"><span data-stu-id="c3bee-258">**Computer**</span></span>](c-computer.md)<br/> |



 

 





