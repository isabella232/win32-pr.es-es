---
title: Script-Path atributo)
description: Este atributo especifica la ruta de acceso del script de inicio de sesión del usuario. La cadena puede ser null.
ms.assetid: 356f2ba0-ceca-4805-a536-286c6a8b54fc
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Script-Path
- Esquema de AD del atributo scriptPath
topic_type:
- apiref
api_name:
- Script-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0909c35c41ae65f75481910d1377aa2761e99487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151723"
---
# <a name="script-path-attribute"></a><span data-ttu-id="af0d8-106">Script-Path atributo)</span><span class="sxs-lookup"><span data-stu-id="af0d8-106">Script-Path attribute</span></span>

<span data-ttu-id="af0d8-107">Este atributo especifica la ruta de acceso del script de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="af0d8-107">This attribute specifies the path for the user's logon script.</span></span> <span data-ttu-id="af0d8-108">La cadena puede ser null.</span><span class="sxs-lookup"><span data-stu-id="af0d8-108">The string can be null.</span></span>



| <span data-ttu-id="af0d8-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="af0d8-109">Entry</span></span> | <span data-ttu-id="af0d8-110">Value</span><span class="sxs-lookup"><span data-stu-id="af0d8-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="af0d8-111">CN</span><span class="sxs-lookup"><span data-stu-id="af0d8-111">CN</span></span>                | <span data-ttu-id="af0d8-112">Script-Path</span><span class="sxs-lookup"><span data-stu-id="af0d8-112">Script-Path</span></span>                                                            |
| <span data-ttu-id="af0d8-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="af0d8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="af0d8-114">scriptPath</span><span class="sxs-lookup"><span data-stu-id="af0d8-114">scriptPath</span></span>                                                             |
| <span data-ttu-id="af0d8-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="af0d8-115">Size</span></span>              | \-                                                                     |
| <span data-ttu-id="af0d8-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="af0d8-116">Update Privilege</span></span>  | <span data-ttu-id="af0d8-117">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="af0d8-117">Domain administrator or account owner.</span></span>                                 |
| <span data-ttu-id="af0d8-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="af0d8-118">Update Frequency</span></span>  | <span data-ttu-id="af0d8-119">Cuando se crea el registro de usuario y cada vez que es necesario cambiar la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="af0d8-119">When the user record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="af0d8-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="af0d8-120">Attribute-Id</span></span>      | <span data-ttu-id="af0d8-121">1.2.840.113556.1.4.62</span><span class="sxs-lookup"><span data-stu-id="af0d8-121">1.2.840.113556.1.4.62</span></span>                                                  |
| <span data-ttu-id="af0d8-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="af0d8-122">System-Id-Guid</span></span>    | <span data-ttu-id="af0d8-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="af0d8-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="af0d8-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af0d8-124">Syntax</span></span>            | [<span data-ttu-id="af0d8-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="af0d8-125">**String(Unicode)**</span></span>](s-string-unicode.md)                            |



## <a name="implementations"></a><span data-ttu-id="af0d8-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="af0d8-126">Implementations</span></span>

-   [<span data-ttu-id="af0d8-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="af0d8-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="af0d8-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="af0d8-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="af0d8-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="af0d8-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="af0d8-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="af0d8-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="af0d8-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="af0d8-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="af0d8-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="af0d8-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="af0d8-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="af0d8-133">Windows 2000 Server</span></span>



| <span data-ttu-id="af0d8-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="af0d8-134">Entry</span></span> | <span data-ttu-id="af0d8-135">Value</span><span class="sxs-lookup"><span data-stu-id="af0d8-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="af0d8-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af0d8-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af0d8-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="af0d8-138">System-Only</span></span>            | <span data-ttu-id="af0d8-139">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-139">False</span></span>                             |
| <span data-ttu-id="af0d8-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af0d8-140">Is-Single-Valued</span></span>       | <span data-ttu-id="af0d8-141">True</span><span class="sxs-lookup"><span data-stu-id="af0d8-141">True</span></span>                              |
| <span data-ttu-id="af0d8-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af0d8-142">Is Indexed</span></span>             | <span data-ttu-id="af0d8-143">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-143">False</span></span>                             |
| <span data-ttu-id="af0d8-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af0d8-144">In Global Catalog</span></span>      | <span data-ttu-id="af0d8-145">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-145">False</span></span>                             |
| <span data-ttu-id="af0d8-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af0d8-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="af0d8-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af0d8-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="af0d8-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af0d8-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="af0d8-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af0d8-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="af0d8-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-150">Search-Flags</span></span>           | <span data-ttu-id="af0d8-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-151">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-152">System-Flags</span></span>           | <span data-ttu-id="af0d8-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-153">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af0d8-154">Classes used in</span></span>        | [<span data-ttu-id="af0d8-155">**User**</span><span class="sxs-lookup"><span data-stu-id="af0d8-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="af0d8-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af0d8-156">Windows Server 2003</span></span>



| <span data-ttu-id="af0d8-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="af0d8-157">Entry</span></span> | <span data-ttu-id="af0d8-158">Value</span><span class="sxs-lookup"><span data-stu-id="af0d8-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="af0d8-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af0d8-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af0d8-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="af0d8-161">System-Only</span></span>            | <span data-ttu-id="af0d8-162">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-162">False</span></span>                             |
| <span data-ttu-id="af0d8-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af0d8-163">Is-Single-Valued</span></span>       | <span data-ttu-id="af0d8-164">True</span><span class="sxs-lookup"><span data-stu-id="af0d8-164">True</span></span>                              |
| <span data-ttu-id="af0d8-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af0d8-165">Is Indexed</span></span>             | <span data-ttu-id="af0d8-166">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-166">False</span></span>                             |
| <span data-ttu-id="af0d8-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af0d8-167">In Global Catalog</span></span>      | <span data-ttu-id="af0d8-168">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-168">False</span></span>                             |
| <span data-ttu-id="af0d8-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af0d8-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="af0d8-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af0d8-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="af0d8-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af0d8-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="af0d8-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af0d8-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="af0d8-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-173">Search-Flags</span></span>           | <span data-ttu-id="af0d8-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-174">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-175">System-Flags</span></span>           | <span data-ttu-id="af0d8-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-176">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af0d8-177">Classes used in</span></span>        | [<span data-ttu-id="af0d8-178">**User**</span><span class="sxs-lookup"><span data-stu-id="af0d8-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="af0d8-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="af0d8-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="af0d8-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="af0d8-180">Entry</span></span> | <span data-ttu-id="af0d8-181">Value</span><span class="sxs-lookup"><span data-stu-id="af0d8-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="af0d8-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af0d8-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af0d8-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="af0d8-184">System-Only</span></span>            | <span data-ttu-id="af0d8-185">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-185">False</span></span>                             |
| <span data-ttu-id="af0d8-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af0d8-186">Is-Single-Valued</span></span>       | <span data-ttu-id="af0d8-187">True</span><span class="sxs-lookup"><span data-stu-id="af0d8-187">True</span></span>                              |
| <span data-ttu-id="af0d8-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af0d8-188">Is Indexed</span></span>             | <span data-ttu-id="af0d8-189">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-189">False</span></span>                             |
| <span data-ttu-id="af0d8-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af0d8-190">In Global Catalog</span></span>      | <span data-ttu-id="af0d8-191">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-191">False</span></span>                             |
| <span data-ttu-id="af0d8-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af0d8-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="af0d8-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af0d8-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="af0d8-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af0d8-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="af0d8-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af0d8-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="af0d8-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-196">Search-Flags</span></span>           | <span data-ttu-id="af0d8-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-197">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-198">System-Flags</span></span>           | <span data-ttu-id="af0d8-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-199">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af0d8-200">Classes used in</span></span>        | [<span data-ttu-id="af0d8-201">**User**</span><span class="sxs-lookup"><span data-stu-id="af0d8-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="af0d8-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af0d8-202">Windows Server 2008</span></span>



| <span data-ttu-id="af0d8-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="af0d8-203">Entry</span></span> | <span data-ttu-id="af0d8-204">Value</span><span class="sxs-lookup"><span data-stu-id="af0d8-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="af0d8-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af0d8-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af0d8-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="af0d8-207">System-Only</span></span>            | <span data-ttu-id="af0d8-208">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-208">False</span></span>                             |
| <span data-ttu-id="af0d8-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af0d8-209">Is-Single-Valued</span></span>       | <span data-ttu-id="af0d8-210">True</span><span class="sxs-lookup"><span data-stu-id="af0d8-210">True</span></span>                              |
| <span data-ttu-id="af0d8-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af0d8-211">Is Indexed</span></span>             | <span data-ttu-id="af0d8-212">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-212">False</span></span>                             |
| <span data-ttu-id="af0d8-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af0d8-213">In Global Catalog</span></span>      | <span data-ttu-id="af0d8-214">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-214">False</span></span>                             |
| <span data-ttu-id="af0d8-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af0d8-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="af0d8-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af0d8-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="af0d8-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af0d8-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="af0d8-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af0d8-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="af0d8-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-219">Search-Flags</span></span>           | <span data-ttu-id="af0d8-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-220">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-221">System-Flags</span></span>           | <span data-ttu-id="af0d8-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-222">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af0d8-223">Classes used in</span></span>        | [<span data-ttu-id="af0d8-224">**User**</span><span class="sxs-lookup"><span data-stu-id="af0d8-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="af0d8-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af0d8-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="af0d8-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="af0d8-226">Entry</span></span> | <span data-ttu-id="af0d8-227">Value</span><span class="sxs-lookup"><span data-stu-id="af0d8-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="af0d8-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af0d8-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af0d8-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="af0d8-230">System-Only</span></span>            | <span data-ttu-id="af0d8-231">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-231">False</span></span>                             |
| <span data-ttu-id="af0d8-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af0d8-232">Is-Single-Valued</span></span>       | <span data-ttu-id="af0d8-233">True</span><span class="sxs-lookup"><span data-stu-id="af0d8-233">True</span></span>                              |
| <span data-ttu-id="af0d8-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af0d8-234">Is Indexed</span></span>             | <span data-ttu-id="af0d8-235">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-235">False</span></span>                             |
| <span data-ttu-id="af0d8-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af0d8-236">In Global Catalog</span></span>      | <span data-ttu-id="af0d8-237">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-237">False</span></span>                             |
| <span data-ttu-id="af0d8-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af0d8-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="af0d8-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af0d8-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="af0d8-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af0d8-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="af0d8-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af0d8-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="af0d8-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-242">Search-Flags</span></span>           | <span data-ttu-id="af0d8-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-243">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-244">System-Flags</span></span>           | <span data-ttu-id="af0d8-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-245">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af0d8-246">Classes used in</span></span>        | [<span data-ttu-id="af0d8-247">**User**</span><span class="sxs-lookup"><span data-stu-id="af0d8-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="af0d8-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af0d8-248">Windows Server 2012</span></span>



| <span data-ttu-id="af0d8-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="af0d8-249">Entry</span></span> | <span data-ttu-id="af0d8-250">Value</span><span class="sxs-lookup"><span data-stu-id="af0d8-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="af0d8-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="af0d8-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af0d8-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="af0d8-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="af0d8-253">System-Only</span></span>            | <span data-ttu-id="af0d8-254">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-254">False</span></span>                             |
| <span data-ttu-id="af0d8-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="af0d8-255">Is-Single-Valued</span></span>       | <span data-ttu-id="af0d8-256">True</span><span class="sxs-lookup"><span data-stu-id="af0d8-256">True</span></span>                              |
| <span data-ttu-id="af0d8-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="af0d8-257">Is Indexed</span></span>             | <span data-ttu-id="af0d8-258">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-258">False</span></span>                             |
| <span data-ttu-id="af0d8-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="af0d8-259">In Global Catalog</span></span>      | <span data-ttu-id="af0d8-260">False</span><span class="sxs-lookup"><span data-stu-id="af0d8-260">False</span></span>                             |
| <span data-ttu-id="af0d8-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="af0d8-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="af0d8-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af0d8-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="af0d8-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af0d8-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="af0d8-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af0d8-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="af0d8-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-265">Search-Flags</span></span>           | <span data-ttu-id="af0d8-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-266">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af0d8-267">System-Flags</span></span>           | <span data-ttu-id="af0d8-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af0d8-268">0x00000010</span></span>                        |
| <span data-ttu-id="af0d8-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="af0d8-269">Classes used in</span></span>        | [<span data-ttu-id="af0d8-270">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="af0d8-270">**User**</span></span>](c-user.md)<br/> |



 

 





