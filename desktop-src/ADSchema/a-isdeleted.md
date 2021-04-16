---
title: Is-Deleted atributo)
description: Si es TRUE, este objeto se ha marcado para su eliminación y no se pueden crear instancias de él. Una vez que haya expirado el período de desecho, se quitará del sistema.
ms.assetid: 549b5161-5d2f-47d7-8192-4480334ef13d
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Is-Deleted
- Esquema de AD del atributo isDeleted
topic_type:
- apiref
api_name:
- Is-Deleted
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b30dec5ed139da60853324b82cc6e0f55fcc70
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658496"
---
# <a name="is-deleted-attribute"></a><span data-ttu-id="8b20e-106">Is-Deleted atributo)</span><span class="sxs-lookup"><span data-stu-id="8b20e-106">Is-Deleted attribute</span></span>

<span data-ttu-id="8b20e-107">Si **es true**, este objeto se ha marcado para su eliminación y no se pueden crear instancias de él.</span><span class="sxs-lookup"><span data-stu-id="8b20e-107">If **TRUE**, this object has been marked for deletion and cannot be instantiated.</span></span> <span data-ttu-id="8b20e-108">Una vez que haya expirado el período de desecho, se quitará del sistema.</span><span class="sxs-lookup"><span data-stu-id="8b20e-108">After the tombstone period has expired, it will be removed from the system.</span></span>



| <span data-ttu-id="8b20e-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b20e-109">Entry</span></span> | <span data-ttu-id="8b20e-110">Value</span><span class="sxs-lookup"><span data-stu-id="8b20e-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8b20e-111">CN</span><span class="sxs-lookup"><span data-stu-id="8b20e-111">CN</span></span>                | <span data-ttu-id="8b20e-112">Is-Deleted</span><span class="sxs-lookup"><span data-stu-id="8b20e-112">Is-Deleted</span></span>                           |
| <span data-ttu-id="8b20e-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="8b20e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8b20e-114">isDeleted</span><span class="sxs-lookup"><span data-stu-id="8b20e-114">isDeleted</span></span>                            |
| <span data-ttu-id="8b20e-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8b20e-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="8b20e-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="8b20e-116">Update Privilege</span></span>  | <span data-ttu-id="8b20e-117">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="8b20e-117">Domain administrator</span></span>                 |
| <span data-ttu-id="8b20e-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="8b20e-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8b20e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8b20e-119">Attribute-Id</span></span>      | <span data-ttu-id="8b20e-120">1.2.840.113556.1.2.48</span><span class="sxs-lookup"><span data-stu-id="8b20e-120">1.2.840.113556.1.2.48</span></span>                |
| <span data-ttu-id="8b20e-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8b20e-121">System-Id-Guid</span></span>    | <span data-ttu-id="8b20e-122">bf96798f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8b20e-122">bf96798f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="8b20e-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b20e-123">Syntax</span></span>            | [<span data-ttu-id="8b20e-124">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="8b20e-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="8b20e-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="8b20e-125">Implementations</span></span>

-   [<span data-ttu-id="8b20e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8b20e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8b20e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8b20e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8b20e-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8b20e-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8b20e-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8b20e-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8b20e-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8b20e-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8b20e-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8b20e-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8b20e-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8b20e-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8b20e-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b20e-133">Windows 2000 Server</span></span>



| <span data-ttu-id="8b20e-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b20e-134">Entry</span></span> | <span data-ttu-id="8b20e-135">Value</span><span class="sxs-lookup"><span data-stu-id="8b20e-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b20e-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b20e-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b20e-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b20e-137">MAPI-Id</span></span>                | <span data-ttu-id="8b20e-138">0x80C0</span><span class="sxs-lookup"><span data-stu-id="8b20e-138">0x80C0</span></span>                          |
| <span data-ttu-id="8b20e-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b20e-139">System-Only</span></span>            | <span data-ttu-id="8b20e-140">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-140">True</span></span>                            |
| <span data-ttu-id="8b20e-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b20e-141">Is-Single-Valued</span></span>       | <span data-ttu-id="8b20e-142">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-142">True</span></span>                            |
| <span data-ttu-id="8b20e-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b20e-143">Is Indexed</span></span>             | <span data-ttu-id="8b20e-144">False</span><span class="sxs-lookup"><span data-stu-id="8b20e-144">False</span></span>                           |
| <span data-ttu-id="8b20e-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b20e-145">In Global Catalog</span></span>      | <span data-ttu-id="8b20e-146">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-146">True</span></span>                            |
| <span data-ttu-id="8b20e-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b20e-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b20e-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b20e-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b20e-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b20e-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b20e-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b20e-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b20e-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-151">Search-Flags</span></span>           | <span data-ttu-id="8b20e-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b20e-152">0x00000000</span></span>                      |
| <span data-ttu-id="8b20e-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-153">System-Flags</span></span>           | <span data-ttu-id="8b20e-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b20e-154">0x00000012</span></span>                      |
| <span data-ttu-id="8b20e-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b20e-155">Classes used in</span></span>        | [<span data-ttu-id="8b20e-156">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8b20e-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8b20e-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b20e-157">Windows Server 2003</span></span>



| <span data-ttu-id="8b20e-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b20e-158">Entry</span></span> | <span data-ttu-id="8b20e-159">Value</span><span class="sxs-lookup"><span data-stu-id="8b20e-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b20e-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b20e-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b20e-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b20e-161">MAPI-Id</span></span>                | <span data-ttu-id="8b20e-162">0x80C0</span><span class="sxs-lookup"><span data-stu-id="8b20e-162">0x80C0</span></span>                          |
| <span data-ttu-id="8b20e-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b20e-163">System-Only</span></span>            | <span data-ttu-id="8b20e-164">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-164">True</span></span>                            |
| <span data-ttu-id="8b20e-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b20e-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8b20e-166">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-166">True</span></span>                            |
| <span data-ttu-id="8b20e-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b20e-167">Is Indexed</span></span>             | <span data-ttu-id="8b20e-168">False</span><span class="sxs-lookup"><span data-stu-id="8b20e-168">False</span></span>                           |
| <span data-ttu-id="8b20e-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b20e-169">In Global Catalog</span></span>      | <span data-ttu-id="8b20e-170">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-170">True</span></span>                            |
| <span data-ttu-id="8b20e-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b20e-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b20e-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b20e-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b20e-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b20e-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b20e-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b20e-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b20e-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-175">Search-Flags</span></span>           | <span data-ttu-id="8b20e-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b20e-176">0x00000000</span></span>                      |
| <span data-ttu-id="8b20e-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-177">System-Flags</span></span>           | <span data-ttu-id="8b20e-178">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b20e-178">0x00000012</span></span>                      |
| <span data-ttu-id="8b20e-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b20e-179">Classes used in</span></span>        | [<span data-ttu-id="8b20e-180">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8b20e-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8b20e-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="8b20e-181">ADAM</span></span>



| <span data-ttu-id="8b20e-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b20e-182">Entry</span></span> | <span data-ttu-id="8b20e-183">Value</span><span class="sxs-lookup"><span data-stu-id="8b20e-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b20e-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b20e-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b20e-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b20e-185">MAPI-Id</span></span>                | <span data-ttu-id="8b20e-186">0x80C0</span><span class="sxs-lookup"><span data-stu-id="8b20e-186">0x80C0</span></span>                          |
| <span data-ttu-id="8b20e-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b20e-187">System-Only</span></span>            | <span data-ttu-id="8b20e-188">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-188">True</span></span>                            |
| <span data-ttu-id="8b20e-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b20e-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8b20e-190">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-190">True</span></span>                            |
| <span data-ttu-id="8b20e-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b20e-191">Is Indexed</span></span>             | <span data-ttu-id="8b20e-192">False</span><span class="sxs-lookup"><span data-stu-id="8b20e-192">False</span></span>                           |
| <span data-ttu-id="8b20e-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b20e-193">In Global Catalog</span></span>      | <span data-ttu-id="8b20e-194">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-194">True</span></span>                            |
| <span data-ttu-id="8b20e-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b20e-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b20e-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b20e-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b20e-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b20e-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b20e-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b20e-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b20e-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-199">Search-Flags</span></span>           | <span data-ttu-id="8b20e-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b20e-200">0x00000000</span></span>                      |
| <span data-ttu-id="8b20e-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-201">System-Flags</span></span>           | <span data-ttu-id="8b20e-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b20e-202">0x00000012</span></span>                      |
| <span data-ttu-id="8b20e-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b20e-203">Classes used in</span></span>        | [<span data-ttu-id="8b20e-204">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8b20e-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8b20e-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8b20e-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8b20e-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b20e-206">Entry</span></span> | <span data-ttu-id="8b20e-207">Value</span><span class="sxs-lookup"><span data-stu-id="8b20e-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b20e-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b20e-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b20e-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b20e-209">MAPI-Id</span></span>                | <span data-ttu-id="8b20e-210">0x80C0</span><span class="sxs-lookup"><span data-stu-id="8b20e-210">0x80C0</span></span>                          |
| <span data-ttu-id="8b20e-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b20e-211">System-Only</span></span>            | <span data-ttu-id="8b20e-212">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-212">True</span></span>                            |
| <span data-ttu-id="8b20e-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b20e-213">Is-Single-Valued</span></span>       | <span data-ttu-id="8b20e-214">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-214">True</span></span>                            |
| <span data-ttu-id="8b20e-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b20e-215">Is Indexed</span></span>             | <span data-ttu-id="8b20e-216">False</span><span class="sxs-lookup"><span data-stu-id="8b20e-216">False</span></span>                           |
| <span data-ttu-id="8b20e-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b20e-217">In Global Catalog</span></span>      | <span data-ttu-id="8b20e-218">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-218">True</span></span>                            |
| <span data-ttu-id="8b20e-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b20e-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b20e-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b20e-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b20e-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b20e-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b20e-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b20e-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b20e-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-223">Search-Flags</span></span>           | <span data-ttu-id="8b20e-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b20e-224">0x00000000</span></span>                      |
| <span data-ttu-id="8b20e-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-225">System-Flags</span></span>           | <span data-ttu-id="8b20e-226">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b20e-226">0x00000012</span></span>                      |
| <span data-ttu-id="8b20e-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b20e-227">Classes used in</span></span>        | [<span data-ttu-id="8b20e-228">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8b20e-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8b20e-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b20e-229">Windows Server 2008</span></span>



| <span data-ttu-id="8b20e-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b20e-230">Entry</span></span> | <span data-ttu-id="8b20e-231">Value</span><span class="sxs-lookup"><span data-stu-id="8b20e-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b20e-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b20e-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b20e-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b20e-233">MAPI-Id</span></span>                | <span data-ttu-id="8b20e-234">0x80C0</span><span class="sxs-lookup"><span data-stu-id="8b20e-234">0x80C0</span></span>                          |
| <span data-ttu-id="8b20e-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b20e-235">System-Only</span></span>            | <span data-ttu-id="8b20e-236">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-236">True</span></span>                            |
| <span data-ttu-id="8b20e-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b20e-237">Is-Single-Valued</span></span>       | <span data-ttu-id="8b20e-238">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-238">True</span></span>                            |
| <span data-ttu-id="8b20e-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b20e-239">Is Indexed</span></span>             | <span data-ttu-id="8b20e-240">False</span><span class="sxs-lookup"><span data-stu-id="8b20e-240">False</span></span>                           |
| <span data-ttu-id="8b20e-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b20e-241">In Global Catalog</span></span>      | <span data-ttu-id="8b20e-242">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-242">True</span></span>                            |
| <span data-ttu-id="8b20e-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b20e-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b20e-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b20e-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b20e-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b20e-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b20e-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b20e-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b20e-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-247">Search-Flags</span></span>           | <span data-ttu-id="8b20e-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b20e-248">0x00000000</span></span>                      |
| <span data-ttu-id="8b20e-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-249">System-Flags</span></span>           | <span data-ttu-id="8b20e-250">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b20e-250">0x00000012</span></span>                      |
| <span data-ttu-id="8b20e-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b20e-251">Classes used in</span></span>        | [<span data-ttu-id="8b20e-252">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8b20e-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8b20e-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b20e-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8b20e-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b20e-254">Entry</span></span> | <span data-ttu-id="8b20e-255">Value</span><span class="sxs-lookup"><span data-stu-id="8b20e-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b20e-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b20e-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b20e-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b20e-257">MAPI-Id</span></span>                | <span data-ttu-id="8b20e-258">0x80C0</span><span class="sxs-lookup"><span data-stu-id="8b20e-258">0x80C0</span></span>                          |
| <span data-ttu-id="8b20e-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b20e-259">System-Only</span></span>            | <span data-ttu-id="8b20e-260">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-260">True</span></span>                            |
| <span data-ttu-id="8b20e-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b20e-261">Is-Single-Valued</span></span>       | <span data-ttu-id="8b20e-262">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-262">True</span></span>                            |
| <span data-ttu-id="8b20e-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b20e-263">Is Indexed</span></span>             | <span data-ttu-id="8b20e-264">False</span><span class="sxs-lookup"><span data-stu-id="8b20e-264">False</span></span>                           |
| <span data-ttu-id="8b20e-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b20e-265">In Global Catalog</span></span>      | <span data-ttu-id="8b20e-266">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-266">True</span></span>                            |
| <span data-ttu-id="8b20e-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b20e-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b20e-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b20e-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b20e-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b20e-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b20e-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b20e-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b20e-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-271">Search-Flags</span></span>           | <span data-ttu-id="8b20e-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b20e-272">0x00000000</span></span>                      |
| <span data-ttu-id="8b20e-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-273">System-Flags</span></span>           | <span data-ttu-id="8b20e-274">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b20e-274">0x00000012</span></span>                      |
| <span data-ttu-id="8b20e-275">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b20e-275">Classes used in</span></span>        | [<span data-ttu-id="8b20e-276">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8b20e-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8b20e-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b20e-277">Windows Server 2012</span></span>



| <span data-ttu-id="8b20e-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b20e-278">Entry</span></span> | <span data-ttu-id="8b20e-279">Value</span><span class="sxs-lookup"><span data-stu-id="8b20e-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b20e-280">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b20e-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b20e-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b20e-281">MAPI-Id</span></span>                | <span data-ttu-id="8b20e-282">0x80C0</span><span class="sxs-lookup"><span data-stu-id="8b20e-282">0x80C0</span></span>                          |
| <span data-ttu-id="8b20e-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b20e-283">System-Only</span></span>            | <span data-ttu-id="8b20e-284">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-284">True</span></span>                            |
| <span data-ttu-id="8b20e-285">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b20e-285">Is-Single-Valued</span></span>       | <span data-ttu-id="8b20e-286">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-286">True</span></span>                            |
| <span data-ttu-id="8b20e-287">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b20e-287">Is Indexed</span></span>             | <span data-ttu-id="8b20e-288">False</span><span class="sxs-lookup"><span data-stu-id="8b20e-288">False</span></span>                           |
| <span data-ttu-id="8b20e-289">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b20e-289">In Global Catalog</span></span>      | <span data-ttu-id="8b20e-290">True</span><span class="sxs-lookup"><span data-stu-id="8b20e-290">True</span></span>                            |
| <span data-ttu-id="8b20e-291">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b20e-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b20e-292">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b20e-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b20e-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b20e-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b20e-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b20e-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b20e-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-295">Search-Flags</span></span>           | <span data-ttu-id="8b20e-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b20e-296">0x00000000</span></span>                      |
| <span data-ttu-id="8b20e-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b20e-297">System-Flags</span></span>           | <span data-ttu-id="8b20e-298">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b20e-298">0x00000012</span></span>                      |
| <span data-ttu-id="8b20e-299">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b20e-299">Classes used in</span></span>        | [<span data-ttu-id="8b20e-300">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8b20e-300">**Top**</span></span>](c-top.md)<br/> |



 

 





