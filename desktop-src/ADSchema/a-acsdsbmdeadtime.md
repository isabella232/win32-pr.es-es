---
title: Atributo ACS-DSBM-DeadTime
description: Este atributo contiene el intervalo de tiempo de inactividad (DSBMDeadInterval) de elección para un dominio.
ms.assetid: c3a0780c-1786-4631-b870-77146de87f18
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ACS-DSBM-DeadTime
- aCSDSBMDeadTime esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-DSBM-DeadTime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8b1c980175dc985c3a718d15323be0b8d1b411
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151506"
---
# <a name="acs-dsbm-deadtime-attribute"></a><span data-ttu-id="6d160-105">Atributo ACS-DSBM-DeadTime</span><span class="sxs-lookup"><span data-stu-id="6d160-105">ACS-DSBM-DeadTime attribute</span></span>

<span data-ttu-id="6d160-106">Este atributo contiene el intervalo de tiempo de inactividad (DSBMDeadInterval) de elección para un dominio.</span><span class="sxs-lookup"><span data-stu-id="6d160-106">This attribute contains the election dead time interval (DSBMDeadInterval) for a domain.</span></span> <span data-ttu-id="6d160-107">Si el administrador de ancho de banda de subred designado no envía \_ un \_ anuncio soy DSBM durante este intervalo, los demás administradores de ancho de banda de subred (SBMS) del dominio eligen un nuevo DSBM.</span><span class="sxs-lookup"><span data-stu-id="6d160-107">If the Designated Subnet Bandwidth Manager does not send out an I\_AM\_DSBM advertisement during this interval, then the other Subnet Bandwidth Managers (SBMs) in the domain elect a new DSBM.</span></span>



| <span data-ttu-id="6d160-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d160-108">Entry</span></span> | <span data-ttu-id="6d160-109">Value</span><span class="sxs-lookup"><span data-stu-id="6d160-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6d160-110">CN</span><span class="sxs-lookup"><span data-stu-id="6d160-110">CN</span></span>                | <span data-ttu-id="6d160-111">ACS-DSBM-DeadTime</span><span class="sxs-lookup"><span data-stu-id="6d160-111">ACS-DSBM-DeadTime</span></span>                    |
| <span data-ttu-id="6d160-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6d160-112">Ldap-Display-Name</span></span> | <span data-ttu-id="6d160-113">aCSDSBMDeadTime</span><span class="sxs-lookup"><span data-stu-id="6d160-113">aCSDSBMDeadTime</span></span>                      |
| <span data-ttu-id="6d160-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6d160-114">Size</span></span>              | <span data-ttu-id="6d160-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="6d160-115">4 bytes</span></span>                              |
| <span data-ttu-id="6d160-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6d160-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="6d160-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6d160-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6d160-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6d160-118">Attribute-Id</span></span>      | <span data-ttu-id="6d160-119">1.2.840.113556.1.4.778</span><span class="sxs-lookup"><span data-stu-id="6d160-119">1.2.840.113556.1.4.778</span></span>               |
| <span data-ttu-id="6d160-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6d160-120">System-Id-Guid</span></span>    | <span data-ttu-id="6d160-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6d160-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="6d160-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d160-122">Syntax</span></span>            | [<span data-ttu-id="6d160-123">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="6d160-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6d160-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6d160-124">Implementations</span></span>

-   [<span data-ttu-id="6d160-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6d160-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6d160-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6d160-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6d160-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6d160-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6d160-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6d160-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6d160-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6d160-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6d160-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6d160-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6d160-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d160-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6d160-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d160-132">Entry</span></span> | <span data-ttu-id="6d160-133">Value</span><span class="sxs-lookup"><span data-stu-id="6d160-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6d160-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d160-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d160-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d160-136">System-Only</span></span>            | <span data-ttu-id="6d160-137">False</span><span class="sxs-lookup"><span data-stu-id="6d160-137">False</span></span>                                        |
| <span data-ttu-id="6d160-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d160-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6d160-139">True</span><span class="sxs-lookup"><span data-stu-id="6d160-139">True</span></span>                                         |
| <span data-ttu-id="6d160-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d160-140">Is Indexed</span></span>             | <span data-ttu-id="6d160-141">False</span><span class="sxs-lookup"><span data-stu-id="6d160-141">False</span></span>                                        |
| <span data-ttu-id="6d160-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d160-142">In Global Catalog</span></span>      | <span data-ttu-id="6d160-143">False</span><span class="sxs-lookup"><span data-stu-id="6d160-143">False</span></span>                                        |
| <span data-ttu-id="6d160-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d160-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d160-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d160-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6d160-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d160-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6d160-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d160-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6d160-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-148">Search-Flags</span></span>           | <span data-ttu-id="6d160-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d160-149">0x00000000</span></span>                                   |
| <span data-ttu-id="6d160-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-150">System-Flags</span></span>           | <span data-ttu-id="6d160-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d160-151">0x00000010</span></span>                                   |
| <span data-ttu-id="6d160-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d160-152">Classes used in</span></span>        | [<span data-ttu-id="6d160-153">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="6d160-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6d160-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d160-154">Windows Server 2003</span></span>



| <span data-ttu-id="6d160-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d160-155">Entry</span></span> | <span data-ttu-id="6d160-156">Value</span><span class="sxs-lookup"><span data-stu-id="6d160-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6d160-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d160-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d160-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d160-159">System-Only</span></span>            | <span data-ttu-id="6d160-160">False</span><span class="sxs-lookup"><span data-stu-id="6d160-160">False</span></span>                                        |
| <span data-ttu-id="6d160-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d160-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6d160-162">True</span><span class="sxs-lookup"><span data-stu-id="6d160-162">True</span></span>                                         |
| <span data-ttu-id="6d160-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d160-163">Is Indexed</span></span>             | <span data-ttu-id="6d160-164">False</span><span class="sxs-lookup"><span data-stu-id="6d160-164">False</span></span>                                        |
| <span data-ttu-id="6d160-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d160-165">In Global Catalog</span></span>      | <span data-ttu-id="6d160-166">False</span><span class="sxs-lookup"><span data-stu-id="6d160-166">False</span></span>                                        |
| <span data-ttu-id="6d160-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d160-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d160-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d160-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6d160-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d160-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6d160-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d160-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6d160-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-171">Search-Flags</span></span>           | <span data-ttu-id="6d160-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d160-172">0x00000000</span></span>                                   |
| <span data-ttu-id="6d160-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-173">System-Flags</span></span>           | <span data-ttu-id="6d160-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d160-174">0x00000010</span></span>                                   |
| <span data-ttu-id="6d160-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d160-175">Classes used in</span></span>        | [<span data-ttu-id="6d160-176">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="6d160-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6d160-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6d160-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6d160-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d160-178">Entry</span></span> | <span data-ttu-id="6d160-179">Value</span><span class="sxs-lookup"><span data-stu-id="6d160-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6d160-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d160-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d160-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d160-182">System-Only</span></span>            | <span data-ttu-id="6d160-183">False</span><span class="sxs-lookup"><span data-stu-id="6d160-183">False</span></span>                                        |
| <span data-ttu-id="6d160-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d160-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6d160-185">True</span><span class="sxs-lookup"><span data-stu-id="6d160-185">True</span></span>                                         |
| <span data-ttu-id="6d160-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d160-186">Is Indexed</span></span>             | <span data-ttu-id="6d160-187">False</span><span class="sxs-lookup"><span data-stu-id="6d160-187">False</span></span>                                        |
| <span data-ttu-id="6d160-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d160-188">In Global Catalog</span></span>      | <span data-ttu-id="6d160-189">False</span><span class="sxs-lookup"><span data-stu-id="6d160-189">False</span></span>                                        |
| <span data-ttu-id="6d160-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d160-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d160-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d160-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6d160-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d160-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6d160-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d160-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6d160-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-194">Search-Flags</span></span>           | <span data-ttu-id="6d160-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d160-195">0x00000000</span></span>                                   |
| <span data-ttu-id="6d160-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-196">System-Flags</span></span>           | <span data-ttu-id="6d160-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d160-197">0x00000010</span></span>                                   |
| <span data-ttu-id="6d160-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d160-198">Classes used in</span></span>        | [<span data-ttu-id="6d160-199">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="6d160-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6d160-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d160-200">Windows Server 2008</span></span>



| <span data-ttu-id="6d160-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d160-201">Entry</span></span> | <span data-ttu-id="6d160-202">Value</span><span class="sxs-lookup"><span data-stu-id="6d160-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6d160-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d160-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d160-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d160-205">System-Only</span></span>            | <span data-ttu-id="6d160-206">False</span><span class="sxs-lookup"><span data-stu-id="6d160-206">False</span></span>                                        |
| <span data-ttu-id="6d160-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d160-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6d160-208">True</span><span class="sxs-lookup"><span data-stu-id="6d160-208">True</span></span>                                         |
| <span data-ttu-id="6d160-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d160-209">Is Indexed</span></span>             | <span data-ttu-id="6d160-210">False</span><span class="sxs-lookup"><span data-stu-id="6d160-210">False</span></span>                                        |
| <span data-ttu-id="6d160-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d160-211">In Global Catalog</span></span>      | <span data-ttu-id="6d160-212">False</span><span class="sxs-lookup"><span data-stu-id="6d160-212">False</span></span>                                        |
| <span data-ttu-id="6d160-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d160-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d160-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d160-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6d160-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d160-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6d160-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d160-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6d160-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-217">Search-Flags</span></span>           | <span data-ttu-id="6d160-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d160-218">0x00000000</span></span>                                   |
| <span data-ttu-id="6d160-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-219">System-Flags</span></span>           | <span data-ttu-id="6d160-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d160-220">0x00000010</span></span>                                   |
| <span data-ttu-id="6d160-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d160-221">Classes used in</span></span>        | [<span data-ttu-id="6d160-222">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="6d160-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6d160-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d160-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6d160-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d160-224">Entry</span></span> | <span data-ttu-id="6d160-225">Value</span><span class="sxs-lookup"><span data-stu-id="6d160-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6d160-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d160-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d160-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d160-228">System-Only</span></span>            | <span data-ttu-id="6d160-229">False</span><span class="sxs-lookup"><span data-stu-id="6d160-229">False</span></span>                                        |
| <span data-ttu-id="6d160-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d160-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6d160-231">True</span><span class="sxs-lookup"><span data-stu-id="6d160-231">True</span></span>                                         |
| <span data-ttu-id="6d160-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d160-232">Is Indexed</span></span>             | <span data-ttu-id="6d160-233">False</span><span class="sxs-lookup"><span data-stu-id="6d160-233">False</span></span>                                        |
| <span data-ttu-id="6d160-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d160-234">In Global Catalog</span></span>      | <span data-ttu-id="6d160-235">False</span><span class="sxs-lookup"><span data-stu-id="6d160-235">False</span></span>                                        |
| <span data-ttu-id="6d160-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d160-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d160-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d160-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6d160-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d160-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6d160-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d160-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6d160-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-240">Search-Flags</span></span>           | <span data-ttu-id="6d160-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d160-241">0x00000000</span></span>                                   |
| <span data-ttu-id="6d160-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-242">System-Flags</span></span>           | <span data-ttu-id="6d160-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d160-243">0x00000010</span></span>                                   |
| <span data-ttu-id="6d160-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d160-244">Classes used in</span></span>        | [<span data-ttu-id="6d160-245">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="6d160-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6d160-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d160-246">Windows Server 2012</span></span>



| <span data-ttu-id="6d160-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d160-247">Entry</span></span> | <span data-ttu-id="6d160-248">Value</span><span class="sxs-lookup"><span data-stu-id="6d160-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6d160-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d160-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d160-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6d160-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d160-251">System-Only</span></span>            | <span data-ttu-id="6d160-252">False</span><span class="sxs-lookup"><span data-stu-id="6d160-252">False</span></span>                                        |
| <span data-ttu-id="6d160-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d160-253">Is-Single-Valued</span></span>       | <span data-ttu-id="6d160-254">True</span><span class="sxs-lookup"><span data-stu-id="6d160-254">True</span></span>                                         |
| <span data-ttu-id="6d160-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d160-255">Is Indexed</span></span>             | <span data-ttu-id="6d160-256">False</span><span class="sxs-lookup"><span data-stu-id="6d160-256">False</span></span>                                        |
| <span data-ttu-id="6d160-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d160-257">In Global Catalog</span></span>      | <span data-ttu-id="6d160-258">False</span><span class="sxs-lookup"><span data-stu-id="6d160-258">False</span></span>                                        |
| <span data-ttu-id="6d160-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d160-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d160-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d160-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6d160-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d160-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6d160-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d160-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6d160-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-263">Search-Flags</span></span>           | <span data-ttu-id="6d160-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d160-264">0x00000000</span></span>                                   |
| <span data-ttu-id="6d160-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d160-265">System-Flags</span></span>           | <span data-ttu-id="6d160-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d160-266">0x00000010</span></span>                                   |
| <span data-ttu-id="6d160-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d160-267">Classes used in</span></span>        | [<span data-ttu-id="6d160-268">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="6d160-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





