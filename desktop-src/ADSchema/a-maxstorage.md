---
title: Max-Storage atributo)
description: Cantidad máxima de espacio en disco que puede utilizar el usuario. Use el valor especificado en USER \_ MAXSTORAGE \_ Unlimited para usar todo el espacio disponible en disco.
ms.assetid: 69302641-ecfc-4b0f-81f8-f69b48c6faa7
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Max-Storage
- maxStorage esquema de AD de atributos
topic_type:
- apiref
api_name:
- Max-Storage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6caff3f85de7073818096324445b63a3c1c9be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906069"
---
# <a name="max-storage-attribute"></a><span data-ttu-id="e44e4-106">Max-Storage atributo)</span><span class="sxs-lookup"><span data-stu-id="e44e4-106">Max-Storage attribute</span></span>

<span data-ttu-id="e44e4-107">Cantidad máxima de espacio en disco que puede utilizar el usuario.</span><span class="sxs-lookup"><span data-stu-id="e44e4-107">The maximum amount of disk space the user can use.</span></span> <span data-ttu-id="e44e4-108">Use el valor especificado en USER \_ MAXSTORAGE \_ Unlimited para usar todo el espacio disponible en disco.</span><span class="sxs-lookup"><span data-stu-id="e44e4-108">Use the value specified in USER\_MAXSTORAGE\_UNLIMITED to use all available disk space.</span></span>



| <span data-ttu-id="e44e4-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="e44e4-109">Entry</span></span> | <span data-ttu-id="e44e4-110">Value</span><span class="sxs-lookup"><span data-stu-id="e44e4-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="e44e4-111">CN</span><span class="sxs-lookup"><span data-stu-id="e44e4-111">CN</span></span>                | <span data-ttu-id="e44e4-112">Max-Storage</span><span class="sxs-lookup"><span data-stu-id="e44e4-112">Max-Storage</span></span>                                                |
| <span data-ttu-id="e44e4-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e44e4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e44e4-114">maxStorage</span><span class="sxs-lookup"><span data-stu-id="e44e4-114">maxStorage</span></span>                                                 |
| <span data-ttu-id="e44e4-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e44e4-115">Size</span></span>              | <span data-ttu-id="e44e4-116">8 bytes: usuario \_ MAXSTORAGE \_ ilimitado ((unsigned Long)-1L)</span><span class="sxs-lookup"><span data-stu-id="e44e4-116">8 bytes: USER\_MAXSTORAGE\_UNLIMITED ((unsigned long) -1L)</span></span> |
| <span data-ttu-id="e44e4-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e44e4-117">Update Privilege</span></span>  | <span data-ttu-id="e44e4-118">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="e44e4-118">Domain administrator</span></span>                                       |
| <span data-ttu-id="e44e4-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e44e4-119">Update Frequency</span></span>  | <span data-ttu-id="e44e4-120">Cada vez que es necesario cambiar la cuota de disco.</span><span class="sxs-lookup"><span data-stu-id="e44e4-120">Whenever the disk quota needs to change.</span></span>                   |
| <span data-ttu-id="e44e4-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e44e4-121">Attribute-Id</span></span>      | <span data-ttu-id="e44e4-122">1.2.840.113556.1.4.76</span><span class="sxs-lookup"><span data-stu-id="e44e4-122">1.2.840.113556.1.4.76</span></span>                                      |
| <span data-ttu-id="e44e4-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e44e4-123">System-Id-Guid</span></span>    | <span data-ttu-id="e44e4-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e44e4-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span></span>                       |
| <span data-ttu-id="e44e4-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e44e4-125">Syntax</span></span>            | [<span data-ttu-id="e44e4-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="e44e4-126">**Interval**</span></span>](s-interval.md)                             |



## <a name="implementations"></a><span data-ttu-id="e44e4-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e44e4-127">Implementations</span></span>

-   [<span data-ttu-id="e44e4-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e44e4-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e44e4-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e44e4-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e44e4-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e44e4-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e44e4-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e44e4-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e44e4-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e44e4-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e44e4-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e44e4-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e44e4-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e44e4-134">Windows 2000 Server</span></span>



| <span data-ttu-id="e44e4-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="e44e4-135">Entry</span></span> | <span data-ttu-id="e44e4-136">Value</span><span class="sxs-lookup"><span data-stu-id="e44e4-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e44e4-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e44e4-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e44e4-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e44e4-139">System-Only</span></span>            | <span data-ttu-id="e44e4-140">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-140">False</span></span>                             |
| <span data-ttu-id="e44e4-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e44e4-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e44e4-142">True</span><span class="sxs-lookup"><span data-stu-id="e44e4-142">True</span></span>                              |
| <span data-ttu-id="e44e4-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e44e4-143">Is Indexed</span></span>             | <span data-ttu-id="e44e4-144">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-144">False</span></span>                             |
| <span data-ttu-id="e44e4-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e44e4-145">In Global Catalog</span></span>      | <span data-ttu-id="e44e4-146">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-146">False</span></span>                             |
| <span data-ttu-id="e44e4-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e44e4-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e44e4-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e44e4-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e44e4-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e44e4-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e44e4-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e44e4-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e44e4-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-151">Search-Flags</span></span>           | <span data-ttu-id="e44e4-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-152">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-153">System-Flags</span></span>           | <span data-ttu-id="e44e4-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-154">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e44e4-155">Classes used in</span></span>        | [<span data-ttu-id="e44e4-156">**User**</span><span class="sxs-lookup"><span data-stu-id="e44e4-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e44e4-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e44e4-157">Windows Server 2003</span></span>



| <span data-ttu-id="e44e4-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="e44e4-158">Entry</span></span> | <span data-ttu-id="e44e4-159">Value</span><span class="sxs-lookup"><span data-stu-id="e44e4-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e44e4-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e44e4-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e44e4-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="e44e4-162">System-Only</span></span>            | <span data-ttu-id="e44e4-163">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-163">False</span></span>                             |
| <span data-ttu-id="e44e4-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e44e4-164">Is-Single-Valued</span></span>       | <span data-ttu-id="e44e4-165">True</span><span class="sxs-lookup"><span data-stu-id="e44e4-165">True</span></span>                              |
| <span data-ttu-id="e44e4-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e44e4-166">Is Indexed</span></span>             | <span data-ttu-id="e44e4-167">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-167">False</span></span>                             |
| <span data-ttu-id="e44e4-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e44e4-168">In Global Catalog</span></span>      | <span data-ttu-id="e44e4-169">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-169">False</span></span>                             |
| <span data-ttu-id="e44e4-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e44e4-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="e44e4-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e44e4-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e44e4-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e44e4-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e44e4-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e44e4-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e44e4-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-174">Search-Flags</span></span>           | <span data-ttu-id="e44e4-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-175">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-176">System-Flags</span></span>           | <span data-ttu-id="e44e4-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-177">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e44e4-178">Classes used in</span></span>        | [<span data-ttu-id="e44e4-179">**User**</span><span class="sxs-lookup"><span data-stu-id="e44e4-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e44e4-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e44e4-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e44e4-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="e44e4-181">Entry</span></span> | <span data-ttu-id="e44e4-182">Value</span><span class="sxs-lookup"><span data-stu-id="e44e4-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e44e4-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e44e4-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e44e4-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e44e4-185">System-Only</span></span>            | <span data-ttu-id="e44e4-186">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-186">False</span></span>                             |
| <span data-ttu-id="e44e4-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e44e4-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e44e4-188">True</span><span class="sxs-lookup"><span data-stu-id="e44e4-188">True</span></span>                              |
| <span data-ttu-id="e44e4-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e44e4-189">Is Indexed</span></span>             | <span data-ttu-id="e44e4-190">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-190">False</span></span>                             |
| <span data-ttu-id="e44e4-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e44e4-191">In Global Catalog</span></span>      | <span data-ttu-id="e44e4-192">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-192">False</span></span>                             |
| <span data-ttu-id="e44e4-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e44e4-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e44e4-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e44e4-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e44e4-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e44e4-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e44e4-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e44e4-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e44e4-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-197">Search-Flags</span></span>           | <span data-ttu-id="e44e4-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-198">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-199">System-Flags</span></span>           | <span data-ttu-id="e44e4-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-200">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e44e4-201">Classes used in</span></span>        | [<span data-ttu-id="e44e4-202">**User**</span><span class="sxs-lookup"><span data-stu-id="e44e4-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e44e4-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e44e4-203">Windows Server 2008</span></span>



| <span data-ttu-id="e44e4-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="e44e4-204">Entry</span></span> | <span data-ttu-id="e44e4-205">Value</span><span class="sxs-lookup"><span data-stu-id="e44e4-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e44e4-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e44e4-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e44e4-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="e44e4-208">System-Only</span></span>            | <span data-ttu-id="e44e4-209">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-209">False</span></span>                             |
| <span data-ttu-id="e44e4-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e44e4-210">Is-Single-Valued</span></span>       | <span data-ttu-id="e44e4-211">True</span><span class="sxs-lookup"><span data-stu-id="e44e4-211">True</span></span>                              |
| <span data-ttu-id="e44e4-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e44e4-212">Is Indexed</span></span>             | <span data-ttu-id="e44e4-213">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-213">False</span></span>                             |
| <span data-ttu-id="e44e4-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e44e4-214">In Global Catalog</span></span>      | <span data-ttu-id="e44e4-215">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-215">False</span></span>                             |
| <span data-ttu-id="e44e4-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e44e4-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="e44e4-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e44e4-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e44e4-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e44e4-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e44e4-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e44e4-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e44e4-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-220">Search-Flags</span></span>           | <span data-ttu-id="e44e4-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-221">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-222">System-Flags</span></span>           | <span data-ttu-id="e44e4-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-223">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e44e4-224">Classes used in</span></span>        | [<span data-ttu-id="e44e4-225">**User**</span><span class="sxs-lookup"><span data-stu-id="e44e4-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e44e4-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e44e4-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e44e4-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="e44e4-227">Entry</span></span> | <span data-ttu-id="e44e4-228">Value</span><span class="sxs-lookup"><span data-stu-id="e44e4-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e44e4-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e44e4-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e44e4-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="e44e4-231">System-Only</span></span>            | <span data-ttu-id="e44e4-232">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-232">False</span></span>                             |
| <span data-ttu-id="e44e4-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e44e4-233">Is-Single-Valued</span></span>       | <span data-ttu-id="e44e4-234">True</span><span class="sxs-lookup"><span data-stu-id="e44e4-234">True</span></span>                              |
| <span data-ttu-id="e44e4-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e44e4-235">Is Indexed</span></span>             | <span data-ttu-id="e44e4-236">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-236">False</span></span>                             |
| <span data-ttu-id="e44e4-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e44e4-237">In Global Catalog</span></span>      | <span data-ttu-id="e44e4-238">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-238">False</span></span>                             |
| <span data-ttu-id="e44e4-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e44e4-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="e44e4-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e44e4-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e44e4-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e44e4-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e44e4-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e44e4-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e44e4-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-243">Search-Flags</span></span>           | <span data-ttu-id="e44e4-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-244">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-245">System-Flags</span></span>           | <span data-ttu-id="e44e4-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-246">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e44e4-247">Classes used in</span></span>        | [<span data-ttu-id="e44e4-248">**User**</span><span class="sxs-lookup"><span data-stu-id="e44e4-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e44e4-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e44e4-249">Windows Server 2012</span></span>



| <span data-ttu-id="e44e4-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="e44e4-250">Entry</span></span> | <span data-ttu-id="e44e4-251">Value</span><span class="sxs-lookup"><span data-stu-id="e44e4-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e44e4-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e44e4-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e44e4-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e44e4-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="e44e4-254">System-Only</span></span>            | <span data-ttu-id="e44e4-255">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-255">False</span></span>                             |
| <span data-ttu-id="e44e4-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e44e4-256">Is-Single-Valued</span></span>       | <span data-ttu-id="e44e4-257">True</span><span class="sxs-lookup"><span data-stu-id="e44e4-257">True</span></span>                              |
| <span data-ttu-id="e44e4-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e44e4-258">Is Indexed</span></span>             | <span data-ttu-id="e44e4-259">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-259">False</span></span>                             |
| <span data-ttu-id="e44e4-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e44e4-260">In Global Catalog</span></span>      | <span data-ttu-id="e44e4-261">False</span><span class="sxs-lookup"><span data-stu-id="e44e4-261">False</span></span>                             |
| <span data-ttu-id="e44e4-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e44e4-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="e44e4-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e44e4-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e44e4-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e44e4-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e44e4-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e44e4-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e44e4-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-266">Search-Flags</span></span>           | <span data-ttu-id="e44e4-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-267">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e44e4-268">System-Flags</span></span>           | <span data-ttu-id="e44e4-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e44e4-269">0x00000010</span></span>                        |
| <span data-ttu-id="e44e4-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e44e4-270">Classes used in</span></span>        | [<span data-ttu-id="e44e4-271">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="e44e4-271">**User**</span></span>](c-user.md)<br/> |



 

 





