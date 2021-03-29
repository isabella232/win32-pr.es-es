---
title: Operaciones de píxeles
description: Operaciones de píxeles
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Operaciones de píxeles OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda15342b246ba979bdbe60184eeb632368f36b4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904039"
---
# <a name="pixel-operations"></a><span data-ttu-id="e061e-104">Operaciones de píxeles</span><span class="sxs-lookup"><span data-stu-id="e061e-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="e061e-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_prueba de tijeras GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e061e-106">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-106">Description:</span></span>     | <span data-ttu-id="e061e-107">Tijera habilitada</span><span class="sxs-lookup"><span data-stu-id="e061e-107">Scissoring enabled</span></span>                 |
| <span data-ttu-id="e061e-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-108">Attribute group:</span></span> | <span data-ttu-id="e061e-109">tijeras/habilitación</span><span class="sxs-lookup"><span data-stu-id="e061e-109">scissor/enable</span></span>                     |
| <span data-ttu-id="e061e-110">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-110">Initial value:</span></span>   | <span data-ttu-id="e061e-111">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="e061e-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e061e-112">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-112">Get command:</span></span>     | [<span data-ttu-id="e061e-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e061e-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e061e-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_cuadro de tijeras de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-115">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-115">Description:</span></span>     | <span data-ttu-id="e061e-116">Cuadro de tijeras</span><span class="sxs-lookup"><span data-stu-id="e061e-116">Scissor box</span></span>                                                                      |
| <span data-ttu-id="e061e-117">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-117">Attribute group:</span></span> | <span data-ttu-id="e061e-118">tijera</span><span class="sxs-lookup"><span data-stu-id="e061e-118">scissor</span></span>                                                                          |
| <span data-ttu-id="e061e-119">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-119">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="e061e-120">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-120">Get command:</span></span>     | [<span data-ttu-id="e061e-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_prueba de galería de símbolos GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e061e-123">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-123">Description:</span></span>     | <span data-ttu-id="e061e-124">Estarcido habilitado</span><span class="sxs-lookup"><span data-stu-id="e061e-124">Stenciling enabled</span></span>                 |
| <span data-ttu-id="e061e-125">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-125">Attribute group:</span></span> | <span data-ttu-id="e061e-126">Galería de símbolos: búfer/habilitar</span><span class="sxs-lookup"><span data-stu-id="e061e-126">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="e061e-127">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-127">Initial value:</span></span>   | <span data-ttu-id="e061e-128">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="e061e-128">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e061e-129">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-129">Get command:</span></span>     | [<span data-ttu-id="e061e-130">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e061e-130">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e061e-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>la \_ Galería de símbolos GL \_ FUNC</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-132">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-132">Description:</span></span>     | <span data-ttu-id="e061e-133">Función de estarcido</span><span class="sxs-lookup"><span data-stu-id="e061e-133">Stencil function</span></span>                                                                 |
| <span data-ttu-id="e061e-134">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-134">Attribute group:</span></span> | <span data-ttu-id="e061e-135">cliché-búfer</span><span class="sxs-lookup"><span data-stu-id="e061e-135">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e061e-136">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-136">Initial value:</span></span>   | <span data-ttu-id="e061e-137">GL \_ siempre</span><span class="sxs-lookup"><span data-stu-id="e061e-137">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="e061e-138">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-138">Get command:</span></span>     | [<span data-ttu-id="e061e-139">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_máscara de \_ valor de estarcido GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-141">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-141">Description:</span></span>     | <span data-ttu-id="e061e-142">Máscara de galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="e061e-142">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="e061e-143">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-143">Attribute group:</span></span> | <span data-ttu-id="e061e-144">cliché-búfer</span><span class="sxs-lookup"><span data-stu-id="e061e-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e061e-145">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-145">Initial value:</span></span>   | <span data-ttu-id="e061e-146">1</span><span class="sxs-lookup"><span data-stu-id="e061e-146">1's</span></span>                                                                              |
| <span data-ttu-id="e061e-147">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-147">Get command:</span></span>     | [<span data-ttu-id="e061e-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>\_referencia de galería de símbolos GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-150">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-150">Description:</span></span>     | <span data-ttu-id="e061e-151">Valor de referencia de estarcido</span><span class="sxs-lookup"><span data-stu-id="e061e-151">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="e061e-152">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-152">Attribute group:</span></span> | <span data-ttu-id="e061e-153">cliché-búfer</span><span class="sxs-lookup"><span data-stu-id="e061e-153">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e061e-154">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-154">Initial value:</span></span>   | <span data-ttu-id="e061e-155">0</span><span class="sxs-lookup"><span data-stu-id="e061e-155">0</span></span>                                                                                |
| <span data-ttu-id="e061e-156">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-156">Get command:</span></span>     | [<span data-ttu-id="e061e-157">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-157">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>error en la \_ Galería de símbolos GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-159">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-159">Description:</span></span>     | <span data-ttu-id="e061e-160">Acción de error de estarcido</span><span class="sxs-lookup"><span data-stu-id="e061e-160">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="e061e-161">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-161">Attribute group:</span></span> | <span data-ttu-id="e061e-162">cliché-búfer</span><span class="sxs-lookup"><span data-stu-id="e061e-162">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e061e-163">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-163">Initial value:</span></span>   | <span data-ttu-id="e061e-164">mantenimiento de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="e061e-164">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="e061e-165">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-165">Get command:</span></span>     | [<span data-ttu-id="e061e-166">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-166">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>error de profundidad de la \_ fase de estarcido GL \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-168">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-168">Description:</span></span>     | <span data-ttu-id="e061e-169">Acción de error de búfer de profundidad de estarcido</span><span class="sxs-lookup"><span data-stu-id="e061e-169">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="e061e-170">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-170">Attribute group:</span></span> | <span data-ttu-id="e061e-171">cliché-búfer</span><span class="sxs-lookup"><span data-stu-id="e061e-171">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e061e-172">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-172">Initial value:</span></span>   | <span data-ttu-id="e061e-173">mantenimiento de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="e061e-173">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="e061e-174">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-174">Get command:</span></span>     | [<span data-ttu-id="e061e-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>\_paso de \_ \_ profundidad \_ de la galería de símbolos GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-177">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-177">Description:</span></span>     | <span data-ttu-id="e061e-178">Acción de paso de búfer de profundidad de estarcido</span><span class="sxs-lookup"><span data-stu-id="e061e-178">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="e061e-179">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-179">Attribute group:</span></span> | <span data-ttu-id="e061e-180">cliché-búfer</span><span class="sxs-lookup"><span data-stu-id="e061e-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e061e-181">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-181">Initial value:</span></span>   | <span data-ttu-id="e061e-182">mantenimiento de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="e061e-182">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="e061e-183">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-183">Get command:</span></span>     | [<span data-ttu-id="e061e-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>prueba de GL \_ alpha \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e061e-186">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-186">Description:</span></span>     | <span data-ttu-id="e061e-187">Prueba alfa habilitada</span><span class="sxs-lookup"><span data-stu-id="e061e-187">Alpha test enabled</span></span>                 |
| <span data-ttu-id="e061e-188">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-188">Attribute group:</span></span> | <span data-ttu-id="e061e-189">búfer de color/habilitar</span><span class="sxs-lookup"><span data-stu-id="e061e-189">color-buffer/enable</span></span>                |
| <span data-ttu-id="e061e-190">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-190">Initial value:</span></span>   | <span data-ttu-id="e061e-191">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="e061e-191">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e061e-192">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-192">Get command:</span></span>     | [<span data-ttu-id="e061e-193">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e061e-193">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e061e-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>FUNC. de prueba de GL \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-195">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-195">Description:</span></span>     | <span data-ttu-id="e061e-196">Función de prueba alfa</span><span class="sxs-lookup"><span data-stu-id="e061e-196">Alpha test function</span></span>                                                              |
| <span data-ttu-id="e061e-197">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-197">Attribute group:</span></span> | <span data-ttu-id="e061e-198">búfer de color</span><span class="sxs-lookup"><span data-stu-id="e061e-198">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e061e-199">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-199">Initial value:</span></span>   | <span data-ttu-id="e061e-200">GL \_ siempre</span><span class="sxs-lookup"><span data-stu-id="e061e-200">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="e061e-201">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-201">Get command:</span></span>     | [<span data-ttu-id="e061e-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>referencia de prueba de GL \_ alfa \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-204">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-204">Description:</span></span>     | <span data-ttu-id="e061e-205">Valor de referencia de la prueba alfa</span><span class="sxs-lookup"><span data-stu-id="e061e-205">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="e061e-206">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-206">Attribute group:</span></span> | <span data-ttu-id="e061e-207">búfer de color</span><span class="sxs-lookup"><span data-stu-id="e061e-207">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e061e-208">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-208">Initial value:</span></span>   | <span data-ttu-id="e061e-209">0</span><span class="sxs-lookup"><span data-stu-id="e061e-209">0</span></span>                                                                                |
| <span data-ttu-id="e061e-210">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-210">Get command:</span></span>     | [<span data-ttu-id="e061e-211">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-211">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_prueba de profundidad de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e061e-213">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-213">Description:</span></span>     | <span data-ttu-id="e061e-214">Búfer de profundidad habilitado</span><span class="sxs-lookup"><span data-stu-id="e061e-214">Depth buffer enabled</span></span>               |
| <span data-ttu-id="e061e-215">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-215">Attribute group:</span></span> | <span data-ttu-id="e061e-216">profundidad de búfer/habilitación</span><span class="sxs-lookup"><span data-stu-id="e061e-216">depth-buffer/enable</span></span>                |
| <span data-ttu-id="e061e-217">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-217">Initial value:</span></span>   | <span data-ttu-id="e061e-218">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="e061e-218">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e061e-219">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-219">Get command:</span></span>     | [<span data-ttu-id="e061e-220">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e061e-220">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e061e-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>\_FUNC profundidad de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-222">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-222">Description:</span></span>     | <span data-ttu-id="e061e-223">Función de prueba de búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="e061e-223">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="e061e-224">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-224">Attribute group:</span></span> | <span data-ttu-id="e061e-225">búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="e061e-225">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="e061e-226">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-226">Initial value:</span></span>   | <span data-ttu-id="e061e-227">CONTABILIDAD \_ inferior</span><span class="sxs-lookup"><span data-stu-id="e061e-227">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="e061e-228">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-228">Get command:</span></span>     | [<span data-ttu-id="e061e-229">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-229">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>fusión de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e061e-231">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-231">Description:</span></span>     | <span data-ttu-id="e061e-232">Combinación habilitada</span><span class="sxs-lookup"><span data-stu-id="e061e-232">Blending enabled</span></span>                   |
| <span data-ttu-id="e061e-233">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-233">Attribute group:</span></span> | <span data-ttu-id="e061e-234">búfer de color/habilitar</span><span class="sxs-lookup"><span data-stu-id="e061e-234">color-buffer/enable</span></span>                |
| <span data-ttu-id="e061e-235">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-235">Initial value:</span></span>   | <span data-ttu-id="e061e-236">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="e061e-236">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e061e-237">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-237">Get command:</span></span>     | [<span data-ttu-id="e061e-238">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e061e-238">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e061e-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_src BLENC \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-240">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-240">Description:</span></span>     | <span data-ttu-id="e061e-241">Blending (función de origen)</span><span class="sxs-lookup"><span data-stu-id="e061e-241">Blending source function</span></span>                                                         |
| <span data-ttu-id="e061e-242">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-242">Attribute group:</span></span> | <span data-ttu-id="e061e-243">búfer de color</span><span class="sxs-lookup"><span data-stu-id="e061e-243">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e061e-244">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-244">Initial value:</span></span>   | <span data-ttu-id="e061e-245">GL \_ uno</span><span class="sxs-lookup"><span data-stu-id="e061e-245">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="e061e-246">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-246">Get command:</span></span>     | [<span data-ttu-id="e061e-247">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-247">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>DST de contab. \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-249">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-249">Description:</span></span>     | <span data-ttu-id="e061e-250">Función de destino de fusión</span><span class="sxs-lookup"><span data-stu-id="e061e-250">Blending destination function</span></span>                                                    |
| <span data-ttu-id="e061e-251">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-251">Attribute group:</span></span> | <span data-ttu-id="e061e-252">búfer de color</span><span class="sxs-lookup"><span data-stu-id="e061e-252">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e061e-253">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-253">Initial value:</span></span>   | <span data-ttu-id="e061e-254">GL \_ cero</span><span class="sxs-lookup"><span data-stu-id="e061e-254">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="e061e-255">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-255">Get command:</span></span>     | [<span data-ttu-id="e061e-256">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-256">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e061e-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>interpolación en contab. \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e061e-258">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-258">Description:</span></span>     | <span data-ttu-id="e061e-259">Interpolación habilitada</span><span class="sxs-lookup"><span data-stu-id="e061e-259">Dithering enabled</span></span>                  |
| <span data-ttu-id="e061e-260">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-260">Attribute group:</span></span> | <span data-ttu-id="e061e-261">búfer de color/habilitar</span><span class="sxs-lookup"><span data-stu-id="e061e-261">color-buffer/enable</span></span>                |
| <span data-ttu-id="e061e-262">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-262">Initial value:</span></span>   | <span data-ttu-id="e061e-263">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="e061e-263">GL\_TRUE</span></span>                           |
| <span data-ttu-id="e061e-264">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-264">Get command:</span></span>     | [<span data-ttu-id="e061e-265">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e061e-265">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e061e-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>\_OP lógica de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e061e-267">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-267">Description:</span></span>     | <span data-ttu-id="e061e-268">Operación lógica habilitada</span><span class="sxs-lookup"><span data-stu-id="e061e-268">Logical operation enabled</span></span>          |
| <span data-ttu-id="e061e-269">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-269">Attribute group:</span></span> | <span data-ttu-id="e061e-270">búfer de color/habilitar</span><span class="sxs-lookup"><span data-stu-id="e061e-270">color-buffer/enable</span></span>                |
| <span data-ttu-id="e061e-271">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-271">Initial value:</span></span>   | <span data-ttu-id="e061e-272">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="e061e-272">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e061e-273">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-273">Get command:</span></span>     | [<span data-ttu-id="e061e-274">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e061e-274">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e061e-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_modo de \_ OP \_ lógica de contabilidad</dt> </span><span class="sxs-lookup"><span data-stu-id="e061e-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e061e-276">Descripción:</span><span class="sxs-lookup"><span data-stu-id="e061e-276">Description:</span></span>     | <span data-ttu-id="e061e-277">Función de operación lógica</span><span class="sxs-lookup"><span data-stu-id="e061e-277">Logical operation function</span></span>                                                       |
| <span data-ttu-id="e061e-278">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="e061e-278">Attribute group:</span></span> | <span data-ttu-id="e061e-279">búfer de color</span><span class="sxs-lookup"><span data-stu-id="e061e-279">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e061e-280">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="e061e-280">Initial value:</span></span>   | <span data-ttu-id="e061e-281">copia en GL \_</span><span class="sxs-lookup"><span data-stu-id="e061e-281">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="e061e-282">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="e061e-282">Get command:</span></span>     | [<span data-ttu-id="e061e-283">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e061e-283">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




