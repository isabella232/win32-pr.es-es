---
title: Atributo de cuota MS-DS-Machine-Account
description: El número de cuentas de equipo que un usuario puede crear en un dominio.
ms.assetid: bcfc6a9c-b891-48c2-9c42-8154345caf08
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de cuota MS-DS-Machine-Account
- Esquema de AD del atributo MS-DS-MachineAccountQuota
topic_type:
- apiref
api_name:
- MS-DS-Machine-Account-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86de012aa876e5a0d52ac866048801872a365f1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151683"
---
# <a name="ms-ds-machine-account-quota-attribute"></a><span data-ttu-id="f7b6c-105">Atributo de cuota MS-DS-Machine-Account</span><span class="sxs-lookup"><span data-stu-id="f7b6c-105">MS-DS-Machine-Account-Quota attribute</span></span>

<span data-ttu-id="f7b6c-106">El número de cuentas de equipo que un usuario puede crear en un dominio.</span><span class="sxs-lookup"><span data-stu-id="f7b6c-106">The number of computer accounts that a user is allowed to create in a domain.</span></span>



| <span data-ttu-id="f7b6c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7b6c-107">Entry</span></span> | <span data-ttu-id="f7b6c-108">Value</span><span class="sxs-lookup"><span data-stu-id="f7b6c-108">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="f7b6c-109">CN</span><span class="sxs-lookup"><span data-stu-id="f7b6c-109">CN</span></span>                | <span data-ttu-id="f7b6c-110">Cuota de la cuenta de MS-DS-Machine</span><span class="sxs-lookup"><span data-stu-id="f7b6c-110">MS-DS-Machine-Account-Quota</span></span>                      |
| <span data-ttu-id="f7b6c-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f7b6c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f7b6c-112">MS-DS-MachineAccountQuota</span><span class="sxs-lookup"><span data-stu-id="f7b6c-112">ms-DS-MachineAccountQuota</span></span>                        |
| <span data-ttu-id="f7b6c-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f7b6c-113">Size</span></span>              | <span data-ttu-id="f7b6c-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="f7b6c-114">4 bytes</span></span>                                          |
| <span data-ttu-id="f7b6c-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f7b6c-115">Update Privilege</span></span>  | <span data-ttu-id="f7b6c-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="f7b6c-116">Domain administrator</span></span>                             |
| <span data-ttu-id="f7b6c-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f7b6c-117">Update Frequency</span></span>  | <span data-ttu-id="f7b6c-118">Siempre que es necesario cambiar la cuota de un dominio.</span><span class="sxs-lookup"><span data-stu-id="f7b6c-118">Whenever the quota for a domain needs to change.</span></span> |
| <span data-ttu-id="f7b6c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7b6c-119">Attribute-Id</span></span>      | <span data-ttu-id="f7b6c-120">1.2.840.113556.1.4.1411</span><span class="sxs-lookup"><span data-stu-id="f7b6c-120">1.2.840.113556.1.4.1411</span></span>                          |
| <span data-ttu-id="f7b6c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f7b6c-121">System-Id-Guid</span></span>    | <span data-ttu-id="f7b6c-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="f7b6c-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span></span>             |
| <span data-ttu-id="f7b6c-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7b6c-123">Syntax</span></span>            | [<span data-ttu-id="f7b6c-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-124">**Enumeration**</span></span>](s-enumeration.md)             |



## <a name="implementations"></a><span data-ttu-id="f7b6c-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f7b6c-125">Implementations</span></span>

-   [<span data-ttu-id="f7b6c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f7b6c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7b6c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7b6c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7b6c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7b6c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f7b6c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7b6c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f7b6c-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7b6c-133">Entry</span></span> | <span data-ttu-id="f7b6c-134">Value</span><span class="sxs-lookup"><span data-stu-id="f7b6c-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7b6c-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7b6c-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7b6c-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7b6c-137">System-Only</span></span>            | <span data-ttu-id="f7b6c-138">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-138">False</span></span>                                        |
| <span data-ttu-id="f7b6c-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7b6c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f7b6c-140">True</span><span class="sxs-lookup"><span data-stu-id="f7b6c-140">True</span></span>                                         |
| <span data-ttu-id="f7b6c-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7b6c-141">Is Indexed</span></span>             | <span data-ttu-id="f7b6c-142">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-142">False</span></span>                                        |
| <span data-ttu-id="f7b6c-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7b6c-143">In Global Catalog</span></span>      | <span data-ttu-id="f7b6c-144">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-144">False</span></span>                                        |
| <span data-ttu-id="f7b6c-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7b6c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7b6c-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7b6c-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7b6c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7b6c-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7b6c-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-149">Search-Flags</span></span>           | <span data-ttu-id="f7b6c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7b6c-150">0x00000000</span></span>                                   |
| <span data-ttu-id="f7b6c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-151">System-Flags</span></span>           | <span data-ttu-id="f7b6c-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7b6c-152">0x00000010</span></span>                                   |
| <span data-ttu-id="f7b6c-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7b6c-153">Classes used in</span></span>        | [<span data-ttu-id="f7b6c-154">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f7b6c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7b6c-155">Windows Server 2003</span></span>



| <span data-ttu-id="f7b6c-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7b6c-156">Entry</span></span> | <span data-ttu-id="f7b6c-157">Value</span><span class="sxs-lookup"><span data-stu-id="f7b6c-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7b6c-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7b6c-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7b6c-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7b6c-160">System-Only</span></span>            | <span data-ttu-id="f7b6c-161">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-161">False</span></span>                                        |
| <span data-ttu-id="f7b6c-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7b6c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f7b6c-163">True</span><span class="sxs-lookup"><span data-stu-id="f7b6c-163">True</span></span>                                         |
| <span data-ttu-id="f7b6c-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7b6c-164">Is Indexed</span></span>             | <span data-ttu-id="f7b6c-165">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-165">False</span></span>                                        |
| <span data-ttu-id="f7b6c-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7b6c-166">In Global Catalog</span></span>      | <span data-ttu-id="f7b6c-167">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-167">False</span></span>                                        |
| <span data-ttu-id="f7b6c-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7b6c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7b6c-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7b6c-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7b6c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7b6c-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7b6c-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-172">Search-Flags</span></span>           | <span data-ttu-id="f7b6c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7b6c-173">0x00000000</span></span>                                   |
| <span data-ttu-id="f7b6c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-174">System-Flags</span></span>           | <span data-ttu-id="f7b6c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7b6c-175">0x00000010</span></span>                                   |
| <span data-ttu-id="f7b6c-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7b6c-176">Classes used in</span></span>        | [<span data-ttu-id="f7b6c-177">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-177">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7b6c-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7b6c-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7b6c-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7b6c-179">Entry</span></span> | <span data-ttu-id="f7b6c-180">Value</span><span class="sxs-lookup"><span data-stu-id="f7b6c-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7b6c-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7b6c-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7b6c-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7b6c-183">System-Only</span></span>            | <span data-ttu-id="f7b6c-184">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-184">False</span></span>                                        |
| <span data-ttu-id="f7b6c-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7b6c-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f7b6c-186">True</span><span class="sxs-lookup"><span data-stu-id="f7b6c-186">True</span></span>                                         |
| <span data-ttu-id="f7b6c-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7b6c-187">Is Indexed</span></span>             | <span data-ttu-id="f7b6c-188">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-188">False</span></span>                                        |
| <span data-ttu-id="f7b6c-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7b6c-189">In Global Catalog</span></span>      | <span data-ttu-id="f7b6c-190">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-190">False</span></span>                                        |
| <span data-ttu-id="f7b6c-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7b6c-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7b6c-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7b6c-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7b6c-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7b6c-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7b6c-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-195">Search-Flags</span></span>           | <span data-ttu-id="f7b6c-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7b6c-196">0x00000000</span></span>                                   |
| <span data-ttu-id="f7b6c-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-197">System-Flags</span></span>           | <span data-ttu-id="f7b6c-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7b6c-198">0x00000010</span></span>                                   |
| <span data-ttu-id="f7b6c-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7b6c-199">Classes used in</span></span>        | [<span data-ttu-id="f7b6c-200">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-200">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7b6c-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7b6c-201">Windows Server 2008</span></span>



| <span data-ttu-id="f7b6c-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7b6c-202">Entry</span></span> | <span data-ttu-id="f7b6c-203">Value</span><span class="sxs-lookup"><span data-stu-id="f7b6c-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7b6c-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7b6c-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7b6c-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7b6c-206">System-Only</span></span>            | <span data-ttu-id="f7b6c-207">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-207">False</span></span>                                        |
| <span data-ttu-id="f7b6c-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7b6c-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f7b6c-209">True</span><span class="sxs-lookup"><span data-stu-id="f7b6c-209">True</span></span>                                         |
| <span data-ttu-id="f7b6c-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7b6c-210">Is Indexed</span></span>             | <span data-ttu-id="f7b6c-211">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-211">False</span></span>                                        |
| <span data-ttu-id="f7b6c-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7b6c-212">In Global Catalog</span></span>      | <span data-ttu-id="f7b6c-213">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-213">False</span></span>                                        |
| <span data-ttu-id="f7b6c-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7b6c-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7b6c-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7b6c-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7b6c-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7b6c-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7b6c-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-218">Search-Flags</span></span>           | <span data-ttu-id="f7b6c-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7b6c-219">0x00000000</span></span>                                   |
| <span data-ttu-id="f7b6c-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-220">System-Flags</span></span>           | <span data-ttu-id="f7b6c-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7b6c-221">0x00000010</span></span>                                   |
| <span data-ttu-id="f7b6c-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7b6c-222">Classes used in</span></span>        | [<span data-ttu-id="f7b6c-223">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-223">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7b6c-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7b6c-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7b6c-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7b6c-225">Entry</span></span> | <span data-ttu-id="f7b6c-226">Value</span><span class="sxs-lookup"><span data-stu-id="f7b6c-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7b6c-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7b6c-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7b6c-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7b6c-229">System-Only</span></span>            | <span data-ttu-id="f7b6c-230">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-230">False</span></span>                                        |
| <span data-ttu-id="f7b6c-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7b6c-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f7b6c-232">True</span><span class="sxs-lookup"><span data-stu-id="f7b6c-232">True</span></span>                                         |
| <span data-ttu-id="f7b6c-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7b6c-233">Is Indexed</span></span>             | <span data-ttu-id="f7b6c-234">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-234">False</span></span>                                        |
| <span data-ttu-id="f7b6c-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7b6c-235">In Global Catalog</span></span>      | <span data-ttu-id="f7b6c-236">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-236">False</span></span>                                        |
| <span data-ttu-id="f7b6c-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7b6c-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7b6c-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7b6c-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7b6c-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7b6c-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7b6c-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-241">Search-Flags</span></span>           | <span data-ttu-id="f7b6c-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7b6c-242">0x00000000</span></span>                                   |
| <span data-ttu-id="f7b6c-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-243">System-Flags</span></span>           | <span data-ttu-id="f7b6c-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7b6c-244">0x00000010</span></span>                                   |
| <span data-ttu-id="f7b6c-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7b6c-245">Classes used in</span></span>        | [<span data-ttu-id="f7b6c-246">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-246">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7b6c-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7b6c-247">Windows Server 2012</span></span>



| <span data-ttu-id="f7b6c-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7b6c-248">Entry</span></span> | <span data-ttu-id="f7b6c-249">Value</span><span class="sxs-lookup"><span data-stu-id="f7b6c-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7b6c-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f7b6c-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7b6c-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7b6c-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7b6c-252">System-Only</span></span>            | <span data-ttu-id="f7b6c-253">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-253">False</span></span>                                        |
| <span data-ttu-id="f7b6c-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f7b6c-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f7b6c-255">True</span><span class="sxs-lookup"><span data-stu-id="f7b6c-255">True</span></span>                                         |
| <span data-ttu-id="f7b6c-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f7b6c-256">Is Indexed</span></span>             | <span data-ttu-id="f7b6c-257">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-257">False</span></span>                                        |
| <span data-ttu-id="f7b6c-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7b6c-258">In Global Catalog</span></span>      | <span data-ttu-id="f7b6c-259">False</span><span class="sxs-lookup"><span data-stu-id="f7b6c-259">False</span></span>                                        |
| <span data-ttu-id="f7b6c-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f7b6c-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7b6c-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7b6c-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7b6c-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7b6c-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7b6c-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7b6c-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-264">Search-Flags</span></span>           | <span data-ttu-id="f7b6c-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7b6c-265">0x00000000</span></span>                                   |
| <span data-ttu-id="f7b6c-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7b6c-266">System-Flags</span></span>           | <span data-ttu-id="f7b6c-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7b6c-267">0x00000010</span></span>                                   |
| <span data-ttu-id="f7b6c-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f7b6c-268">Classes used in</span></span>        | [<span data-ttu-id="f7b6c-269">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="f7b6c-269">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





