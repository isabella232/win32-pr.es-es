---
title: Initials (atributo)
description: Contiene las iniciales de las partes del nombre completo del usuario. Puede usarse como inicial central en la libreta de direcciones de Windows.
ms.assetid: 220b4448-5276-4c3f-8a1b-217cec06135a
ms.tgt_platform: multiple
keywords:
- Atributo iniciales esquema de AD
- atributo iniciales esquema de AD
topic_type:
- apiref
api_name:
- Initials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 946f6c9633c1126a30ae4898274096a54db9a402
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658953"
---
# <a name="initials-attribute"></a><span data-ttu-id="0c525-106">Initials (atributo)</span><span class="sxs-lookup"><span data-stu-id="0c525-106">Initials attribute</span></span>

<span data-ttu-id="0c525-107">Contiene las iniciales de las partes del nombre completo del usuario.</span><span class="sxs-lookup"><span data-stu-id="0c525-107">Contains the initials for parts of the user's full name.</span></span> <span data-ttu-id="0c525-108">Puede usarse como inicial central en la libreta de direcciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="0c525-108">This may be used as the middle initial in the Windows Address Book.</span></span>



| <span data-ttu-id="0c525-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c525-109">Entry</span></span> | <span data-ttu-id="0c525-110">Value</span><span class="sxs-lookup"><span data-stu-id="0c525-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0c525-111">CN</span><span class="sxs-lookup"><span data-stu-id="0c525-111">CN</span></span>                | <span data-ttu-id="0c525-112">Iniciales</span><span class="sxs-lookup"><span data-stu-id="0c525-112">Initials</span></span>                                    |
| <span data-ttu-id="0c525-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="0c525-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0c525-114">Initials</span><span class="sxs-lookup"><span data-stu-id="0c525-114">initials</span></span>                                    |
| <span data-ttu-id="0c525-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="0c525-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="0c525-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="0c525-116">Update Privilege</span></span>  | <span data-ttu-id="0c525-117">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="0c525-117">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="0c525-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="0c525-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="0c525-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0c525-119">Attribute-Id</span></span>      | <span data-ttu-id="0c525-120">2.5.4.43</span><span class="sxs-lookup"><span data-stu-id="0c525-120">2.5.4.43</span></span>                                    |
| <span data-ttu-id="0c525-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0c525-121">System-Id-Guid</span></span>    | <span data-ttu-id="0c525-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="0c525-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="0c525-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c525-123">Syntax</span></span>            | [<span data-ttu-id="0c525-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0c525-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0c525-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="0c525-125">Implementations</span></span>

-   [<span data-ttu-id="0c525-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0c525-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0c525-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0c525-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0c525-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0c525-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0c525-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0c525-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0c525-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0c525-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0c525-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0c525-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0c525-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c525-132">Windows 2000 Server</span></span>



| <span data-ttu-id="0c525-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c525-133">Entry</span></span> | <span data-ttu-id="0c525-134">Value</span><span class="sxs-lookup"><span data-stu-id="0c525-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0c525-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0c525-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0c525-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c525-136">MAPI-Id</span></span>                | <span data-ttu-id="0c525-137">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="0c525-137">0x3A0A</span></span>                                                             |
| <span data-ttu-id="0c525-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c525-138">System-Only</span></span>            | <span data-ttu-id="0c525-139">False</span><span class="sxs-lookup"><span data-stu-id="0c525-139">False</span></span>                                                              |
| <span data-ttu-id="0c525-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0c525-140">Is-Single-Valued</span></span>       | <span data-ttu-id="0c525-141">True</span><span class="sxs-lookup"><span data-stu-id="0c525-141">True</span></span>                                                               |
| <span data-ttu-id="0c525-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0c525-142">Is Indexed</span></span>             | <span data-ttu-id="0c525-143">False</span><span class="sxs-lookup"><span data-stu-id="0c525-143">False</span></span>                                                              |
| <span data-ttu-id="0c525-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c525-144">In Global Catalog</span></span>      | <span data-ttu-id="0c525-145">False</span><span class="sxs-lookup"><span data-stu-id="0c525-145">False</span></span>                                                              |
| <span data-ttu-id="0c525-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0c525-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c525-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0c525-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0c525-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c525-148">Range-Lower</span></span>            | <span data-ttu-id="0c525-149">1</span><span class="sxs-lookup"><span data-stu-id="0c525-149">1</span></span>                                                                  |
| <span data-ttu-id="0c525-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c525-150">Range-Upper</span></span>            | <span data-ttu-id="0c525-151">6</span><span class="sxs-lookup"><span data-stu-id="0c525-151">6</span></span>                                                                  |
| <span data-ttu-id="0c525-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-152">Search-Flags</span></span>           | <span data-ttu-id="0c525-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c525-153">0x00000000</span></span>                                                         |
| <span data-ttu-id="0c525-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-154">System-Flags</span></span>           | <span data-ttu-id="0c525-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c525-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="0c525-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0c525-156">Classes used in</span></span>        | [<span data-ttu-id="0c525-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c525-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0c525-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c525-158">Windows Server 2003</span></span>



| <span data-ttu-id="0c525-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c525-159">Entry</span></span> | <span data-ttu-id="0c525-160">Value</span><span class="sxs-lookup"><span data-stu-id="0c525-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c525-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0c525-161">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0c525-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c525-162">MAPI-Id</span></span>                | <span data-ttu-id="0c525-163">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="0c525-163">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="0c525-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c525-164">System-Only</span></span>            | <span data-ttu-id="0c525-165">False</span><span class="sxs-lookup"><span data-stu-id="0c525-165">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0c525-166">Is-Single-Valued</span></span>       | <span data-ttu-id="0c525-167">True</span><span class="sxs-lookup"><span data-stu-id="0c525-167">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c525-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0c525-168">Is Indexed</span></span>             | <span data-ttu-id="0c525-169">False</span><span class="sxs-lookup"><span data-stu-id="0c525-169">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c525-170">In Global Catalog</span></span>      | <span data-ttu-id="0c525-171">False</span><span class="sxs-lookup"><span data-stu-id="0c525-171">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0c525-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c525-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0c525-173">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0c525-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c525-174">Range-Lower</span></span>            | <span data-ttu-id="0c525-175">1</span><span class="sxs-lookup"><span data-stu-id="0c525-175">1</span></span>                                                                                                                      |
| <span data-ttu-id="0c525-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c525-176">Range-Upper</span></span>            | <span data-ttu-id="0c525-177">6</span><span class="sxs-lookup"><span data-stu-id="0c525-177">6</span></span>                                                                                                                      |
| <span data-ttu-id="0c525-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-178">Search-Flags</span></span>           | <span data-ttu-id="0c525-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c525-179">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="0c525-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-180">System-Flags</span></span>           | <span data-ttu-id="0c525-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c525-181">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0c525-182">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0c525-182">Classes used in</span></span>        | [<span data-ttu-id="0c525-183">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="0c525-183">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="0c525-184">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c525-184">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0c525-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c525-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0c525-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c525-186">Entry</span></span> | <span data-ttu-id="0c525-187">Value</span><span class="sxs-lookup"><span data-stu-id="0c525-187">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c525-188">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0c525-188">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0c525-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c525-189">MAPI-Id</span></span>                | <span data-ttu-id="0c525-190">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="0c525-190">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="0c525-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c525-191">System-Only</span></span>            | <span data-ttu-id="0c525-192">False</span><span class="sxs-lookup"><span data-stu-id="0c525-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-193">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0c525-193">Is-Single-Valued</span></span>       | <span data-ttu-id="0c525-194">True</span><span class="sxs-lookup"><span data-stu-id="0c525-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c525-195">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0c525-195">Is Indexed</span></span>             | <span data-ttu-id="0c525-196">False</span><span class="sxs-lookup"><span data-stu-id="0c525-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-197">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c525-197">In Global Catalog</span></span>      | <span data-ttu-id="0c525-198">False</span><span class="sxs-lookup"><span data-stu-id="0c525-198">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-199">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0c525-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c525-200">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0c525-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0c525-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c525-201">Range-Lower</span></span>            | <span data-ttu-id="0c525-202">1</span><span class="sxs-lookup"><span data-stu-id="0c525-202">1</span></span>                                                                                                                      |
| <span data-ttu-id="0c525-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c525-203">Range-Upper</span></span>            | <span data-ttu-id="0c525-204">6</span><span class="sxs-lookup"><span data-stu-id="0c525-204">6</span></span>                                                                                                                      |
| <span data-ttu-id="0c525-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-205">Search-Flags</span></span>           | <span data-ttu-id="0c525-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c525-206">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="0c525-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-207">System-Flags</span></span>           | <span data-ttu-id="0c525-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c525-208">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0c525-209">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0c525-209">Classes used in</span></span>        | [<span data-ttu-id="0c525-210">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="0c525-210">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="0c525-211">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c525-211">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0c525-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c525-212">Windows Server 2008</span></span>



| <span data-ttu-id="0c525-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c525-213">Entry</span></span> | <span data-ttu-id="0c525-214">Value</span><span class="sxs-lookup"><span data-stu-id="0c525-214">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c525-215">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0c525-215">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0c525-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c525-216">MAPI-Id</span></span>                | <span data-ttu-id="0c525-217">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="0c525-217">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="0c525-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c525-218">System-Only</span></span>            | <span data-ttu-id="0c525-219">False</span><span class="sxs-lookup"><span data-stu-id="0c525-219">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-220">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0c525-220">Is-Single-Valued</span></span>       | <span data-ttu-id="0c525-221">True</span><span class="sxs-lookup"><span data-stu-id="0c525-221">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c525-222">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0c525-222">Is Indexed</span></span>             | <span data-ttu-id="0c525-223">False</span><span class="sxs-lookup"><span data-stu-id="0c525-223">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-224">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c525-224">In Global Catalog</span></span>      | <span data-ttu-id="0c525-225">False</span><span class="sxs-lookup"><span data-stu-id="0c525-225">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-226">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0c525-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c525-227">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0c525-227">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0c525-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c525-228">Range-Lower</span></span>            | <span data-ttu-id="0c525-229">1</span><span class="sxs-lookup"><span data-stu-id="0c525-229">1</span></span>                                                                                                                      |
| <span data-ttu-id="0c525-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c525-230">Range-Upper</span></span>            | <span data-ttu-id="0c525-231">6</span><span class="sxs-lookup"><span data-stu-id="0c525-231">6</span></span>                                                                                                                      |
| <span data-ttu-id="0c525-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-232">Search-Flags</span></span>           | <span data-ttu-id="0c525-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c525-233">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="0c525-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-234">System-Flags</span></span>           | <span data-ttu-id="0c525-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c525-235">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0c525-236">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0c525-236">Classes used in</span></span>        | [<span data-ttu-id="0c525-237">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="0c525-237">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="0c525-238">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c525-238">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0c525-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c525-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0c525-240">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c525-240">Entry</span></span> | <span data-ttu-id="0c525-241">Value</span><span class="sxs-lookup"><span data-stu-id="0c525-241">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c525-242">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0c525-242">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0c525-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c525-243">MAPI-Id</span></span>                | <span data-ttu-id="0c525-244">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="0c525-244">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="0c525-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c525-245">System-Only</span></span>            | <span data-ttu-id="0c525-246">False</span><span class="sxs-lookup"><span data-stu-id="0c525-246">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-247">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0c525-247">Is-Single-Valued</span></span>       | <span data-ttu-id="0c525-248">True</span><span class="sxs-lookup"><span data-stu-id="0c525-248">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c525-249">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0c525-249">Is Indexed</span></span>             | <span data-ttu-id="0c525-250">False</span><span class="sxs-lookup"><span data-stu-id="0c525-250">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-251">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c525-251">In Global Catalog</span></span>      | <span data-ttu-id="0c525-252">False</span><span class="sxs-lookup"><span data-stu-id="0c525-252">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-253">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0c525-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c525-254">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0c525-254">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0c525-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c525-255">Range-Lower</span></span>            | <span data-ttu-id="0c525-256">1</span><span class="sxs-lookup"><span data-stu-id="0c525-256">1</span></span>                                                                                                                      |
| <span data-ttu-id="0c525-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c525-257">Range-Upper</span></span>            | <span data-ttu-id="0c525-258">6</span><span class="sxs-lookup"><span data-stu-id="0c525-258">6</span></span>                                                                                                                      |
| <span data-ttu-id="0c525-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-259">Search-Flags</span></span>           | <span data-ttu-id="0c525-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c525-260">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="0c525-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-261">System-Flags</span></span>           | <span data-ttu-id="0c525-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c525-262">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0c525-263">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0c525-263">Classes used in</span></span>        | [<span data-ttu-id="0c525-264">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="0c525-264">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="0c525-265">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c525-265">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0c525-266">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c525-266">Windows Server 2012</span></span>



| <span data-ttu-id="0c525-267">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c525-267">Entry</span></span> | <span data-ttu-id="0c525-268">Value</span><span class="sxs-lookup"><span data-stu-id="0c525-268">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c525-269">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="0c525-269">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0c525-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c525-270">MAPI-Id</span></span>                | <span data-ttu-id="0c525-271">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="0c525-271">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="0c525-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c525-272">System-Only</span></span>            | <span data-ttu-id="0c525-273">False</span><span class="sxs-lookup"><span data-stu-id="0c525-273">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-274">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="0c525-274">Is-Single-Valued</span></span>       | <span data-ttu-id="0c525-275">True</span><span class="sxs-lookup"><span data-stu-id="0c525-275">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c525-276">Está indexado</span><span class="sxs-lookup"><span data-stu-id="0c525-276">Is Indexed</span></span>             | <span data-ttu-id="0c525-277">False</span><span class="sxs-lookup"><span data-stu-id="0c525-277">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-278">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c525-278">In Global Catalog</span></span>      | <span data-ttu-id="0c525-279">False</span><span class="sxs-lookup"><span data-stu-id="0c525-279">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c525-280">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="0c525-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c525-281">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0c525-281">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0c525-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c525-282">Range-Lower</span></span>            | <span data-ttu-id="0c525-283">1</span><span class="sxs-lookup"><span data-stu-id="0c525-283">1</span></span>                                                                                                                      |
| <span data-ttu-id="0c525-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c525-284">Range-Upper</span></span>            | <span data-ttu-id="0c525-285">6</span><span class="sxs-lookup"><span data-stu-id="0c525-285">6</span></span>                                                                                                                      |
| <span data-ttu-id="0c525-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-286">Search-Flags</span></span>           | <span data-ttu-id="0c525-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c525-287">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="0c525-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c525-288">System-Flags</span></span>           | <span data-ttu-id="0c525-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c525-289">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0c525-290">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="0c525-290">Classes used in</span></span>        | [<span data-ttu-id="0c525-291">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="0c525-291">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="0c525-292">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c525-292">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





