---
title: atributo MS-DS-SPN-Suffixs
description: Este atributo describe los sufijos de los nombres de host DNS que usan los servidores del bosque. Estos sufijos DNS se compartirán con otros bosques que tengan confianza entre bosques con este bosque.
ms.assetid: 56153832-1228-419f-99d4-eb1ce3edc867
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-SPN-Suffixs
- Esquema de AD de atributo msDS-SPNSuffixes
topic_type:
- apiref
api_name:
- ms-DS-SPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91f7ce8c92e8a81437d90bb0d80383b9ad334ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997432"
---
# <a name="ms-ds-spn-suffixes-attribute"></a><span data-ttu-id="c2ab2-106">atributo MS-DS-SPN-Suffixs</span><span class="sxs-lookup"><span data-stu-id="c2ab2-106">ms-DS-SPN-Suffixes attribute</span></span>

<span data-ttu-id="c2ab2-107">Este atributo describe los sufijos de los nombres de host DNS que usan los servidores del bosque.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-107">This attribute describes the suffixes of DNS host names used by servers in the forest.</span></span> <span data-ttu-id="c2ab2-108">Estos sufijos DNS se compartirán con otros bosques que tengan confianza entre bosques con este bosque.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-108">These DNS suffixes will be shared with other forests that have cross-forest trust with this forest.</span></span>



| <span data-ttu-id="c2ab2-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2ab2-109">Entry</span></span> | <span data-ttu-id="c2ab2-110">Value</span><span class="sxs-lookup"><span data-stu-id="c2ab2-110">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="c2ab2-111">CN</span><span class="sxs-lookup"><span data-stu-id="c2ab2-111">CN</span></span>                | <span data-ttu-id="c2ab2-112">MS-DS-SPN-sufijos</span><span class="sxs-lookup"><span data-stu-id="c2ab2-112">ms-DS-SPN-Suffixes</span></span>                           |
| <span data-ttu-id="c2ab2-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c2ab2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c2ab2-114">msDS-SPNSuffixes</span><span class="sxs-lookup"><span data-stu-id="c2ab2-114">msDS-SPNSuffixes</span></span>                             |
| <span data-ttu-id="c2ab2-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c2ab2-115">Size</span></span>              | <span data-ttu-id="c2ab2-116">255 bytes</span><span class="sxs-lookup"><span data-stu-id="c2ab2-116">255 bytes</span></span>                                    |
| <span data-ttu-id="c2ab2-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c2ab2-117">Update Privilege</span></span>  | <span data-ttu-id="c2ab2-118">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="c2ab2-118">Domain administrator</span></span>                         |
| <span data-ttu-id="c2ab2-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c2ab2-119">Update Frequency</span></span>  | <span data-ttu-id="c2ab2-120">Cuando los servidores del bosque obtienen un nuevo sufijo.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-120">When servers in the forest get a new suffix.</span></span> |
| <span data-ttu-id="c2ab2-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c2ab2-121">Attribute-Id</span></span>      | <span data-ttu-id="c2ab2-122">1.2.840.113556.1.4.1715</span><span class="sxs-lookup"><span data-stu-id="c2ab2-122">1.2.840.113556.1.4.1715</span></span>                      |
| <span data-ttu-id="c2ab2-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c2ab2-123">System-Id-Guid</span></span>    | <span data-ttu-id="c2ab2-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span><span class="sxs-lookup"><span data-stu-id="c2ab2-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span></span>         |
| <span data-ttu-id="c2ab2-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2ab2-125">Syntax</span></span>            | [<span data-ttu-id="c2ab2-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c2ab2-126">**String(Unicode)**</span></span>](s-string-unicode.md)  |



## <a name="implementations"></a><span data-ttu-id="c2ab2-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c2ab2-127">Implementations</span></span>

-   [<span data-ttu-id="c2ab2-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c2ab2-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c2ab2-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c2ab2-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c2ab2-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c2ab2-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c2ab2-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c2ab2-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c2ab2-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c2ab2-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c2ab2-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2ab2-133">Windows Server 2003</span></span>



| <span data-ttu-id="c2ab2-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2ab2-134">Entry</span></span> | <span data-ttu-id="c2ab2-135">Value</span><span class="sxs-lookup"><span data-stu-id="c2ab2-135">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c2ab2-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2ab2-136">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c2ab2-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2ab2-137">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c2ab2-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2ab2-138">System-Only</span></span>            | <span data-ttu-id="c2ab2-139">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-139">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2ab2-140">Is-Single-Valued</span></span>       | <span data-ttu-id="c2ab2-141">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-141">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2ab2-142">Is Indexed</span></span>             | <span data-ttu-id="c2ab2-143">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-143">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2ab2-144">In Global Catalog</span></span>      | <span data-ttu-id="c2ab2-145">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-145">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2ab2-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2ab2-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2ab2-147">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c2ab2-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2ab2-148">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c2ab2-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2ab2-149">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c2ab2-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2ab2-150">Search-Flags</span></span>           | <span data-ttu-id="c2ab2-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2ab2-151">0x00000000</span></span>                                                    |
| <span data-ttu-id="c2ab2-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2ab2-152">System-Flags</span></span>           | <span data-ttu-id="c2ab2-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2ab2-153">0x00000010</span></span>                                                    |
| <span data-ttu-id="c2ab2-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2ab2-154">Classes used in</span></span>        | [<span data-ttu-id="c2ab2-155">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="c2ab2-155">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c2ab2-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c2ab2-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c2ab2-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2ab2-157">Entry</span></span> | <span data-ttu-id="c2ab2-158">Value</span><span class="sxs-lookup"><span data-stu-id="c2ab2-158">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c2ab2-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2ab2-159">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c2ab2-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2ab2-160">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c2ab2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2ab2-161">System-Only</span></span>            | <span data-ttu-id="c2ab2-162">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-162">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2ab2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="c2ab2-164">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-164">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2ab2-165">Is Indexed</span></span>             | <span data-ttu-id="c2ab2-166">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-166">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2ab2-167">In Global Catalog</span></span>      | <span data-ttu-id="c2ab2-168">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-168">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2ab2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2ab2-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2ab2-170">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c2ab2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2ab2-171">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c2ab2-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2ab2-172">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c2ab2-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2ab2-173">Search-Flags</span></span>           | <span data-ttu-id="c2ab2-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2ab2-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="c2ab2-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2ab2-175">System-Flags</span></span>           | <span data-ttu-id="c2ab2-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2ab2-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="c2ab2-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2ab2-177">Classes used in</span></span>        | [<span data-ttu-id="c2ab2-178">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="c2ab2-178">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c2ab2-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2ab2-179">Windows Server 2008</span></span>



| <span data-ttu-id="c2ab2-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2ab2-180">Entry</span></span> | <span data-ttu-id="c2ab2-181">Value</span><span class="sxs-lookup"><span data-stu-id="c2ab2-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c2ab2-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2ab2-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c2ab2-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2ab2-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c2ab2-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2ab2-184">System-Only</span></span>            | <span data-ttu-id="c2ab2-185">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-185">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2ab2-186">Is-Single-Valued</span></span>       | <span data-ttu-id="c2ab2-187">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-187">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2ab2-188">Is Indexed</span></span>             | <span data-ttu-id="c2ab2-189">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-189">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2ab2-190">In Global Catalog</span></span>      | <span data-ttu-id="c2ab2-191">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-191">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2ab2-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2ab2-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2ab2-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c2ab2-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2ab2-194">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c2ab2-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2ab2-195">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c2ab2-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2ab2-196">Search-Flags</span></span>           | <span data-ttu-id="c2ab2-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2ab2-197">0x00000000</span></span>                                                    |
| <span data-ttu-id="c2ab2-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2ab2-198">System-Flags</span></span>           | <span data-ttu-id="c2ab2-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2ab2-199">0x00000010</span></span>                                                    |
| <span data-ttu-id="c2ab2-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2ab2-200">Classes used in</span></span>        | [<span data-ttu-id="c2ab2-201">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="c2ab2-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c2ab2-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2ab2-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c2ab2-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2ab2-203">Entry</span></span> | <span data-ttu-id="c2ab2-204">Value</span><span class="sxs-lookup"><span data-stu-id="c2ab2-204">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c2ab2-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2ab2-205">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c2ab2-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2ab2-206">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c2ab2-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2ab2-207">System-Only</span></span>            | <span data-ttu-id="c2ab2-208">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-208">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2ab2-209">Is-Single-Valued</span></span>       | <span data-ttu-id="c2ab2-210">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-210">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2ab2-211">Is Indexed</span></span>             | <span data-ttu-id="c2ab2-212">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-212">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2ab2-213">In Global Catalog</span></span>      | <span data-ttu-id="c2ab2-214">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-214">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2ab2-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2ab2-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2ab2-216">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c2ab2-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2ab2-217">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c2ab2-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2ab2-218">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c2ab2-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2ab2-219">Search-Flags</span></span>           | <span data-ttu-id="c2ab2-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2ab2-220">0x00000000</span></span>                                                    |
| <span data-ttu-id="c2ab2-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2ab2-221">System-Flags</span></span>           | <span data-ttu-id="c2ab2-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2ab2-222">0x00000010</span></span>                                                    |
| <span data-ttu-id="c2ab2-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2ab2-223">Classes used in</span></span>        | [<span data-ttu-id="c2ab2-224">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="c2ab2-224">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c2ab2-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2ab2-225">Windows Server 2012</span></span>



| <span data-ttu-id="c2ab2-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="c2ab2-226">Entry</span></span> | <span data-ttu-id="c2ab2-227">Value</span><span class="sxs-lookup"><span data-stu-id="c2ab2-227">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c2ab2-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c2ab2-228">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c2ab2-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2ab2-229">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c2ab2-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2ab2-230">System-Only</span></span>            | <span data-ttu-id="c2ab2-231">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-231">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c2ab2-232">Is-Single-Valued</span></span>       | <span data-ttu-id="c2ab2-233">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-233">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c2ab2-234">Is Indexed</span></span>             | <span data-ttu-id="c2ab2-235">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-235">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c2ab2-236">In Global Catalog</span></span>      | <span data-ttu-id="c2ab2-237">False</span><span class="sxs-lookup"><span data-stu-id="c2ab2-237">False</span></span>                                                         |
| <span data-ttu-id="c2ab2-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c2ab2-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2ab2-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c2ab2-239">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c2ab2-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2ab2-240">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c2ab2-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2ab2-241">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c2ab2-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2ab2-242">Search-Flags</span></span>           | <span data-ttu-id="c2ab2-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2ab2-243">0x00000000</span></span>                                                    |
| <span data-ttu-id="c2ab2-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2ab2-244">System-Flags</span></span>           | <span data-ttu-id="c2ab2-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2ab2-245">0x00000010</span></span>                                                    |
| <span data-ttu-id="c2ab2-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c2ab2-246">Classes used in</span></span>        | [<span data-ttu-id="c2ab2-247">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="c2ab2-247">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





