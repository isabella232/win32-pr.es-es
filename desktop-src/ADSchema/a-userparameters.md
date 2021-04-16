---
title: User-Parameters atributo)
description: Parámetros del usuario.
ms.assetid: e3d6d22d-5112-4dfe-af55-a17a63e5f2e4
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de User-Parameters
- userParameters esquema de AD de atributos
topic_type:
- apiref
api_name:
- User-Parameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c1d593f0a655dea4fa3ddb25753de712ab83cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536118"
---
# <a name="user-parameters-attribute"></a><span data-ttu-id="da3f0-105">User-Parameters atributo)</span><span class="sxs-lookup"><span data-stu-id="da3f0-105">User-Parameters attribute</span></span>

<span data-ttu-id="da3f0-106">Parámetros del usuario.</span><span class="sxs-lookup"><span data-stu-id="da3f0-106">Parameters of the user.</span></span> <span data-ttu-id="da3f0-107">Apunta a una cadena Unicode que se reserva para su uso por parte de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="da3f0-107">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="da3f0-108">Esta cadena puede ser una cadena nula o puede tener cualquier número de caracteres antes del carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="da3f0-108">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="da3f0-109">Los productos de Microsoft usan este miembro para almacenar los datos de usuario específicos del programa individual.</span><span class="sxs-lookup"><span data-stu-id="da3f0-109">Microsoft products use this member to store user data specific to the individual program.</span></span>



| <span data-ttu-id="da3f0-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="da3f0-110">Entry</span></span> | <span data-ttu-id="da3f0-111">Value</span><span class="sxs-lookup"><span data-stu-id="da3f0-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="da3f0-112">CN</span><span class="sxs-lookup"><span data-stu-id="da3f0-112">CN</span></span>                | <span data-ttu-id="da3f0-113">User-Parameters</span><span class="sxs-lookup"><span data-stu-id="da3f0-113">User-Parameters</span></span>                             |
| <span data-ttu-id="da3f0-114">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="da3f0-114">Ldap-Display-Name</span></span> | <span data-ttu-id="da3f0-115">userParameters</span><span class="sxs-lookup"><span data-stu-id="da3f0-115">userParameters</span></span>                              |
| <span data-ttu-id="da3f0-116">Tamaño</span><span class="sxs-lookup"><span data-stu-id="da3f0-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="da3f0-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="da3f0-117">Update Privilege</span></span>  | <span data-ttu-id="da3f0-118">Modificado por aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="da3f0-118">Modified by applications.</span></span>                   |
| <span data-ttu-id="da3f0-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="da3f0-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="da3f0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="da3f0-120">Attribute-Id</span></span>      | <span data-ttu-id="da3f0-121">1.2.840.113556.1.4.138</span><span class="sxs-lookup"><span data-stu-id="da3f0-121">1.2.840.113556.1.4.138</span></span>                      |
| <span data-ttu-id="da3f0-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="da3f0-122">System-Id-Guid</span></span>    | <span data-ttu-id="da3f0-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="da3f0-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="da3f0-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da3f0-124">Syntax</span></span>            | [<span data-ttu-id="da3f0-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="da3f0-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="da3f0-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="da3f0-126">Implementations</span></span>

-   [<span data-ttu-id="da3f0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="da3f0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="da3f0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="da3f0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="da3f0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="da3f0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="da3f0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="da3f0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="da3f0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="da3f0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="da3f0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="da3f0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="da3f0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="da3f0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="da3f0-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="da3f0-134">Entry</span></span> | <span data-ttu-id="da3f0-135">Value</span><span class="sxs-lookup"><span data-stu-id="da3f0-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da3f0-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="da3f0-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3f0-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3f0-138">System-Only</span></span>            | <span data-ttu-id="da3f0-139">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-139">False</span></span>                             |
| <span data-ttu-id="da3f0-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="da3f0-140">Is-Single-Valued</span></span>       | <span data-ttu-id="da3f0-141">True</span><span class="sxs-lookup"><span data-stu-id="da3f0-141">True</span></span>                              |
| <span data-ttu-id="da3f0-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="da3f0-142">Is Indexed</span></span>             | <span data-ttu-id="da3f0-143">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-143">False</span></span>                             |
| <span data-ttu-id="da3f0-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="da3f0-144">In Global Catalog</span></span>      | <span data-ttu-id="da3f0-145">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-145">False</span></span>                             |
| <span data-ttu-id="da3f0-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="da3f0-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3f0-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="da3f0-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da3f0-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3f0-148">Range-Lower</span></span>            | <span data-ttu-id="da3f0-149">0</span><span class="sxs-lookup"><span data-stu-id="da3f0-149">0</span></span>                                 |
| <span data-ttu-id="da3f0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3f0-150">Range-Upper</span></span>            | <span data-ttu-id="da3f0-151">32767</span><span class="sxs-lookup"><span data-stu-id="da3f0-151">32767</span></span>                             |
| <span data-ttu-id="da3f0-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-152">Search-Flags</span></span>           | <span data-ttu-id="da3f0-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3f0-153">0x00000000</span></span>                        |
| <span data-ttu-id="da3f0-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-154">System-Flags</span></span>           | <span data-ttu-id="da3f0-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3f0-155">0x00000010</span></span>                        |
| <span data-ttu-id="da3f0-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="da3f0-156">Classes used in</span></span>        | [<span data-ttu-id="da3f0-157">**User**</span><span class="sxs-lookup"><span data-stu-id="da3f0-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="da3f0-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da3f0-158">Windows Server 2003</span></span>



| <span data-ttu-id="da3f0-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="da3f0-159">Entry</span></span> | <span data-ttu-id="da3f0-160">Value</span><span class="sxs-lookup"><span data-stu-id="da3f0-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da3f0-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="da3f0-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3f0-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3f0-163">System-Only</span></span>            | <span data-ttu-id="da3f0-164">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-164">False</span></span>                             |
| <span data-ttu-id="da3f0-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="da3f0-165">Is-Single-Valued</span></span>       | <span data-ttu-id="da3f0-166">True</span><span class="sxs-lookup"><span data-stu-id="da3f0-166">True</span></span>                              |
| <span data-ttu-id="da3f0-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="da3f0-167">Is Indexed</span></span>             | <span data-ttu-id="da3f0-168">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-168">False</span></span>                             |
| <span data-ttu-id="da3f0-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="da3f0-169">In Global Catalog</span></span>      | <span data-ttu-id="da3f0-170">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-170">False</span></span>                             |
| <span data-ttu-id="da3f0-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="da3f0-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3f0-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="da3f0-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da3f0-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3f0-173">Range-Lower</span></span>            | <span data-ttu-id="da3f0-174">0</span><span class="sxs-lookup"><span data-stu-id="da3f0-174">0</span></span>                                 |
| <span data-ttu-id="da3f0-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3f0-175">Range-Upper</span></span>            | <span data-ttu-id="da3f0-176">32767</span><span class="sxs-lookup"><span data-stu-id="da3f0-176">32767</span></span>                             |
| <span data-ttu-id="da3f0-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-177">Search-Flags</span></span>           | <span data-ttu-id="da3f0-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3f0-178">0x00000000</span></span>                        |
| <span data-ttu-id="da3f0-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-179">System-Flags</span></span>           | <span data-ttu-id="da3f0-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3f0-180">0x00000010</span></span>                        |
| <span data-ttu-id="da3f0-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="da3f0-181">Classes used in</span></span>        | [<span data-ttu-id="da3f0-182">**User**</span><span class="sxs-lookup"><span data-stu-id="da3f0-182">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="da3f0-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="da3f0-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="da3f0-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="da3f0-184">Entry</span></span> | <span data-ttu-id="da3f0-185">Value</span><span class="sxs-lookup"><span data-stu-id="da3f0-185">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da3f0-186">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="da3f0-186">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3f0-187">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3f0-188">System-Only</span></span>            | <span data-ttu-id="da3f0-189">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-189">False</span></span>                             |
| <span data-ttu-id="da3f0-190">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="da3f0-190">Is-Single-Valued</span></span>       | <span data-ttu-id="da3f0-191">True</span><span class="sxs-lookup"><span data-stu-id="da3f0-191">True</span></span>                              |
| <span data-ttu-id="da3f0-192">Está indexado</span><span class="sxs-lookup"><span data-stu-id="da3f0-192">Is Indexed</span></span>             | <span data-ttu-id="da3f0-193">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-193">False</span></span>                             |
| <span data-ttu-id="da3f0-194">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="da3f0-194">In Global Catalog</span></span>      | <span data-ttu-id="da3f0-195">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-195">False</span></span>                             |
| <span data-ttu-id="da3f0-196">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="da3f0-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3f0-197">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="da3f0-197">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da3f0-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3f0-198">Range-Lower</span></span>            | <span data-ttu-id="da3f0-199">0</span><span class="sxs-lookup"><span data-stu-id="da3f0-199">0</span></span>                                 |
| <span data-ttu-id="da3f0-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3f0-200">Range-Upper</span></span>            | <span data-ttu-id="da3f0-201">32767</span><span class="sxs-lookup"><span data-stu-id="da3f0-201">32767</span></span>                             |
| <span data-ttu-id="da3f0-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-202">Search-Flags</span></span>           | <span data-ttu-id="da3f0-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3f0-203">0x00000000</span></span>                        |
| <span data-ttu-id="da3f0-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-204">System-Flags</span></span>           | <span data-ttu-id="da3f0-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3f0-205">0x00000010</span></span>                        |
| <span data-ttu-id="da3f0-206">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="da3f0-206">Classes used in</span></span>        | [<span data-ttu-id="da3f0-207">**User**</span><span class="sxs-lookup"><span data-stu-id="da3f0-207">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="da3f0-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da3f0-208">Windows Server 2008</span></span>



| <span data-ttu-id="da3f0-209">Entrada</span><span class="sxs-lookup"><span data-stu-id="da3f0-209">Entry</span></span> | <span data-ttu-id="da3f0-210">Value</span><span class="sxs-lookup"><span data-stu-id="da3f0-210">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da3f0-211">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="da3f0-211">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3f0-212">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3f0-213">System-Only</span></span>            | <span data-ttu-id="da3f0-214">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-214">False</span></span>                             |
| <span data-ttu-id="da3f0-215">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="da3f0-215">Is-Single-Valued</span></span>       | <span data-ttu-id="da3f0-216">True</span><span class="sxs-lookup"><span data-stu-id="da3f0-216">True</span></span>                              |
| <span data-ttu-id="da3f0-217">Está indexado</span><span class="sxs-lookup"><span data-stu-id="da3f0-217">Is Indexed</span></span>             | <span data-ttu-id="da3f0-218">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-218">False</span></span>                             |
| <span data-ttu-id="da3f0-219">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="da3f0-219">In Global Catalog</span></span>      | <span data-ttu-id="da3f0-220">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-220">False</span></span>                             |
| <span data-ttu-id="da3f0-221">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="da3f0-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3f0-222">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="da3f0-222">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da3f0-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3f0-223">Range-Lower</span></span>            | <span data-ttu-id="da3f0-224">0</span><span class="sxs-lookup"><span data-stu-id="da3f0-224">0</span></span>                                 |
| <span data-ttu-id="da3f0-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3f0-225">Range-Upper</span></span>            | <span data-ttu-id="da3f0-226">32767</span><span class="sxs-lookup"><span data-stu-id="da3f0-226">32767</span></span>                             |
| <span data-ttu-id="da3f0-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-227">Search-Flags</span></span>           | <span data-ttu-id="da3f0-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3f0-228">0x00000000</span></span>                        |
| <span data-ttu-id="da3f0-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-229">System-Flags</span></span>           | <span data-ttu-id="da3f0-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3f0-230">0x00000010</span></span>                        |
| <span data-ttu-id="da3f0-231">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="da3f0-231">Classes used in</span></span>        | [<span data-ttu-id="da3f0-232">**User**</span><span class="sxs-lookup"><span data-stu-id="da3f0-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="da3f0-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="da3f0-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="da3f0-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="da3f0-234">Entry</span></span> | <span data-ttu-id="da3f0-235">Value</span><span class="sxs-lookup"><span data-stu-id="da3f0-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da3f0-236">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="da3f0-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3f0-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3f0-238">System-Only</span></span>            | <span data-ttu-id="da3f0-239">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-239">False</span></span>                             |
| <span data-ttu-id="da3f0-240">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="da3f0-240">Is-Single-Valued</span></span>       | <span data-ttu-id="da3f0-241">True</span><span class="sxs-lookup"><span data-stu-id="da3f0-241">True</span></span>                              |
| <span data-ttu-id="da3f0-242">Está indexado</span><span class="sxs-lookup"><span data-stu-id="da3f0-242">Is Indexed</span></span>             | <span data-ttu-id="da3f0-243">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-243">False</span></span>                             |
| <span data-ttu-id="da3f0-244">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="da3f0-244">In Global Catalog</span></span>      | <span data-ttu-id="da3f0-245">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-245">False</span></span>                             |
| <span data-ttu-id="da3f0-246">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="da3f0-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3f0-247">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="da3f0-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da3f0-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3f0-248">Range-Lower</span></span>            | <span data-ttu-id="da3f0-249">0</span><span class="sxs-lookup"><span data-stu-id="da3f0-249">0</span></span>                                 |
| <span data-ttu-id="da3f0-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3f0-250">Range-Upper</span></span>            | <span data-ttu-id="da3f0-251">32767</span><span class="sxs-lookup"><span data-stu-id="da3f0-251">32767</span></span>                             |
| <span data-ttu-id="da3f0-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-252">Search-Flags</span></span>           | <span data-ttu-id="da3f0-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3f0-253">0x00000000</span></span>                        |
| <span data-ttu-id="da3f0-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-254">System-Flags</span></span>           | <span data-ttu-id="da3f0-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3f0-255">0x00000010</span></span>                        |
| <span data-ttu-id="da3f0-256">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="da3f0-256">Classes used in</span></span>        | [<span data-ttu-id="da3f0-257">**User**</span><span class="sxs-lookup"><span data-stu-id="da3f0-257">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="da3f0-258">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da3f0-258">Windows Server 2012</span></span>



| <span data-ttu-id="da3f0-259">Entrada</span><span class="sxs-lookup"><span data-stu-id="da3f0-259">Entry</span></span> | <span data-ttu-id="da3f0-260">Value</span><span class="sxs-lookup"><span data-stu-id="da3f0-260">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da3f0-261">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="da3f0-261">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3f0-262">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da3f0-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3f0-263">System-Only</span></span>            | <span data-ttu-id="da3f0-264">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-264">False</span></span>                             |
| <span data-ttu-id="da3f0-265">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="da3f0-265">Is-Single-Valued</span></span>       | <span data-ttu-id="da3f0-266">True</span><span class="sxs-lookup"><span data-stu-id="da3f0-266">True</span></span>                              |
| <span data-ttu-id="da3f0-267">Está indexado</span><span class="sxs-lookup"><span data-stu-id="da3f0-267">Is Indexed</span></span>             | <span data-ttu-id="da3f0-268">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-268">False</span></span>                             |
| <span data-ttu-id="da3f0-269">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="da3f0-269">In Global Catalog</span></span>      | <span data-ttu-id="da3f0-270">False</span><span class="sxs-lookup"><span data-stu-id="da3f0-270">False</span></span>                             |
| <span data-ttu-id="da3f0-271">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="da3f0-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3f0-272">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="da3f0-272">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da3f0-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3f0-273">Range-Lower</span></span>            | <span data-ttu-id="da3f0-274">0</span><span class="sxs-lookup"><span data-stu-id="da3f0-274">0</span></span>                                 |
| <span data-ttu-id="da3f0-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3f0-275">Range-Upper</span></span>            | <span data-ttu-id="da3f0-276">32767</span><span class="sxs-lookup"><span data-stu-id="da3f0-276">32767</span></span>                             |
| <span data-ttu-id="da3f0-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-277">Search-Flags</span></span>           | <span data-ttu-id="da3f0-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3f0-278">0x00000000</span></span>                        |
| <span data-ttu-id="da3f0-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3f0-279">System-Flags</span></span>           | <span data-ttu-id="da3f0-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3f0-280">0x00000010</span></span>                        |
| <span data-ttu-id="da3f0-281">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="da3f0-281">Classes used in</span></span>        | [<span data-ttu-id="da3f0-282">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="da3f0-282">**User**</span></span>](c-user.md)<br/> |



 

 





