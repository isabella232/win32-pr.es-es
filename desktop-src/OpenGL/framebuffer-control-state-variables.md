---
title: Variables de estado del control fotogramas
description: Variables de estado del control fotogramas
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Variables de estado del control fotogramas OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103903938"
---
# <a name="framebuffer-control-state-variables"></a><span data-ttu-id="0144c-104">Variables de estado del control fotogramas</span><span class="sxs-lookup"><span data-stu-id="0144c-104">Framebuffer Control State Variables</span></span>

<dl> <span data-ttu-id="0144c-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_búfer de dibujo de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0144c-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL\_DRAW\_BUFFER</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="0144c-106">Descripción:</span><span class="sxs-lookup"><span data-stu-id="0144c-106">Description:</span></span>     | <span data-ttu-id="0144c-107">Búferes seleccionados para dibujar</span><span class="sxs-lookup"><span data-stu-id="0144c-107">Buffers selected for drawing</span></span>           |
| <span data-ttu-id="0144c-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="0144c-108">Attribute group:</span></span> | <span data-ttu-id="0144c-109">búfer de color</span><span class="sxs-lookup"><span data-stu-id="0144c-109">color-buffer</span></span>                           |
| <span data-ttu-id="0144c-110">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="0144c-110">Initial value:</span></span>   |                                        |
| <span data-ttu-id="0144c-111">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="0144c-111">Get command:</span></span>     | [<span data-ttu-id="0144c-112">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0144c-112">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="0144c-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL \_ index \_ WRITEMASK</dt> </span><span class="sxs-lookup"><span data-stu-id="0144c-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL\_INDEX\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0144c-114">Descripción:</span><span class="sxs-lookup"><span data-stu-id="0144c-114">Description:</span></span>     | <span data-ttu-id="0144c-115">Writemask de índice de color</span><span class="sxs-lookup"><span data-stu-id="0144c-115">Color-index writemask</span></span>                                                            |
| <span data-ttu-id="0144c-116">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="0144c-116">Attribute group:</span></span> | <span data-ttu-id="0144c-117">búfer de color</span><span class="sxs-lookup"><span data-stu-id="0144c-117">color-buffer</span></span>                                                                     |
| <span data-ttu-id="0144c-118">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="0144c-118">Initial value:</span></span>   | <span data-ttu-id="0144c-119">1</span><span class="sxs-lookup"><span data-stu-id="0144c-119">1's</span></span>                                                                              |
| <span data-ttu-id="0144c-120">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="0144c-120">Get command:</span></span>     | [<span data-ttu-id="0144c-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0144c-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0144c-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK de color de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0144c-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL\_COLOR\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0144c-123">Descripción:</span><span class="sxs-lookup"><span data-stu-id="0144c-123">Description:</span></span>     | <span data-ttu-id="0144c-124">La escritura en color habilita; R, G, B o A</span><span class="sxs-lookup"><span data-stu-id="0144c-124">Color write enables; R, G, B, or A</span></span>                                               |
| <span data-ttu-id="0144c-125">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="0144c-125">Attribute group:</span></span> | <span data-ttu-id="0144c-126">búfer de color</span><span class="sxs-lookup"><span data-stu-id="0144c-126">color-buffer</span></span>                                                                     |
| <span data-ttu-id="0144c-127">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="0144c-127">Initial value:</span></span>   | <span data-ttu-id="0144c-128">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="0144c-128">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="0144c-129">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="0144c-129">Get command:</span></span>     | [<span data-ttu-id="0144c-130">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="0144c-130">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0144c-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>profundidad de GL \_ \_ WRITEMASK</dt> </span><span class="sxs-lookup"><span data-stu-id="0144c-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL\_DEPTH\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0144c-132">Descripción:</span><span class="sxs-lookup"><span data-stu-id="0144c-132">Description:</span></span>     | <span data-ttu-id="0144c-133">Búfer de profundidad habilitado para escritura</span><span class="sxs-lookup"><span data-stu-id="0144c-133">Depth buffer enabled for writing</span></span>                                                 |
| <span data-ttu-id="0144c-134">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="0144c-134">Attribute group:</span></span> | <span data-ttu-id="0144c-135">búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="0144c-135">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="0144c-136">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="0144c-136">Initial value:</span></span>   | <span data-ttu-id="0144c-137">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="0144c-137">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="0144c-138">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="0144c-138">Get command:</span></span>     | [<span data-ttu-id="0144c-139">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="0144c-139">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0144c-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_Galería de símbolos GL \_ WRITEMASK</dt> </span><span class="sxs-lookup"><span data-stu-id="0144c-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL\_STENCIL\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0144c-141">Descripción:</span><span class="sxs-lookup"><span data-stu-id="0144c-141">Description:</span></span>     | <span data-ttu-id="0144c-142">Cliché-búfer writemask</span><span class="sxs-lookup"><span data-stu-id="0144c-142">Stencil-buffer writemask</span></span>                                                         |
| <span data-ttu-id="0144c-143">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="0144c-143">Attribute group:</span></span> | <span data-ttu-id="0144c-144">cliché-búfer</span><span class="sxs-lookup"><span data-stu-id="0144c-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="0144c-145">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="0144c-145">Initial value:</span></span>   | <span data-ttu-id="0144c-146">1</span><span class="sxs-lookup"><span data-stu-id="0144c-146">1's</span></span>                                                                              |
| <span data-ttu-id="0144c-147">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="0144c-147">Get command:</span></span>     | [<span data-ttu-id="0144c-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0144c-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0144c-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_ \_ valor sin formato de color de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0144c-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL\_COLOR\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0144c-150">Descripción:</span><span class="sxs-lookup"><span data-stu-id="0144c-150">Description:</span></span>     | <span data-ttu-id="0144c-151">Valor sin formato del búfer de color (modo RGBA)</span><span class="sxs-lookup"><span data-stu-id="0144c-151">Color-buffer clear value (RGBA mode)</span></span>                                           |
| <span data-ttu-id="0144c-152">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="0144c-152">Attribute group:</span></span> | <span data-ttu-id="0144c-153">búfer de color</span><span class="sxs-lookup"><span data-stu-id="0144c-153">color-buffer</span></span>                                                                   |
| <span data-ttu-id="0144c-154">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="0144c-154">Initial value:</span></span>   | <span data-ttu-id="0144c-155">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="0144c-155">0, 0, 0, 0</span></span>                                                                     |
| <span data-ttu-id="0144c-156">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="0144c-156">Get command:</span></span>     | [<span data-ttu-id="0144c-157">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="0144c-157">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0144c-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_ \_ valor sin formato de índice de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0144c-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL\_INDEX\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0144c-159">Descripción:</span><span class="sxs-lookup"><span data-stu-id="0144c-159">Description:</span></span>     | <span data-ttu-id="0144c-160">Valor sin formato de búfer de color (modo de índice de color)</span><span class="sxs-lookup"><span data-stu-id="0144c-160">Color-buffer clear value (color-index mode)</span></span>                                    |
| <span data-ttu-id="0144c-161">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="0144c-161">Attribute group:</span></span> | <span data-ttu-id="0144c-162">búfer de color</span><span class="sxs-lookup"><span data-stu-id="0144c-162">color-buffer</span></span>                                                                   |
| <span data-ttu-id="0144c-163">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="0144c-163">Initial value:</span></span>   | <span data-ttu-id="0144c-164">0</span><span class="sxs-lookup"><span data-stu-id="0144c-164">0</span></span>                                                                              |
| <span data-ttu-id="0144c-165">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="0144c-165">Get command:</span></span>     | [<span data-ttu-id="0144c-166">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="0144c-166">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0144c-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_ \_ valor sin formato de profundidad de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0144c-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL\_DEPTH\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0144c-168">Descripción:</span><span class="sxs-lookup"><span data-stu-id="0144c-168">Description:</span></span>     | <span data-ttu-id="0144c-169">Valor sin formato de búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="0144c-169">Depth-buffer clear value</span></span>                                                         |
| <span data-ttu-id="0144c-170">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="0144c-170">Attribute group:</span></span> | <span data-ttu-id="0144c-171">búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="0144c-171">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="0144c-172">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="0144c-172">Initial value:</span></span>   | <span data-ttu-id="0144c-173">1</span><span class="sxs-lookup"><span data-stu-id="0144c-173">1</span></span>                                                                                |
| <span data-ttu-id="0144c-174">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="0144c-174">Get command:</span></span>     | [<span data-ttu-id="0144c-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0144c-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0144c-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_ \_ valor sin formato de estarcido GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0144c-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL\_STENCIL\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0144c-177">Descripción:</span><span class="sxs-lookup"><span data-stu-id="0144c-177">Description:</span></span>     | <span data-ttu-id="0144c-178">Estarcido: valor sin formato del búfer</span><span class="sxs-lookup"><span data-stu-id="0144c-178">Stencil-buffer clear value</span></span>                                                       |
| <span data-ttu-id="0144c-179">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="0144c-179">Attribute group:</span></span> | <span data-ttu-id="0144c-180">cliché-búfer</span><span class="sxs-lookup"><span data-stu-id="0144c-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="0144c-181">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="0144c-181">Initial value:</span></span>   | <span data-ttu-id="0144c-182">0</span><span class="sxs-lookup"><span data-stu-id="0144c-182">0</span></span>                                                                                |
| <span data-ttu-id="0144c-183">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="0144c-183">Get command:</span></span>     | [<span data-ttu-id="0144c-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0144c-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0144c-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>\_valor no \_ cifrado de GL acumulado \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0144c-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL\_ACCUM\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0144c-186">Descripción:</span><span class="sxs-lookup"><span data-stu-id="0144c-186">Description:</span></span>     | <span data-ttu-id="0144c-187">Acumulación: valor sin formato del búfer</span><span class="sxs-lookup"><span data-stu-id="0144c-187">Accumulation-buffer clear value</span></span>                                                |
| <span data-ttu-id="0144c-188">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="0144c-188">Attribute group:</span></span> | <span data-ttu-id="0144c-189">búfer acumulado</span><span class="sxs-lookup"><span data-stu-id="0144c-189">accum-buffer</span></span>                                                                   |
| <span data-ttu-id="0144c-190">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="0144c-190">Initial value:</span></span>   | <span data-ttu-id="0144c-191">0</span><span class="sxs-lookup"><span data-stu-id="0144c-191">0</span></span>                                                                              |
| <span data-ttu-id="0144c-192">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="0144c-192">Get command:</span></span>     | [<span data-ttu-id="0144c-193">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="0144c-193">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




