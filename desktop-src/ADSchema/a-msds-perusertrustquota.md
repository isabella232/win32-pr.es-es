---
title: Atributo MS-DS-per-user-Trust-quota
description: Se utiliza para exigir una cuota por usuario para crear Trusted-Domain objetos autorizados por el permiso de acceso de control nuevo, crear-entrada-bosque-confianza.
ms.assetid: 3b198b24-5282-4d13-8d35-88f34c11ce94
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DS-per-user-Trust-quota
- Esquema de AD de atributo msDS-PerUserTrustQuota
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3bd6ffcac01de8997f806e6aa8a8e3bd6afbb66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659121"
---
# <a name="ms-ds-per-user-trust-quota-attribute"></a><span data-ttu-id="7002b-105">Atributo MS-DS-per-user-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="7002b-105">MS-DS-Per-User-Trust-Quota attribute</span></span>

<span data-ttu-id="7002b-106">Se utiliza para exigir una cuota por usuario para crear Trusted-Domain objetos autorizados por el permiso de acceso de control nuevo, crear-entrada-bosque-confianza.</span><span class="sxs-lookup"><span data-stu-id="7002b-106">Used to enforce a per-user quota for creating Trusted-Domain objects that are authorized by the new control access right, Create-Inbound-Forest-Trust.</span></span> <span data-ttu-id="7002b-107">Este atributo limita el número de objetos de Trusted-Domain que un solo usuario no administrador puede crear.</span><span class="sxs-lookup"><span data-stu-id="7002b-107">This attribute limits the number of Trusted-Domain objects that can be created by a single non-admin user.</span></span>



| <span data-ttu-id="7002b-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="7002b-108">Entry</span></span> | <span data-ttu-id="7002b-109">Value</span><span class="sxs-lookup"><span data-stu-id="7002b-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="7002b-110">CN</span><span class="sxs-lookup"><span data-stu-id="7002b-110">CN</span></span>                | <span data-ttu-id="7002b-111">MS-DS-per-user-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="7002b-111">MS-DS-Per-User-Trust-Quota</span></span>                |
| <span data-ttu-id="7002b-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="7002b-112">Ldap-Display-Name</span></span> | <span data-ttu-id="7002b-113">msDS-PerUserTrustQuota</span><span class="sxs-lookup"><span data-stu-id="7002b-113">msDS-PerUserTrustQuota</span></span>                    |
| <span data-ttu-id="7002b-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="7002b-114">Size</span></span>              | \-                                        |
| <span data-ttu-id="7002b-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="7002b-115">Update Privilege</span></span>  | <span data-ttu-id="7002b-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="7002b-116">Domain administrator</span></span>                      |
| <span data-ttu-id="7002b-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="7002b-117">Update Frequency</span></span>  | <span data-ttu-id="7002b-118">Al crear el bosque y raramente después.</span><span class="sxs-lookup"><span data-stu-id="7002b-118">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="7002b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7002b-119">Attribute-Id</span></span>      | <span data-ttu-id="7002b-120">1.2.840.113556.1.4.1788</span><span class="sxs-lookup"><span data-stu-id="7002b-120">1.2.840.113556.1.4.1788</span></span>                   |
| <span data-ttu-id="7002b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7002b-121">System-Id-Guid</span></span>    | <span data-ttu-id="7002b-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span><span class="sxs-lookup"><span data-stu-id="7002b-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span></span>      |
| <span data-ttu-id="7002b-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7002b-123">Syntax</span></span>            | [<span data-ttu-id="7002b-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="7002b-124">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="7002b-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="7002b-125">Implementations</span></span>

-   [<span data-ttu-id="7002b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7002b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7002b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7002b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7002b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7002b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7002b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7002b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7002b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7002b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7002b-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7002b-131">Windows Server 2003</span></span>



| <span data-ttu-id="7002b-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="7002b-132">Entry</span></span> | <span data-ttu-id="7002b-133">Value</span><span class="sxs-lookup"><span data-stu-id="7002b-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7002b-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7002b-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7002b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7002b-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7002b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7002b-136">System-Only</span></span>            | <span data-ttu-id="7002b-137">False</span><span class="sxs-lookup"><span data-stu-id="7002b-137">False</span></span>                                        |
| <span data-ttu-id="7002b-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7002b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7002b-139">True</span><span class="sxs-lookup"><span data-stu-id="7002b-139">True</span></span>                                         |
| <span data-ttu-id="7002b-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7002b-140">Is Indexed</span></span>             | <span data-ttu-id="7002b-141">False</span><span class="sxs-lookup"><span data-stu-id="7002b-141">False</span></span>                                        |
| <span data-ttu-id="7002b-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7002b-142">In Global Catalog</span></span>      | <span data-ttu-id="7002b-143">False</span><span class="sxs-lookup"><span data-stu-id="7002b-143">False</span></span>                                        |
| <span data-ttu-id="7002b-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7002b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7002b-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7002b-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7002b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7002b-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7002b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7002b-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7002b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7002b-148">Search-Flags</span></span>           | <span data-ttu-id="7002b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7002b-149">0x00000000</span></span>                                   |
| <span data-ttu-id="7002b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7002b-150">System-Flags</span></span>           | <span data-ttu-id="7002b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7002b-151">0x00000010</span></span>                                   |
| <span data-ttu-id="7002b-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7002b-152">Classes used in</span></span>        | [<span data-ttu-id="7002b-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7002b-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7002b-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7002b-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7002b-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="7002b-155">Entry</span></span> | <span data-ttu-id="7002b-156">Value</span><span class="sxs-lookup"><span data-stu-id="7002b-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7002b-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7002b-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7002b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7002b-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7002b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7002b-159">System-Only</span></span>            | <span data-ttu-id="7002b-160">False</span><span class="sxs-lookup"><span data-stu-id="7002b-160">False</span></span>                                        |
| <span data-ttu-id="7002b-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7002b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7002b-162">True</span><span class="sxs-lookup"><span data-stu-id="7002b-162">True</span></span>                                         |
| <span data-ttu-id="7002b-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7002b-163">Is Indexed</span></span>             | <span data-ttu-id="7002b-164">False</span><span class="sxs-lookup"><span data-stu-id="7002b-164">False</span></span>                                        |
| <span data-ttu-id="7002b-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7002b-165">In Global Catalog</span></span>      | <span data-ttu-id="7002b-166">False</span><span class="sxs-lookup"><span data-stu-id="7002b-166">False</span></span>                                        |
| <span data-ttu-id="7002b-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7002b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7002b-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7002b-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7002b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7002b-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7002b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7002b-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7002b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7002b-171">Search-Flags</span></span>           | <span data-ttu-id="7002b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7002b-172">0x00000000</span></span>                                   |
| <span data-ttu-id="7002b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7002b-173">System-Flags</span></span>           | <span data-ttu-id="7002b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7002b-174">0x00000010</span></span>                                   |
| <span data-ttu-id="7002b-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7002b-175">Classes used in</span></span>        | [<span data-ttu-id="7002b-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7002b-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7002b-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7002b-177">Windows Server 2008</span></span>



| <span data-ttu-id="7002b-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="7002b-178">Entry</span></span> | <span data-ttu-id="7002b-179">Value</span><span class="sxs-lookup"><span data-stu-id="7002b-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7002b-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7002b-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7002b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7002b-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7002b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7002b-182">System-Only</span></span>            | <span data-ttu-id="7002b-183">False</span><span class="sxs-lookup"><span data-stu-id="7002b-183">False</span></span>                                        |
| <span data-ttu-id="7002b-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7002b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7002b-185">True</span><span class="sxs-lookup"><span data-stu-id="7002b-185">True</span></span>                                         |
| <span data-ttu-id="7002b-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7002b-186">Is Indexed</span></span>             | <span data-ttu-id="7002b-187">False</span><span class="sxs-lookup"><span data-stu-id="7002b-187">False</span></span>                                        |
| <span data-ttu-id="7002b-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7002b-188">In Global Catalog</span></span>      | <span data-ttu-id="7002b-189">False</span><span class="sxs-lookup"><span data-stu-id="7002b-189">False</span></span>                                        |
| <span data-ttu-id="7002b-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7002b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7002b-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7002b-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7002b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7002b-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7002b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7002b-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7002b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7002b-194">Search-Flags</span></span>           | <span data-ttu-id="7002b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7002b-195">0x00000000</span></span>                                   |
| <span data-ttu-id="7002b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7002b-196">System-Flags</span></span>           | <span data-ttu-id="7002b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7002b-197">0x00000010</span></span>                                   |
| <span data-ttu-id="7002b-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7002b-198">Classes used in</span></span>        | [<span data-ttu-id="7002b-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7002b-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7002b-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7002b-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7002b-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="7002b-201">Entry</span></span> | <span data-ttu-id="7002b-202">Value</span><span class="sxs-lookup"><span data-stu-id="7002b-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7002b-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7002b-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7002b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7002b-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7002b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7002b-205">System-Only</span></span>            | <span data-ttu-id="7002b-206">False</span><span class="sxs-lookup"><span data-stu-id="7002b-206">False</span></span>                                        |
| <span data-ttu-id="7002b-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7002b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7002b-208">True</span><span class="sxs-lookup"><span data-stu-id="7002b-208">True</span></span>                                         |
| <span data-ttu-id="7002b-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7002b-209">Is Indexed</span></span>             | <span data-ttu-id="7002b-210">False</span><span class="sxs-lookup"><span data-stu-id="7002b-210">False</span></span>                                        |
| <span data-ttu-id="7002b-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7002b-211">In Global Catalog</span></span>      | <span data-ttu-id="7002b-212">False</span><span class="sxs-lookup"><span data-stu-id="7002b-212">False</span></span>                                        |
| <span data-ttu-id="7002b-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7002b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7002b-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7002b-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7002b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7002b-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7002b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7002b-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7002b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7002b-217">Search-Flags</span></span>           | <span data-ttu-id="7002b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7002b-218">0x00000000</span></span>                                   |
| <span data-ttu-id="7002b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7002b-219">System-Flags</span></span>           | <span data-ttu-id="7002b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7002b-220">0x00000010</span></span>                                   |
| <span data-ttu-id="7002b-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7002b-221">Classes used in</span></span>        | [<span data-ttu-id="7002b-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7002b-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7002b-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7002b-223">Windows Server 2012</span></span>



| <span data-ttu-id="7002b-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="7002b-224">Entry</span></span> | <span data-ttu-id="7002b-225">Value</span><span class="sxs-lookup"><span data-stu-id="7002b-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7002b-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7002b-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7002b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7002b-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7002b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7002b-228">System-Only</span></span>            | <span data-ttu-id="7002b-229">False</span><span class="sxs-lookup"><span data-stu-id="7002b-229">False</span></span>                                        |
| <span data-ttu-id="7002b-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7002b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7002b-231">True</span><span class="sxs-lookup"><span data-stu-id="7002b-231">True</span></span>                                         |
| <span data-ttu-id="7002b-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7002b-232">Is Indexed</span></span>             | <span data-ttu-id="7002b-233">False</span><span class="sxs-lookup"><span data-stu-id="7002b-233">False</span></span>                                        |
| <span data-ttu-id="7002b-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7002b-234">In Global Catalog</span></span>      | <span data-ttu-id="7002b-235">False</span><span class="sxs-lookup"><span data-stu-id="7002b-235">False</span></span>                                        |
| <span data-ttu-id="7002b-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7002b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7002b-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7002b-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7002b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7002b-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7002b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7002b-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7002b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7002b-240">Search-Flags</span></span>           | <span data-ttu-id="7002b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7002b-241">0x00000000</span></span>                                   |
| <span data-ttu-id="7002b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7002b-242">System-Flags</span></span>           | <span data-ttu-id="7002b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7002b-243">0x00000010</span></span>                                   |
| <span data-ttu-id="7002b-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7002b-244">Classes used in</span></span>        | [<span data-ttu-id="7002b-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7002b-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





