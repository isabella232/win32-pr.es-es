---
title: Atributo apellido
description: Este atributo contiene la familia o el apellido de un usuario.
ms.assetid: d9d53c9f-4efa-47c4-aec4-518fb8a868b3
ms.tgt_platform: multiple
keywords:
- Atributo de apellidos esquema de AD
- atributo SN del esquema de AD
topic_type:
- apiref
api_name:
- Surname
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453352574a7aec10c56492060ac2de6ceeca030f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997364"
---
# <a name="surname-attribute"></a><span data-ttu-id="6d12d-105">Atributo apellido</span><span class="sxs-lookup"><span data-stu-id="6d12d-105">Surname attribute</span></span>

<span data-ttu-id="6d12d-106">Este atributo contiene la familia o el apellido de un usuario.</span><span class="sxs-lookup"><span data-stu-id="6d12d-106">This attribute contains the family or last name for a user.</span></span>



| <span data-ttu-id="6d12d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d12d-107">Entry</span></span> | <span data-ttu-id="6d12d-108">Value</span><span class="sxs-lookup"><span data-stu-id="6d12d-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6d12d-109">CN</span><span class="sxs-lookup"><span data-stu-id="6d12d-109">CN</span></span>                | <span data-ttu-id="6d12d-110">Surname</span><span class="sxs-lookup"><span data-stu-id="6d12d-110">Surname</span></span>                                                                          |
| <span data-ttu-id="6d12d-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6d12d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6d12d-112">sn</span><span class="sxs-lookup"><span data-stu-id="6d12d-112">sn</span></span>                                                                               |
| <span data-ttu-id="6d12d-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6d12d-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="6d12d-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6d12d-114">Update Privilege</span></span>  | <span data-ttu-id="6d12d-115">Cualquier usuario puede actualizar este objeto en función de la seguridad del objeto que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="6d12d-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="6d12d-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6d12d-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="6d12d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6d12d-117">Attribute-Id</span></span>      | <span data-ttu-id="6d12d-118">2.5.4.4</span><span class="sxs-lookup"><span data-stu-id="6d12d-118">2.5.4.4</span></span>                                                                          |
| <span data-ttu-id="6d12d-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6d12d-119">System-Id-Guid</span></span>    | <span data-ttu-id="6d12d-120">bf967a41-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6d12d-120">bf967a41-0de6-11d0-a285-00aa003049e2</span></span>                                             |
| <span data-ttu-id="6d12d-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d12d-121">Syntax</span></span>            | [<span data-ttu-id="6d12d-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6d12d-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="6d12d-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6d12d-123">Implementations</span></span>

-   [<span data-ttu-id="6d12d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6d12d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6d12d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6d12d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6d12d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6d12d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6d12d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6d12d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6d12d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6d12d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6d12d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6d12d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6d12d-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d12d-130">Windows 2000 Server</span></span>



| <span data-ttu-id="6d12d-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d12d-131">Entry</span></span> | <span data-ttu-id="6d12d-132">Value</span><span class="sxs-lookup"><span data-stu-id="6d12d-132">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="6d12d-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d12d-133">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="6d12d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d12d-134">MAPI-Id</span></span>                | <span data-ttu-id="6d12d-135">0x3A11</span><span class="sxs-lookup"><span data-stu-id="6d12d-135">0x3A11</span></span>                                |
| <span data-ttu-id="6d12d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d12d-136">System-Only</span></span>            | <span data-ttu-id="6d12d-137">False</span><span class="sxs-lookup"><span data-stu-id="6d12d-137">False</span></span>                                 |
| <span data-ttu-id="6d12d-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d12d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6d12d-139">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-139">True</span></span>                                  |
| <span data-ttu-id="6d12d-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d12d-140">Is Indexed</span></span>             | <span data-ttu-id="6d12d-141">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-141">True</span></span>                                  |
| <span data-ttu-id="6d12d-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d12d-142">In Global Catalog</span></span>      | <span data-ttu-id="6d12d-143">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-143">True</span></span>                                  |
| <span data-ttu-id="6d12d-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d12d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d12d-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d12d-145">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="6d12d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d12d-146">Range-Lower</span></span>            | <span data-ttu-id="6d12d-147">1</span><span class="sxs-lookup"><span data-stu-id="6d12d-147">1</span></span>                                     |
| <span data-ttu-id="6d12d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d12d-148">Range-Upper</span></span>            | <span data-ttu-id="6d12d-149">64</span><span class="sxs-lookup"><span data-stu-id="6d12d-149">64</span></span>                                    |
| <span data-ttu-id="6d12d-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-150">Search-Flags</span></span>           | <span data-ttu-id="6d12d-151">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6d12d-151">0x00000005</span></span>                            |
| <span data-ttu-id="6d12d-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-152">System-Flags</span></span>           | <span data-ttu-id="6d12d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d12d-153">0x00000010</span></span>                            |
| <span data-ttu-id="6d12d-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d12d-154">Classes used in</span></span>        | [<span data-ttu-id="6d12d-155">**Person**</span><span class="sxs-lookup"><span data-stu-id="6d12d-155">**Person**</span></span>](c-person.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6d12d-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d12d-156">Windows Server 2003</span></span>



| <span data-ttu-id="6d12d-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d12d-157">Entry</span></span> | <span data-ttu-id="6d12d-158">Value</span><span class="sxs-lookup"><span data-stu-id="6d12d-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d12d-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d12d-159">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="6d12d-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d12d-160">MAPI-Id</span></span>                | <span data-ttu-id="6d12d-161">0x3A11</span><span class="sxs-lookup"><span data-stu-id="6d12d-161">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="6d12d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d12d-162">System-Only</span></span>            | <span data-ttu-id="6d12d-163">False</span><span class="sxs-lookup"><span data-stu-id="6d12d-163">False</span></span>                                                                                         |
| <span data-ttu-id="6d12d-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d12d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="6d12d-165">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-165">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d12d-166">Is Indexed</span></span>             | <span data-ttu-id="6d12d-167">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-167">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d12d-168">In Global Catalog</span></span>      | <span data-ttu-id="6d12d-169">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-169">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d12d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d12d-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d12d-171">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="6d12d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d12d-172">Range-Lower</span></span>            | <span data-ttu-id="6d12d-173">1</span><span class="sxs-lookup"><span data-stu-id="6d12d-173">1</span></span>                                                                                             |
| <span data-ttu-id="6d12d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d12d-174">Range-Upper</span></span>            | <span data-ttu-id="6d12d-175">64</span><span class="sxs-lookup"><span data-stu-id="6d12d-175">64</span></span>                                                                                            |
| <span data-ttu-id="6d12d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-176">Search-Flags</span></span>           | <span data-ttu-id="6d12d-177">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6d12d-177">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="6d12d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-178">System-Flags</span></span>           | <span data-ttu-id="6d12d-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d12d-179">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="6d12d-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d12d-180">Classes used in</span></span>        | [<span data-ttu-id="6d12d-181">**Person**</span><span class="sxs-lookup"><span data-stu-id="6d12d-181">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="6d12d-182">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="6d12d-182">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6d12d-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6d12d-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6d12d-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d12d-184">Entry</span></span> | <span data-ttu-id="6d12d-185">Value</span><span class="sxs-lookup"><span data-stu-id="6d12d-185">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d12d-186">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d12d-186">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="6d12d-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d12d-187">MAPI-Id</span></span>                | <span data-ttu-id="6d12d-188">0x3A11</span><span class="sxs-lookup"><span data-stu-id="6d12d-188">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="6d12d-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d12d-189">System-Only</span></span>            | <span data-ttu-id="6d12d-190">False</span><span class="sxs-lookup"><span data-stu-id="6d12d-190">False</span></span>                                                                                         |
| <span data-ttu-id="6d12d-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d12d-191">Is-Single-Valued</span></span>       | <span data-ttu-id="6d12d-192">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-192">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d12d-193">Is Indexed</span></span>             | <span data-ttu-id="6d12d-194">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-194">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d12d-195">In Global Catalog</span></span>      | <span data-ttu-id="6d12d-196">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-196">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d12d-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d12d-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d12d-198">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="6d12d-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d12d-199">Range-Lower</span></span>            | <span data-ttu-id="6d12d-200">1</span><span class="sxs-lookup"><span data-stu-id="6d12d-200">1</span></span>                                                                                             |
| <span data-ttu-id="6d12d-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d12d-201">Range-Upper</span></span>            | <span data-ttu-id="6d12d-202">64</span><span class="sxs-lookup"><span data-stu-id="6d12d-202">64</span></span>                                                                                            |
| <span data-ttu-id="6d12d-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-203">Search-Flags</span></span>           | <span data-ttu-id="6d12d-204">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6d12d-204">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="6d12d-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-205">System-Flags</span></span>           | <span data-ttu-id="6d12d-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d12d-206">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="6d12d-207">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d12d-207">Classes used in</span></span>        | [<span data-ttu-id="6d12d-208">**Person**</span><span class="sxs-lookup"><span data-stu-id="6d12d-208">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="6d12d-209">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="6d12d-209">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6d12d-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d12d-210">Windows Server 2008</span></span>



| <span data-ttu-id="6d12d-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d12d-211">Entry</span></span> | <span data-ttu-id="6d12d-212">Value</span><span class="sxs-lookup"><span data-stu-id="6d12d-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d12d-213">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d12d-213">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="6d12d-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d12d-214">MAPI-Id</span></span>                | <span data-ttu-id="6d12d-215">0x3A11</span><span class="sxs-lookup"><span data-stu-id="6d12d-215">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="6d12d-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d12d-216">System-Only</span></span>            | <span data-ttu-id="6d12d-217">False</span><span class="sxs-lookup"><span data-stu-id="6d12d-217">False</span></span>                                                                                         |
| <span data-ttu-id="6d12d-218">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d12d-218">Is-Single-Valued</span></span>       | <span data-ttu-id="6d12d-219">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-219">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-220">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d12d-220">Is Indexed</span></span>             | <span data-ttu-id="6d12d-221">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-221">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-222">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d12d-222">In Global Catalog</span></span>      | <span data-ttu-id="6d12d-223">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-223">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-224">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d12d-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d12d-225">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d12d-225">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="6d12d-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d12d-226">Range-Lower</span></span>            | <span data-ttu-id="6d12d-227">1</span><span class="sxs-lookup"><span data-stu-id="6d12d-227">1</span></span>                                                                                             |
| <span data-ttu-id="6d12d-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d12d-228">Range-Upper</span></span>            | <span data-ttu-id="6d12d-229">64</span><span class="sxs-lookup"><span data-stu-id="6d12d-229">64</span></span>                                                                                            |
| <span data-ttu-id="6d12d-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-230">Search-Flags</span></span>           | <span data-ttu-id="6d12d-231">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6d12d-231">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="6d12d-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-232">System-Flags</span></span>           | <span data-ttu-id="6d12d-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d12d-233">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="6d12d-234">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d12d-234">Classes used in</span></span>        | [<span data-ttu-id="6d12d-235">**Person**</span><span class="sxs-lookup"><span data-stu-id="6d12d-235">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="6d12d-236">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="6d12d-236">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6d12d-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d12d-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6d12d-238">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d12d-238">Entry</span></span> | <span data-ttu-id="6d12d-239">Value</span><span class="sxs-lookup"><span data-stu-id="6d12d-239">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d12d-240">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d12d-240">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="6d12d-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d12d-241">MAPI-Id</span></span>                | <span data-ttu-id="6d12d-242">0x3A11</span><span class="sxs-lookup"><span data-stu-id="6d12d-242">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="6d12d-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d12d-243">System-Only</span></span>            | <span data-ttu-id="6d12d-244">False</span><span class="sxs-lookup"><span data-stu-id="6d12d-244">False</span></span>                                                                                         |
| <span data-ttu-id="6d12d-245">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d12d-245">Is-Single-Valued</span></span>       | <span data-ttu-id="6d12d-246">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-246">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-247">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d12d-247">Is Indexed</span></span>             | <span data-ttu-id="6d12d-248">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-248">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-249">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d12d-249">In Global Catalog</span></span>      | <span data-ttu-id="6d12d-250">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-250">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-251">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d12d-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d12d-252">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d12d-252">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="6d12d-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d12d-253">Range-Lower</span></span>            | <span data-ttu-id="6d12d-254">1</span><span class="sxs-lookup"><span data-stu-id="6d12d-254">1</span></span>                                                                                             |
| <span data-ttu-id="6d12d-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d12d-255">Range-Upper</span></span>            | <span data-ttu-id="6d12d-256">64</span><span class="sxs-lookup"><span data-stu-id="6d12d-256">64</span></span>                                                                                            |
| <span data-ttu-id="6d12d-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-257">Search-Flags</span></span>           | <span data-ttu-id="6d12d-258">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6d12d-258">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="6d12d-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-259">System-Flags</span></span>           | <span data-ttu-id="6d12d-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d12d-260">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="6d12d-261">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d12d-261">Classes used in</span></span>        | [<span data-ttu-id="6d12d-262">**Person**</span><span class="sxs-lookup"><span data-stu-id="6d12d-262">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="6d12d-263">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="6d12d-263">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6d12d-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d12d-264">Windows Server 2012</span></span>



| <span data-ttu-id="6d12d-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="6d12d-265">Entry</span></span> | <span data-ttu-id="6d12d-266">Value</span><span class="sxs-lookup"><span data-stu-id="6d12d-266">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d12d-267">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6d12d-267">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="6d12d-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d12d-268">MAPI-Id</span></span>                | <span data-ttu-id="6d12d-269">0x3A11</span><span class="sxs-lookup"><span data-stu-id="6d12d-269">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="6d12d-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d12d-270">System-Only</span></span>            | <span data-ttu-id="6d12d-271">False</span><span class="sxs-lookup"><span data-stu-id="6d12d-271">False</span></span>                                                                                         |
| <span data-ttu-id="6d12d-272">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6d12d-272">Is-Single-Valued</span></span>       | <span data-ttu-id="6d12d-273">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-273">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-274">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6d12d-274">Is Indexed</span></span>             | <span data-ttu-id="6d12d-275">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-275">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-276">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6d12d-276">In Global Catalog</span></span>      | <span data-ttu-id="6d12d-277">True</span><span class="sxs-lookup"><span data-stu-id="6d12d-277">True</span></span>                                                                                          |
| <span data-ttu-id="6d12d-278">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6d12d-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d12d-279">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6d12d-279">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="6d12d-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d12d-280">Range-Lower</span></span>            | <span data-ttu-id="6d12d-281">1</span><span class="sxs-lookup"><span data-stu-id="6d12d-281">1</span></span>                                                                                             |
| <span data-ttu-id="6d12d-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d12d-282">Range-Upper</span></span>            | <span data-ttu-id="6d12d-283">64</span><span class="sxs-lookup"><span data-stu-id="6d12d-283">64</span></span>                                                                                            |
| <span data-ttu-id="6d12d-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-284">Search-Flags</span></span>           | <span data-ttu-id="6d12d-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6d12d-285">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="6d12d-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d12d-286">System-Flags</span></span>           | <span data-ttu-id="6d12d-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d12d-287">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="6d12d-288">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6d12d-288">Classes used in</span></span>        | [<span data-ttu-id="6d12d-289">**Person**</span><span class="sxs-lookup"><span data-stu-id="6d12d-289">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="6d12d-290">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="6d12d-290">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



 

 





