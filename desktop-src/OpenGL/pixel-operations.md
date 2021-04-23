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
ms.openlocfilehash: 45d36fc22ace4ee18303ce0eb16c5a10f901510f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908883"
---
# <a name="pixel-operations"></a><span data-ttu-id="bb3ff-104">Operaciones de píxeles</span><span class="sxs-lookup"><span data-stu-id="bb3ff-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="bb3ff-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>PRUEBA \_ DE GL DE LA \_ LONBA</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-106">Property</span></span> | <span data-ttu-id="bb3ff-107">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="bb3ff-108">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-108">Description:</span></span>     | <span data-ttu-id="bb3ff-109">Habilitación de la ingesación</span><span class="sxs-lookup"><span data-stu-id="bb3ff-109">Scissoring enabled</span></span>                 |
| <span data-ttu-id="bb3ff-110">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-110">Attribute group:</span></span> | <span data-ttu-id="bb3ff-111">y habilitar</span><span class="sxs-lookup"><span data-stu-id="bb3ff-111">scissor/enable</span></span>                     |
| <span data-ttu-id="bb3ff-112">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-112">Initial value:</span></span>   | <span data-ttu-id="bb3ff-113">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="bb3ff-113">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bb3ff-114">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-114">Get command:</span></span>     | [<span data-ttu-id="bb3ff-115">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-115">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bb3ff-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL \_ DESERCIÓN \_ BOX</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-117">Property</span></span> | <span data-ttu-id="bb3ff-118">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-118">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-119">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-119">Description:</span></span>     | <span data-ttu-id="bb3ff-120">Caja de la incoerción</span><span class="sxs-lookup"><span data-stu-id="bb3ff-120">Scissor box</span></span>                                                                      |
| <span data-ttu-id="bb3ff-121">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-121">Attribute group:</span></span> | <span data-ttu-id="bb3ff-122">Tijera</span><span class="sxs-lookup"><span data-stu-id="bb3ff-122">scissor</span></span>                                                                          |
| <span data-ttu-id="bb3ff-123">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-123">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="bb3ff-124">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-124">Get command:</span></span>     | [<span data-ttu-id="bb3ff-125">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-125">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL \_ STENCIL \_ TEST</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-127">Property</span></span> | <span data-ttu-id="bb3ff-128">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-128">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="bb3ff-129">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-129">Description:</span></span>     | <span data-ttu-id="bb3ff-130">Galería de símbolos habilitada</span><span class="sxs-lookup"><span data-stu-id="bb3ff-130">Stenciling enabled</span></span>                 |
| <span data-ttu-id="bb3ff-131">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-131">Attribute group:</span></span> | <span data-ttu-id="bb3ff-132">stencil-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="bb3ff-132">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="bb3ff-133">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-133">Initial value:</span></span>   | <span data-ttu-id="bb3ff-134">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="bb3ff-134">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bb3ff-135">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-135">Get command:</span></span>     | [<span data-ttu-id="bb3ff-136">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-136">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bb3ff-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>FUNC \_ de GL STENCIL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-138">Property</span></span> | <span data-ttu-id="bb3ff-139">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-139">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-140">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-140">Description:</span></span>     | <span data-ttu-id="bb3ff-141">Función de galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="bb3ff-141">Stencil function</span></span>                                                                 |
| <span data-ttu-id="bb3ff-142">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-142">Attribute group:</span></span> | <span data-ttu-id="bb3ff-143">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="bb3ff-143">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="bb3ff-144">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-144">Initial value:</span></span>   | <span data-ttu-id="bb3ff-145">GL \_ ALWAYS</span><span class="sxs-lookup"><span data-stu-id="bb3ff-145">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="bb3ff-146">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-146">Get command:</span></span>     | [<span data-ttu-id="bb3ff-147">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL \_ STENCIL \_ VALUE \_ MASK</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-149">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-149">Property</span></span> | <span data-ttu-id="bb3ff-150">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-150">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-151">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-151">Description:</span></span>     | <span data-ttu-id="bb3ff-152">Máscara de galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="bb3ff-152">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="bb3ff-153">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-153">Attribute group:</span></span> | <span data-ttu-id="bb3ff-154">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="bb3ff-154">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="bb3ff-155">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-155">Initial value:</span></span>   | <span data-ttu-id="bb3ff-156">1</span><span class="sxs-lookup"><span data-stu-id="bb3ff-156">1's</span></span>                                                                              |
| <span data-ttu-id="bb3ff-157">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-157">Get command:</span></span>     | [<span data-ttu-id="bb3ff-158">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-158">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL \_ STENCIL \_ REF</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-160">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-160">Property</span></span> | <span data-ttu-id="bb3ff-161">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-161">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-162">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-162">Description:</span></span>     | <span data-ttu-id="bb3ff-163">Valor de referencia de galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="bb3ff-163">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="bb3ff-164">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-164">Attribute group:</span></span> | <span data-ttu-id="bb3ff-165">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="bb3ff-165">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="bb3ff-166">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-166">Initial value:</span></span>   | <span data-ttu-id="bb3ff-167">0</span><span class="sxs-lookup"><span data-stu-id="bb3ff-167">0</span></span>                                                                                |
| <span data-ttu-id="bb3ff-168">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-168">Get command:</span></span>     | [<span data-ttu-id="bb3ff-169">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-169">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>ERROR \_ DE GL STENCIL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-171">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-171">Property</span></span> | <span data-ttu-id="bb3ff-172">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-172">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-173">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-173">Description:</span></span>     | <span data-ttu-id="bb3ff-174">Acción de error de galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="bb3ff-174">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="bb3ff-175">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-175">Attribute group:</span></span> | <span data-ttu-id="bb3ff-176">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="bb3ff-176">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="bb3ff-177">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-177">Initial value:</span></span>   | <span data-ttu-id="bb3ff-178">GL \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="bb3ff-178">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="bb3ff-179">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-179">Get command:</span></span>     | [<span data-ttu-id="bb3ff-180">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-180">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>ERROR DE PROFUNDIDAD DE PASO DE GALERÍA DE SÍMBOLOS \_ \_ DE \_ \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-182">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-182">Property</span></span> | <span data-ttu-id="bb3ff-183">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-183">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-184">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-184">Description:</span></span>     | <span data-ttu-id="bb3ff-185">Acción de error del búfer de profundidad de galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="bb3ff-185">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="bb3ff-186">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-186">Attribute group:</span></span> | <span data-ttu-id="bb3ff-187">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="bb3ff-187">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="bb3ff-188">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-188">Initial value:</span></span>   | <span data-ttu-id="bb3ff-189">GL \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="bb3ff-189">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="bb3ff-190">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-190">Get command:</span></span>     | [<span data-ttu-id="bb3ff-191">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-191">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>PASO DE PROFUNDIDAD DE PASO DE GALERÍA \_ \_ DE SÍMBOLOS DE \_ \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-193">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-193">Property</span></span> | <span data-ttu-id="bb3ff-194">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-194">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-195">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-195">Description:</span></span>     | <span data-ttu-id="bb3ff-196">Acción de paso de búfer de profundidad de galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="bb3ff-196">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="bb3ff-197">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-197">Attribute group:</span></span> | <span data-ttu-id="bb3ff-198">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="bb3ff-198">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="bb3ff-199">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-199">Initial value:</span></span>   | <span data-ttu-id="bb3ff-200">GL \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="bb3ff-200">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="bb3ff-201">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-201">Get command:</span></span>     | [<span data-ttu-id="bb3ff-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>PRUEBA \_ ALFA DE \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-204">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-204">Property</span></span> | <span data-ttu-id="bb3ff-205">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-205">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="bb3ff-206">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-206">Description:</span></span>     | <span data-ttu-id="bb3ff-207">Prueba alfa habilitada</span><span class="sxs-lookup"><span data-stu-id="bb3ff-207">Alpha test enabled</span></span>                 |
| <span data-ttu-id="bb3ff-208">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-208">Attribute group:</span></span> | <span data-ttu-id="bb3ff-209">color-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="bb3ff-209">color-buffer/enable</span></span>                |
| <span data-ttu-id="bb3ff-210">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-210">Initial value:</span></span>   | <span data-ttu-id="bb3ff-211">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="bb3ff-211">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bb3ff-212">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-212">Get command:</span></span>     | [<span data-ttu-id="bb3ff-213">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-213">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bb3ff-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL \_ ALPHA \_ TEST \_ FUNC</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-215">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-215">Property</span></span> | <span data-ttu-id="bb3ff-216">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-216">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-217">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-217">Description:</span></span>     | <span data-ttu-id="bb3ff-218">Función de prueba alfa</span><span class="sxs-lookup"><span data-stu-id="bb3ff-218">Alpha test function</span></span>                                                              |
| <span data-ttu-id="bb3ff-219">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-219">Attribute group:</span></span> | <span data-ttu-id="bb3ff-220">búfer de color</span><span class="sxs-lookup"><span data-stu-id="bb3ff-220">color-buffer</span></span>                                                                     |
| <span data-ttu-id="bb3ff-221">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-221">Initial value:</span></span>   | <span data-ttu-id="bb3ff-222">GL \_ ALWAYS</span><span class="sxs-lookup"><span data-stu-id="bb3ff-222">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="bb3ff-223">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-223">Get command:</span></span>     | [<span data-ttu-id="bb3ff-224">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-224">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL \_ ALPHA \_ TEST \_ REF</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-226">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-226">Property</span></span> | <span data-ttu-id="bb3ff-227">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-227">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-228">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-228">Description:</span></span>     | <span data-ttu-id="bb3ff-229">Valor de referencia de prueba alfa</span><span class="sxs-lookup"><span data-stu-id="bb3ff-229">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="bb3ff-230">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-230">Attribute group:</span></span> | <span data-ttu-id="bb3ff-231">búfer de color</span><span class="sxs-lookup"><span data-stu-id="bb3ff-231">color-buffer</span></span>                                                                     |
| <span data-ttu-id="bb3ff-232">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-232">Initial value:</span></span>   | <span data-ttu-id="bb3ff-233">0</span><span class="sxs-lookup"><span data-stu-id="bb3ff-233">0</span></span>                                                                                |
| <span data-ttu-id="bb3ff-234">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-234">Get command:</span></span>     | [<span data-ttu-id="bb3ff-235">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-235">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>PRUEBA \_ DE PROFUNDIDAD DE \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-237">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-237">Property</span></span> | <span data-ttu-id="bb3ff-238">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-238">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="bb3ff-239">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-239">Description:</span></span>     | <span data-ttu-id="bb3ff-240">Búfer de profundidad habilitado</span><span class="sxs-lookup"><span data-stu-id="bb3ff-240">Depth buffer enabled</span></span>               |
| <span data-ttu-id="bb3ff-241">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-241">Attribute group:</span></span> | <span data-ttu-id="bb3ff-242">depth-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="bb3ff-242">depth-buffer/enable</span></span>                |
| <span data-ttu-id="bb3ff-243">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-243">Initial value:</span></span>   | <span data-ttu-id="bb3ff-244">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="bb3ff-244">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bb3ff-245">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-245">Get command:</span></span>     | [<span data-ttu-id="bb3ff-246">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-246">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bb3ff-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL \_ DEPTH \_ FUNC</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-248">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-248">Property</span></span> | <span data-ttu-id="bb3ff-249">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-249">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-250">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-250">Description:</span></span>     | <span data-ttu-id="bb3ff-251">Función de prueba de búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-251">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="bb3ff-252">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-252">Attribute group:</span></span> | <span data-ttu-id="bb3ff-253">búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-253">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="bb3ff-254">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-254">Initial value:</span></span>   | <span data-ttu-id="bb3ff-255">GL \_ LESS</span><span class="sxs-lookup"><span data-stu-id="bb3ff-255">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="bb3ff-256">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-256">Get command:</span></span>     | [<span data-ttu-id="bb3ff-257">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-257">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL \_ BLEND</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-259">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-259">Property</span></span> | <span data-ttu-id="bb3ff-260">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-260">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="bb3ff-261">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-261">Description:</span></span>     | <span data-ttu-id="bb3ff-262">Mezcla habilitada</span><span class="sxs-lookup"><span data-stu-id="bb3ff-262">Blending enabled</span></span>                   |
| <span data-ttu-id="bb3ff-263">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-263">Attribute group:</span></span> | <span data-ttu-id="bb3ff-264">color-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="bb3ff-264">color-buffer/enable</span></span>                |
| <span data-ttu-id="bb3ff-265">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-265">Initial value:</span></span>   | <span data-ttu-id="bb3ff-266">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="bb3ff-266">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bb3ff-267">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-267">Get command:</span></span>     | [<span data-ttu-id="bb3ff-268">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-268">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bb3ff-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL \_ BLENC \_ SRC</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-270">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-270">Property</span></span> | <span data-ttu-id="bb3ff-271">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-271">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-272">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-272">Description:</span></span>     | <span data-ttu-id="bb3ff-273">Función de origen de combinación</span><span class="sxs-lookup"><span data-stu-id="bb3ff-273">Blending source function</span></span>                                                         |
| <span data-ttu-id="bb3ff-274">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-274">Attribute group:</span></span> | <span data-ttu-id="bb3ff-275">búfer de color</span><span class="sxs-lookup"><span data-stu-id="bb3ff-275">color-buffer</span></span>                                                                     |
| <span data-ttu-id="bb3ff-276">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-276">Initial value:</span></span>   | <span data-ttu-id="bb3ff-277">GL \_ ONE</span><span class="sxs-lookup"><span data-stu-id="bb3ff-277">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="bb3ff-278">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-278">Get command:</span></span>     | [<span data-ttu-id="bb3ff-279">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-279">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL \_ BLEND \_ DST</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-281">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-281">Property</span></span> | <span data-ttu-id="bb3ff-282">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-282">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-283">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-283">Description:</span></span>     | <span data-ttu-id="bb3ff-284">Función de destino de mezcla</span><span class="sxs-lookup"><span data-stu-id="bb3ff-284">Blending destination function</span></span>                                                    |
| <span data-ttu-id="bb3ff-285">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-285">Attribute group:</span></span> | <span data-ttu-id="bb3ff-286">búfer de color</span><span class="sxs-lookup"><span data-stu-id="bb3ff-286">color-buffer</span></span>                                                                     |
| <span data-ttu-id="bb3ff-287">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-287">Initial value:</span></span>   | <span data-ttu-id="bb3ff-288">GL \_ ZERO</span><span class="sxs-lookup"><span data-stu-id="bb3ff-288">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="bb3ff-289">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-289">Get command:</span></span>     | [<span data-ttu-id="bb3ff-290">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-290">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bb3ff-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL \_ DITHER</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-292">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-292">Property</span></span> | <span data-ttu-id="bb3ff-293">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-293">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="bb3ff-294">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-294">Description:</span></span>     | <span data-ttu-id="bb3ff-295">Dithering enabled</span><span class="sxs-lookup"><span data-stu-id="bb3ff-295">Dithering enabled</span></span>                  |
| <span data-ttu-id="bb3ff-296">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-296">Attribute group:</span></span> | <span data-ttu-id="bb3ff-297">color-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="bb3ff-297">color-buffer/enable</span></span>                |
| <span data-ttu-id="bb3ff-298">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-298">Initial value:</span></span>   | <span data-ttu-id="bb3ff-299">GL \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="bb3ff-299">GL\_TRUE</span></span>                           |
| <span data-ttu-id="bb3ff-300">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-300">Get command:</span></span>     | [<span data-ttu-id="bb3ff-301">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-301">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bb3ff-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL \_ LOGIC \_ OP</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-303">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-303">Property</span></span> | <span data-ttu-id="bb3ff-304">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-304">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="bb3ff-305">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-305">Description:</span></span>     | <span data-ttu-id="bb3ff-306">Operación lógica habilitada</span><span class="sxs-lookup"><span data-stu-id="bb3ff-306">Logical operation enabled</span></span>          |
| <span data-ttu-id="bb3ff-307">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-307">Attribute group:</span></span> | <span data-ttu-id="bb3ff-308">color-buffer/enable</span><span class="sxs-lookup"><span data-stu-id="bb3ff-308">color-buffer/enable</span></span>                |
| <span data-ttu-id="bb3ff-309">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-309">Initial value:</span></span>   | <span data-ttu-id="bb3ff-310">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="bb3ff-310">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bb3ff-311">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-311">Get command:</span></span>     | [<span data-ttu-id="bb3ff-312">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-312">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bb3ff-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>MODO \_ DE OPERACIÓN LÓGICA DE \_ \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="bb3ff-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="bb3ff-314">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb3ff-314">Property</span></span> | <span data-ttu-id="bb3ff-315">Value</span><span class="sxs-lookup"><span data-stu-id="bb3ff-315">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb3ff-316">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-316">Description:</span></span>     | <span data-ttu-id="bb3ff-317">Función de operación lógica</span><span class="sxs-lookup"><span data-stu-id="bb3ff-317">Logical operation function</span></span>                                                       |
| <span data-ttu-id="bb3ff-318">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-318">Attribute group:</span></span> | <span data-ttu-id="bb3ff-319">búfer de color</span><span class="sxs-lookup"><span data-stu-id="bb3ff-319">color-buffer</span></span>                                                                     |
| <span data-ttu-id="bb3ff-320">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-320">Initial value:</span></span>   | <span data-ttu-id="bb3ff-321">GL \_ COPY</span><span class="sxs-lookup"><span data-stu-id="bb3ff-321">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="bb3ff-322">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="bb3ff-322">Get command:</span></span>     | [<span data-ttu-id="bb3ff-323">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bb3ff-323">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




