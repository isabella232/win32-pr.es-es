---
title: Variables de estado de iluminación
description: Variables de estado de iluminación
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Variables de estado de iluminación OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7144e284b5be5abd5a6dc4e08fe2228b621465
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904101"
---
# <a name="lighting-state-variables"></a><span data-ttu-id="f8de3-104">Variables de estado de iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-104">Lighting State Variables</span></span>

<dl> <span data-ttu-id="f8de3-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>iluminación de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL\_LIGHTING</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-106">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-106">Description:</span></span>     | <span data-ttu-id="f8de3-107">True si está habilitada la iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-107">True if lighting is enabled</span></span>        |
| <span data-ttu-id="f8de3-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-108">Attribute group:</span></span> | <span data-ttu-id="f8de3-109">iluminación/habilitar</span><span class="sxs-lookup"><span data-stu-id="f8de3-109">lighting/enable</span></span>                    |
| <span data-ttu-id="f8de3-110">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-110">Initial value:</span></span>   | <span data-ttu-id="f8de3-111">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="f8de3-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f8de3-112">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-112">Get command:</span></span>     | [<span data-ttu-id="f8de3-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f8de3-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f8de3-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>\_material de color GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL\_COLOR\_MATERIAL</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-115">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-115">Description:</span></span>     | <span data-ttu-id="f8de3-116">True si está habilitado el seguimiento de color</span><span class="sxs-lookup"><span data-stu-id="f8de3-116">True if color tracking is enabled</span></span>  |
| <span data-ttu-id="f8de3-117">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-117">Attribute group:</span></span> | <span data-ttu-id="f8de3-118">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-118">lighting</span></span>                           |
| <span data-ttu-id="f8de3-119">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-119">Initial value:</span></span>   | <span data-ttu-id="f8de3-120">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="f8de3-120">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f8de3-121">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-121">Get command:</span></span>     | [<span data-ttu-id="f8de3-122">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f8de3-122">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f8de3-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>\_parámetro de \_ material de color GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL\_COLOR\_MATERIAL\_PARAMETER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f8de3-124">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-124">Description:</span></span>     | <span data-ttu-id="f8de3-125">Propiedades del material seguimiento del color actual</span><span class="sxs-lookup"><span data-stu-id="f8de3-125">Material properties tracking current color</span></span>                                       |
| <span data-ttu-id="f8de3-126">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-126">Attribute group:</span></span> | <span data-ttu-id="f8de3-127">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-127">lighting</span></span>                                                                         |
| <span data-ttu-id="f8de3-128">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-128">Initial value:</span></span>   | <span data-ttu-id="f8de3-129">\_ambiente de contabilidad general \_ y \_ difuso</span><span class="sxs-lookup"><span data-stu-id="f8de3-129">GL\_AMBIENT\_AND\_DIFFUSE</span></span>                                                        |
| <span data-ttu-id="f8de3-130">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-130">Get command:</span></span>     | [<span data-ttu-id="f8de3-131">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-131">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f8de3-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>\_superficie del \_ material de color de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL\_COLOR\_MATERIAL\_FACE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f8de3-133">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-133">Description:</span></span>     | <span data-ttu-id="f8de3-134">Caras afectadas por el seguimiento de color</span><span class="sxs-lookup"><span data-stu-id="f8de3-134">Faces affected by color tracking</span></span>                                                 |
| <span data-ttu-id="f8de3-135">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-135">Attribute group:</span></span> | <span data-ttu-id="f8de3-136">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-136">lighting</span></span>                                                                         |
| <span data-ttu-id="f8de3-137">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-137">Initial value:</span></span>   | <span data-ttu-id="f8de3-138">\_anverso \_ y \_ atrás de GL</span><span class="sxs-lookup"><span data-stu-id="f8de3-138">GL\_FRONT\_AND\_BACK</span></span>                                                             |
| <span data-ttu-id="f8de3-139">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-139">Get command:</span></span>     | [<span data-ttu-id="f8de3-140">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-140">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f8de3-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>ambiente de contabilidad general \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="f8de3-142">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-142">Description:</span></span>     | <span data-ttu-id="f8de3-143">Color de material ambiente</span><span class="sxs-lookup"><span data-stu-id="f8de3-143">Ambient material color</span></span>                   |
| <span data-ttu-id="f8de3-144">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-144">Attribute group:</span></span> | <span data-ttu-id="f8de3-145">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-145">lighting</span></span>                                 |
| <span data-ttu-id="f8de3-146">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-146">Initial value:</span></span>   | <span data-ttu-id="f8de3-147">(0,2, 0,2, 0,2, 1,0)</span><span class="sxs-lookup"><span data-stu-id="f8de3-147">(0.2,0.2,0.2,1.0)</span></span>                        |
| <span data-ttu-id="f8de3-148">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-148">Get command:</span></span>     | [<span data-ttu-id="f8de3-149">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-149">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="f8de3-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>difusión en contab. \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="f8de3-151">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-151">Description:</span></span>     | <span data-ttu-id="f8de3-152">Color de material difuso</span><span class="sxs-lookup"><span data-stu-id="f8de3-152">Diffuse material color</span></span>                   |
| <span data-ttu-id="f8de3-153">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-153">Attribute group:</span></span> | <span data-ttu-id="f8de3-154">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-154">lighting</span></span>                                 |
| <span data-ttu-id="f8de3-155">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-155">Initial value:</span></span>   | <span data-ttu-id="f8de3-156">(0,8, 0,8, 0,8, 1,0)</span><span class="sxs-lookup"><span data-stu-id="f8de3-156">(0.8,0.8,0.8,1.0)</span></span>                        |
| <span data-ttu-id="f8de3-157">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-157">Get command:</span></span>     | [<span data-ttu-id="f8de3-158">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-158">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="f8de3-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_especular GL</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="f8de3-160">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-160">Description:</span></span>     | <span data-ttu-id="f8de3-161">Color de material especular</span><span class="sxs-lookup"><span data-stu-id="f8de3-161">Specular material color</span></span>                  |
| <span data-ttu-id="f8de3-162">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-162">Attribute group:</span></span> | <span data-ttu-id="f8de3-163">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-163">lighting</span></span>                                 |
| <span data-ttu-id="f8de3-164">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-164">Initial value:</span></span>   | <span data-ttu-id="f8de3-165">(0,0, 0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="f8de3-165">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="f8de3-166">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-166">Get command:</span></span>     | [<span data-ttu-id="f8de3-167">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-167">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="f8de3-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>emisión de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL\_EMISSION</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="f8de3-169">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-169">Description:</span></span>     | <span data-ttu-id="f8de3-170">Color del material de emisor</span><span class="sxs-lookup"><span data-stu-id="f8de3-170">Emissive material color</span></span>                  |
| <span data-ttu-id="f8de3-171">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-171">Attribute group:</span></span> | <span data-ttu-id="f8de3-172">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-172">lighting</span></span>                                 |
| <span data-ttu-id="f8de3-173">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-173">Initial value:</span></span>   | <span data-ttu-id="f8de3-174">(0,0, 0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="f8de3-174">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="f8de3-175">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-175">Get command:</span></span>     | [<span data-ttu-id="f8de3-176">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-176">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="f8de3-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>brillo de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL\_SHININESS</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="f8de3-178">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-178">Description:</span></span>     | <span data-ttu-id="f8de3-179">Exponente especular de material</span><span class="sxs-lookup"><span data-stu-id="f8de3-179">Specular exponent of material</span></span>            |
| <span data-ttu-id="f8de3-180">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-180">Attribute group:</span></span> | <span data-ttu-id="f8de3-181">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-181">lighting</span></span>                                 |
| <span data-ttu-id="f8de3-182">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-182">Initial value:</span></span>   | <span data-ttu-id="f8de3-183">0,0</span><span class="sxs-lookup"><span data-stu-id="f8de3-183">0.0</span></span>                                      |
| <span data-ttu-id="f8de3-184">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-184">Get command:</span></span>     | [<span data-ttu-id="f8de3-185">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-185">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="f8de3-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>\_ambiente de \_ modelo de luz de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL\_LIGHT\_MODEL\_AMBIENT</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f8de3-187">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-187">Description:</span></span>     | <span data-ttu-id="f8de3-188">Color de la escena ambiente</span><span class="sxs-lookup"><span data-stu-id="f8de3-188">Ambient scene color</span></span>                                                            |
| <span data-ttu-id="f8de3-189">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-189">Attribute group:</span></span> | <span data-ttu-id="f8de3-190">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-190">lighting</span></span>                                                                       |
| <span data-ttu-id="f8de3-191">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-191">Initial value:</span></span>   | <span data-ttu-id="f8de3-192">(0,2, 0,2, 0,2, 1,0)</span><span class="sxs-lookup"><span data-stu-id="f8de3-192">(0.2,0.2,0.2,1.0)</span></span>                                                              |
| <span data-ttu-id="f8de3-193">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-193">Get command:</span></span>     | [<span data-ttu-id="f8de3-194">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-194">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f8de3-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ \_ visor local del modelo \_ de contabilidad solar</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f8de3-196">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-196">Description:</span></span>     | <span data-ttu-id="f8de3-197">El visor es local</span><span class="sxs-lookup"><span data-stu-id="f8de3-197">Viewer is local</span></span>                                                                  |
| <span data-ttu-id="f8de3-198">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-198">Attribute group:</span></span> | <span data-ttu-id="f8de3-199">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-199">lighting</span></span>                                                                         |
| <span data-ttu-id="f8de3-200">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-200">Initial value:</span></span>   | <span data-ttu-id="f8de3-201">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="f8de3-201">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="f8de3-202">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-202">Get command:</span></span>     | [<span data-ttu-id="f8de3-203">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-203">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f8de3-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>modelo de la luz de contabilidad \_ \_ \_ dos \_ lados</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL\_LIGHT\_MODEL\_TWO\_SIDE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f8de3-205">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-205">Description:</span></span>     | <span data-ttu-id="f8de3-206">Usar luz de dos caras</span><span class="sxs-lookup"><span data-stu-id="f8de3-206">Use two-sided lighting</span></span>                                                           |
| <span data-ttu-id="f8de3-207">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-207">Attribute group:</span></span> | <span data-ttu-id="f8de3-208">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-208">lighting</span></span>                                                                         |
| <span data-ttu-id="f8de3-209">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-209">Initial value:</span></span>   | <span data-ttu-id="f8de3-210">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="f8de3-210">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="f8de3-211">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-211">Get command:</span></span>     | [<span data-ttu-id="f8de3-212">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-212">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f8de3-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>ambiente de contabilidad general \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-214">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-214">Description:</span></span>     | <span data-ttu-id="f8de3-215">Intensidad ambiental de la *luz*</span><span class="sxs-lookup"><span data-stu-id="f8de3-215">Ambient intensity of light *i*</span></span>     |
| <span data-ttu-id="f8de3-216">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-216">Attribute group:</span></span> | <span data-ttu-id="f8de3-217">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-217">lighting</span></span>                           |
| <span data-ttu-id="f8de3-218">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-218">Initial value:</span></span>   | <span data-ttu-id="f8de3-219">(0,0, 0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="f8de3-219">(0.0,0.0,0.0,1.0)</span></span>                  |
| <span data-ttu-id="f8de3-220">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-220">Get command:</span></span>     | [<span data-ttu-id="f8de3-221">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-221">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="f8de3-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>difusión en contab. \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-223">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-223">Description:</span></span>     | <span data-ttu-id="f8de3-224">Intensidad de *la luz difusa*</span><span class="sxs-lookup"><span data-stu-id="f8de3-224">Diffuse intensity of light *i*</span></span>     |
| <span data-ttu-id="f8de3-225">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-225">Attribute group:</span></span> | <span data-ttu-id="f8de3-226">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-226">lighting</span></span>                           |
| <span data-ttu-id="f8de3-227">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-227">Initial value:</span></span>   |                                    |
| <span data-ttu-id="f8de3-228">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-228">Get command:</span></span>     | [<span data-ttu-id="f8de3-229">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-229">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="f8de3-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_especular GL</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-231">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-231">Description:</span></span>     | <span data-ttu-id="f8de3-232">Intensidad especular de *i*</span><span class="sxs-lookup"><span data-stu-id="f8de3-232">Specular intensity of light *i*</span></span>    |
| <span data-ttu-id="f8de3-233">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-233">Attribute group:</span></span> | <span data-ttu-id="f8de3-234">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-234">lighting</span></span>                           |
| <span data-ttu-id="f8de3-235">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-235">Initial value:</span></span>   |                                    |
| <span data-ttu-id="f8de3-236">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-236">Get command:</span></span>     | [<span data-ttu-id="f8de3-237">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-237">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="f8de3-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>posición de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL\_POSITION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-239">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-239">Description:</span></span>     | <span data-ttu-id="f8de3-240">Posición de la luz *i*</span><span class="sxs-lookup"><span data-stu-id="f8de3-240">Position of light *i*</span></span>              |
| <span data-ttu-id="f8de3-241">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-241">Attribute group:</span></span> | <span data-ttu-id="f8de3-242">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-242">lighting</span></span>                           |
| <span data-ttu-id="f8de3-243">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-243">Initial value:</span></span>   | <span data-ttu-id="f8de3-244">(0,0, 0,0, 1,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="f8de3-244">(0.0,0.0,1.0,0.0)</span></span>                  |
| <span data-ttu-id="f8de3-245">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-245">Get command:</span></span>     | [<span data-ttu-id="f8de3-246">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-246">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="f8de3-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>\_atenuación de constantes de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL\_CONSTANT\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-248">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-248">Description:</span></span>     | <span data-ttu-id="f8de3-249">Factor de atenuación constante</span><span class="sxs-lookup"><span data-stu-id="f8de3-249">Constant attenuation factor</span></span>        |
| <span data-ttu-id="f8de3-250">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-250">Attribute group:</span></span> | <span data-ttu-id="f8de3-251">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-251">lighting</span></span>                           |
| <span data-ttu-id="f8de3-252">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-252">Initial value:</span></span>   | <span data-ttu-id="f8de3-253">1,0</span><span class="sxs-lookup"><span data-stu-id="f8de3-253">1.0</span></span>                                |
| <span data-ttu-id="f8de3-254">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-254">Get command:</span></span>     | [<span data-ttu-id="f8de3-255">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-255">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="f8de3-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_atenuación lineal de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL\_LINEAR\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-257">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-257">Description:</span></span>     | <span data-ttu-id="f8de3-258">Factor de atenuación lineal</span><span class="sxs-lookup"><span data-stu-id="f8de3-258">Linear attenuation factor</span></span>          |
| <span data-ttu-id="f8de3-259">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-259">Attribute group:</span></span> | <span data-ttu-id="f8de3-260">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-260">lighting</span></span>                           |
| <span data-ttu-id="f8de3-261">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-261">Initial value:</span></span>   | <span data-ttu-id="f8de3-262">0,0</span><span class="sxs-lookup"><span data-stu-id="f8de3-262">0.0</span></span>                                |
| <span data-ttu-id="f8de3-263">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-263">Get command:</span></span>     | [<span data-ttu-id="f8de3-264">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-264">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="f8de3-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>\_atenuación cuadrática de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL\_QUADRATIC\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-266">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-266">Description:</span></span>     | <span data-ttu-id="f8de3-267">Factor de atenuación cuadrático</span><span class="sxs-lookup"><span data-stu-id="f8de3-267">Quadratic attenuation factor</span></span>       |
| <span data-ttu-id="f8de3-268">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-268">Attribute group:</span></span> | <span data-ttu-id="f8de3-269">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-269">lighting</span></span>                           |
| <span data-ttu-id="f8de3-270">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-270">Initial value:</span></span>   | <span data-ttu-id="f8de3-271">0,0</span><span class="sxs-lookup"><span data-stu-id="f8de3-271">0.0</span></span>                                |
| <span data-ttu-id="f8de3-272">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-272">Get command:</span></span>     | [<span data-ttu-id="f8de3-273">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-273">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="f8de3-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>Dirección de la zona de contabilidad \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL\_SPOT\_DIRECTION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-275">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-275">Description:</span></span>     | <span data-ttu-id="f8de3-276">Dirección de Spotlight de *la luz*</span><span class="sxs-lookup"><span data-stu-id="f8de3-276">Spotlight direction of light *i*</span></span>   |
| <span data-ttu-id="f8de3-277">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-277">Attribute group:</span></span> | <span data-ttu-id="f8de3-278">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-278">lighting</span></span>                           |
| <span data-ttu-id="f8de3-279">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-279">Initial value:</span></span>   | <span data-ttu-id="f8de3-280">(0,0, 0.0,-1,0)</span><span class="sxs-lookup"><span data-stu-id="f8de3-280">(0.0,0.0,-1.0)</span></span>                     |
| <span data-ttu-id="f8de3-281">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-281">Get command:</span></span>     | [<span data-ttu-id="f8de3-282">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-282">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="f8de3-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>exponente de la zona de contabilidad \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL\_SPOT\_EXPONENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-284">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-284">Description:</span></span>     | <span data-ttu-id="f8de3-285">Exponente destacado de la luz *i*</span><span class="sxs-lookup"><span data-stu-id="f8de3-285">Spotlight exponent of light *i*</span></span>    |
| <span data-ttu-id="f8de3-286">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-286">Attribute group:</span></span> | <span data-ttu-id="f8de3-287">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-287">lighting</span></span>                           |
| <span data-ttu-id="f8de3-288">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-288">Initial value:</span></span>   | <span data-ttu-id="f8de3-289">0,0</span><span class="sxs-lookup"><span data-stu-id="f8de3-289">0.0</span></span>                                |
| <span data-ttu-id="f8de3-290">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-290">Get command:</span></span>     | [<span data-ttu-id="f8de3-291">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-291">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="f8de3-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>límite de la zona de contabilidad \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL\_SPOT\_CUTOFF</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-293">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-293">Description:</span></span>     | <span data-ttu-id="f8de3-294">Ángulo destacado de la *luz*</span><span class="sxs-lookup"><span data-stu-id="f8de3-294">Spotlight angle of light *i*</span></span>       |
| <span data-ttu-id="f8de3-295">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-295">Attribute group:</span></span> | <span data-ttu-id="f8de3-296">iluminación</span><span class="sxs-lookup"><span data-stu-id="f8de3-296">lighting</span></span>                           |
| <span data-ttu-id="f8de3-297">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-297">Initial value:</span></span>   | <span data-ttu-id="f8de3-298">180,0</span><span class="sxs-lookup"><span data-stu-id="f8de3-298">180.0</span></span>                              |
| <span data-ttu-id="f8de3-299">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-299">Get command:</span></span>     | [<span data-ttu-id="f8de3-300">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-300">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="f8de3-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ claro *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL\_LIGHT *i*</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f8de3-302">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-302">Description:</span></span>     | <span data-ttu-id="f8de3-303">True *si está* habilitada la luz</span><span class="sxs-lookup"><span data-stu-id="f8de3-303">True if light *i* enabled</span></span>          |
| <span data-ttu-id="f8de3-304">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-304">Attribute group:</span></span> | <span data-ttu-id="f8de3-305">iluminación/habilitar</span><span class="sxs-lookup"><span data-stu-id="f8de3-305">lighting/enable</span></span>                    |
| <span data-ttu-id="f8de3-306">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-306">Initial value:</span></span>   | <span data-ttu-id="f8de3-307">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="f8de3-307">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f8de3-308">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-308">Get command:</span></span>     | [<span data-ttu-id="f8de3-309">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f8de3-309">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f8de3-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>\_índices de color de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f8de3-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL\_COLOR\_INDEXES</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f8de3-311">Descripción:</span><span class="sxs-lookup"><span data-stu-id="f8de3-311">Description:</span></span>     | <span data-ttu-id="f8de3-312">*C (a)*, *c (d)* y *c (s)* para la iluminación de índice de color</span><span class="sxs-lookup"><span data-stu-id="f8de3-312">*C (a)*, *C (d)*, and *C (s)* for color-index lighting</span></span>                         |
| <span data-ttu-id="f8de3-313">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="f8de3-313">Attribute group:</span></span> | <span data-ttu-id="f8de3-314">iluminación/habilitar</span><span class="sxs-lookup"><span data-stu-id="f8de3-314">lighting/enable</span></span>                                                                |
| <span data-ttu-id="f8de3-315">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="f8de3-315">Initial value:</span></span>   | <span data-ttu-id="f8de3-316">0, 1, 1</span><span class="sxs-lookup"><span data-stu-id="f8de3-316">0,1,1</span></span>                                                                          |
| <span data-ttu-id="f8de3-317">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="f8de3-317">Get command:</span></span>     | [<span data-ttu-id="f8de3-318">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="f8de3-318">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




