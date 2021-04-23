---
title: Variables de estado de transformación
description: Variables de estado de transformación
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Variables de estado de transformación OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b53e0abae08447df86d8968a33a361be08a1e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908833"
---
# <a name="transformation-state-variables"></a><span data-ttu-id="fb35c-104">Variables de estado de transformación</span><span class="sxs-lookup"><span data-stu-id="fb35c-104">Transformation State Variables</span></span>

<dl> <span data-ttu-id="fb35c-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL \_ MODELVIEW \_ MATRIX</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL\_MODELVIEW\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-106">Property</span></span> | <span data-ttu-id="fb35c-107">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="fb35c-108">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-108">Description:</span></span>     | <span data-ttu-id="fb35c-109">Pila de matriz modelview</span><span class="sxs-lookup"><span data-stu-id="fb35c-109">Modelview matrix stack</span></span>             |
| <span data-ttu-id="fb35c-110">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-110">Attribute group:</span></span> |                                    |
| <span data-ttu-id="fb35c-111">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-111">Initial value:</span></span>   | <span data-ttu-id="fb35c-112">Identidad</span><span class="sxs-lookup"><span data-stu-id="fb35c-112">Identity</span></span>                           |
| <span data-ttu-id="fb35c-113">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-113">Get command:</span></span>     | [<span data-ttu-id="fb35c-114">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="fb35c-114">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="fb35c-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>MATRIZ \_ DE \_ PROYECCIÓN DE GL</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL\_PROJECTION\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-116">Property</span></span> | <span data-ttu-id="fb35c-117">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-117">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="fb35c-118">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-118">Description:</span></span>     | <span data-ttu-id="fb35c-119">Pila de matriz de proyección</span><span class="sxs-lookup"><span data-stu-id="fb35c-119">Projection matrix stack</span></span>                                                        |
| <span data-ttu-id="fb35c-120">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-120">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="fb35c-121">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-121">Initial value:</span></span>   | <span data-ttu-id="fb35c-122">Identidad</span><span class="sxs-lookup"><span data-stu-id="fb35c-122">Identity</span></span>                                                                       |
| <span data-ttu-id="fb35c-123">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-123">Get command:</span></span>     | [<span data-ttu-id="fb35c-124">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="fb35c-124">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="fb35c-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>MATRIZ \_ DE TEXTURA \_ DE GL</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL\_TEXTURE\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-126">Property</span></span> | <span data-ttu-id="fb35c-127">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-127">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="fb35c-128">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-128">Description:</span></span>     | <span data-ttu-id="fb35c-129">Pila de matriz de textura</span><span class="sxs-lookup"><span data-stu-id="fb35c-129">Texture matrix stack</span></span>                                                           |
| <span data-ttu-id="fb35c-130">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-130">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="fb35c-131">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-131">Initial value:</span></span>   | <span data-ttu-id="fb35c-132">Identidad</span><span class="sxs-lookup"><span data-stu-id="fb35c-132">Identity</span></span>                                                                       |
| <span data-ttu-id="fb35c-133">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-133">Get command:</span></span>     | [<span data-ttu-id="fb35c-134">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="fb35c-134">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="fb35c-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>VENTANILLA \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL\_VIEWPORT</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-136">Property</span></span> | <span data-ttu-id="fb35c-137">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-137">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fb35c-138">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-138">Description:</span></span>     | <span data-ttu-id="fb35c-139">Origen y extensión de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="fb35c-139">Viewport origin and extent</span></span>                                                       |
| <span data-ttu-id="fb35c-140">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-140">Attribute group:</span></span> | <span data-ttu-id="fb35c-141">ventanilla</span><span class="sxs-lookup"><span data-stu-id="fb35c-141">viewport</span></span>                                                                         |
| <span data-ttu-id="fb35c-142">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-142">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="fb35c-143">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-143">Get command:</span></span>     | [<span data-ttu-id="fb35c-144">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="fb35c-144">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="fb35c-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>INTERVALO \_ DE PROFUNDIDAD DE \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL\_DEPTH\_RANGE</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-146">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-146">Property</span></span> | <span data-ttu-id="fb35c-147">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-147">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="fb35c-148">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-148">Description:</span></span>     | <span data-ttu-id="fb35c-149">Intervalo de profundidad cerca y lejos</span><span class="sxs-lookup"><span data-stu-id="fb35c-149">Depth range near and far</span></span>                                                       |
| <span data-ttu-id="fb35c-150">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-150">Attribute group:</span></span> | <span data-ttu-id="fb35c-151">ventanilla</span><span class="sxs-lookup"><span data-stu-id="fb35c-151">viewport</span></span>                                                                       |
| <span data-ttu-id="fb35c-152">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-152">Initial value:</span></span>   | <span data-ttu-id="fb35c-153">0, 1</span><span class="sxs-lookup"><span data-stu-id="fb35c-153">0, 1</span></span>                                                                           |
| <span data-ttu-id="fb35c-154">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-154">Get command:</span></span>     | [<span data-ttu-id="fb35c-155">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="fb35c-155">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="fb35c-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>PROFUNDIDAD DE \_ PILA DE GL MODELVIEW \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-157">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-157">Property</span></span> | <span data-ttu-id="fb35c-158">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-158">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fb35c-159">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-159">Description:</span></span>     | <span data-ttu-id="fb35c-160">Puntero de pila de la matriz modelview</span><span class="sxs-lookup"><span data-stu-id="fb35c-160">Modelview matrix stack pointer</span></span>                                                   |
| <span data-ttu-id="fb35c-161">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-161">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="fb35c-162">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-162">Initial value:</span></span>   | <span data-ttu-id="fb35c-163">1</span><span class="sxs-lookup"><span data-stu-id="fb35c-163">1</span></span>                                                                                |
| <span data-ttu-id="fb35c-164">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-164">Get command:</span></span>     | [<span data-ttu-id="fb35c-165">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="fb35c-165">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="fb35c-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>PROFUNDIDAD DE \_ LA PILA \_ DE \_ PROYECCIÓN DE GL</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-167">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-167">Property</span></span> | <span data-ttu-id="fb35c-168">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-168">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fb35c-169">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-169">Description:</span></span>     | <span data-ttu-id="fb35c-170">Puntero de pila de matriz de proyección</span><span class="sxs-lookup"><span data-stu-id="fb35c-170">Projection matrix stack pointer</span></span>                                                  |
| <span data-ttu-id="fb35c-171">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-171">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="fb35c-172">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-172">Initial value:</span></span>   | <span data-ttu-id="fb35c-173">1</span><span class="sxs-lookup"><span data-stu-id="fb35c-173">1</span></span>                                                                                |
| <span data-ttu-id="fb35c-174">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-174">Get command:</span></span>     | [<span data-ttu-id="fb35c-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="fb35c-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="fb35c-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>PROFUNDIDAD DE \_ LA PILA DE TEXTURA \_ \_ DE GL</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-177">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-177">Property</span></span> | <span data-ttu-id="fb35c-178">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-178">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fb35c-179">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-179">Description:</span></span>     | <span data-ttu-id="fb35c-180">Puntero de pila de la matriz de textura</span><span class="sxs-lookup"><span data-stu-id="fb35c-180">Texture matrix stack pointer</span></span>                                                     |
| <span data-ttu-id="fb35c-181">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-181">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="fb35c-182">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-182">Initial value:</span></span>   | <span data-ttu-id="fb35c-183">1</span><span class="sxs-lookup"><span data-stu-id="fb35c-183">1</span></span>                                                                                |
| <span data-ttu-id="fb35c-184">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-184">Get command:</span></span>     | [<span data-ttu-id="fb35c-185">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="fb35c-185">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="fb35c-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>MODO DE \_ \_ MATRIZ DE GL</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL\_MATRIX\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-187">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-187">Property</span></span> | <span data-ttu-id="fb35c-188">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-188">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fb35c-189">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-189">Description:</span></span>     | <span data-ttu-id="fb35c-190">Modo de matriz actual</span><span class="sxs-lookup"><span data-stu-id="fb35c-190">Current matrix mode</span></span>                                                              |
| <span data-ttu-id="fb35c-191">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-191">Attribute group:</span></span> | <span data-ttu-id="fb35c-192">transform</span><span class="sxs-lookup"><span data-stu-id="fb35c-192">transform</span></span>                                                                        |
| <span data-ttu-id="fb35c-193">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-193">Initial value:</span></span>   | <span data-ttu-id="fb35c-194">GL \_ MODELVIEW</span><span class="sxs-lookup"><span data-stu-id="fb35c-194">GL\_MODELVIEW</span></span>                                                                    |
| <span data-ttu-id="fb35c-195">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-195">Get command:</span></span>     | [<span data-ttu-id="fb35c-196">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="fb35c-196">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="fb35c-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL \_ NORMALIZE</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL\_NORMALIZE</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-198">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-198">Property</span></span> | <span data-ttu-id="fb35c-199">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-199">Value</span></span> |
|------------------|-------------------------------------|
| <span data-ttu-id="fb35c-200">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-200">Description:</span></span>     | <span data-ttu-id="fb35c-201">Normalización actual de encendido y apagado</span><span class="sxs-lookup"><span data-stu-id="fb35c-201">Current normal normalization on/off</span></span> |
| <span data-ttu-id="fb35c-202">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-202">Attribute group:</span></span> | <span data-ttu-id="fb35c-203">transform/enable</span><span class="sxs-lookup"><span data-stu-id="fb35c-203">transform/enable</span></span>                    |
| <span data-ttu-id="fb35c-204">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-204">Initial value:</span></span>   | <span data-ttu-id="fb35c-205">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="fb35c-205">GL\_FALSE</span></span>                           |
| <span data-ttu-id="fb35c-206">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-206">Get command:</span></span>     | [<span data-ttu-id="fb35c-207">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="fb35c-207">**glIsEnabled**</span></span>](glisenabled.md)  |



 

<span data-ttu-id="fb35c-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ CLIP \_ PLANE *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-209">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-209">Property</span></span> | <span data-ttu-id="fb35c-210">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-210">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="fb35c-211">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-211">Description:</span></span>     | <span data-ttu-id="fb35c-212">Coeficientes del plano de recorte de usuario</span><span class="sxs-lookup"><span data-stu-id="fb35c-212">User clipping plane coefficients</span></span>         |
| <span data-ttu-id="fb35c-213">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-213">Attribute group:</span></span> | <span data-ttu-id="fb35c-214">transform</span><span class="sxs-lookup"><span data-stu-id="fb35c-214">transform</span></span>                                |
| <span data-ttu-id="fb35c-215">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-215">Initial value:</span></span>   | <span data-ttu-id="fb35c-216">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="fb35c-216">0, 0, 0, 0</span></span>                               |
| <span data-ttu-id="fb35c-217">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-217">Get command:</span></span>     | [<span data-ttu-id="fb35c-218">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="fb35c-218">**glGetClipPlane**</span></span>](glgetclipplane.md) |



 

<span data-ttu-id="fb35c-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ CLIP \_ PLANE *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="fb35c-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="fb35c-220">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb35c-220">Property</span></span> | <span data-ttu-id="fb35c-221">Value</span><span class="sxs-lookup"><span data-stu-id="fb35c-221">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="fb35c-222">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fb35c-222">Description:</span></span>     | <span data-ttu-id="fb35c-223">*Plano de* recorte de usuario habilitado</span><span class="sxs-lookup"><span data-stu-id="fb35c-223">*i* th user clipping plane enabled</span></span> |
| <span data-ttu-id="fb35c-224">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fb35c-224">Attribute group:</span></span> | <span data-ttu-id="fb35c-225">transform/enable</span><span class="sxs-lookup"><span data-stu-id="fb35c-225">transform/enable</span></span>                   |
| <span data-ttu-id="fb35c-226">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fb35c-226">Initial value:</span></span>   | <span data-ttu-id="fb35c-227">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="fb35c-227">GL\_FALSE</span></span>                          |
| <span data-ttu-id="fb35c-228">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="fb35c-228">Get command:</span></span>     | [<span data-ttu-id="fb35c-229">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="fb35c-229">**glIsEnabled**</span></span>](glisenabled.md) |



 

</dd> </dl>

 

 




