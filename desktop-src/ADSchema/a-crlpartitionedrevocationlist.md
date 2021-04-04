---
title: CRL-Particionad-revocación-atributo de lista
description: Infraestructura de clave pública \ 8211; listas de revocación.
ms.assetid: ecee7ee6-21e7-4861-a7f5-5e8e3579978a
ms.tgt_platform: multiple
keywords:
- CRL-Particionad-revocación-esquema de AD de atributo de lista
- cRLPartitionedRevocationList esquema de AD de atributos
topic_type:
- apiref
api_name:
- CRL-Partitioned-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6c19629cab11e9e6e02069213487135bea4d2aa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906263"
---
# <a name="crl-partitioned-revocation-list-attribute"></a><span data-ttu-id="19809-105">CRL-Particionad-revocación-atributo de lista</span><span class="sxs-lookup"><span data-stu-id="19809-105">CRL-Partitioned-Revocation-List attribute</span></span>

<span data-ttu-id="19809-106">Listas de revocación de infraestructura de clave pública.</span><span class="sxs-lookup"><span data-stu-id="19809-106">Public Key Infrastructure revocation lists.</span></span>



| <span data-ttu-id="19809-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="19809-107">Entry</span></span> | <span data-ttu-id="19809-108">Value</span><span class="sxs-lookup"><span data-stu-id="19809-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="19809-109">CN</span><span class="sxs-lookup"><span data-stu-id="19809-109">CN</span></span>                | <span data-ttu-id="19809-110">CRL con particiones-lista de revocación</span><span class="sxs-lookup"><span data-stu-id="19809-110">CRL-Partitioned-Revocation-List</span></span>                       |
| <span data-ttu-id="19809-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="19809-111">Ldap-Display-Name</span></span> | <span data-ttu-id="19809-112">cRLPartitionedRevocationList</span><span class="sxs-lookup"><span data-stu-id="19809-112">cRLPartitionedRevocationList</span></span>                          |
| <span data-ttu-id="19809-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="19809-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="19809-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="19809-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="19809-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="19809-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="19809-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="19809-116">Attribute-Id</span></span>      | <span data-ttu-id="19809-117">1.2.840.113556.1.4.683</span><span class="sxs-lookup"><span data-stu-id="19809-117">1.2.840.113556.1.4.683</span></span>                                |
| <span data-ttu-id="19809-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="19809-118">System-Id-Guid</span></span>    | <span data-ttu-id="19809-119">963d2731-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="19809-119">963d2731-48be-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="19809-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19809-120">Syntax</span></span>            | [<span data-ttu-id="19809-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="19809-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="19809-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="19809-122">Implementations</span></span>

-   [<span data-ttu-id="19809-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="19809-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="19809-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="19809-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="19809-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="19809-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="19809-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="19809-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="19809-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="19809-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="19809-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="19809-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="19809-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="19809-129">Windows 2000 Server</span></span>



| <span data-ttu-id="19809-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="19809-130">Entry</span></span> | <span data-ttu-id="19809-131">Value</span><span class="sxs-lookup"><span data-stu-id="19809-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="19809-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19809-132">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19809-133">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="19809-134">System-Only</span></span>            | <span data-ttu-id="19809-135">False</span><span class="sxs-lookup"><span data-stu-id="19809-135">False</span></span>                                                               |
| <span data-ttu-id="19809-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19809-136">Is-Single-Valued</span></span>       | <span data-ttu-id="19809-137">True</span><span class="sxs-lookup"><span data-stu-id="19809-137">True</span></span>                                                                |
| <span data-ttu-id="19809-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19809-138">Is Indexed</span></span>             | <span data-ttu-id="19809-139">False</span><span class="sxs-lookup"><span data-stu-id="19809-139">False</span></span>                                                               |
| <span data-ttu-id="19809-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19809-140">In Global Catalog</span></span>      | <span data-ttu-id="19809-141">False</span><span class="sxs-lookup"><span data-stu-id="19809-141">False</span></span>                                                               |
| <span data-ttu-id="19809-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19809-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="19809-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19809-143">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="19809-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19809-144">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19809-145">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-146">Search-Flags</span></span>           | <span data-ttu-id="19809-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19809-147">0x00000000</span></span>                                                          |
| <span data-ttu-id="19809-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-148">System-Flags</span></span>           | <span data-ttu-id="19809-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19809-149">0x00000010</span></span>                                                          |
| <span data-ttu-id="19809-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19809-150">Classes used in</span></span>        | [<span data-ttu-id="19809-151">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="19809-151">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="19809-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="19809-152">Windows Server 2003</span></span>



| <span data-ttu-id="19809-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="19809-153">Entry</span></span> | <span data-ttu-id="19809-154">Value</span><span class="sxs-lookup"><span data-stu-id="19809-154">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="19809-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19809-155">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19809-156">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="19809-157">System-Only</span></span>            | <span data-ttu-id="19809-158">False</span><span class="sxs-lookup"><span data-stu-id="19809-158">False</span></span>                                                               |
| <span data-ttu-id="19809-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19809-159">Is-Single-Valued</span></span>       | <span data-ttu-id="19809-160">True</span><span class="sxs-lookup"><span data-stu-id="19809-160">True</span></span>                                                                |
| <span data-ttu-id="19809-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19809-161">Is Indexed</span></span>             | <span data-ttu-id="19809-162">False</span><span class="sxs-lookup"><span data-stu-id="19809-162">False</span></span>                                                               |
| <span data-ttu-id="19809-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19809-163">In Global Catalog</span></span>      | <span data-ttu-id="19809-164">False</span><span class="sxs-lookup"><span data-stu-id="19809-164">False</span></span>                                                               |
| <span data-ttu-id="19809-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19809-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="19809-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19809-166">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="19809-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19809-167">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19809-168">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-169">Search-Flags</span></span>           | <span data-ttu-id="19809-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19809-170">0x00000000</span></span>                                                          |
| <span data-ttu-id="19809-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-171">System-Flags</span></span>           | <span data-ttu-id="19809-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19809-172">0x00000010</span></span>                                                          |
| <span data-ttu-id="19809-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19809-173">Classes used in</span></span>        | [<span data-ttu-id="19809-174">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="19809-174">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="19809-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="19809-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="19809-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="19809-176">Entry</span></span> | <span data-ttu-id="19809-177">Value</span><span class="sxs-lookup"><span data-stu-id="19809-177">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="19809-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19809-178">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19809-179">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="19809-180">System-Only</span></span>            | <span data-ttu-id="19809-181">False</span><span class="sxs-lookup"><span data-stu-id="19809-181">False</span></span>                                                               |
| <span data-ttu-id="19809-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19809-182">Is-Single-Valued</span></span>       | <span data-ttu-id="19809-183">True</span><span class="sxs-lookup"><span data-stu-id="19809-183">True</span></span>                                                                |
| <span data-ttu-id="19809-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19809-184">Is Indexed</span></span>             | <span data-ttu-id="19809-185">False</span><span class="sxs-lookup"><span data-stu-id="19809-185">False</span></span>                                                               |
| <span data-ttu-id="19809-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19809-186">In Global Catalog</span></span>      | <span data-ttu-id="19809-187">False</span><span class="sxs-lookup"><span data-stu-id="19809-187">False</span></span>                                                               |
| <span data-ttu-id="19809-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19809-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="19809-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19809-189">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="19809-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19809-190">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19809-191">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-192">Search-Flags</span></span>           | <span data-ttu-id="19809-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19809-193">0x00000000</span></span>                                                          |
| <span data-ttu-id="19809-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-194">System-Flags</span></span>           | <span data-ttu-id="19809-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19809-195">0x00000010</span></span>                                                          |
| <span data-ttu-id="19809-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19809-196">Classes used in</span></span>        | [<span data-ttu-id="19809-197">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="19809-197">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="19809-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19809-198">Windows Server 2008</span></span>



| <span data-ttu-id="19809-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="19809-199">Entry</span></span> | <span data-ttu-id="19809-200">Value</span><span class="sxs-lookup"><span data-stu-id="19809-200">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="19809-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19809-201">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19809-202">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="19809-203">System-Only</span></span>            | <span data-ttu-id="19809-204">False</span><span class="sxs-lookup"><span data-stu-id="19809-204">False</span></span>                                                               |
| <span data-ttu-id="19809-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19809-205">Is-Single-Valued</span></span>       | <span data-ttu-id="19809-206">True</span><span class="sxs-lookup"><span data-stu-id="19809-206">True</span></span>                                                                |
| <span data-ttu-id="19809-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19809-207">Is Indexed</span></span>             | <span data-ttu-id="19809-208">False</span><span class="sxs-lookup"><span data-stu-id="19809-208">False</span></span>                                                               |
| <span data-ttu-id="19809-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19809-209">In Global Catalog</span></span>      | <span data-ttu-id="19809-210">False</span><span class="sxs-lookup"><span data-stu-id="19809-210">False</span></span>                                                               |
| <span data-ttu-id="19809-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19809-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="19809-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19809-212">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="19809-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19809-213">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19809-214">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-215">Search-Flags</span></span>           | <span data-ttu-id="19809-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19809-216">0x00000000</span></span>                                                          |
| <span data-ttu-id="19809-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-217">System-Flags</span></span>           | <span data-ttu-id="19809-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19809-218">0x00000010</span></span>                                                          |
| <span data-ttu-id="19809-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19809-219">Classes used in</span></span>        | [<span data-ttu-id="19809-220">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="19809-220">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="19809-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19809-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="19809-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="19809-222">Entry</span></span> | <span data-ttu-id="19809-223">Value</span><span class="sxs-lookup"><span data-stu-id="19809-223">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="19809-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19809-224">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19809-225">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="19809-226">System-Only</span></span>            | <span data-ttu-id="19809-227">False</span><span class="sxs-lookup"><span data-stu-id="19809-227">False</span></span>                                                               |
| <span data-ttu-id="19809-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19809-228">Is-Single-Valued</span></span>       | <span data-ttu-id="19809-229">True</span><span class="sxs-lookup"><span data-stu-id="19809-229">True</span></span>                                                                |
| <span data-ttu-id="19809-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19809-230">Is Indexed</span></span>             | <span data-ttu-id="19809-231">False</span><span class="sxs-lookup"><span data-stu-id="19809-231">False</span></span>                                                               |
| <span data-ttu-id="19809-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19809-232">In Global Catalog</span></span>      | <span data-ttu-id="19809-233">False</span><span class="sxs-lookup"><span data-stu-id="19809-233">False</span></span>                                                               |
| <span data-ttu-id="19809-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19809-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="19809-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19809-235">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="19809-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19809-236">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19809-237">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-238">Search-Flags</span></span>           | <span data-ttu-id="19809-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19809-239">0x00000000</span></span>                                                          |
| <span data-ttu-id="19809-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-240">System-Flags</span></span>           | <span data-ttu-id="19809-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19809-241">0x00000010</span></span>                                                          |
| <span data-ttu-id="19809-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19809-242">Classes used in</span></span>        | [<span data-ttu-id="19809-243">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="19809-243">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="19809-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19809-244">Windows Server 2012</span></span>



| <span data-ttu-id="19809-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="19809-245">Entry</span></span> | <span data-ttu-id="19809-246">Value</span><span class="sxs-lookup"><span data-stu-id="19809-246">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="19809-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="19809-247">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19809-248">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="19809-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="19809-249">System-Only</span></span>            | <span data-ttu-id="19809-250">False</span><span class="sxs-lookup"><span data-stu-id="19809-250">False</span></span>                                                               |
| <span data-ttu-id="19809-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="19809-251">Is-Single-Valued</span></span>       | <span data-ttu-id="19809-252">True</span><span class="sxs-lookup"><span data-stu-id="19809-252">True</span></span>                                                                |
| <span data-ttu-id="19809-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="19809-253">Is Indexed</span></span>             | <span data-ttu-id="19809-254">False</span><span class="sxs-lookup"><span data-stu-id="19809-254">False</span></span>                                                               |
| <span data-ttu-id="19809-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="19809-255">In Global Catalog</span></span>      | <span data-ttu-id="19809-256">False</span><span class="sxs-lookup"><span data-stu-id="19809-256">False</span></span>                                                               |
| <span data-ttu-id="19809-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="19809-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="19809-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19809-258">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="19809-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19809-259">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19809-260">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="19809-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-261">Search-Flags</span></span>           | <span data-ttu-id="19809-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19809-262">0x00000000</span></span>                                                          |
| <span data-ttu-id="19809-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19809-263">System-Flags</span></span>           | <span data-ttu-id="19809-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19809-264">0x00000010</span></span>                                                          |
| <span data-ttu-id="19809-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="19809-265">Classes used in</span></span>        | [<span data-ttu-id="19809-266">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="19809-266">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





