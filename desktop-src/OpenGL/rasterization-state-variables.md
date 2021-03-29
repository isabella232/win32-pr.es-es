---
title: Variables de estado de rasterización
description: Variables de estado de rasterización
ms.assetid: 57ce3dc0-3983-449a-bbe1-153232727ff8
keywords:
- Variables de estado de rasterización OpenGL
topic_type:
- apiref
api_name:
- Rasterization State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1667c530ea1db8c9e463be0edad5de98e8b107
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784036"
---
# <a name="rasterization-state-variables"></a><span data-ttu-id="bd8b4-104">Variables de estado de rasterización</span><span class="sxs-lookup"><span data-stu-id="bd8b4-104">Rasterization State Variables</span></span>

<dl> <span data-ttu-id="bd8b4-105"><dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>tamaño de los puntos de contabilidad \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-105"><dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>GL\_POINT\_SIZE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="bd8b4-106">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-106">Description:</span></span>     | <span data-ttu-id="bd8b4-107">Tamaño del punto</span><span class="sxs-lookup"><span data-stu-id="bd8b4-107">Point size</span></span>                         |
| <span data-ttu-id="bd8b4-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-108">Attribute group:</span></span> | <span data-ttu-id="bd8b4-109">point</span><span class="sxs-lookup"><span data-stu-id="bd8b4-109">point</span></span>                              |
| <span data-ttu-id="bd8b4-110">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-110">Initial value:</span></span>   | <span data-ttu-id="bd8b4-111">1,0</span><span class="sxs-lookup"><span data-stu-id="bd8b4-111">1.0</span></span>                                |
| <span data-ttu-id="bd8b4-112">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-112">Get command:</span></span>     | [<span data-ttu-id="bd8b4-113">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-113">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="bd8b4-114"></dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>\_suavidad de punto de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-114"></dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>GL\_POINT\_SMOOTH</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="bd8b4-115">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-115">Description:</span></span>     | <span data-ttu-id="bd8b4-116">Alias de punto activado</span><span class="sxs-lookup"><span data-stu-id="bd8b4-116">Point aliasing on</span></span>                  |
| <span data-ttu-id="bd8b4-117">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-117">Attribute group:</span></span> | <span data-ttu-id="bd8b4-118">señalar/habilitar</span><span class="sxs-lookup"><span data-stu-id="bd8b4-118">point/enable</span></span>                       |
| <span data-ttu-id="bd8b4-119">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-119">Initial value:</span></span>   | <span data-ttu-id="bd8b4-120">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="bd8b4-120">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bd8b4-121">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-121">Get command:</span></span>     | [<span data-ttu-id="bd8b4-122">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-122">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bd8b4-123"></dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>\_ancho de línea de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-123"></dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>GL\_LINE\_WIDTH</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="bd8b4-124">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-124">Description:</span></span>     | <span data-ttu-id="bd8b4-125">Ancho de línea</span><span class="sxs-lookup"><span data-stu-id="bd8b4-125">Line width</span></span>                                                                     |
| <span data-ttu-id="bd8b4-126">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-126">Attribute group:</span></span> | <span data-ttu-id="bd8b4-127">line</span><span class="sxs-lookup"><span data-stu-id="bd8b4-127">line</span></span>                                                                           |
| <span data-ttu-id="bd8b4-128">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-128">Initial value:</span></span>   | <span data-ttu-id="bd8b4-129">1,0</span><span class="sxs-lookup"><span data-stu-id="bd8b4-129">1.0</span></span>                                                                            |
| <span data-ttu-id="bd8b4-130">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-130">Get command:</span></span>     | [<span data-ttu-id="bd8b4-131">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-131">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bd8b4-132"></dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>\_suavizado de línea de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-132"></dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>GL\_LINE\_SMOOTH</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="bd8b4-133">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-133">Description:</span></span>     | <span data-ttu-id="bd8b4-134">Suavizado de línea en</span><span class="sxs-lookup"><span data-stu-id="bd8b4-134">Line antialiasing on</span></span>               |
| <span data-ttu-id="bd8b4-135">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-135">Attribute group:</span></span> | <span data-ttu-id="bd8b4-136">línea/habilitar</span><span class="sxs-lookup"><span data-stu-id="bd8b4-136">line/enable</span></span>                        |
| <span data-ttu-id="bd8b4-137">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-137">Initial value:</span></span>   | <span data-ttu-id="bd8b4-138">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="bd8b4-138">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bd8b4-139">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-139">Get command:</span></span>     | [<span data-ttu-id="bd8b4-140">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-140">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bd8b4-141"></dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>\_ \_ patrón punteado de línea de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-141"></dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>GL\_LINE\_STIPPLE\_PATTERN</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bd8b4-142">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-142">Description:</span></span>     | <span data-ttu-id="bd8b4-143">Línea punteada</span><span class="sxs-lookup"><span data-stu-id="bd8b4-143">Line stipple</span></span>                                                                     |
| <span data-ttu-id="bd8b4-144">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-144">Attribute group:</span></span> | <span data-ttu-id="bd8b4-145">line</span><span class="sxs-lookup"><span data-stu-id="bd8b4-145">line</span></span>                                                                             |
| <span data-ttu-id="bd8b4-146">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-146">Initial value:</span></span>   | <span data-ttu-id="bd8b4-147">1</span><span class="sxs-lookup"><span data-stu-id="bd8b4-147">1's</span></span>                                                                              |
| <span data-ttu-id="bd8b4-148">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-148">Get command:</span></span>     | [<span data-ttu-id="bd8b4-149">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-149">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bd8b4-150"></dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>\_ \_ repetición punteada de línea de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-150"></dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>GL\_LINE\_STIPPLE\_REPEAT</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bd8b4-151">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-151">Description:</span></span>     | <span data-ttu-id="bd8b4-152">Repetición punteada de línea</span><span class="sxs-lookup"><span data-stu-id="bd8b4-152">Line stipple repeat</span></span>                                                              |
| <span data-ttu-id="bd8b4-153">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-153">Attribute group:</span></span> | <span data-ttu-id="bd8b4-154">line</span><span class="sxs-lookup"><span data-stu-id="bd8b4-154">line</span></span>                                                                             |
| <span data-ttu-id="bd8b4-155">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-155">Initial value:</span></span>   | <span data-ttu-id="bd8b4-156">1</span><span class="sxs-lookup"><span data-stu-id="bd8b4-156">1</span></span>                                                                                |
| <span data-ttu-id="bd8b4-157">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-157">Get command:</span></span>     | [<span data-ttu-id="bd8b4-158">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-158">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bd8b4-159"></dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>línea de contabilidad \_ \_ punteada</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-159"></dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>GL\_LINE\_STIPPLE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="bd8b4-160">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-160">Description:</span></span>     | <span data-ttu-id="bd8b4-161">Habilitar línea punteada</span><span class="sxs-lookup"><span data-stu-id="bd8b4-161">Line stipple enable</span></span>                |
| <span data-ttu-id="bd8b4-162">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-162">Attribute group:</span></span> | <span data-ttu-id="bd8b4-163">línea/habilitar</span><span class="sxs-lookup"><span data-stu-id="bd8b4-163">line/enable</span></span>                        |
| <span data-ttu-id="bd8b4-164">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-164">Initial value:</span></span>   | <span data-ttu-id="bd8b4-165">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="bd8b4-165">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bd8b4-166">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-166">Get command:</span></span>     | [<span data-ttu-id="bd8b4-167">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-167">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bd8b4-168"></dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>\_cara de selección de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-168"></dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>GL\_CULL\_FACE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="bd8b4-169">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-169">Description:</span></span>     | <span data-ttu-id="bd8b4-170">Selección de polígonos habilitada</span><span class="sxs-lookup"><span data-stu-id="bd8b4-170">Polygon culling enabled</span></span>            |
| <span data-ttu-id="bd8b4-171">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-171">Attribute group:</span></span> | <span data-ttu-id="bd8b4-172">Polígono/habilitar</span><span class="sxs-lookup"><span data-stu-id="bd8b4-172">polygon/enable</span></span>                     |
| <span data-ttu-id="bd8b4-173">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-173">Initial value:</span></span>   | <span data-ttu-id="bd8b4-174">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="bd8b4-174">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bd8b4-175">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-175">Get command:</span></span>     | [<span data-ttu-id="bd8b4-176">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-176">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bd8b4-177"></dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>\_modo de \_ cara de selección de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-177"></dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>GL\_CULL\_FACE\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bd8b4-178">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-178">Description:</span></span>     | <span data-ttu-id="bd8b4-179">Desactivación de polígonos hacia delante o hacia atrás</span><span class="sxs-lookup"><span data-stu-id="bd8b4-179">Cull front-facing/back-facing polygons</span></span>                                           |
| <span data-ttu-id="bd8b4-180">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-180">Attribute group:</span></span> | <span data-ttu-id="bd8b4-181">polygon</span><span class="sxs-lookup"><span data-stu-id="bd8b4-181">polygon</span></span>                                                                          |
| <span data-ttu-id="bd8b4-182">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-182">Initial value:</span></span>   | <span data-ttu-id="bd8b4-183">libro \_ de contabilidad</span><span class="sxs-lookup"><span data-stu-id="bd8b4-183">GL\_BACK</span></span>                                                                         |
| <span data-ttu-id="bd8b4-184">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-184">Get command:</span></span>     | [<span data-ttu-id="bd8b4-185">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-185">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bd8b4-186"></dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>\_cara frontal de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-186"></dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>GL\_FRONT\_FACE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bd8b4-187">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-187">Description:</span></span>     | <span data-ttu-id="bd8b4-188">Indicador de la cara frontal CW/CCW</span><span class="sxs-lookup"><span data-stu-id="bd8b4-188">Polygon front-face CW/CCW indicator</span></span>                                              |
| <span data-ttu-id="bd8b4-189">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-189">Attribute group:</span></span> | <span data-ttu-id="bd8b4-190">polygon</span><span class="sxs-lookup"><span data-stu-id="bd8b4-190">polygon</span></span>                                                                          |
| <span data-ttu-id="bd8b4-191">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-191">Initial value:</span></span>   | <span data-ttu-id="bd8b4-192">CCW de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="bd8b4-192">GL\_CCW</span></span>                                                                          |
| <span data-ttu-id="bd8b4-193">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-193">Get command:</span></span>     | [<span data-ttu-id="bd8b4-194">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-194">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bd8b4-195"></dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>retorno de polígono de GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-195"></dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>GL\_POLYGON\_SMOOTH</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="bd8b4-196">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-196">Description:</span></span>     | <span data-ttu-id="bd8b4-197">Suavizado de contorno de polígono activado</span><span class="sxs-lookup"><span data-stu-id="bd8b4-197">Polygon antialiasing on</span></span>            |
| <span data-ttu-id="bd8b4-198">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-198">Attribute group:</span></span> | <span data-ttu-id="bd8b4-199">Polígono/habilitar</span><span class="sxs-lookup"><span data-stu-id="bd8b4-199">polygon/enable</span></span>                     |
| <span data-ttu-id="bd8b4-200">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-200">Initial value:</span></span>   | <span data-ttu-id="bd8b4-201">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="bd8b4-201">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bd8b4-202">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-202">Get command:</span></span>     | [<span data-ttu-id="bd8b4-203">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-203">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="bd8b4-204"></dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>\_modo de polígono de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-204"></dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>GL\_POLYGON\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bd8b4-205">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-205">Description:</span></span>     | <span data-ttu-id="bd8b4-206">Modo de rasterización de Polígono (anverso y trasero)</span><span class="sxs-lookup"><span data-stu-id="bd8b4-206">Polygon rasterization mode (front and back)</span></span>                                      |
| <span data-ttu-id="bd8b4-207">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-207">Attribute group:</span></span> | <span data-ttu-id="bd8b4-208">polygon</span><span class="sxs-lookup"><span data-stu-id="bd8b4-208">polygon</span></span>                                                                          |
| <span data-ttu-id="bd8b4-209">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-209">Initial value:</span></span>   | <span data-ttu-id="bd8b4-210">relleno de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="bd8b4-210">GL\_FILL</span></span>                                                                         |
| <span data-ttu-id="bd8b4-211">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-211">Get command:</span></span>     | [<span data-ttu-id="bd8b4-212">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-212">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="bd8b4-213"></dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>punteado de cont. \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="bd8b4-213"></dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>GL\_POLYGON\_STIPPLE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="bd8b4-214">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-214">Description:</span></span>     | <span data-ttu-id="bd8b4-215">Habilitar polígono punteado</span><span class="sxs-lookup"><span data-stu-id="bd8b4-215">Polygon stipple enable</span></span>             |
| <span data-ttu-id="bd8b4-216">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-216">Attribute group:</span></span> | <span data-ttu-id="bd8b4-217">Polígono/habilitar</span><span class="sxs-lookup"><span data-stu-id="bd8b4-217">polygon/enable</span></span>                     |
| <span data-ttu-id="bd8b4-218">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-218">Initial value:</span></span>   | <span data-ttu-id="bd8b4-219">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="bd8b4-219">GL\_FALSE</span></span>                          |
| <span data-ttu-id="bd8b4-220">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-220">Get command:</span></span>     | [<span data-ttu-id="bd8b4-221">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-221">**glIsEnabled**</span></span>](glisenabled.md) |



 



|                  |                                                    |
|------------------|----------------------------------------------------|
| <span data-ttu-id="bd8b4-222">Descripción:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-222">Description:</span></span>     | <span data-ttu-id="bd8b4-223">Patrón punteado de polígono</span><span class="sxs-lookup"><span data-stu-id="bd8b4-223">Polygon stipple pattern</span></span>                            |
| <span data-ttu-id="bd8b4-224">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-224">Attribute group:</span></span> | <span data-ttu-id="bd8b4-225">Polígono-punteado</span><span class="sxs-lookup"><span data-stu-id="bd8b4-225">polygon-stipple</span></span>                                    |
| <span data-ttu-id="bd8b4-226">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-226">Initial value:</span></span>   | <span data-ttu-id="bd8b4-227">1</span><span class="sxs-lookup"><span data-stu-id="bd8b4-227">1's</span></span>                                                |
| <span data-ttu-id="bd8b4-228">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="bd8b4-228">Get command:</span></span>     | [<span data-ttu-id="bd8b4-229">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="bd8b4-229">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




