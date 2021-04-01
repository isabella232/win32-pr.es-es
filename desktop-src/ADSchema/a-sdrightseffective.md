---
title: 'SD: atributo de derechos efectivos'
description: Este atributo construido devuelve un valor DWORD único que puede tener hasta tres bits establecer seguridad de \_ propietario \_ INFORMATIONDACL \_ seguridad \_ INFORMATIONSACL \_ \_ información de seguridad si se establece un bit, el usuario tiene acceso de escritura a la parte correspondiente del descriptor de seguridad. Propietario significa el propietario y el grupo.
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- 'SD: esquema de AD de atributos efectivos'
- sDRightsEffective esquema de AD de atributos
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac449cd18b3fb75a61f04fffc266c290b7763295
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905925"
---
# <a name="sd-rights-effective-attribute"></a><span data-ttu-id="bda29-106">SD: atributo de derechos efectivos</span><span class="sxs-lookup"><span data-stu-id="bda29-106">SD-Rights-Effective attribute</span></span>

<span data-ttu-id="bda29-107">Este atributo construido devuelve un valor **DWORD** único que puede tener hasta tres bits establecidos:</span><span class="sxs-lookup"><span data-stu-id="bda29-107">This constructed attribute returns a single **DWORD** value that can have up to three bits set:</span></span>

-   <span data-ttu-id="bda29-108">\_información de seguridad del propietario \_</span><span class="sxs-lookup"><span data-stu-id="bda29-108">OWNER\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="bda29-109">\_información de seguridad de DACL \_</span><span class="sxs-lookup"><span data-stu-id="bda29-109">DACL\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="bda29-110">\_información de seguridad de SACL \_</span><span class="sxs-lookup"><span data-stu-id="bda29-110">SACL\_SECURITY\_INFORMATION</span></span>

<span data-ttu-id="bda29-111">Si se establece un bit, el usuario tiene acceso de escritura a la parte correspondiente del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bda29-111">If a bit is set, then the user has write access to the corresponding part of the security descriptor.</span></span> <span data-ttu-id="bda29-112">Propietario significa el propietario y el grupo.</span><span class="sxs-lookup"><span data-stu-id="bda29-112">Owner means both owner and group.</span></span>



| <span data-ttu-id="bda29-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="bda29-113">Entry</span></span> | <span data-ttu-id="bda29-114">Value</span><span class="sxs-lookup"><span data-stu-id="bda29-114">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bda29-115">CN</span><span class="sxs-lookup"><span data-stu-id="bda29-115">CN</span></span>                | <span data-ttu-id="bda29-116">SD-derechos-efectivos</span><span class="sxs-lookup"><span data-stu-id="bda29-116">SD-Rights-Effective</span></span>                  |
| <span data-ttu-id="bda29-117">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="bda29-117">Ldap-Display-Name</span></span> | <span data-ttu-id="bda29-118">sDRightsEffective</span><span class="sxs-lookup"><span data-stu-id="bda29-118">sDRightsEffective</span></span>                    |
| <span data-ttu-id="bda29-119">Tamaño</span><span class="sxs-lookup"><span data-stu-id="bda29-119">Size</span></span>              | \-                                   |
| <span data-ttu-id="bda29-120">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="bda29-120">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="bda29-121">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="bda29-121">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="bda29-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bda29-122">Attribute-Id</span></span>      | <span data-ttu-id="bda29-123">1.2.840.113556.1.4.1304</span><span class="sxs-lookup"><span data-stu-id="bda29-123">1.2.840.113556.1.4.1304</span></span>              |
| <span data-ttu-id="bda29-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bda29-124">System-Id-Guid</span></span>    | <span data-ttu-id="bda29-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="bda29-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="bda29-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bda29-126">Syntax</span></span>            | [<span data-ttu-id="bda29-127">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="bda29-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="bda29-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="bda29-128">Implementations</span></span>

-   [<span data-ttu-id="bda29-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bda29-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bda29-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bda29-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bda29-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bda29-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bda29-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bda29-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bda29-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bda29-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bda29-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bda29-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bda29-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bda29-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bda29-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bda29-136">Windows 2000 Server</span></span>



| <span data-ttu-id="bda29-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="bda29-137">Entry</span></span> | <span data-ttu-id="bda29-138">Value</span><span class="sxs-lookup"><span data-stu-id="bda29-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bda29-139">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bda29-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda29-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda29-141">System-Only</span></span>            | <span data-ttu-id="bda29-142">False</span><span class="sxs-lookup"><span data-stu-id="bda29-142">False</span></span>                           |
| <span data-ttu-id="bda29-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bda29-143">Is-Single-Valued</span></span>       | <span data-ttu-id="bda29-144">True</span><span class="sxs-lookup"><span data-stu-id="bda29-144">True</span></span>                            |
| <span data-ttu-id="bda29-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bda29-145">Is Indexed</span></span>             | <span data-ttu-id="bda29-146">False</span><span class="sxs-lookup"><span data-stu-id="bda29-146">False</span></span>                           |
| <span data-ttu-id="bda29-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bda29-147">In Global Catalog</span></span>      | <span data-ttu-id="bda29-148">False</span><span class="sxs-lookup"><span data-stu-id="bda29-148">False</span></span>                           |
| <span data-ttu-id="bda29-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bda29-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda29-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bda29-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bda29-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda29-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bda29-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda29-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bda29-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-153">Search-Flags</span></span>           | <span data-ttu-id="bda29-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda29-154">0x00000000</span></span>                      |
| <span data-ttu-id="bda29-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-155">System-Flags</span></span>           | <span data-ttu-id="bda29-156">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bda29-156">0x08000014</span></span>                      |
| <span data-ttu-id="bda29-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bda29-157">Classes used in</span></span>        | [<span data-ttu-id="bda29-158">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="bda29-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bda29-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bda29-159">Windows Server 2003</span></span>



| <span data-ttu-id="bda29-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="bda29-160">Entry</span></span> | <span data-ttu-id="bda29-161">Value</span><span class="sxs-lookup"><span data-stu-id="bda29-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bda29-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bda29-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda29-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda29-164">System-Only</span></span>            | <span data-ttu-id="bda29-165">False</span><span class="sxs-lookup"><span data-stu-id="bda29-165">False</span></span>                           |
| <span data-ttu-id="bda29-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bda29-166">Is-Single-Valued</span></span>       | <span data-ttu-id="bda29-167">True</span><span class="sxs-lookup"><span data-stu-id="bda29-167">True</span></span>                            |
| <span data-ttu-id="bda29-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bda29-168">Is Indexed</span></span>             | <span data-ttu-id="bda29-169">False</span><span class="sxs-lookup"><span data-stu-id="bda29-169">False</span></span>                           |
| <span data-ttu-id="bda29-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bda29-170">In Global Catalog</span></span>      | <span data-ttu-id="bda29-171">False</span><span class="sxs-lookup"><span data-stu-id="bda29-171">False</span></span>                           |
| <span data-ttu-id="bda29-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bda29-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda29-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bda29-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bda29-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda29-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bda29-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda29-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bda29-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-176">Search-Flags</span></span>           | <span data-ttu-id="bda29-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda29-177">0x00000000</span></span>                      |
| <span data-ttu-id="bda29-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-178">System-Flags</span></span>           | <span data-ttu-id="bda29-179">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bda29-179">0x08000014</span></span>                      |
| <span data-ttu-id="bda29-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bda29-180">Classes used in</span></span>        | [<span data-ttu-id="bda29-181">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="bda29-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bda29-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="bda29-182">ADAM</span></span>



| <span data-ttu-id="bda29-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="bda29-183">Entry</span></span> | <span data-ttu-id="bda29-184">Value</span><span class="sxs-lookup"><span data-stu-id="bda29-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bda29-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bda29-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda29-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda29-187">System-Only</span></span>            | <span data-ttu-id="bda29-188">False</span><span class="sxs-lookup"><span data-stu-id="bda29-188">False</span></span>                           |
| <span data-ttu-id="bda29-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bda29-189">Is-Single-Valued</span></span>       | <span data-ttu-id="bda29-190">True</span><span class="sxs-lookup"><span data-stu-id="bda29-190">True</span></span>                            |
| <span data-ttu-id="bda29-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bda29-191">Is Indexed</span></span>             | <span data-ttu-id="bda29-192">False</span><span class="sxs-lookup"><span data-stu-id="bda29-192">False</span></span>                           |
| <span data-ttu-id="bda29-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bda29-193">In Global Catalog</span></span>      | <span data-ttu-id="bda29-194">False</span><span class="sxs-lookup"><span data-stu-id="bda29-194">False</span></span>                           |
| <span data-ttu-id="bda29-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bda29-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda29-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bda29-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bda29-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda29-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bda29-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda29-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bda29-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-199">Search-Flags</span></span>           | <span data-ttu-id="bda29-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda29-200">0x00000000</span></span>                      |
| <span data-ttu-id="bda29-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-201">System-Flags</span></span>           | <span data-ttu-id="bda29-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bda29-202">0x08000014</span></span>                      |
| <span data-ttu-id="bda29-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bda29-203">Classes used in</span></span>        | [<span data-ttu-id="bda29-204">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="bda29-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bda29-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bda29-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bda29-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="bda29-206">Entry</span></span> | <span data-ttu-id="bda29-207">Value</span><span class="sxs-lookup"><span data-stu-id="bda29-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bda29-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bda29-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda29-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda29-210">System-Only</span></span>            | <span data-ttu-id="bda29-211">False</span><span class="sxs-lookup"><span data-stu-id="bda29-211">False</span></span>                           |
| <span data-ttu-id="bda29-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bda29-212">Is-Single-Valued</span></span>       | <span data-ttu-id="bda29-213">True</span><span class="sxs-lookup"><span data-stu-id="bda29-213">True</span></span>                            |
| <span data-ttu-id="bda29-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bda29-214">Is Indexed</span></span>             | <span data-ttu-id="bda29-215">False</span><span class="sxs-lookup"><span data-stu-id="bda29-215">False</span></span>                           |
| <span data-ttu-id="bda29-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bda29-216">In Global Catalog</span></span>      | <span data-ttu-id="bda29-217">False</span><span class="sxs-lookup"><span data-stu-id="bda29-217">False</span></span>                           |
| <span data-ttu-id="bda29-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bda29-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda29-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bda29-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bda29-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda29-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bda29-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda29-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bda29-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-222">Search-Flags</span></span>           | <span data-ttu-id="bda29-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda29-223">0x00000000</span></span>                      |
| <span data-ttu-id="bda29-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-224">System-Flags</span></span>           | <span data-ttu-id="bda29-225">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bda29-225">0x08000014</span></span>                      |
| <span data-ttu-id="bda29-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bda29-226">Classes used in</span></span>        | [<span data-ttu-id="bda29-227">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="bda29-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bda29-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bda29-228">Windows Server 2008</span></span>



| <span data-ttu-id="bda29-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="bda29-229">Entry</span></span> | <span data-ttu-id="bda29-230">Value</span><span class="sxs-lookup"><span data-stu-id="bda29-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bda29-231">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bda29-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda29-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda29-233">System-Only</span></span>            | <span data-ttu-id="bda29-234">False</span><span class="sxs-lookup"><span data-stu-id="bda29-234">False</span></span>                           |
| <span data-ttu-id="bda29-235">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bda29-235">Is-Single-Valued</span></span>       | <span data-ttu-id="bda29-236">True</span><span class="sxs-lookup"><span data-stu-id="bda29-236">True</span></span>                            |
| <span data-ttu-id="bda29-237">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bda29-237">Is Indexed</span></span>             | <span data-ttu-id="bda29-238">False</span><span class="sxs-lookup"><span data-stu-id="bda29-238">False</span></span>                           |
| <span data-ttu-id="bda29-239">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bda29-239">In Global Catalog</span></span>      | <span data-ttu-id="bda29-240">False</span><span class="sxs-lookup"><span data-stu-id="bda29-240">False</span></span>                           |
| <span data-ttu-id="bda29-241">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bda29-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda29-242">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bda29-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bda29-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda29-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bda29-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda29-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bda29-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-245">Search-Flags</span></span>           | <span data-ttu-id="bda29-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda29-246">0x00000000</span></span>                      |
| <span data-ttu-id="bda29-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-247">System-Flags</span></span>           | <span data-ttu-id="bda29-248">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bda29-248">0x08000014</span></span>                      |
| <span data-ttu-id="bda29-249">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bda29-249">Classes used in</span></span>        | [<span data-ttu-id="bda29-250">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="bda29-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bda29-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bda29-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bda29-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="bda29-252">Entry</span></span> | <span data-ttu-id="bda29-253">Value</span><span class="sxs-lookup"><span data-stu-id="bda29-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bda29-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bda29-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda29-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda29-256">System-Only</span></span>            | <span data-ttu-id="bda29-257">False</span><span class="sxs-lookup"><span data-stu-id="bda29-257">False</span></span>                           |
| <span data-ttu-id="bda29-258">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bda29-258">Is-Single-Valued</span></span>       | <span data-ttu-id="bda29-259">True</span><span class="sxs-lookup"><span data-stu-id="bda29-259">True</span></span>                            |
| <span data-ttu-id="bda29-260">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bda29-260">Is Indexed</span></span>             | <span data-ttu-id="bda29-261">False</span><span class="sxs-lookup"><span data-stu-id="bda29-261">False</span></span>                           |
| <span data-ttu-id="bda29-262">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bda29-262">In Global Catalog</span></span>      | <span data-ttu-id="bda29-263">False</span><span class="sxs-lookup"><span data-stu-id="bda29-263">False</span></span>                           |
| <span data-ttu-id="bda29-264">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bda29-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda29-265">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bda29-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bda29-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda29-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bda29-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda29-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bda29-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-268">Search-Flags</span></span>           | <span data-ttu-id="bda29-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda29-269">0x00000000</span></span>                      |
| <span data-ttu-id="bda29-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-270">System-Flags</span></span>           | <span data-ttu-id="bda29-271">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bda29-271">0x08000014</span></span>                      |
| <span data-ttu-id="bda29-272">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bda29-272">Classes used in</span></span>        | [<span data-ttu-id="bda29-273">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="bda29-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bda29-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bda29-274">Windows Server 2012</span></span>



| <span data-ttu-id="bda29-275">Entrada</span><span class="sxs-lookup"><span data-stu-id="bda29-275">Entry</span></span> | <span data-ttu-id="bda29-276">Value</span><span class="sxs-lookup"><span data-stu-id="bda29-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bda29-277">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="bda29-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bda29-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bda29-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="bda29-279">System-Only</span></span>            | <span data-ttu-id="bda29-280">False</span><span class="sxs-lookup"><span data-stu-id="bda29-280">False</span></span>                           |
| <span data-ttu-id="bda29-281">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="bda29-281">Is-Single-Valued</span></span>       | <span data-ttu-id="bda29-282">True</span><span class="sxs-lookup"><span data-stu-id="bda29-282">True</span></span>                            |
| <span data-ttu-id="bda29-283">Está indexado</span><span class="sxs-lookup"><span data-stu-id="bda29-283">Is Indexed</span></span>             | <span data-ttu-id="bda29-284">False</span><span class="sxs-lookup"><span data-stu-id="bda29-284">False</span></span>                           |
| <span data-ttu-id="bda29-285">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="bda29-285">In Global Catalog</span></span>      | <span data-ttu-id="bda29-286">False</span><span class="sxs-lookup"><span data-stu-id="bda29-286">False</span></span>                           |
| <span data-ttu-id="bda29-287">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="bda29-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="bda29-288">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bda29-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bda29-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bda29-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bda29-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bda29-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bda29-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-291">Search-Flags</span></span>           | <span data-ttu-id="bda29-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bda29-292">0x00000000</span></span>                      |
| <span data-ttu-id="bda29-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bda29-293">System-Flags</span></span>           | <span data-ttu-id="bda29-294">0x08000014</span><span class="sxs-lookup"><span data-stu-id="bda29-294">0x08000014</span></span>                      |
| <span data-ttu-id="bda29-295">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="bda29-295">Classes used in</span></span>        | [<span data-ttu-id="bda29-296">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="bda29-296">**Top**</span></span>](c-top.md)<br/> |



 

 





