---
title: atributo de calculado de la cuenta de usuario de MS-DS-control
description: msDS-User-Account-Control-Compute es muy similar a userAccountControl, pero el valor del atributo puede contener bits adicionales que no se conservan.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos calculados de Microsoft-DS-User-Account-control
- msDS-User-Account-Control-esquema de AD de atributos calculados
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b5e9b047dd44d637b56cae8ded9e0991c46025
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658848"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a><span data-ttu-id="38bf6-105">atributo de calculado de la cuenta de usuario de MS-DS-control</span><span class="sxs-lookup"><span data-stu-id="38bf6-105">ms-DS-User-Account-Control-Computed attribute</span></span>

<span data-ttu-id="38bf6-106">**MSDS-User-Account-Control-Compute** es muy similar a [**UserAccountControl**](a-useraccountcontrol.md), pero el valor del atributo puede contener bits adicionales que no se conservan.</span><span class="sxs-lookup"><span data-stu-id="38bf6-106">**msDS-User-Account-Control-Computed** is much like [**userAccountControl**](a-useraccountcontrol.md), but the attribute's value can contain additional bits that are not persisted.</span></span> <span data-ttu-id="38bf6-107">Entre los bits calculados se incluyen los siguientes.</span><span class="sxs-lookup"><span data-stu-id="38bf6-107">The computed bits include the following.</span></span>



| <span data-ttu-id="38bf6-108">Value</span><span class="sxs-lookup"><span data-stu-id="38bf6-108">Value</span></span>                | <span data-ttu-id="38bf6-109">Nombre (definido en iAds. h)</span><span class="sxs-lookup"><span data-stu-id="38bf6-109">Name (defined in Iads.h)</span></span>                     |
|----------------------|----------------------------------------------|
| <span data-ttu-id="38bf6-110">0x0010</span><span class="sxs-lookup"><span data-stu-id="38bf6-110">0x0010</span></span><br/>    | <span data-ttu-id="38bf6-111">**bloqueo de fi \_**</span><span class="sxs-lookup"><span data-stu-id="38bf6-111">**UF\_LOCKOUT**</span></span><br/>                   |
| <span data-ttu-id="38bf6-112">0x800000</span><span class="sxs-lookup"><span data-stu-id="38bf6-112">0x800000</span></span><br/>  | <span data-ttu-id="38bf6-113">**la contraseña de la up ha \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="38bf6-113">**UF\_PASSWORD\_EXPIRED**</span></span><br/>         |
| <span data-ttu-id="38bf6-114">0x4000000</span><span class="sxs-lookup"><span data-stu-id="38bf6-114">0x4000000</span></span><br/> | <span data-ttu-id="38bf6-115">**\_cuenta de \_ secretos \_ parciales de la up**</span><span class="sxs-lookup"><span data-stu-id="38bf6-115">**UF\_PARTIAL\_SECRETS\_ACCOUNT**</span></span><br/> |
| <span data-ttu-id="38bf6-116">0x8000000</span><span class="sxs-lookup"><span data-stu-id="38bf6-116">0x8000000</span></span><br/> | <span data-ttu-id="38bf6-117">**FI \_ usar \_ \_ claves AES**</span><span class="sxs-lookup"><span data-stu-id="38bf6-117">**UF\_USE\_AES\_KEYS**</span></span><br/>            |



 

<span data-ttu-id="38bf6-118">La lista completa de bits que [**User-Account-Control**](a-useraccountcontrol.md) y, por lo tanto, **MSDS-User-Account-Control-Compute** también puede contener en la página de referencia de **User-Account-Control** (asignada a través de [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) flagset) o en las páginas de referencia de administración de redes de la estructura [**User \_ info \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) .</span><span class="sxs-lookup"><span data-stu-id="38bf6-118">The full list of bits that [**User-Account-Control**](a-useraccountcontrol.md) and therefore **msDS-User-Account-Control-Computed** can also contain can be found in the **User-Account-Control** reference page (mapped through the [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) flagset) or on the network management reference pages for the [**user\_info\_1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) structure.</span></span>



| <span data-ttu-id="38bf6-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="38bf6-119">Entry</span></span> | <span data-ttu-id="38bf6-120">Value</span><span class="sxs-lookup"><span data-stu-id="38bf6-120">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="38bf6-121">CN</span><span class="sxs-lookup"><span data-stu-id="38bf6-121">CN</span></span>                | <span data-ttu-id="38bf6-122">MS-DS-User-Account-control-calculado</span><span class="sxs-lookup"><span data-stu-id="38bf6-122">ms-DS-User-Account-Control-Computed</span></span>  |
| <span data-ttu-id="38bf6-123">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="38bf6-123">Ldap-Display-Name</span></span> | <span data-ttu-id="38bf6-124">msDS-User-Account-control-calculado</span><span class="sxs-lookup"><span data-stu-id="38bf6-124">msDS-User-Account-Control-Computed</span></span>   |
| <span data-ttu-id="38bf6-125">Tamaño</span><span class="sxs-lookup"><span data-stu-id="38bf6-125">Size</span></span>              | \-                                   |
| <span data-ttu-id="38bf6-126">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="38bf6-126">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="38bf6-127">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="38bf6-127">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="38bf6-128">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38bf6-128">Attribute-Id</span></span>      | <span data-ttu-id="38bf6-129">1.2.840.113556.1.4.1460</span><span class="sxs-lookup"><span data-stu-id="38bf6-129">1.2.840.113556.1.4.1460</span></span>              |
| <span data-ttu-id="38bf6-130">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="38bf6-130">System-Id-Guid</span></span>    | <span data-ttu-id="38bf6-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span><span class="sxs-lookup"><span data-stu-id="38bf6-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span></span> |
| <span data-ttu-id="38bf6-132">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38bf6-132">Syntax</span></span>            | [<span data-ttu-id="38bf6-133">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="38bf6-133">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="38bf6-134">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="38bf6-134">Implementations</span></span>

-   [<span data-ttu-id="38bf6-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="38bf6-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="38bf6-136">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="38bf6-136">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="38bf6-137">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="38bf6-137">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="38bf6-138">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38bf6-138">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38bf6-139">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38bf6-139">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38bf6-140">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38bf6-140">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="38bf6-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38bf6-141">Windows Server 2003</span></span>



| <span data-ttu-id="38bf6-142">Entrada</span><span class="sxs-lookup"><span data-stu-id="38bf6-142">Entry</span></span> | <span data-ttu-id="38bf6-143">Value</span><span class="sxs-lookup"><span data-stu-id="38bf6-143">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38bf6-144">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38bf6-144">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38bf6-145">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38bf6-145">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38bf6-146">System-Only</span><span class="sxs-lookup"><span data-stu-id="38bf6-146">System-Only</span></span>            | <span data-ttu-id="38bf6-147">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-147">False</span></span>                             |
| <span data-ttu-id="38bf6-148">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38bf6-148">Is-Single-Valued</span></span>       | <span data-ttu-id="38bf6-149">True</span><span class="sxs-lookup"><span data-stu-id="38bf6-149">True</span></span>                              |
| <span data-ttu-id="38bf6-150">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38bf6-150">Is Indexed</span></span>             | <span data-ttu-id="38bf6-151">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-151">False</span></span>                             |
| <span data-ttu-id="38bf6-152">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38bf6-152">In Global Catalog</span></span>      | <span data-ttu-id="38bf6-153">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-153">False</span></span>                             |
| <span data-ttu-id="38bf6-154">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38bf6-154">NT-Security-Descriptor</span></span> | <span data-ttu-id="38bf6-155">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38bf6-155">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38bf6-156">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38bf6-156">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38bf6-157">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38bf6-157">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38bf6-158">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-158">Search-Flags</span></span>           | <span data-ttu-id="38bf6-159">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38bf6-159">0x00000000</span></span>                        |
| <span data-ttu-id="38bf6-160">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-160">System-Flags</span></span>           | <span data-ttu-id="38bf6-161">0x00000014</span><span class="sxs-lookup"><span data-stu-id="38bf6-161">0x00000014</span></span>                        |
| <span data-ttu-id="38bf6-162">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38bf6-162">Classes used in</span></span>        | [<span data-ttu-id="38bf6-163">**User**</span><span class="sxs-lookup"><span data-stu-id="38bf6-163">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="38bf6-164">ADAM</span><span class="sxs-lookup"><span data-stu-id="38bf6-164">ADAM</span></span>



| <span data-ttu-id="38bf6-165">Entrada</span><span class="sxs-lookup"><span data-stu-id="38bf6-165">Entry</span></span> | <span data-ttu-id="38bf6-166">Value</span><span class="sxs-lookup"><span data-stu-id="38bf6-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="38bf6-167">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38bf6-167">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="38bf6-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38bf6-168">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="38bf6-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="38bf6-169">System-Only</span></span>            | <span data-ttu-id="38bf6-170">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-170">False</span></span>                                                             |
| <span data-ttu-id="38bf6-171">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38bf6-171">Is-Single-Valued</span></span>       | <span data-ttu-id="38bf6-172">True</span><span class="sxs-lookup"><span data-stu-id="38bf6-172">True</span></span>                                                              |
| <span data-ttu-id="38bf6-173">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38bf6-173">Is Indexed</span></span>             | <span data-ttu-id="38bf6-174">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-174">False</span></span>                                                             |
| <span data-ttu-id="38bf6-175">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38bf6-175">In Global Catalog</span></span>      | <span data-ttu-id="38bf6-176">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-176">False</span></span>                                                             |
| <span data-ttu-id="38bf6-177">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38bf6-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="38bf6-178">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38bf6-178">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="38bf6-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38bf6-179">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="38bf6-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38bf6-180">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="38bf6-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-181">Search-Flags</span></span>           | <span data-ttu-id="38bf6-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38bf6-182">0x00000000</span></span>                                                        |
| <span data-ttu-id="38bf6-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-183">System-Flags</span></span>           | <span data-ttu-id="38bf6-184">0x00000014</span><span class="sxs-lookup"><span data-stu-id="38bf6-184">0x00000014</span></span>                                                        |
| <span data-ttu-id="38bf6-185">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38bf6-185">Classes used in</span></span>        | [<span data-ttu-id="38bf6-186">**Objeto MS-DS-Bindable**</span><span class="sxs-lookup"><span data-stu-id="38bf6-186">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="38bf6-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="38bf6-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="38bf6-188">Entrada</span><span class="sxs-lookup"><span data-stu-id="38bf6-188">Entry</span></span> | <span data-ttu-id="38bf6-189">Value</span><span class="sxs-lookup"><span data-stu-id="38bf6-189">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38bf6-190">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38bf6-190">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38bf6-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38bf6-191">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38bf6-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="38bf6-192">System-Only</span></span>            | <span data-ttu-id="38bf6-193">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-193">False</span></span>                             |
| <span data-ttu-id="38bf6-194">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38bf6-194">Is-Single-Valued</span></span>       | <span data-ttu-id="38bf6-195">True</span><span class="sxs-lookup"><span data-stu-id="38bf6-195">True</span></span>                              |
| <span data-ttu-id="38bf6-196">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38bf6-196">Is Indexed</span></span>             | <span data-ttu-id="38bf6-197">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-197">False</span></span>                             |
| <span data-ttu-id="38bf6-198">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38bf6-198">In Global Catalog</span></span>      | <span data-ttu-id="38bf6-199">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-199">False</span></span>                             |
| <span data-ttu-id="38bf6-200">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38bf6-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="38bf6-201">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38bf6-201">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38bf6-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38bf6-202">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38bf6-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38bf6-203">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38bf6-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-204">Search-Flags</span></span>           | <span data-ttu-id="38bf6-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38bf6-205">0x00000000</span></span>                        |
| <span data-ttu-id="38bf6-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-206">System-Flags</span></span>           | <span data-ttu-id="38bf6-207">0x00000014</span><span class="sxs-lookup"><span data-stu-id="38bf6-207">0x00000014</span></span>                        |
| <span data-ttu-id="38bf6-208">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38bf6-208">Classes used in</span></span>        | [<span data-ttu-id="38bf6-209">**User**</span><span class="sxs-lookup"><span data-stu-id="38bf6-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="38bf6-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38bf6-210">Windows Server 2008</span></span>



| <span data-ttu-id="38bf6-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="38bf6-211">Entry</span></span> | <span data-ttu-id="38bf6-212">Value</span><span class="sxs-lookup"><span data-stu-id="38bf6-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38bf6-213">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38bf6-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38bf6-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38bf6-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38bf6-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="38bf6-215">System-Only</span></span>            | <span data-ttu-id="38bf6-216">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-216">False</span></span>                             |
| <span data-ttu-id="38bf6-217">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38bf6-217">Is-Single-Valued</span></span>       | <span data-ttu-id="38bf6-218">True</span><span class="sxs-lookup"><span data-stu-id="38bf6-218">True</span></span>                              |
| <span data-ttu-id="38bf6-219">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38bf6-219">Is Indexed</span></span>             | <span data-ttu-id="38bf6-220">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-220">False</span></span>                             |
| <span data-ttu-id="38bf6-221">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38bf6-221">In Global Catalog</span></span>      | <span data-ttu-id="38bf6-222">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-222">False</span></span>                             |
| <span data-ttu-id="38bf6-223">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38bf6-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="38bf6-224">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38bf6-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38bf6-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38bf6-225">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38bf6-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38bf6-226">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38bf6-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-227">Search-Flags</span></span>           | <span data-ttu-id="38bf6-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38bf6-228">0x00000000</span></span>                        |
| <span data-ttu-id="38bf6-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-229">System-Flags</span></span>           | <span data-ttu-id="38bf6-230">0x00000014</span><span class="sxs-lookup"><span data-stu-id="38bf6-230">0x00000014</span></span>                        |
| <span data-ttu-id="38bf6-231">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38bf6-231">Classes used in</span></span>        | [<span data-ttu-id="38bf6-232">**User**</span><span class="sxs-lookup"><span data-stu-id="38bf6-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38bf6-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38bf6-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38bf6-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="38bf6-234">Entry</span></span> | <span data-ttu-id="38bf6-235">Value</span><span class="sxs-lookup"><span data-stu-id="38bf6-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38bf6-236">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38bf6-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38bf6-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38bf6-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38bf6-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="38bf6-238">System-Only</span></span>            | <span data-ttu-id="38bf6-239">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-239">False</span></span>                             |
| <span data-ttu-id="38bf6-240">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38bf6-240">Is-Single-Valued</span></span>       | <span data-ttu-id="38bf6-241">True</span><span class="sxs-lookup"><span data-stu-id="38bf6-241">True</span></span>                              |
| <span data-ttu-id="38bf6-242">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38bf6-242">Is Indexed</span></span>             | <span data-ttu-id="38bf6-243">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-243">False</span></span>                             |
| <span data-ttu-id="38bf6-244">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38bf6-244">In Global Catalog</span></span>      | <span data-ttu-id="38bf6-245">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-245">False</span></span>                             |
| <span data-ttu-id="38bf6-246">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38bf6-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="38bf6-247">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38bf6-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38bf6-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38bf6-248">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38bf6-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38bf6-249">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38bf6-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-250">Search-Flags</span></span>           | <span data-ttu-id="38bf6-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38bf6-251">0x00000000</span></span>                        |
| <span data-ttu-id="38bf6-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-252">System-Flags</span></span>           | <span data-ttu-id="38bf6-253">0x00000014</span><span class="sxs-lookup"><span data-stu-id="38bf6-253">0x00000014</span></span>                        |
| <span data-ttu-id="38bf6-254">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38bf6-254">Classes used in</span></span>        | [<span data-ttu-id="38bf6-255">**User**</span><span class="sxs-lookup"><span data-stu-id="38bf6-255">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38bf6-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38bf6-256">Windows Server 2012</span></span>



| <span data-ttu-id="38bf6-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="38bf6-257">Entry</span></span> | <span data-ttu-id="38bf6-258">Value</span><span class="sxs-lookup"><span data-stu-id="38bf6-258">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="38bf6-259">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="38bf6-259">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="38bf6-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38bf6-260">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="38bf6-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="38bf6-261">System-Only</span></span>            | <span data-ttu-id="38bf6-262">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-262">False</span></span>                             |
| <span data-ttu-id="38bf6-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="38bf6-263">Is-Single-Valued</span></span>       | <span data-ttu-id="38bf6-264">True</span><span class="sxs-lookup"><span data-stu-id="38bf6-264">True</span></span>                              |
| <span data-ttu-id="38bf6-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="38bf6-265">Is Indexed</span></span>             | <span data-ttu-id="38bf6-266">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-266">False</span></span>                             |
| <span data-ttu-id="38bf6-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="38bf6-267">In Global Catalog</span></span>      | <span data-ttu-id="38bf6-268">False</span><span class="sxs-lookup"><span data-stu-id="38bf6-268">False</span></span>                             |
| <span data-ttu-id="38bf6-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="38bf6-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="38bf6-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38bf6-270">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="38bf6-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38bf6-271">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="38bf6-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38bf6-272">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="38bf6-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-273">Search-Flags</span></span>           | <span data-ttu-id="38bf6-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38bf6-274">0x00000000</span></span>                        |
| <span data-ttu-id="38bf6-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38bf6-275">System-Flags</span></span>           | <span data-ttu-id="38bf6-276">0x00000014</span><span class="sxs-lookup"><span data-stu-id="38bf6-276">0x00000014</span></span>                        |
| <span data-ttu-id="38bf6-277">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="38bf6-277">Classes used in</span></span>        | [<span data-ttu-id="38bf6-278">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="38bf6-278">**User**</span></span>](c-user.md)<br/> |



 

