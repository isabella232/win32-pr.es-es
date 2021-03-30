---
title: atributo MS-DS-AZ-LDAP-Query
description: Cadena que define la consulta LDAP (longitud máxima 4096) que determina la pertenencia de un objeto de usuario al grupo.
ms.assetid: e24d4c50-2153-49a6-8aef-4872ccaab13e
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-AZ-LDAP-Query
- Esquema de AD de atributo msDS-AzLDAPQuery
topic_type:
- apiref
api_name:
- ms-DS-Az-LDAP-Query
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1f6c21d5ed28a9d2419b16c6ce7986f3250488
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151673"
---
# <a name="ms-ds-az-ldap-query-attribute"></a><span data-ttu-id="97c13-105">atributo MS-DS-AZ-LDAP-Query</span><span class="sxs-lookup"><span data-stu-id="97c13-105">ms-DS-Az-LDAP-Query attribute</span></span>

<span data-ttu-id="97c13-106">Cadena que define la consulta LDAP (longitud máxima 4096) que determina la pertenencia de un objeto de usuario al grupo.</span><span class="sxs-lookup"><span data-stu-id="97c13-106">A string that defines the LDAP query (max length 4096) which determines the membership of a user object to the group.</span></span>



| <span data-ttu-id="97c13-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="97c13-107">Entry</span></span> | <span data-ttu-id="97c13-108">Value</span><span class="sxs-lookup"><span data-stu-id="97c13-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="97c13-109">CN</span><span class="sxs-lookup"><span data-stu-id="97c13-109">CN</span></span>                | <span data-ttu-id="97c13-110">MS-DS-AZ-LDAP-Query</span><span class="sxs-lookup"><span data-stu-id="97c13-110">ms-DS-Az-LDAP-Query</span></span>                         |
| <span data-ttu-id="97c13-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="97c13-111">Ldap-Display-Name</span></span> | <span data-ttu-id="97c13-112">msDS-AzLDAPQuery</span><span class="sxs-lookup"><span data-stu-id="97c13-112">msDS-AzLDAPQuery</span></span>                            |
| <span data-ttu-id="97c13-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="97c13-113">Size</span></span>              | <span data-ttu-id="97c13-114">4096 caracteres</span><span class="sxs-lookup"><span data-stu-id="97c13-114">4096 characters</span></span>                             |
| <span data-ttu-id="97c13-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="97c13-115">Update Privilege</span></span>  | <span data-ttu-id="97c13-116">Administrador de AzRoles</span><span class="sxs-lookup"><span data-stu-id="97c13-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="97c13-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="97c13-117">Update Frequency</span></span>  | <span data-ttu-id="97c13-118">Durante la inicialización o el cambio de directiva.</span><span class="sxs-lookup"><span data-stu-id="97c13-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="97c13-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="97c13-119">Attribute-Id</span></span>      | <span data-ttu-id="97c13-120">1.2.840.113556.1.4.1792</span><span class="sxs-lookup"><span data-stu-id="97c13-120">1.2.840.113556.1.4.1792</span></span>                     |
| <span data-ttu-id="97c13-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="97c13-121">System-Id-Guid</span></span>    | <span data-ttu-id="97c13-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span><span class="sxs-lookup"><span data-stu-id="97c13-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span></span>        |
| <span data-ttu-id="97c13-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97c13-123">Syntax</span></span>            | [<span data-ttu-id="97c13-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="97c13-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="97c13-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="97c13-125">Implementations</span></span>

-   [<span data-ttu-id="97c13-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="97c13-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="97c13-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="97c13-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="97c13-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="97c13-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="97c13-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="97c13-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="97c13-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="97c13-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="97c13-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="97c13-131">Windows Server 2003</span></span>



| <span data-ttu-id="97c13-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="97c13-132">Entry</span></span> | <span data-ttu-id="97c13-133">Value</span><span class="sxs-lookup"><span data-stu-id="97c13-133">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="97c13-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="97c13-134">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="97c13-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97c13-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="97c13-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="97c13-136">System-Only</span></span>            | <span data-ttu-id="97c13-137">False</span><span class="sxs-lookup"><span data-stu-id="97c13-137">False</span></span>                               |
| <span data-ttu-id="97c13-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="97c13-138">Is-Single-Valued</span></span>       | <span data-ttu-id="97c13-139">True</span><span class="sxs-lookup"><span data-stu-id="97c13-139">True</span></span>                                |
| <span data-ttu-id="97c13-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="97c13-140">Is Indexed</span></span>             | <span data-ttu-id="97c13-141">False</span><span class="sxs-lookup"><span data-stu-id="97c13-141">False</span></span>                               |
| <span data-ttu-id="97c13-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="97c13-142">In Global Catalog</span></span>      | <span data-ttu-id="97c13-143">False</span><span class="sxs-lookup"><span data-stu-id="97c13-143">False</span></span>                               |
| <span data-ttu-id="97c13-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="97c13-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="97c13-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="97c13-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="97c13-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97c13-146">Range-Lower</span></span>            | <span data-ttu-id="97c13-147">0</span><span class="sxs-lookup"><span data-stu-id="97c13-147">0</span></span>                                   |
| <span data-ttu-id="97c13-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97c13-148">Range-Upper</span></span>            | <span data-ttu-id="97c13-149">4096</span><span class="sxs-lookup"><span data-stu-id="97c13-149">4096</span></span>                                |
| <span data-ttu-id="97c13-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97c13-150">Search-Flags</span></span>           | <span data-ttu-id="97c13-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97c13-151">0x00000000</span></span>                          |
| <span data-ttu-id="97c13-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97c13-152">System-Flags</span></span>           | <span data-ttu-id="97c13-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97c13-153">0x00000010</span></span>                          |
| <span data-ttu-id="97c13-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="97c13-154">Classes used in</span></span>        | [<span data-ttu-id="97c13-155">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="97c13-155">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="97c13-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="97c13-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="97c13-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="97c13-157">Entry</span></span> | <span data-ttu-id="97c13-158">Value</span><span class="sxs-lookup"><span data-stu-id="97c13-158">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="97c13-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="97c13-159">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="97c13-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97c13-160">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="97c13-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="97c13-161">System-Only</span></span>            | <span data-ttu-id="97c13-162">False</span><span class="sxs-lookup"><span data-stu-id="97c13-162">False</span></span>                               |
| <span data-ttu-id="97c13-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="97c13-163">Is-Single-Valued</span></span>       | <span data-ttu-id="97c13-164">True</span><span class="sxs-lookup"><span data-stu-id="97c13-164">True</span></span>                                |
| <span data-ttu-id="97c13-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="97c13-165">Is Indexed</span></span>             | <span data-ttu-id="97c13-166">False</span><span class="sxs-lookup"><span data-stu-id="97c13-166">False</span></span>                               |
| <span data-ttu-id="97c13-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="97c13-167">In Global Catalog</span></span>      | <span data-ttu-id="97c13-168">False</span><span class="sxs-lookup"><span data-stu-id="97c13-168">False</span></span>                               |
| <span data-ttu-id="97c13-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="97c13-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="97c13-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="97c13-170">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="97c13-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97c13-171">Range-Lower</span></span>            | <span data-ttu-id="97c13-172">0</span><span class="sxs-lookup"><span data-stu-id="97c13-172">0</span></span>                                   |
| <span data-ttu-id="97c13-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97c13-173">Range-Upper</span></span>            | <span data-ttu-id="97c13-174">4096</span><span class="sxs-lookup"><span data-stu-id="97c13-174">4096</span></span>                                |
| <span data-ttu-id="97c13-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97c13-175">Search-Flags</span></span>           | <span data-ttu-id="97c13-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97c13-176">0x00000000</span></span>                          |
| <span data-ttu-id="97c13-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97c13-177">System-Flags</span></span>           | <span data-ttu-id="97c13-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97c13-178">0x00000010</span></span>                          |
| <span data-ttu-id="97c13-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="97c13-179">Classes used in</span></span>        | [<span data-ttu-id="97c13-180">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="97c13-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="97c13-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97c13-181">Windows Server 2008</span></span>



| <span data-ttu-id="97c13-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="97c13-182">Entry</span></span> | <span data-ttu-id="97c13-183">Value</span><span class="sxs-lookup"><span data-stu-id="97c13-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="97c13-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="97c13-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="97c13-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97c13-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="97c13-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="97c13-186">System-Only</span></span>            | <span data-ttu-id="97c13-187">False</span><span class="sxs-lookup"><span data-stu-id="97c13-187">False</span></span>                               |
| <span data-ttu-id="97c13-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="97c13-188">Is-Single-Valued</span></span>       | <span data-ttu-id="97c13-189">True</span><span class="sxs-lookup"><span data-stu-id="97c13-189">True</span></span>                                |
| <span data-ttu-id="97c13-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="97c13-190">Is Indexed</span></span>             | <span data-ttu-id="97c13-191">False</span><span class="sxs-lookup"><span data-stu-id="97c13-191">False</span></span>                               |
| <span data-ttu-id="97c13-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="97c13-192">In Global Catalog</span></span>      | <span data-ttu-id="97c13-193">False</span><span class="sxs-lookup"><span data-stu-id="97c13-193">False</span></span>                               |
| <span data-ttu-id="97c13-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="97c13-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="97c13-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="97c13-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="97c13-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97c13-196">Range-Lower</span></span>            | <span data-ttu-id="97c13-197">0</span><span class="sxs-lookup"><span data-stu-id="97c13-197">0</span></span>                                   |
| <span data-ttu-id="97c13-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97c13-198">Range-Upper</span></span>            | <span data-ttu-id="97c13-199">4096</span><span class="sxs-lookup"><span data-stu-id="97c13-199">4096</span></span>                                |
| <span data-ttu-id="97c13-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97c13-200">Search-Flags</span></span>           | <span data-ttu-id="97c13-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97c13-201">0x00000000</span></span>                          |
| <span data-ttu-id="97c13-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97c13-202">System-Flags</span></span>           | <span data-ttu-id="97c13-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97c13-203">0x00000010</span></span>                          |
| <span data-ttu-id="97c13-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="97c13-204">Classes used in</span></span>        | [<span data-ttu-id="97c13-205">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="97c13-205">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="97c13-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="97c13-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="97c13-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="97c13-207">Entry</span></span> | <span data-ttu-id="97c13-208">Value</span><span class="sxs-lookup"><span data-stu-id="97c13-208">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="97c13-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="97c13-209">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="97c13-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97c13-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="97c13-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="97c13-211">System-Only</span></span>            | <span data-ttu-id="97c13-212">False</span><span class="sxs-lookup"><span data-stu-id="97c13-212">False</span></span>                               |
| <span data-ttu-id="97c13-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="97c13-213">Is-Single-Valued</span></span>       | <span data-ttu-id="97c13-214">True</span><span class="sxs-lookup"><span data-stu-id="97c13-214">True</span></span>                                |
| <span data-ttu-id="97c13-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="97c13-215">Is Indexed</span></span>             | <span data-ttu-id="97c13-216">False</span><span class="sxs-lookup"><span data-stu-id="97c13-216">False</span></span>                               |
| <span data-ttu-id="97c13-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="97c13-217">In Global Catalog</span></span>      | <span data-ttu-id="97c13-218">False</span><span class="sxs-lookup"><span data-stu-id="97c13-218">False</span></span>                               |
| <span data-ttu-id="97c13-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="97c13-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="97c13-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="97c13-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="97c13-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97c13-221">Range-Lower</span></span>            | <span data-ttu-id="97c13-222">0</span><span class="sxs-lookup"><span data-stu-id="97c13-222">0</span></span>                                   |
| <span data-ttu-id="97c13-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97c13-223">Range-Upper</span></span>            | <span data-ttu-id="97c13-224">4096</span><span class="sxs-lookup"><span data-stu-id="97c13-224">4096</span></span>                                |
| <span data-ttu-id="97c13-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97c13-225">Search-Flags</span></span>           | <span data-ttu-id="97c13-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97c13-226">0x00000000</span></span>                          |
| <span data-ttu-id="97c13-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97c13-227">System-Flags</span></span>           | <span data-ttu-id="97c13-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97c13-228">0x00000010</span></span>                          |
| <span data-ttu-id="97c13-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="97c13-229">Classes used in</span></span>        | [<span data-ttu-id="97c13-230">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="97c13-230">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="97c13-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="97c13-231">Windows Server 2012</span></span>



| <span data-ttu-id="97c13-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="97c13-232">Entry</span></span> | <span data-ttu-id="97c13-233">Value</span><span class="sxs-lookup"><span data-stu-id="97c13-233">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="97c13-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="97c13-234">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="97c13-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97c13-235">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="97c13-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="97c13-236">System-Only</span></span>            | <span data-ttu-id="97c13-237">False</span><span class="sxs-lookup"><span data-stu-id="97c13-237">False</span></span>                               |
| <span data-ttu-id="97c13-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="97c13-238">Is-Single-Valued</span></span>       | <span data-ttu-id="97c13-239">True</span><span class="sxs-lookup"><span data-stu-id="97c13-239">True</span></span>                                |
| <span data-ttu-id="97c13-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="97c13-240">Is Indexed</span></span>             | <span data-ttu-id="97c13-241">False</span><span class="sxs-lookup"><span data-stu-id="97c13-241">False</span></span>                               |
| <span data-ttu-id="97c13-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="97c13-242">In Global Catalog</span></span>      | <span data-ttu-id="97c13-243">False</span><span class="sxs-lookup"><span data-stu-id="97c13-243">False</span></span>                               |
| <span data-ttu-id="97c13-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="97c13-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="97c13-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="97c13-245">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="97c13-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97c13-246">Range-Lower</span></span>            | <span data-ttu-id="97c13-247">0</span><span class="sxs-lookup"><span data-stu-id="97c13-247">0</span></span>                                   |
| <span data-ttu-id="97c13-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97c13-248">Range-Upper</span></span>            | <span data-ttu-id="97c13-249">4096</span><span class="sxs-lookup"><span data-stu-id="97c13-249">4096</span></span>                                |
| <span data-ttu-id="97c13-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97c13-250">Search-Flags</span></span>           | <span data-ttu-id="97c13-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97c13-251">0x00000000</span></span>                          |
| <span data-ttu-id="97c13-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97c13-252">System-Flags</span></span>           | <span data-ttu-id="97c13-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97c13-253">0x00000010</span></span>                          |
| <span data-ttu-id="97c13-254">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="97c13-254">Classes used in</span></span>        | [<span data-ttu-id="97c13-255">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="97c13-255">**Group**</span></span>](c-group.md)<br/> |



 

 





