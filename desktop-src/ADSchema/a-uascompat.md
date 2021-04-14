---
title: UAS-Compat atributo)
description: Indica si el administrador de cuentas de seguridad aplicará tamaños de datos para que Active Directory compatibles con el sistema de cuentas de usuario LanManager (UAS).
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de UAS-Compat
- uASCompat esquema de AD de atributos
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658965"
---
# <a name="uas-compat-attribute"></a><span data-ttu-id="e6df0-105">UAS-Compat atributo)</span><span class="sxs-lookup"><span data-stu-id="e6df0-105">UAS-Compat attribute</span></span>

<span data-ttu-id="e6df0-106">Indica si el administrador de cuentas de seguridad aplicará tamaños de datos para que Active Directory compatibles con el sistema de cuentas de usuario LanManager (UAS).</span><span class="sxs-lookup"><span data-stu-id="e6df0-106">Indicates if the security account manager will enforce data sizes to make Active Directory compatible with the LanManager User Account System (UAS).</span></span> <span data-ttu-id="e6df0-107">Si este valor es 0, no se aplica ningún límite.</span><span class="sxs-lookup"><span data-stu-id="e6df0-107">If this value is 0, no limits are enforced.</span></span> <span data-ttu-id="e6df0-108">Si este valor es 1, se aplican los límites siguientes.</span><span class="sxs-lookup"><span data-stu-id="e6df0-108">If this value is 1, the following limits are enforced.</span></span>



| <span data-ttu-id="e6df0-109">Value</span><span class="sxs-lookup"><span data-stu-id="e6df0-109">Value</span></span>                          | <span data-ttu-id="e6df0-110">Length</span><span class="sxs-lookup"><span data-stu-id="e6df0-110">Length</span></span>                         |
|--------------------------------|--------------------------------|
| <span data-ttu-id="e6df0-111">Contraseña</span><span class="sxs-lookup"><span data-stu-id="e6df0-111">Password</span></span><br/>            | <span data-ttu-id="e6df0-112">de 0 a 14 caracteres</span><span class="sxs-lookup"><span data-stu-id="e6df0-112">0 to 14 characters</span></span><br/>  |
| <span data-ttu-id="e6df0-113">Nombre de cuenta</span><span class="sxs-lookup"><span data-stu-id="e6df0-113">Account Name</span></span><br/>        | <span data-ttu-id="e6df0-114">de 0 a 20 caracteres</span><span class="sxs-lookup"><span data-stu-id="e6df0-114">0 to 20 characters</span></span><br/>  |
| <span data-ttu-id="e6df0-115">Nombre de dominio</span><span class="sxs-lookup"><span data-stu-id="e6df0-115">Domain Name</span></span><br/>         | <span data-ttu-id="e6df0-116">de 0 a 15 caracteres</span><span class="sxs-lookup"><span data-stu-id="e6df0-116">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="e6df0-117">Nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="e6df0-117">Computer Name</span></span><br/>       | <span data-ttu-id="e6df0-118">de 0 a 15 caracteres</span><span class="sxs-lookup"><span data-stu-id="e6df0-118">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="e6df0-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6df0-119">Comments</span></span><br/>            | <span data-ttu-id="e6df0-120">de 0 a 48 caracteres</span><span class="sxs-lookup"><span data-stu-id="e6df0-120">0 to 48 characters</span></span><br/>  |
| <span data-ttu-id="e6df0-121">Directorio particular</span><span class="sxs-lookup"><span data-stu-id="e6df0-121">Home Directory</span></span><br/>      | <span data-ttu-id="e6df0-122">de 0 a 256 caracteres</span><span class="sxs-lookup"><span data-stu-id="e6df0-122">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="e6df0-123">Ruta de acceso del script</span><span class="sxs-lookup"><span data-stu-id="e6df0-123">Script Path</span></span><br/>         | <span data-ttu-id="e6df0-124">de 0 a 256 caracteres</span><span class="sxs-lookup"><span data-stu-id="e6df0-124">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="e6df0-125">Unidades de tiempo por semana</span><span class="sxs-lookup"><span data-stu-id="e6df0-125">Time Units Per Week</span></span><br/> | <span data-ttu-id="e6df0-126">168 bits (21 bytes)</span><span class="sxs-lookup"><span data-stu-id="e6df0-126">168 bits (21 bytes)</span></span><br/> |



 



| <span data-ttu-id="e6df0-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6df0-127">Entry</span></span> | <span data-ttu-id="e6df0-128">Value</span><span class="sxs-lookup"><span data-stu-id="e6df0-128">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e6df0-129">CN</span><span class="sxs-lookup"><span data-stu-id="e6df0-129">CN</span></span>                | <span data-ttu-id="e6df0-130">UAS-Compat</span><span class="sxs-lookup"><span data-stu-id="e6df0-130">UAS-Compat</span></span>                           |
| <span data-ttu-id="e6df0-131">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e6df0-131">Ldap-Display-Name</span></span> | <span data-ttu-id="e6df0-132">uASCompat</span><span class="sxs-lookup"><span data-stu-id="e6df0-132">uASCompat</span></span>                            |
| <span data-ttu-id="e6df0-133">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e6df0-133">Size</span></span>              | \-                                   |
| <span data-ttu-id="e6df0-134">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e6df0-134">Update Privilege</span></span>  | <span data-ttu-id="e6df0-135">Lo lleva a cabo un administrador.</span><span class="sxs-lookup"><span data-stu-id="e6df0-135">Performed by an administrator.</span></span>       |
| <span data-ttu-id="e6df0-136">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e6df0-136">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e6df0-137">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e6df0-137">Attribute-Id</span></span>      | <span data-ttu-id="e6df0-138">1.2.840.113556.1.4.155</span><span class="sxs-lookup"><span data-stu-id="e6df0-138">1.2.840.113556.1.4.155</span></span>               |
| <span data-ttu-id="e6df0-139">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e6df0-139">System-Id-Guid</span></span>    | <span data-ttu-id="e6df0-140">bf967a61-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e6df0-140">bf967a61-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="e6df0-141">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6df0-141">Syntax</span></span>            | [<span data-ttu-id="e6df0-142">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="e6df0-142">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e6df0-143">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e6df0-143">Implementations</span></span>

-   [<span data-ttu-id="e6df0-144">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e6df0-144">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e6df0-145">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e6df0-145">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e6df0-146">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e6df0-146">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e6df0-147">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e6df0-147">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e6df0-148">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e6df0-148">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e6df0-149">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e6df0-149">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e6df0-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e6df0-150">Windows 2000 Server</span></span>



| <span data-ttu-id="e6df0-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6df0-151">Entry</span></span> | <span data-ttu-id="e6df0-152">Value</span><span class="sxs-lookup"><span data-stu-id="e6df0-152">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e6df0-153">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e6df0-153">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6df0-154">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6df0-155">System-Only</span></span>            | <span data-ttu-id="e6df0-156">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-156">False</span></span>                                                 |
| <span data-ttu-id="e6df0-157">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e6df0-157">Is-Single-Valued</span></span>       | <span data-ttu-id="e6df0-158">True</span><span class="sxs-lookup"><span data-stu-id="e6df0-158">True</span></span>                                                  |
| <span data-ttu-id="e6df0-159">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e6df0-159">Is Indexed</span></span>             | <span data-ttu-id="e6df0-160">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-160">False</span></span>                                                 |
| <span data-ttu-id="e6df0-161">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6df0-161">In Global Catalog</span></span>      | <span data-ttu-id="e6df0-162">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-162">False</span></span>                                                 |
| <span data-ttu-id="e6df0-163">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e6df0-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6df0-164">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6df0-164">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e6df0-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6df0-165">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6df0-166">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-167">Search-Flags</span></span>           | <span data-ttu-id="e6df0-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6df0-168">0x00000000</span></span>                                            |
| <span data-ttu-id="e6df0-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-169">System-Flags</span></span>           | <span data-ttu-id="e6df0-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6df0-170">0x00000010</span></span>                                            |
| <span data-ttu-id="e6df0-171">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e6df0-171">Classes used in</span></span>        | [<span data-ttu-id="e6df0-172">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="e6df0-172">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e6df0-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e6df0-173">Windows Server 2003</span></span>



| <span data-ttu-id="e6df0-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6df0-174">Entry</span></span> | <span data-ttu-id="e6df0-175">Value</span><span class="sxs-lookup"><span data-stu-id="e6df0-175">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e6df0-176">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e6df0-176">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6df0-177">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6df0-178">System-Only</span></span>            | <span data-ttu-id="e6df0-179">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-179">False</span></span>                                                 |
| <span data-ttu-id="e6df0-180">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e6df0-180">Is-Single-Valued</span></span>       | <span data-ttu-id="e6df0-181">True</span><span class="sxs-lookup"><span data-stu-id="e6df0-181">True</span></span>                                                  |
| <span data-ttu-id="e6df0-182">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e6df0-182">Is Indexed</span></span>             | <span data-ttu-id="e6df0-183">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-183">False</span></span>                                                 |
| <span data-ttu-id="e6df0-184">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6df0-184">In Global Catalog</span></span>      | <span data-ttu-id="e6df0-185">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-185">False</span></span>                                                 |
| <span data-ttu-id="e6df0-186">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e6df0-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6df0-187">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6df0-187">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e6df0-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6df0-188">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6df0-189">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-190">Search-Flags</span></span>           | <span data-ttu-id="e6df0-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6df0-191">0x00000000</span></span>                                            |
| <span data-ttu-id="e6df0-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-192">System-Flags</span></span>           | <span data-ttu-id="e6df0-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6df0-193">0x00000010</span></span>                                            |
| <span data-ttu-id="e6df0-194">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e6df0-194">Classes used in</span></span>        | [<span data-ttu-id="e6df0-195">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="e6df0-195">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e6df0-196">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e6df0-196">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e6df0-197">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6df0-197">Entry</span></span> | <span data-ttu-id="e6df0-198">Value</span><span class="sxs-lookup"><span data-stu-id="e6df0-198">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e6df0-199">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e6df0-199">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-200">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6df0-200">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-201">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6df0-201">System-Only</span></span>            | <span data-ttu-id="e6df0-202">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-202">False</span></span>                                                 |
| <span data-ttu-id="e6df0-203">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e6df0-203">Is-Single-Valued</span></span>       | <span data-ttu-id="e6df0-204">True</span><span class="sxs-lookup"><span data-stu-id="e6df0-204">True</span></span>                                                  |
| <span data-ttu-id="e6df0-205">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e6df0-205">Is Indexed</span></span>             | <span data-ttu-id="e6df0-206">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-206">False</span></span>                                                 |
| <span data-ttu-id="e6df0-207">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6df0-207">In Global Catalog</span></span>      | <span data-ttu-id="e6df0-208">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-208">False</span></span>                                                 |
| <span data-ttu-id="e6df0-209">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e6df0-209">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6df0-210">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6df0-210">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e6df0-211">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6df0-211">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6df0-212">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-213">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-213">Search-Flags</span></span>           | <span data-ttu-id="e6df0-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6df0-214">0x00000000</span></span>                                            |
| <span data-ttu-id="e6df0-215">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-215">System-Flags</span></span>           | <span data-ttu-id="e6df0-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6df0-216">0x00000010</span></span>                                            |
| <span data-ttu-id="e6df0-217">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e6df0-217">Classes used in</span></span>        | [<span data-ttu-id="e6df0-218">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="e6df0-218">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e6df0-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6df0-219">Windows Server 2008</span></span>



| <span data-ttu-id="e6df0-220">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6df0-220">Entry</span></span> | <span data-ttu-id="e6df0-221">Value</span><span class="sxs-lookup"><span data-stu-id="e6df0-221">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e6df0-222">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e6df0-222">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-223">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6df0-223">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-224">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6df0-224">System-Only</span></span>            | <span data-ttu-id="e6df0-225">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-225">False</span></span>                                                 |
| <span data-ttu-id="e6df0-226">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e6df0-226">Is-Single-Valued</span></span>       | <span data-ttu-id="e6df0-227">True</span><span class="sxs-lookup"><span data-stu-id="e6df0-227">True</span></span>                                                  |
| <span data-ttu-id="e6df0-228">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e6df0-228">Is Indexed</span></span>             | <span data-ttu-id="e6df0-229">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-229">False</span></span>                                                 |
| <span data-ttu-id="e6df0-230">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6df0-230">In Global Catalog</span></span>      | <span data-ttu-id="e6df0-231">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-231">False</span></span>                                                 |
| <span data-ttu-id="e6df0-232">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e6df0-232">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6df0-233">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6df0-233">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e6df0-234">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6df0-234">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-235">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6df0-235">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-236">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-236">Search-Flags</span></span>           | <span data-ttu-id="e6df0-237">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6df0-237">0x00000000</span></span>                                            |
| <span data-ttu-id="e6df0-238">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-238">System-Flags</span></span>           | <span data-ttu-id="e6df0-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6df0-239">0x00000010</span></span>                                            |
| <span data-ttu-id="e6df0-240">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e6df0-240">Classes used in</span></span>        | [<span data-ttu-id="e6df0-241">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="e6df0-241">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e6df0-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6df0-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e6df0-243">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6df0-243">Entry</span></span> | <span data-ttu-id="e6df0-244">Value</span><span class="sxs-lookup"><span data-stu-id="e6df0-244">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e6df0-245">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e6df0-245">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6df0-246">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6df0-247">System-Only</span></span>            | <span data-ttu-id="e6df0-248">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-248">False</span></span>                                                 |
| <span data-ttu-id="e6df0-249">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e6df0-249">Is-Single-Valued</span></span>       | <span data-ttu-id="e6df0-250">True</span><span class="sxs-lookup"><span data-stu-id="e6df0-250">True</span></span>                                                  |
| <span data-ttu-id="e6df0-251">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e6df0-251">Is Indexed</span></span>             | <span data-ttu-id="e6df0-252">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-252">False</span></span>                                                 |
| <span data-ttu-id="e6df0-253">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6df0-253">In Global Catalog</span></span>      | <span data-ttu-id="e6df0-254">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-254">False</span></span>                                                 |
| <span data-ttu-id="e6df0-255">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e6df0-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6df0-256">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6df0-256">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e6df0-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6df0-257">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6df0-258">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-259">Search-Flags</span></span>           | <span data-ttu-id="e6df0-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6df0-260">0x00000000</span></span>                                            |
| <span data-ttu-id="e6df0-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-261">System-Flags</span></span>           | <span data-ttu-id="e6df0-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6df0-262">0x00000010</span></span>                                            |
| <span data-ttu-id="e6df0-263">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e6df0-263">Classes used in</span></span>        | [<span data-ttu-id="e6df0-264">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="e6df0-264">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e6df0-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6df0-265">Windows Server 2012</span></span>



| <span data-ttu-id="e6df0-266">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6df0-266">Entry</span></span> | <span data-ttu-id="e6df0-267">Value</span><span class="sxs-lookup"><span data-stu-id="e6df0-267">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e6df0-268">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e6df0-268">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6df0-269">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="e6df0-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6df0-270">System-Only</span></span>            | <span data-ttu-id="e6df0-271">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-271">False</span></span>                                                 |
| <span data-ttu-id="e6df0-272">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e6df0-272">Is-Single-Valued</span></span>       | <span data-ttu-id="e6df0-273">True</span><span class="sxs-lookup"><span data-stu-id="e6df0-273">True</span></span>                                                  |
| <span data-ttu-id="e6df0-274">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e6df0-274">Is Indexed</span></span>             | <span data-ttu-id="e6df0-275">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-275">False</span></span>                                                 |
| <span data-ttu-id="e6df0-276">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6df0-276">In Global Catalog</span></span>      | <span data-ttu-id="e6df0-277">False</span><span class="sxs-lookup"><span data-stu-id="e6df0-277">False</span></span>                                                 |
| <span data-ttu-id="e6df0-278">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e6df0-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6df0-279">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6df0-279">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="e6df0-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6df0-280">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6df0-281">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="e6df0-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-282">Search-Flags</span></span>           | <span data-ttu-id="e6df0-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6df0-283">0x00000000</span></span>                                            |
| <span data-ttu-id="e6df0-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6df0-284">System-Flags</span></span>           | <span data-ttu-id="e6df0-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6df0-285">0x00000010</span></span>                                            |
| <span data-ttu-id="e6df0-286">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e6df0-286">Classes used in</span></span>        | [<span data-ttu-id="e6df0-287">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="e6df0-287">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





