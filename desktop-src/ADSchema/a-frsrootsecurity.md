---
title: Atributo FRS-root-Security
description: Descriptor de seguridad de la raíz del conjunto de réplicas para la replicación de archivos.
ms.assetid: 1db92f68-465a-4d93-ad4d-706ef4761ddc
ms.tgt_platform: multiple
keywords:
- FRS-raíz-atributo de AD esquema de AD
- fRSRootSecurity esquema de AD de atributos
topic_type:
- apiref
api_name:
- FRS-Root-Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a84059902998b120ad38215257fdddcb1c21ea6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658528"
---
# <a name="frs-root-security-attribute"></a><span data-ttu-id="5629e-105">Atributo FRS-root-Security</span><span class="sxs-lookup"><span data-stu-id="5629e-105">FRS-Root-Security attribute</span></span>

<span data-ttu-id="5629e-106">Descriptor de seguridad de la raíz del conjunto de réplicas para la replicación de archivos.</span><span class="sxs-lookup"><span data-stu-id="5629e-106">The security descriptor of replica set root for file replication.</span></span>



| <span data-ttu-id="5629e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="5629e-107">Entry</span></span> | <span data-ttu-id="5629e-108">Value</span><span class="sxs-lookup"><span data-stu-id="5629e-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="5629e-109">CN</span><span class="sxs-lookup"><span data-stu-id="5629e-109">CN</span></span>                | <span data-ttu-id="5629e-110">FRS-raíz-seguridad</span><span class="sxs-lookup"><span data-stu-id="5629e-110">FRS-Root-Security</span></span>                                   |
| <span data-ttu-id="5629e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="5629e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5629e-112">fRSRootSecurity</span><span class="sxs-lookup"><span data-stu-id="5629e-112">fRSRootSecurity</span></span>                                     |
| <span data-ttu-id="5629e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5629e-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="5629e-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="5629e-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="5629e-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="5629e-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="5629e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5629e-116">Attribute-Id</span></span>      | <span data-ttu-id="5629e-117">1.2.840.113556.1.4.535</span><span class="sxs-lookup"><span data-stu-id="5629e-117">1.2.840.113556.1.4.535</span></span>                              |
| <span data-ttu-id="5629e-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5629e-118">System-Id-Guid</span></span>    | <span data-ttu-id="5629e-119">5245801f-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="5629e-119">5245801f-ca6a-11d0-afff-0000f80367c1</span></span>                |
| <span data-ttu-id="5629e-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5629e-120">Syntax</span></span>            | [<span data-ttu-id="5629e-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="5629e-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="5629e-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="5629e-122">Implementations</span></span>

-   [<span data-ttu-id="5629e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5629e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5629e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5629e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5629e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5629e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5629e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5629e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5629e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5629e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5629e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5629e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5629e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5629e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="5629e-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="5629e-130">Entry</span></span> | <span data-ttu-id="5629e-131">Value</span><span class="sxs-lookup"><span data-stu-id="5629e-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5629e-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5629e-132">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5629e-133">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="5629e-134">System-Only</span></span>            | <span data-ttu-id="5629e-135">False</span><span class="sxs-lookup"><span data-stu-id="5629e-135">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5629e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="5629e-137">True</span><span class="sxs-lookup"><span data-stu-id="5629e-137">True</span></span>                                                                                                       |
| <span data-ttu-id="5629e-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5629e-138">Is Indexed</span></span>             | <span data-ttu-id="5629e-139">False</span><span class="sxs-lookup"><span data-stu-id="5629e-139">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5629e-140">In Global Catalog</span></span>      | <span data-ttu-id="5629e-141">False</span><span class="sxs-lookup"><span data-stu-id="5629e-141">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5629e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="5629e-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5629e-143">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="5629e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5629e-144">Range-Lower</span></span>            | <span data-ttu-id="5629e-145">0</span><span class="sxs-lookup"><span data-stu-id="5629e-145">0</span></span>                                                                                                          |
| <span data-ttu-id="5629e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5629e-146">Range-Upper</span></span>            | <span data-ttu-id="5629e-147">65535</span><span class="sxs-lookup"><span data-stu-id="5629e-147">65535</span></span>                                                                                                      |
| <span data-ttu-id="5629e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-148">Search-Flags</span></span>           | <span data-ttu-id="5629e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5629e-149">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="5629e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-150">System-Flags</span></span>           | <span data-ttu-id="5629e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5629e-151">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="5629e-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5629e-152">Classes used in</span></span>        | [<span data-ttu-id="5629e-153">**Miembro de NTFRS**</span><span class="sxs-lookup"><span data-stu-id="5629e-153">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="5629e-154">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="5629e-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5629e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5629e-155">Windows Server 2003</span></span>



| <span data-ttu-id="5629e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="5629e-156">Entry</span></span> | <span data-ttu-id="5629e-157">Value</span><span class="sxs-lookup"><span data-stu-id="5629e-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5629e-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5629e-158">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5629e-159">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5629e-160">System-Only</span></span>            | <span data-ttu-id="5629e-161">False</span><span class="sxs-lookup"><span data-stu-id="5629e-161">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5629e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5629e-163">True</span><span class="sxs-lookup"><span data-stu-id="5629e-163">True</span></span>                                                                                                       |
| <span data-ttu-id="5629e-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5629e-164">Is Indexed</span></span>             | <span data-ttu-id="5629e-165">False</span><span class="sxs-lookup"><span data-stu-id="5629e-165">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5629e-166">In Global Catalog</span></span>      | <span data-ttu-id="5629e-167">False</span><span class="sxs-lookup"><span data-stu-id="5629e-167">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5629e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5629e-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5629e-169">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="5629e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5629e-170">Range-Lower</span></span>            | <span data-ttu-id="5629e-171">0</span><span class="sxs-lookup"><span data-stu-id="5629e-171">0</span></span>                                                                                                          |
| <span data-ttu-id="5629e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5629e-172">Range-Upper</span></span>            | <span data-ttu-id="5629e-173">65535</span><span class="sxs-lookup"><span data-stu-id="5629e-173">65535</span></span>                                                                                                      |
| <span data-ttu-id="5629e-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-174">Search-Flags</span></span>           | <span data-ttu-id="5629e-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5629e-175">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="5629e-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-176">System-Flags</span></span>           | <span data-ttu-id="5629e-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5629e-177">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="5629e-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5629e-178">Classes used in</span></span>        | [<span data-ttu-id="5629e-179">**Miembro de NTFRS**</span><span class="sxs-lookup"><span data-stu-id="5629e-179">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="5629e-180">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="5629e-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5629e-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5629e-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5629e-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="5629e-182">Entry</span></span> | <span data-ttu-id="5629e-183">Value</span><span class="sxs-lookup"><span data-stu-id="5629e-183">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5629e-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5629e-184">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5629e-185">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="5629e-186">System-Only</span></span>            | <span data-ttu-id="5629e-187">False</span><span class="sxs-lookup"><span data-stu-id="5629e-187">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5629e-188">Is-Single-Valued</span></span>       | <span data-ttu-id="5629e-189">True</span><span class="sxs-lookup"><span data-stu-id="5629e-189">True</span></span>                                                                                                       |
| <span data-ttu-id="5629e-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5629e-190">Is Indexed</span></span>             | <span data-ttu-id="5629e-191">False</span><span class="sxs-lookup"><span data-stu-id="5629e-191">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5629e-192">In Global Catalog</span></span>      | <span data-ttu-id="5629e-193">False</span><span class="sxs-lookup"><span data-stu-id="5629e-193">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5629e-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="5629e-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5629e-195">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="5629e-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5629e-196">Range-Lower</span></span>            | <span data-ttu-id="5629e-197">0</span><span class="sxs-lookup"><span data-stu-id="5629e-197">0</span></span>                                                                                                          |
| <span data-ttu-id="5629e-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5629e-198">Range-Upper</span></span>            | <span data-ttu-id="5629e-199">65535</span><span class="sxs-lookup"><span data-stu-id="5629e-199">65535</span></span>                                                                                                      |
| <span data-ttu-id="5629e-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-200">Search-Flags</span></span>           | <span data-ttu-id="5629e-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5629e-201">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="5629e-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-202">System-Flags</span></span>           | <span data-ttu-id="5629e-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5629e-203">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="5629e-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5629e-204">Classes used in</span></span>        | [<span data-ttu-id="5629e-205">**Miembro de NTFRS**</span><span class="sxs-lookup"><span data-stu-id="5629e-205">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="5629e-206">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="5629e-206">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5629e-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5629e-207">Windows Server 2008</span></span>



| <span data-ttu-id="5629e-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="5629e-208">Entry</span></span> | <span data-ttu-id="5629e-209">Value</span><span class="sxs-lookup"><span data-stu-id="5629e-209">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5629e-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5629e-210">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5629e-211">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="5629e-212">System-Only</span></span>            | <span data-ttu-id="5629e-213">False</span><span class="sxs-lookup"><span data-stu-id="5629e-213">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-214">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5629e-214">Is-Single-Valued</span></span>       | <span data-ttu-id="5629e-215">True</span><span class="sxs-lookup"><span data-stu-id="5629e-215">True</span></span>                                                                                                       |
| <span data-ttu-id="5629e-216">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5629e-216">Is Indexed</span></span>             | <span data-ttu-id="5629e-217">False</span><span class="sxs-lookup"><span data-stu-id="5629e-217">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-218">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5629e-218">In Global Catalog</span></span>      | <span data-ttu-id="5629e-219">False</span><span class="sxs-lookup"><span data-stu-id="5629e-219">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-220">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5629e-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="5629e-221">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5629e-221">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="5629e-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5629e-222">Range-Lower</span></span>            | <span data-ttu-id="5629e-223">0</span><span class="sxs-lookup"><span data-stu-id="5629e-223">0</span></span>                                                                                                          |
| <span data-ttu-id="5629e-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5629e-224">Range-Upper</span></span>            | <span data-ttu-id="5629e-225">65535</span><span class="sxs-lookup"><span data-stu-id="5629e-225">65535</span></span>                                                                                                      |
| <span data-ttu-id="5629e-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-226">Search-Flags</span></span>           | <span data-ttu-id="5629e-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5629e-227">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="5629e-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-228">System-Flags</span></span>           | <span data-ttu-id="5629e-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5629e-229">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="5629e-230">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5629e-230">Classes used in</span></span>        | [<span data-ttu-id="5629e-231">**Miembro de NTFRS**</span><span class="sxs-lookup"><span data-stu-id="5629e-231">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="5629e-232">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="5629e-232">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5629e-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5629e-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5629e-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="5629e-234">Entry</span></span> | <span data-ttu-id="5629e-235">Value</span><span class="sxs-lookup"><span data-stu-id="5629e-235">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5629e-236">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5629e-236">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5629e-237">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="5629e-238">System-Only</span></span>            | <span data-ttu-id="5629e-239">False</span><span class="sxs-lookup"><span data-stu-id="5629e-239">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-240">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5629e-240">Is-Single-Valued</span></span>       | <span data-ttu-id="5629e-241">True</span><span class="sxs-lookup"><span data-stu-id="5629e-241">True</span></span>                                                                                                       |
| <span data-ttu-id="5629e-242">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5629e-242">Is Indexed</span></span>             | <span data-ttu-id="5629e-243">False</span><span class="sxs-lookup"><span data-stu-id="5629e-243">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-244">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5629e-244">In Global Catalog</span></span>      | <span data-ttu-id="5629e-245">False</span><span class="sxs-lookup"><span data-stu-id="5629e-245">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-246">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5629e-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="5629e-247">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5629e-247">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="5629e-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5629e-248">Range-Lower</span></span>            | <span data-ttu-id="5629e-249">0</span><span class="sxs-lookup"><span data-stu-id="5629e-249">0</span></span>                                                                                                          |
| <span data-ttu-id="5629e-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5629e-250">Range-Upper</span></span>            | <span data-ttu-id="5629e-251">65535</span><span class="sxs-lookup"><span data-stu-id="5629e-251">65535</span></span>                                                                                                      |
| <span data-ttu-id="5629e-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-252">Search-Flags</span></span>           | <span data-ttu-id="5629e-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5629e-253">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="5629e-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-254">System-Flags</span></span>           | <span data-ttu-id="5629e-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5629e-255">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="5629e-256">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5629e-256">Classes used in</span></span>        | [<span data-ttu-id="5629e-257">**Miembro de NTFRS**</span><span class="sxs-lookup"><span data-stu-id="5629e-257">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="5629e-258">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="5629e-258">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5629e-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5629e-259">Windows Server 2012</span></span>



| <span data-ttu-id="5629e-260">Entrada</span><span class="sxs-lookup"><span data-stu-id="5629e-260">Entry</span></span> | <span data-ttu-id="5629e-261">Value</span><span class="sxs-lookup"><span data-stu-id="5629e-261">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5629e-262">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5629e-262">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5629e-263">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="5629e-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="5629e-264">System-Only</span></span>            | <span data-ttu-id="5629e-265">False</span><span class="sxs-lookup"><span data-stu-id="5629e-265">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-266">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5629e-266">Is-Single-Valued</span></span>       | <span data-ttu-id="5629e-267">True</span><span class="sxs-lookup"><span data-stu-id="5629e-267">True</span></span>                                                                                                       |
| <span data-ttu-id="5629e-268">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5629e-268">Is Indexed</span></span>             | <span data-ttu-id="5629e-269">False</span><span class="sxs-lookup"><span data-stu-id="5629e-269">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-270">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5629e-270">In Global Catalog</span></span>      | <span data-ttu-id="5629e-271">False</span><span class="sxs-lookup"><span data-stu-id="5629e-271">False</span></span>                                                                                                      |
| <span data-ttu-id="5629e-272">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5629e-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="5629e-273">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5629e-273">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="5629e-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5629e-274">Range-Lower</span></span>            | <span data-ttu-id="5629e-275">0</span><span class="sxs-lookup"><span data-stu-id="5629e-275">0</span></span>                                                                                                          |
| <span data-ttu-id="5629e-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5629e-276">Range-Upper</span></span>            | <span data-ttu-id="5629e-277">65535</span><span class="sxs-lookup"><span data-stu-id="5629e-277">65535</span></span>                                                                                                      |
| <span data-ttu-id="5629e-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-278">Search-Flags</span></span>           | <span data-ttu-id="5629e-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5629e-279">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="5629e-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5629e-280">System-Flags</span></span>           | <span data-ttu-id="5629e-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5629e-281">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="5629e-282">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5629e-282">Classes used in</span></span>        | [<span data-ttu-id="5629e-283">**Miembro de NTFRS**</span><span class="sxs-lookup"><span data-stu-id="5629e-283">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="5629e-284">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="5629e-284">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





