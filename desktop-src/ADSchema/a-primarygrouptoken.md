---
title: Atributo Primary-Group-token
description: Atributo calculado que se usa para recuperar la lista de miembros de un grupo, como usuarios del dominio. La pertenencia completa de estos grupos no se almacena explícitamente por motivos de escala.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de grupo principal-de-token
- primaryGroupToken esquema de AD de atributos
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b237ab5998ca3f38f2d07128b36d9337c96935d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151595"
---
# <a name="primary-group-token-attribute"></a><span data-ttu-id="1ab42-106">Atributo Primary-Group-token</span><span class="sxs-lookup"><span data-stu-id="1ab42-106">Primary-Group-Token attribute</span></span>

<span data-ttu-id="1ab42-107">Atributo calculado que se usa para recuperar la lista de miembros de un grupo, como usuarios del dominio.</span><span class="sxs-lookup"><span data-stu-id="1ab42-107">A computed attribute that is used in retrieving the membership list of a group, such as Domain Users.</span></span> <span data-ttu-id="1ab42-108">La pertenencia completa de estos grupos no se almacena explícitamente por motivos de escala.</span><span class="sxs-lookup"><span data-stu-id="1ab42-108">The complete membership of such groups is not stored explicitly for scaling reasons.</span></span>



| <span data-ttu-id="1ab42-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ab42-109">Entry</span></span> | <span data-ttu-id="1ab42-110">Value</span><span class="sxs-lookup"><span data-stu-id="1ab42-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="1ab42-111">CN</span><span class="sxs-lookup"><span data-stu-id="1ab42-111">CN</span></span>                | <span data-ttu-id="1ab42-112">Token de grupo principal</span><span class="sxs-lookup"><span data-stu-id="1ab42-112">Primary-Group-Token</span></span>                        |
| <span data-ttu-id="1ab42-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1ab42-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1ab42-114">primaryGroupToken</span><span class="sxs-lookup"><span data-stu-id="1ab42-114">primaryGroupToken</span></span>                          |
| <span data-ttu-id="1ab42-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1ab42-115">Size</span></span>              | <span data-ttu-id="1ab42-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="1ab42-116">4 bytes</span></span>                                    |
| <span data-ttu-id="1ab42-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1ab42-117">Update Privilege</span></span>  | <span data-ttu-id="1ab42-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="1ab42-118">This value is set by the system.</span></span>           |
| <span data-ttu-id="1ab42-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1ab42-119">Update Frequency</span></span>  | <span data-ttu-id="1ab42-120">Cada vez que cambia un grupo primario de objetos.</span><span class="sxs-lookup"><span data-stu-id="1ab42-120">Whenever an objects primary group changes.</span></span> |
| <span data-ttu-id="1ab42-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1ab42-121">Attribute-Id</span></span>      | <span data-ttu-id="1ab42-122">1.2.840.113556.1.4.1412</span><span class="sxs-lookup"><span data-stu-id="1ab42-122">1.2.840.113556.1.4.1412</span></span>                    |
| <span data-ttu-id="1ab42-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1ab42-123">System-Id-Guid</span></span>    | <span data-ttu-id="1ab42-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span><span class="sxs-lookup"><span data-stu-id="1ab42-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span></span>       |
| <span data-ttu-id="1ab42-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ab42-125">Syntax</span></span>            | [<span data-ttu-id="1ab42-126">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="1ab42-126">**Enumeration**</span></span>](s-enumeration.md)       |



## <a name="implementations"></a><span data-ttu-id="1ab42-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1ab42-127">Implementations</span></span>

-   [<span data-ttu-id="1ab42-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1ab42-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1ab42-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1ab42-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1ab42-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1ab42-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1ab42-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1ab42-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1ab42-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1ab42-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1ab42-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1ab42-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1ab42-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1ab42-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1ab42-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ab42-135">Windows 2000 Server</span></span>



| <span data-ttu-id="1ab42-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ab42-136">Entry</span></span> | <span data-ttu-id="1ab42-137">Value</span><span class="sxs-lookup"><span data-stu-id="1ab42-137">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1ab42-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1ab42-138">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab42-139">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab42-140">System-Only</span></span>            | <span data-ttu-id="1ab42-141">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-141">True</span></span>                                |
| <span data-ttu-id="1ab42-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1ab42-142">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab42-143">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-143">True</span></span>                                |
| <span data-ttu-id="1ab42-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1ab42-144">Is Indexed</span></span>             | <span data-ttu-id="1ab42-145">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-145">False</span></span>                               |
| <span data-ttu-id="1ab42-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ab42-146">In Global Catalog</span></span>      | <span data-ttu-id="1ab42-147">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-147">False</span></span>                               |
| <span data-ttu-id="1ab42-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1ab42-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab42-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab42-149">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1ab42-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab42-150">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab42-151">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-152">Search-Flags</span></span>           | <span data-ttu-id="1ab42-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab42-153">0x00000000</span></span>                          |
| <span data-ttu-id="1ab42-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-154">System-Flags</span></span>           | <span data-ttu-id="1ab42-155">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1ab42-155">0x00000014</span></span>                          |
| <span data-ttu-id="1ab42-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1ab42-156">Classes used in</span></span>        | [<span data-ttu-id="1ab42-157">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1ab42-157">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1ab42-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ab42-158">Windows Server 2003</span></span>



| <span data-ttu-id="1ab42-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ab42-159">Entry</span></span> | <span data-ttu-id="1ab42-160">Value</span><span class="sxs-lookup"><span data-stu-id="1ab42-160">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1ab42-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1ab42-161">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab42-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab42-163">System-Only</span></span>            | <span data-ttu-id="1ab42-164">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-164">True</span></span>                                |
| <span data-ttu-id="1ab42-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1ab42-165">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab42-166">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-166">True</span></span>                                |
| <span data-ttu-id="1ab42-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1ab42-167">Is Indexed</span></span>             | <span data-ttu-id="1ab42-168">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-168">False</span></span>                               |
| <span data-ttu-id="1ab42-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ab42-169">In Global Catalog</span></span>      | <span data-ttu-id="1ab42-170">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-170">False</span></span>                               |
| <span data-ttu-id="1ab42-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1ab42-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab42-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab42-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1ab42-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab42-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab42-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-175">Search-Flags</span></span>           | <span data-ttu-id="1ab42-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab42-176">0x00000000</span></span>                          |
| <span data-ttu-id="1ab42-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-177">System-Flags</span></span>           | <span data-ttu-id="1ab42-178">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1ab42-178">0x00000014</span></span>                          |
| <span data-ttu-id="1ab42-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1ab42-179">Classes used in</span></span>        | [<span data-ttu-id="1ab42-180">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1ab42-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1ab42-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="1ab42-181">ADAM</span></span>



| <span data-ttu-id="1ab42-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ab42-182">Entry</span></span> | <span data-ttu-id="1ab42-183">Value</span><span class="sxs-lookup"><span data-stu-id="1ab42-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1ab42-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1ab42-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab42-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab42-186">System-Only</span></span>            | <span data-ttu-id="1ab42-187">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-187">True</span></span>                                |
| <span data-ttu-id="1ab42-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1ab42-188">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab42-189">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-189">True</span></span>                                |
| <span data-ttu-id="1ab42-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1ab42-190">Is Indexed</span></span>             | <span data-ttu-id="1ab42-191">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-191">False</span></span>                               |
| <span data-ttu-id="1ab42-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ab42-192">In Global Catalog</span></span>      | <span data-ttu-id="1ab42-193">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-193">False</span></span>                               |
| <span data-ttu-id="1ab42-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1ab42-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab42-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab42-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1ab42-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab42-196">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab42-197">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-198">Search-Flags</span></span>           | <span data-ttu-id="1ab42-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab42-199">0x00000000</span></span>                          |
| <span data-ttu-id="1ab42-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-200">System-Flags</span></span>           | <span data-ttu-id="1ab42-201">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1ab42-201">0x00000014</span></span>                          |
| <span data-ttu-id="1ab42-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1ab42-202">Classes used in</span></span>        | [<span data-ttu-id="1ab42-203">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1ab42-203">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1ab42-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1ab42-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1ab42-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ab42-205">Entry</span></span> | <span data-ttu-id="1ab42-206">Value</span><span class="sxs-lookup"><span data-stu-id="1ab42-206">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1ab42-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1ab42-207">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab42-208">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab42-209">System-Only</span></span>            | <span data-ttu-id="1ab42-210">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-210">True</span></span>                                |
| <span data-ttu-id="1ab42-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1ab42-211">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab42-212">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-212">True</span></span>                                |
| <span data-ttu-id="1ab42-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1ab42-213">Is Indexed</span></span>             | <span data-ttu-id="1ab42-214">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-214">False</span></span>                               |
| <span data-ttu-id="1ab42-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ab42-215">In Global Catalog</span></span>      | <span data-ttu-id="1ab42-216">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-216">False</span></span>                               |
| <span data-ttu-id="1ab42-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1ab42-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab42-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab42-218">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1ab42-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab42-219">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab42-220">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-221">Search-Flags</span></span>           | <span data-ttu-id="1ab42-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab42-222">0x00000000</span></span>                          |
| <span data-ttu-id="1ab42-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-223">System-Flags</span></span>           | <span data-ttu-id="1ab42-224">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1ab42-224">0x00000014</span></span>                          |
| <span data-ttu-id="1ab42-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1ab42-225">Classes used in</span></span>        | [<span data-ttu-id="1ab42-226">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1ab42-226">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1ab42-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ab42-227">Windows Server 2008</span></span>



| <span data-ttu-id="1ab42-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ab42-228">Entry</span></span> | <span data-ttu-id="1ab42-229">Value</span><span class="sxs-lookup"><span data-stu-id="1ab42-229">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1ab42-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1ab42-230">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab42-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab42-232">System-Only</span></span>            | <span data-ttu-id="1ab42-233">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-233">True</span></span>                                |
| <span data-ttu-id="1ab42-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1ab42-234">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab42-235">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-235">True</span></span>                                |
| <span data-ttu-id="1ab42-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1ab42-236">Is Indexed</span></span>             | <span data-ttu-id="1ab42-237">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-237">False</span></span>                               |
| <span data-ttu-id="1ab42-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ab42-238">In Global Catalog</span></span>      | <span data-ttu-id="1ab42-239">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-239">False</span></span>                               |
| <span data-ttu-id="1ab42-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1ab42-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab42-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab42-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1ab42-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab42-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab42-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-244">Search-Flags</span></span>           | <span data-ttu-id="1ab42-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab42-245">0x00000000</span></span>                          |
| <span data-ttu-id="1ab42-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-246">System-Flags</span></span>           | <span data-ttu-id="1ab42-247">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1ab42-247">0x00000014</span></span>                          |
| <span data-ttu-id="1ab42-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1ab42-248">Classes used in</span></span>        | [<span data-ttu-id="1ab42-249">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1ab42-249">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1ab42-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ab42-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1ab42-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ab42-251">Entry</span></span> | <span data-ttu-id="1ab42-252">Value</span><span class="sxs-lookup"><span data-stu-id="1ab42-252">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1ab42-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1ab42-253">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab42-254">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab42-255">System-Only</span></span>            | <span data-ttu-id="1ab42-256">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-256">True</span></span>                                |
| <span data-ttu-id="1ab42-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1ab42-257">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab42-258">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-258">True</span></span>                                |
| <span data-ttu-id="1ab42-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1ab42-259">Is Indexed</span></span>             | <span data-ttu-id="1ab42-260">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-260">False</span></span>                               |
| <span data-ttu-id="1ab42-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ab42-261">In Global Catalog</span></span>      | <span data-ttu-id="1ab42-262">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-262">False</span></span>                               |
| <span data-ttu-id="1ab42-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1ab42-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab42-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab42-264">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1ab42-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab42-265">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab42-266">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-267">Search-Flags</span></span>           | <span data-ttu-id="1ab42-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab42-268">0x00000000</span></span>                          |
| <span data-ttu-id="1ab42-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-269">System-Flags</span></span>           | <span data-ttu-id="1ab42-270">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1ab42-270">0x00000014</span></span>                          |
| <span data-ttu-id="1ab42-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1ab42-271">Classes used in</span></span>        | [<span data-ttu-id="1ab42-272">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1ab42-272">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1ab42-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ab42-273">Windows Server 2012</span></span>



| <span data-ttu-id="1ab42-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ab42-274">Entry</span></span> | <span data-ttu-id="1ab42-275">Value</span><span class="sxs-lookup"><span data-stu-id="1ab42-275">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1ab42-276">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1ab42-276">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ab42-277">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1ab42-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ab42-278">System-Only</span></span>            | <span data-ttu-id="1ab42-279">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-279">True</span></span>                                |
| <span data-ttu-id="1ab42-280">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1ab42-280">Is-Single-Valued</span></span>       | <span data-ttu-id="1ab42-281">True</span><span class="sxs-lookup"><span data-stu-id="1ab42-281">True</span></span>                                |
| <span data-ttu-id="1ab42-282">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1ab42-282">Is Indexed</span></span>             | <span data-ttu-id="1ab42-283">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-283">False</span></span>                               |
| <span data-ttu-id="1ab42-284">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ab42-284">In Global Catalog</span></span>      | <span data-ttu-id="1ab42-285">False</span><span class="sxs-lookup"><span data-stu-id="1ab42-285">False</span></span>                               |
| <span data-ttu-id="1ab42-286">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1ab42-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ab42-287">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ab42-287">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1ab42-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ab42-288">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ab42-289">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1ab42-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-290">Search-Flags</span></span>           | <span data-ttu-id="1ab42-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ab42-291">0x00000000</span></span>                          |
| <span data-ttu-id="1ab42-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ab42-292">System-Flags</span></span>           | <span data-ttu-id="1ab42-293">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1ab42-293">0x00000014</span></span>                          |
| <span data-ttu-id="1ab42-294">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1ab42-294">Classes used in</span></span>        | [<span data-ttu-id="1ab42-295">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1ab42-295">**Group**</span></span>](c-group.md)<br/> |



 

 





