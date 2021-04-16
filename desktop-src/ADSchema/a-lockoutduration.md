---
title: Lockout-Duration atributo)
description: La cantidad de tiempo que se bloquea una cuenta debido a que el Lockout-Threshold se supera.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Lockout-Duration
- lockoutDuration esquema de AD de atributos
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658624"
---
# <a name="lockout-duration-attribute"></a><span data-ttu-id="8b3ab-105">Lockout-Duration atributo)</span><span class="sxs-lookup"><span data-stu-id="8b3ab-105">Lockout-Duration attribute</span></span>

<span data-ttu-id="8b3ab-106">La cantidad de tiempo que se bloquea una cuenta debido a que se supera el [**umbral de bloqueo**](a-lockoutthreshold.md) .</span><span class="sxs-lookup"><span data-stu-id="8b3ab-106">The amount of time that an account is locked due to the [**Lockout-Threshold**](a-lockoutthreshold.md) being exceeded.</span></span> <span data-ttu-id="8b3ab-107">Este valor se almacena como un entero grande que representa el negativo del número de intervalos de 100 segundos a partir del momento en que se supera el [**umbral de bloqueo y**](a-lockoutthreshold.md) que debe transcurrir antes de que se desbloquee la cuenta.</span><span class="sxs-lookup"><span data-stu-id="8b3ab-107">This value is stored as a large integer that represents the negative of the number of 100-nanosecond intervals from the time the [**Lockout-Threshold**](a-lockoutthreshold.md) is exceeded that must elapse before the account is unlocked.</span></span>



| <span data-ttu-id="8b3ab-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b3ab-108">Entry</span></span> | <span data-ttu-id="8b3ab-109">Value</span><span class="sxs-lookup"><span data-stu-id="8b3ab-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8b3ab-110">CN</span><span class="sxs-lookup"><span data-stu-id="8b3ab-110">CN</span></span>                | <span data-ttu-id="8b3ab-111">Lockout-Duration</span><span class="sxs-lookup"><span data-stu-id="8b3ab-111">Lockout-Duration</span></span>                     |
| <span data-ttu-id="8b3ab-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="8b3ab-112">Ldap-Display-Name</span></span> | <span data-ttu-id="8b3ab-113">lockoutDuration</span><span class="sxs-lookup"><span data-stu-id="8b3ab-113">lockoutDuration</span></span>                      |
| <span data-ttu-id="8b3ab-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8b3ab-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="8b3ab-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="8b3ab-115">Update Privilege</span></span>  | <span data-ttu-id="8b3ab-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="8b3ab-116">Domain administrator</span></span>                 |
| <span data-ttu-id="8b3ab-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="8b3ab-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8b3ab-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8b3ab-118">Attribute-Id</span></span>      | <span data-ttu-id="8b3ab-119">1.2.840.113556.1.4.60</span><span class="sxs-lookup"><span data-stu-id="8b3ab-119">1.2.840.113556.1.4.60</span></span>                |
| <span data-ttu-id="8b3ab-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8b3ab-120">System-Id-Guid</span></span>    | <span data-ttu-id="8b3ab-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8b3ab-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="8b3ab-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b3ab-122">Syntax</span></span>            | [<span data-ttu-id="8b3ab-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8b3ab-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="8b3ab-124">Implementations</span></span>

-   [<span data-ttu-id="8b3ab-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8b3ab-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8b3ab-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8b3ab-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8b3ab-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8b3ab-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8b3ab-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b3ab-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8b3ab-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b3ab-132">Entry</span></span> | <span data-ttu-id="8b3ab-133">Value</span><span class="sxs-lookup"><span data-stu-id="8b3ab-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3ab-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b3ab-134">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b3ab-135">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b3ab-136">System-Only</span></span>            | <span data-ttu-id="8b3ab-137">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-137">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b3ab-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8b3ab-139">True</span><span class="sxs-lookup"><span data-stu-id="8b3ab-139">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8b3ab-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b3ab-140">Is Indexed</span></span>             | <span data-ttu-id="8b3ab-141">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-141">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b3ab-142">In Global Catalog</span></span>      | <span data-ttu-id="8b3ab-143">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-143">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b3ab-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b3ab-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b3ab-145">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8b3ab-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b3ab-146">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b3ab-147">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-148">Search-Flags</span></span>           | <span data-ttu-id="8b3ab-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b3ab-149">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-150">System-Flags</span></span>           | <span data-ttu-id="8b3ab-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b3ab-151">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b3ab-152">Classes used in</span></span>        | [<span data-ttu-id="8b3ab-153">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8b3ab-154">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8b3ab-155">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-155">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8b3ab-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b3ab-156">Windows Server 2003</span></span>



| <span data-ttu-id="8b3ab-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b3ab-157">Entry</span></span> | <span data-ttu-id="8b3ab-158">Value</span><span class="sxs-lookup"><span data-stu-id="8b3ab-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3ab-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b3ab-159">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b3ab-160">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b3ab-161">System-Only</span></span>            | <span data-ttu-id="8b3ab-162">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-162">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b3ab-163">Is-Single-Valued</span></span>       | <span data-ttu-id="8b3ab-164">True</span><span class="sxs-lookup"><span data-stu-id="8b3ab-164">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8b3ab-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b3ab-165">Is Indexed</span></span>             | <span data-ttu-id="8b3ab-166">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-166">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b3ab-167">In Global Catalog</span></span>      | <span data-ttu-id="8b3ab-168">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-168">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b3ab-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b3ab-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b3ab-170">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8b3ab-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b3ab-171">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b3ab-172">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-173">Search-Flags</span></span>           | <span data-ttu-id="8b3ab-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b3ab-174">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-175">System-Flags</span></span>           | <span data-ttu-id="8b3ab-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b3ab-176">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b3ab-177">Classes used in</span></span>        | [<span data-ttu-id="8b3ab-178">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-178">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8b3ab-179">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8b3ab-180">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8b3ab-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8b3ab-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8b3ab-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b3ab-182">Entry</span></span> | <span data-ttu-id="8b3ab-183">Value</span><span class="sxs-lookup"><span data-stu-id="8b3ab-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3ab-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b3ab-184">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b3ab-185">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b3ab-186">System-Only</span></span>            | <span data-ttu-id="8b3ab-187">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-187">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b3ab-188">Is-Single-Valued</span></span>       | <span data-ttu-id="8b3ab-189">True</span><span class="sxs-lookup"><span data-stu-id="8b3ab-189">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8b3ab-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b3ab-190">Is Indexed</span></span>             | <span data-ttu-id="8b3ab-191">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-191">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b3ab-192">In Global Catalog</span></span>      | <span data-ttu-id="8b3ab-193">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-193">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b3ab-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b3ab-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b3ab-195">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8b3ab-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b3ab-196">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b3ab-197">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-198">Search-Flags</span></span>           | <span data-ttu-id="8b3ab-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b3ab-199">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-200">System-Flags</span></span>           | <span data-ttu-id="8b3ab-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b3ab-201">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b3ab-202">Classes used in</span></span>        | [<span data-ttu-id="8b3ab-203">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-203">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8b3ab-204">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-204">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8b3ab-205">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-205">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8b3ab-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b3ab-206">Windows Server 2008</span></span>



| <span data-ttu-id="8b3ab-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b3ab-207">Entry</span></span> | <span data-ttu-id="8b3ab-208">Value</span><span class="sxs-lookup"><span data-stu-id="8b3ab-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3ab-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b3ab-209">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b3ab-210">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b3ab-211">System-Only</span></span>            | <span data-ttu-id="8b3ab-212">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-212">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b3ab-213">Is-Single-Valued</span></span>       | <span data-ttu-id="8b3ab-214">True</span><span class="sxs-lookup"><span data-stu-id="8b3ab-214">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8b3ab-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b3ab-215">Is Indexed</span></span>             | <span data-ttu-id="8b3ab-216">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-216">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b3ab-217">In Global Catalog</span></span>      | <span data-ttu-id="8b3ab-218">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-218">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b3ab-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b3ab-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b3ab-220">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8b3ab-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b3ab-221">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b3ab-222">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-223">Search-Flags</span></span>           | <span data-ttu-id="8b3ab-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b3ab-224">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-225">System-Flags</span></span>           | <span data-ttu-id="8b3ab-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b3ab-226">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b3ab-227">Classes used in</span></span>        | [<span data-ttu-id="8b3ab-228">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-228">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8b3ab-229">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-229">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8b3ab-230">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-230">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8b3ab-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b3ab-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8b3ab-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b3ab-232">Entry</span></span> | <span data-ttu-id="8b3ab-233">Value</span><span class="sxs-lookup"><span data-stu-id="8b3ab-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3ab-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b3ab-234">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b3ab-235">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b3ab-236">System-Only</span></span>            | <span data-ttu-id="8b3ab-237">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-237">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b3ab-238">Is-Single-Valued</span></span>       | <span data-ttu-id="8b3ab-239">True</span><span class="sxs-lookup"><span data-stu-id="8b3ab-239">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8b3ab-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b3ab-240">Is Indexed</span></span>             | <span data-ttu-id="8b3ab-241">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-241">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b3ab-242">In Global Catalog</span></span>      | <span data-ttu-id="8b3ab-243">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-243">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b3ab-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b3ab-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b3ab-245">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8b3ab-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b3ab-246">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b3ab-247">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-248">Search-Flags</span></span>           | <span data-ttu-id="8b3ab-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b3ab-249">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-250">System-Flags</span></span>           | <span data-ttu-id="8b3ab-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b3ab-251">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-252">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b3ab-252">Classes used in</span></span>        | [<span data-ttu-id="8b3ab-253">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-253">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8b3ab-254">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-254">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8b3ab-255">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-255">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8b3ab-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b3ab-256">Windows Server 2012</span></span>



| <span data-ttu-id="8b3ab-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b3ab-257">Entry</span></span> | <span data-ttu-id="8b3ab-258">Value</span><span class="sxs-lookup"><span data-stu-id="8b3ab-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3ab-259">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8b3ab-259">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b3ab-260">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b3ab-261">System-Only</span></span>            | <span data-ttu-id="8b3ab-262">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-262">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8b3ab-263">Is-Single-Valued</span></span>       | <span data-ttu-id="8b3ab-264">True</span><span class="sxs-lookup"><span data-stu-id="8b3ab-264">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8b3ab-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8b3ab-265">Is Indexed</span></span>             | <span data-ttu-id="8b3ab-266">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-266">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b3ab-267">In Global Catalog</span></span>      | <span data-ttu-id="8b3ab-268">False</span><span class="sxs-lookup"><span data-stu-id="8b3ab-268">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b3ab-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8b3ab-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b3ab-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b3ab-270">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8b3ab-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b3ab-271">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b3ab-272">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8b3ab-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-273">Search-Flags</span></span>           | <span data-ttu-id="8b3ab-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b3ab-274">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b3ab-275">System-Flags</span></span>           | <span data-ttu-id="8b3ab-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b3ab-276">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8b3ab-277">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8b3ab-277">Classes used in</span></span>        | [<span data-ttu-id="8b3ab-278">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-278">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8b3ab-279">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-279">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8b3ab-280">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-280">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="8b3ab-281">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b3ab-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b3ab-282">**Bloqueo: umbral**</span><span class="sxs-lookup"><span data-stu-id="8b3ab-282">**Lockout-Threshold**</span></span>](a-lockoutthreshold.md)
</dt> </dl>

 

 





