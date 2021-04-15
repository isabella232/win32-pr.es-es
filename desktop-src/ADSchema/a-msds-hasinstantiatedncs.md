---
title: atributo MS-DS-ha-created-NC
description: Información de estado de replicación de DS, análoga a (y un superconjunto de) los atributos existentes hasMasterNCs y hasPartialReplicaNCs. Que va a usar el KCC al configurar los asociados de replicación.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- MS-DS-ha-created-NC atributo AD Schema
- Esquema de AD de atributo msDS-HasInstantiatedNCs
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2900d68f82e859bac7ce1dabbfea2d28fd8998b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493822"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a><span data-ttu-id="cbb49-106">atributo MS-DS-ha-created-NC</span><span class="sxs-lookup"><span data-stu-id="cbb49-106">ms-DS-Has-Instantiated-NCs attribute</span></span>

<span data-ttu-id="cbb49-107">Información de estado de replicación de DS, análoga a (y un superconjunto de) los atributos existentes hasMasterNCs y hasPartialReplicaNCs.</span><span class="sxs-lookup"><span data-stu-id="cbb49-107">DS replication state information, analogous to (and a superset of) the existing attributes hasMasterNCs and hasPartialReplicaNCs.</span></span> <span data-ttu-id="cbb49-108">Que va a usar el KCC al configurar los asociados de replicación.</span><span class="sxs-lookup"><span data-stu-id="cbb49-108">To be used by the KCC when setting up replication partners.</span></span>



| <span data-ttu-id="cbb49-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb49-109">Entry</span></span> | <span data-ttu-id="cbb49-110">Value</span><span class="sxs-lookup"><span data-stu-id="cbb49-110">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb49-111">CN</span><span class="sxs-lookup"><span data-stu-id="cbb49-111">CN</span></span>                | <span data-ttu-id="cbb49-112">MS-DS-se ha creado una instancia-NC</span><span class="sxs-lookup"><span data-stu-id="cbb49-112">ms-DS-Has-Instantiated-NCs</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="cbb49-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="cbb49-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cbb49-114">msDS-HasInstantiatedNCs</span><span class="sxs-lookup"><span data-stu-id="cbb49-114">msDS-HasInstantiatedNCs</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="cbb49-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="cbb49-115">Size</span></span>              | <span data-ttu-id="cbb49-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="cbb49-116">4 bytes</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="cbb49-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="cbb49-117">Update Privilege</span></span>  | <span data-ttu-id="cbb49-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="cbb49-118">This value is set by the system.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="cbb49-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="cbb49-119">Update Frequency</span></span>  | <span data-ttu-id="cbb49-120">Casi el doble de la frecuencia que hasMasterNCs/hasPartialReplicaNCs.</span><span class="sxs-lookup"><span data-stu-id="cbb49-120">Roughly twice as often as hasMasterNCs / hasPartialReplicaNCs.</span></span> <span data-ttu-id="cbb49-121">Estos atributos existentes solo se actualizan cuando el controlador de dominio agrega o quita una partición (por ejemplo, al cambiar de DC a GC o viceversa).</span><span class="sxs-lookup"><span data-stu-id="cbb49-121">These existing attributes are updated only when the DC adds or removes a partition (For example, when changing from DC to GC or vice versa).</span></span> |
| <span data-ttu-id="cbb49-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cbb49-122">Attribute-Id</span></span>      | <span data-ttu-id="cbb49-123">1.2.840.113556.1.4.1709</span><span class="sxs-lookup"><span data-stu-id="cbb49-123">1.2.840.113556.1.4.1709</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="cbb49-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cbb49-124">System-Id-Guid</span></span>    | <span data-ttu-id="cbb49-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span><span class="sxs-lookup"><span data-stu-id="cbb49-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span></span>                                                                                                                                                                        |
| <span data-ttu-id="cbb49-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbb49-126">Syntax</span></span>            | [<span data-ttu-id="cbb49-127">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="cbb49-127">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a><span data-ttu-id="cbb49-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="cbb49-128">Implementations</span></span>

-   [<span data-ttu-id="cbb49-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cbb49-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cbb49-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cbb49-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cbb49-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cbb49-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cbb49-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cbb49-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cbb49-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cbb49-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cbb49-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cbb49-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cbb49-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cbb49-135">Windows Server 2003</span></span>



| <span data-ttu-id="cbb49-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb49-136">Entry</span></span> | <span data-ttu-id="cbb49-137">Value</span><span class="sxs-lookup"><span data-stu-id="cbb49-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="cbb49-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cbb49-138">Link-Id</span></span>                | <span data-ttu-id="cbb49-139">2002</span><span class="sxs-lookup"><span data-stu-id="cbb49-139">2002</span></span>                                     |
| <span data-ttu-id="cbb49-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb49-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="cbb49-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb49-141">System-Only</span></span>            | <span data-ttu-id="cbb49-142">True</span><span class="sxs-lookup"><span data-stu-id="cbb49-142">True</span></span>                                     |
| <span data-ttu-id="cbb49-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cbb49-143">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb49-144">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-144">False</span></span>                                    |
| <span data-ttu-id="cbb49-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cbb49-145">Is Indexed</span></span>             | <span data-ttu-id="cbb49-146">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-146">False</span></span>                                    |
| <span data-ttu-id="cbb49-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cbb49-147">In Global Catalog</span></span>      | <span data-ttu-id="cbb49-148">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-148">False</span></span>                                    |
| <span data-ttu-id="cbb49-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cbb49-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb49-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cbb49-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="cbb49-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb49-151">Range-Lower</span></span>            | <span data-ttu-id="cbb49-152">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-152">4</span></span>                                        |
| <span data-ttu-id="cbb49-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb49-153">Range-Upper</span></span>            | <span data-ttu-id="cbb49-154">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-154">4</span></span>                                        |
| <span data-ttu-id="cbb49-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-155">Search-Flags</span></span>           | <span data-ttu-id="cbb49-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb49-156">0x00000000</span></span>                               |
| <span data-ttu-id="cbb49-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-157">System-Flags</span></span>           | <span data-ttu-id="cbb49-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb49-158">0x00000010</span></span>                               |
| <span data-ttu-id="cbb49-159">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cbb49-159">Classes used in</span></span>        | [<span data-ttu-id="cbb49-160">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="cbb49-160">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cbb49-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="cbb49-161">ADAM</span></span>



| <span data-ttu-id="cbb49-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb49-162">Entry</span></span> | <span data-ttu-id="cbb49-163">Value</span><span class="sxs-lookup"><span data-stu-id="cbb49-163">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="cbb49-164">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cbb49-164">Link-Id</span></span>                | <span data-ttu-id="cbb49-165">2002</span><span class="sxs-lookup"><span data-stu-id="cbb49-165">2002</span></span>                                     |
| <span data-ttu-id="cbb49-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb49-166">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="cbb49-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb49-167">System-Only</span></span>            | <span data-ttu-id="cbb49-168">True</span><span class="sxs-lookup"><span data-stu-id="cbb49-168">True</span></span>                                     |
| <span data-ttu-id="cbb49-169">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cbb49-169">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb49-170">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-170">False</span></span>                                    |
| <span data-ttu-id="cbb49-171">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cbb49-171">Is Indexed</span></span>             | <span data-ttu-id="cbb49-172">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-172">False</span></span>                                    |
| <span data-ttu-id="cbb49-173">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cbb49-173">In Global Catalog</span></span>      | <span data-ttu-id="cbb49-174">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-174">False</span></span>                                    |
| <span data-ttu-id="cbb49-175">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cbb49-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb49-176">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cbb49-176">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="cbb49-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb49-177">Range-Lower</span></span>            | <span data-ttu-id="cbb49-178">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-178">4</span></span>                                        |
| <span data-ttu-id="cbb49-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb49-179">Range-Upper</span></span>            | <span data-ttu-id="cbb49-180">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-180">4</span></span>                                        |
| <span data-ttu-id="cbb49-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-181">Search-Flags</span></span>           | <span data-ttu-id="cbb49-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb49-182">0x00000000</span></span>                               |
| <span data-ttu-id="cbb49-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-183">System-Flags</span></span>           | <span data-ttu-id="cbb49-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb49-184">0x00000010</span></span>                               |
| <span data-ttu-id="cbb49-185">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cbb49-185">Classes used in</span></span>        | [<span data-ttu-id="cbb49-186">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="cbb49-186">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cbb49-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cbb49-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cbb49-188">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb49-188">Entry</span></span> | <span data-ttu-id="cbb49-189">Value</span><span class="sxs-lookup"><span data-stu-id="cbb49-189">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="cbb49-190">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cbb49-190">Link-Id</span></span>                | <span data-ttu-id="cbb49-191">2002</span><span class="sxs-lookup"><span data-stu-id="cbb49-191">2002</span></span>                                     |
| <span data-ttu-id="cbb49-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb49-192">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="cbb49-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb49-193">System-Only</span></span>            | <span data-ttu-id="cbb49-194">True</span><span class="sxs-lookup"><span data-stu-id="cbb49-194">True</span></span>                                     |
| <span data-ttu-id="cbb49-195">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cbb49-195">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb49-196">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-196">False</span></span>                                    |
| <span data-ttu-id="cbb49-197">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cbb49-197">Is Indexed</span></span>             | <span data-ttu-id="cbb49-198">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-198">False</span></span>                                    |
| <span data-ttu-id="cbb49-199">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cbb49-199">In Global Catalog</span></span>      | <span data-ttu-id="cbb49-200">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-200">False</span></span>                                    |
| <span data-ttu-id="cbb49-201">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cbb49-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb49-202">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cbb49-202">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="cbb49-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb49-203">Range-Lower</span></span>            | <span data-ttu-id="cbb49-204">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-204">4</span></span>                                        |
| <span data-ttu-id="cbb49-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb49-205">Range-Upper</span></span>            | <span data-ttu-id="cbb49-206">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-206">4</span></span>                                        |
| <span data-ttu-id="cbb49-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-207">Search-Flags</span></span>           | <span data-ttu-id="cbb49-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb49-208">0x00000000</span></span>                               |
| <span data-ttu-id="cbb49-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-209">System-Flags</span></span>           | <span data-ttu-id="cbb49-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb49-210">0x00000010</span></span>                               |
| <span data-ttu-id="cbb49-211">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cbb49-211">Classes used in</span></span>        | [<span data-ttu-id="cbb49-212">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="cbb49-212">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cbb49-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbb49-213">Windows Server 2008</span></span>



| <span data-ttu-id="cbb49-214">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb49-214">Entry</span></span> | <span data-ttu-id="cbb49-215">Value</span><span class="sxs-lookup"><span data-stu-id="cbb49-215">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="cbb49-216">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cbb49-216">Link-Id</span></span>                | <span data-ttu-id="cbb49-217">2002</span><span class="sxs-lookup"><span data-stu-id="cbb49-217">2002</span></span>                                     |
| <span data-ttu-id="cbb49-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb49-218">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="cbb49-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb49-219">System-Only</span></span>            | <span data-ttu-id="cbb49-220">True</span><span class="sxs-lookup"><span data-stu-id="cbb49-220">True</span></span>                                     |
| <span data-ttu-id="cbb49-221">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cbb49-221">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb49-222">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-222">False</span></span>                                    |
| <span data-ttu-id="cbb49-223">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cbb49-223">Is Indexed</span></span>             | <span data-ttu-id="cbb49-224">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-224">False</span></span>                                    |
| <span data-ttu-id="cbb49-225">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cbb49-225">In Global Catalog</span></span>      | <span data-ttu-id="cbb49-226">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-226">False</span></span>                                    |
| <span data-ttu-id="cbb49-227">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cbb49-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb49-228">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cbb49-228">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="cbb49-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb49-229">Range-Lower</span></span>            | <span data-ttu-id="cbb49-230">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-230">4</span></span>                                        |
| <span data-ttu-id="cbb49-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb49-231">Range-Upper</span></span>            | <span data-ttu-id="cbb49-232">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-232">4</span></span>                                        |
| <span data-ttu-id="cbb49-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-233">Search-Flags</span></span>           | <span data-ttu-id="cbb49-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb49-234">0x00000000</span></span>                               |
| <span data-ttu-id="cbb49-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-235">System-Flags</span></span>           | <span data-ttu-id="cbb49-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb49-236">0x00000010</span></span>                               |
| <span data-ttu-id="cbb49-237">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cbb49-237">Classes used in</span></span>        | [<span data-ttu-id="cbb49-238">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="cbb49-238">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cbb49-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cbb49-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cbb49-240">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb49-240">Entry</span></span> | <span data-ttu-id="cbb49-241">Value</span><span class="sxs-lookup"><span data-stu-id="cbb49-241">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="cbb49-242">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cbb49-242">Link-Id</span></span>                | <span data-ttu-id="cbb49-243">2002</span><span class="sxs-lookup"><span data-stu-id="cbb49-243">2002</span></span>                                     |
| <span data-ttu-id="cbb49-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb49-244">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="cbb49-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb49-245">System-Only</span></span>            | <span data-ttu-id="cbb49-246">True</span><span class="sxs-lookup"><span data-stu-id="cbb49-246">True</span></span>                                     |
| <span data-ttu-id="cbb49-247">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cbb49-247">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb49-248">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-248">False</span></span>                                    |
| <span data-ttu-id="cbb49-249">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cbb49-249">Is Indexed</span></span>             | <span data-ttu-id="cbb49-250">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-250">False</span></span>                                    |
| <span data-ttu-id="cbb49-251">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cbb49-251">In Global Catalog</span></span>      | <span data-ttu-id="cbb49-252">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-252">False</span></span>                                    |
| <span data-ttu-id="cbb49-253">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cbb49-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb49-254">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cbb49-254">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="cbb49-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb49-255">Range-Lower</span></span>            | <span data-ttu-id="cbb49-256">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-256">4</span></span>                                        |
| <span data-ttu-id="cbb49-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb49-257">Range-Upper</span></span>            | <span data-ttu-id="cbb49-258">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-258">4</span></span>                                        |
| <span data-ttu-id="cbb49-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-259">Search-Flags</span></span>           | <span data-ttu-id="cbb49-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb49-260">0x00000000</span></span>                               |
| <span data-ttu-id="cbb49-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-261">System-Flags</span></span>           | <span data-ttu-id="cbb49-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb49-262">0x00000010</span></span>                               |
| <span data-ttu-id="cbb49-263">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cbb49-263">Classes used in</span></span>        | [<span data-ttu-id="cbb49-264">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="cbb49-264">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cbb49-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cbb49-265">Windows Server 2012</span></span>



| <span data-ttu-id="cbb49-266">Entrada</span><span class="sxs-lookup"><span data-stu-id="cbb49-266">Entry</span></span> | <span data-ttu-id="cbb49-267">Value</span><span class="sxs-lookup"><span data-stu-id="cbb49-267">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="cbb49-268">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cbb49-268">Link-Id</span></span>                | <span data-ttu-id="cbb49-269">2002</span><span class="sxs-lookup"><span data-stu-id="cbb49-269">2002</span></span>                                     |
| <span data-ttu-id="cbb49-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cbb49-270">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="cbb49-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="cbb49-271">System-Only</span></span>            | <span data-ttu-id="cbb49-272">True</span><span class="sxs-lookup"><span data-stu-id="cbb49-272">True</span></span>                                     |
| <span data-ttu-id="cbb49-273">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cbb49-273">Is-Single-Valued</span></span>       | <span data-ttu-id="cbb49-274">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-274">False</span></span>                                    |
| <span data-ttu-id="cbb49-275">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cbb49-275">Is Indexed</span></span>             | <span data-ttu-id="cbb49-276">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-276">False</span></span>                                    |
| <span data-ttu-id="cbb49-277">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cbb49-277">In Global Catalog</span></span>      | <span data-ttu-id="cbb49-278">False</span><span class="sxs-lookup"><span data-stu-id="cbb49-278">False</span></span>                                    |
| <span data-ttu-id="cbb49-279">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cbb49-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="cbb49-280">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cbb49-280">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="cbb49-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cbb49-281">Range-Lower</span></span>            | <span data-ttu-id="cbb49-282">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-282">4</span></span>                                        |
| <span data-ttu-id="cbb49-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cbb49-283">Range-Upper</span></span>            | <span data-ttu-id="cbb49-284">4</span><span class="sxs-lookup"><span data-stu-id="cbb49-284">4</span></span>                                        |
| <span data-ttu-id="cbb49-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-285">Search-Flags</span></span>           | <span data-ttu-id="cbb49-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbb49-286">0x00000000</span></span>                               |
| <span data-ttu-id="cbb49-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cbb49-287">System-Flags</span></span>           | <span data-ttu-id="cbb49-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbb49-288">0x00000010</span></span>                               |
| <span data-ttu-id="cbb49-289">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cbb49-289">Classes used in</span></span>        | [<span data-ttu-id="cbb49-290">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="cbb49-290">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





