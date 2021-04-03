---
title: Atributo ACS-DSBM-Refresh
description: Este atributo contiene el valor de temporizador de intervalo que determina si el administrador de ancho de banda de subred designado (DSBM) envía un mensaje de actualización (soy \_ \_ DSBM) a todos los administradores de ancho de banda de subred de un dominio.
ms.assetid: 018fd748-ca2e-41e1-a920-224a32e13e21
ms.tgt_platform: multiple
keywords:
- Esquema AD de atributo ACS-DSBM-Refresh
- aCSDSBMRefresh esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-DSBM-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d662b886a8c97f3d155d3c1b40efcef67f7f1f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997320"
---
# <a name="acs-dsbm-refresh-attribute"></a><span data-ttu-id="affae-105">Atributo ACS-DSBM-Refresh</span><span class="sxs-lookup"><span data-stu-id="affae-105">ACS-DSBM-Refresh attribute</span></span>

<span data-ttu-id="affae-106">Este atributo contiene el valor de temporizador de intervalo que determina si el administrador de ancho de banda de subred designado (DSBM) envía un mensaje de actualización (soy \_ \_ DSBM) a todos los administradores de ancho de banda de subred de un dominio.</span><span class="sxs-lookup"><span data-stu-id="affae-106">This attribute contains the interval timer value that determines when the Designated Subnet Bandwidth Manager (DSBM) sends out a refresh message (I\_AM\_DSBM) to all of the Subnet Bandwidth Managers in a domain.</span></span>



| <span data-ttu-id="affae-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="affae-107">Entry</span></span> | <span data-ttu-id="affae-108">Value</span><span class="sxs-lookup"><span data-stu-id="affae-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="affae-109">CN</span><span class="sxs-lookup"><span data-stu-id="affae-109">CN</span></span>                | <span data-ttu-id="affae-110">ACS-DSBM-actualizar</span><span class="sxs-lookup"><span data-stu-id="affae-110">ACS-DSBM-Refresh</span></span>                     |
| <span data-ttu-id="affae-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="affae-111">Ldap-Display-Name</span></span> | <span data-ttu-id="affae-112">aCSDSBMRefresh</span><span class="sxs-lookup"><span data-stu-id="affae-112">aCSDSBMRefresh</span></span>                       |
| <span data-ttu-id="affae-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="affae-113">Size</span></span>              | <span data-ttu-id="affae-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="affae-114">4 bytes</span></span>                              |
| <span data-ttu-id="affae-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="affae-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="affae-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="affae-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="affae-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="affae-117">Attribute-Id</span></span>      | <span data-ttu-id="affae-118">1.2.840.113556.1.4.777</span><span class="sxs-lookup"><span data-stu-id="affae-118">1.2.840.113556.1.4.777</span></span>               |
| <span data-ttu-id="affae-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="affae-119">System-Id-Guid</span></span>    | <span data-ttu-id="affae-120">1cb3559f-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="affae-120">1cb3559f-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="affae-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="affae-121">Syntax</span></span>            | [<span data-ttu-id="affae-122">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="affae-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="affae-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="affae-123">Implementations</span></span>

-   [<span data-ttu-id="affae-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="affae-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="affae-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="affae-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="affae-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="affae-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="affae-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="affae-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="affae-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="affae-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="affae-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="affae-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="affae-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="affae-130">Windows 2000 Server</span></span>



| <span data-ttu-id="affae-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="affae-131">Entry</span></span> | <span data-ttu-id="affae-132">Value</span><span class="sxs-lookup"><span data-stu-id="affae-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="affae-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="affae-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="affae-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="affae-135">System-Only</span></span>            | <span data-ttu-id="affae-136">False</span><span class="sxs-lookup"><span data-stu-id="affae-136">False</span></span>                                        |
| <span data-ttu-id="affae-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="affae-137">Is-Single-Valued</span></span>       | <span data-ttu-id="affae-138">True</span><span class="sxs-lookup"><span data-stu-id="affae-138">True</span></span>                                         |
| <span data-ttu-id="affae-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="affae-139">Is Indexed</span></span>             | <span data-ttu-id="affae-140">False</span><span class="sxs-lookup"><span data-stu-id="affae-140">False</span></span>                                        |
| <span data-ttu-id="affae-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="affae-141">In Global Catalog</span></span>      | <span data-ttu-id="affae-142">False</span><span class="sxs-lookup"><span data-stu-id="affae-142">False</span></span>                                        |
| <span data-ttu-id="affae-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="affae-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="affae-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="affae-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="affae-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="affae-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="affae-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="affae-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="affae-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-147">Search-Flags</span></span>           | <span data-ttu-id="affae-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="affae-148">0x00000000</span></span>                                   |
| <span data-ttu-id="affae-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-149">System-Flags</span></span>           | <span data-ttu-id="affae-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="affae-150">0x00000010</span></span>                                   |
| <span data-ttu-id="affae-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="affae-151">Classes used in</span></span>        | [<span data-ttu-id="affae-152">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="affae-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="affae-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="affae-153">Windows Server 2003</span></span>



| <span data-ttu-id="affae-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="affae-154">Entry</span></span> | <span data-ttu-id="affae-155">Value</span><span class="sxs-lookup"><span data-stu-id="affae-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="affae-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="affae-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="affae-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="affae-158">System-Only</span></span>            | <span data-ttu-id="affae-159">False</span><span class="sxs-lookup"><span data-stu-id="affae-159">False</span></span>                                        |
| <span data-ttu-id="affae-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="affae-160">Is-Single-Valued</span></span>       | <span data-ttu-id="affae-161">True</span><span class="sxs-lookup"><span data-stu-id="affae-161">True</span></span>                                         |
| <span data-ttu-id="affae-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="affae-162">Is Indexed</span></span>             | <span data-ttu-id="affae-163">False</span><span class="sxs-lookup"><span data-stu-id="affae-163">False</span></span>                                        |
| <span data-ttu-id="affae-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="affae-164">In Global Catalog</span></span>      | <span data-ttu-id="affae-165">False</span><span class="sxs-lookup"><span data-stu-id="affae-165">False</span></span>                                        |
| <span data-ttu-id="affae-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="affae-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="affae-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="affae-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="affae-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="affae-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="affae-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="affae-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="affae-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-170">Search-Flags</span></span>           | <span data-ttu-id="affae-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="affae-171">0x00000000</span></span>                                   |
| <span data-ttu-id="affae-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-172">System-Flags</span></span>           | <span data-ttu-id="affae-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="affae-173">0x00000010</span></span>                                   |
| <span data-ttu-id="affae-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="affae-174">Classes used in</span></span>        | [<span data-ttu-id="affae-175">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="affae-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="affae-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="affae-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="affae-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="affae-177">Entry</span></span> | <span data-ttu-id="affae-178">Value</span><span class="sxs-lookup"><span data-stu-id="affae-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="affae-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="affae-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="affae-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="affae-181">System-Only</span></span>            | <span data-ttu-id="affae-182">False</span><span class="sxs-lookup"><span data-stu-id="affae-182">False</span></span>                                        |
| <span data-ttu-id="affae-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="affae-183">Is-Single-Valued</span></span>       | <span data-ttu-id="affae-184">True</span><span class="sxs-lookup"><span data-stu-id="affae-184">True</span></span>                                         |
| <span data-ttu-id="affae-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="affae-185">Is Indexed</span></span>             | <span data-ttu-id="affae-186">False</span><span class="sxs-lookup"><span data-stu-id="affae-186">False</span></span>                                        |
| <span data-ttu-id="affae-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="affae-187">In Global Catalog</span></span>      | <span data-ttu-id="affae-188">False</span><span class="sxs-lookup"><span data-stu-id="affae-188">False</span></span>                                        |
| <span data-ttu-id="affae-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="affae-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="affae-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="affae-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="affae-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="affae-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="affae-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="affae-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="affae-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-193">Search-Flags</span></span>           | <span data-ttu-id="affae-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="affae-194">0x00000000</span></span>                                   |
| <span data-ttu-id="affae-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-195">System-Flags</span></span>           | <span data-ttu-id="affae-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="affae-196">0x00000010</span></span>                                   |
| <span data-ttu-id="affae-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="affae-197">Classes used in</span></span>        | [<span data-ttu-id="affae-198">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="affae-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="affae-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="affae-199">Windows Server 2008</span></span>



| <span data-ttu-id="affae-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="affae-200">Entry</span></span> | <span data-ttu-id="affae-201">Value</span><span class="sxs-lookup"><span data-stu-id="affae-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="affae-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="affae-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="affae-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="affae-204">System-Only</span></span>            | <span data-ttu-id="affae-205">False</span><span class="sxs-lookup"><span data-stu-id="affae-205">False</span></span>                                        |
| <span data-ttu-id="affae-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="affae-206">Is-Single-Valued</span></span>       | <span data-ttu-id="affae-207">True</span><span class="sxs-lookup"><span data-stu-id="affae-207">True</span></span>                                         |
| <span data-ttu-id="affae-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="affae-208">Is Indexed</span></span>             | <span data-ttu-id="affae-209">False</span><span class="sxs-lookup"><span data-stu-id="affae-209">False</span></span>                                        |
| <span data-ttu-id="affae-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="affae-210">In Global Catalog</span></span>      | <span data-ttu-id="affae-211">False</span><span class="sxs-lookup"><span data-stu-id="affae-211">False</span></span>                                        |
| <span data-ttu-id="affae-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="affae-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="affae-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="affae-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="affae-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="affae-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="affae-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="affae-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="affae-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-216">Search-Flags</span></span>           | <span data-ttu-id="affae-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="affae-217">0x00000000</span></span>                                   |
| <span data-ttu-id="affae-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-218">System-Flags</span></span>           | <span data-ttu-id="affae-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="affae-219">0x00000010</span></span>                                   |
| <span data-ttu-id="affae-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="affae-220">Classes used in</span></span>        | [<span data-ttu-id="affae-221">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="affae-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="affae-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="affae-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="affae-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="affae-223">Entry</span></span> | <span data-ttu-id="affae-224">Value</span><span class="sxs-lookup"><span data-stu-id="affae-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="affae-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="affae-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="affae-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="affae-227">System-Only</span></span>            | <span data-ttu-id="affae-228">False</span><span class="sxs-lookup"><span data-stu-id="affae-228">False</span></span>                                        |
| <span data-ttu-id="affae-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="affae-229">Is-Single-Valued</span></span>       | <span data-ttu-id="affae-230">True</span><span class="sxs-lookup"><span data-stu-id="affae-230">True</span></span>                                         |
| <span data-ttu-id="affae-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="affae-231">Is Indexed</span></span>             | <span data-ttu-id="affae-232">False</span><span class="sxs-lookup"><span data-stu-id="affae-232">False</span></span>                                        |
| <span data-ttu-id="affae-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="affae-233">In Global Catalog</span></span>      | <span data-ttu-id="affae-234">False</span><span class="sxs-lookup"><span data-stu-id="affae-234">False</span></span>                                        |
| <span data-ttu-id="affae-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="affae-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="affae-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="affae-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="affae-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="affae-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="affae-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="affae-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="affae-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-239">Search-Flags</span></span>           | <span data-ttu-id="affae-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="affae-240">0x00000000</span></span>                                   |
| <span data-ttu-id="affae-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-241">System-Flags</span></span>           | <span data-ttu-id="affae-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="affae-242">0x00000010</span></span>                                   |
| <span data-ttu-id="affae-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="affae-243">Classes used in</span></span>        | [<span data-ttu-id="affae-244">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="affae-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="affae-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="affae-245">Windows Server 2012</span></span>



| <span data-ttu-id="affae-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="affae-246">Entry</span></span> | <span data-ttu-id="affae-247">Value</span><span class="sxs-lookup"><span data-stu-id="affae-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="affae-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="affae-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="affae-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="affae-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="affae-250">System-Only</span></span>            | <span data-ttu-id="affae-251">False</span><span class="sxs-lookup"><span data-stu-id="affae-251">False</span></span>                                        |
| <span data-ttu-id="affae-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="affae-252">Is-Single-Valued</span></span>       | <span data-ttu-id="affae-253">True</span><span class="sxs-lookup"><span data-stu-id="affae-253">True</span></span>                                         |
| <span data-ttu-id="affae-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="affae-254">Is Indexed</span></span>             | <span data-ttu-id="affae-255">False</span><span class="sxs-lookup"><span data-stu-id="affae-255">False</span></span>                                        |
| <span data-ttu-id="affae-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="affae-256">In Global Catalog</span></span>      | <span data-ttu-id="affae-257">False</span><span class="sxs-lookup"><span data-stu-id="affae-257">False</span></span>                                        |
| <span data-ttu-id="affae-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="affae-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="affae-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="affae-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="affae-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="affae-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="affae-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="affae-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="affae-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-262">Search-Flags</span></span>           | <span data-ttu-id="affae-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="affae-263">0x00000000</span></span>                                   |
| <span data-ttu-id="affae-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="affae-264">System-Flags</span></span>           | <span data-ttu-id="affae-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="affae-265">0x00000010</span></span>                                   |
| <span data-ttu-id="affae-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="affae-266">Classes used in</span></span>        | [<span data-ttu-id="affae-267">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="affae-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





