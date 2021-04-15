---
title: Variables de estado de texturización
description: Variables de estado de texturización
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Variables de estado de texturización OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a9894e9f3723cca957fdeeb2882ede8f689ee7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105665757"
---
# <a name="texturing-state-variables"></a><span data-ttu-id="fc335-104">Variables de estado de texturización</span><span class="sxs-lookup"><span data-stu-id="fc335-104">Texturing State Variables</span></span>

<dl> <span data-ttu-id="fc335-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>\_Textura GL \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL\_TEXTURE\_*x*</dt> </span></span><dd> 

|                  |                                                       |
|------------------|-------------------------------------------------------|
| <span data-ttu-id="fc335-106">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-106">Description:</span></span>     | <span data-ttu-id="fc335-107">True si está   habilitada la texturización x-d (*x* es 1-d o 2-d)</span><span class="sxs-lookup"><span data-stu-id="fc335-107">True if *x* - D texturing enabled (*x* is 1-D or 2-D)</span></span> |
| <span data-ttu-id="fc335-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-108">Attribute group:</span></span> | <span data-ttu-id="fc335-109">textura/habilitar</span><span class="sxs-lookup"><span data-stu-id="fc335-109">texture/enable</span></span>                                        |
| <span data-ttu-id="fc335-110">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-110">Initial value:</span></span>   | <span data-ttu-id="fc335-111">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="fc335-111">GL\_FALSE</span></span>                                             |
| <span data-ttu-id="fc335-112">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-112">Get command:</span></span>     | [<span data-ttu-id="fc335-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="fc335-113">**glIsEnabled**</span></span>](glisenabled.md)                    |



 

<span data-ttu-id="fc335-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>\_textura GL</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL\_TEXTURE</dt> </span></span><dd> 

|                  |                                              |
|------------------|----------------------------------------------|
| <span data-ttu-id="fc335-115">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-115">Description:</span></span>     | <span data-ttu-id="fc335-116">*x*   -D imagen de textura en el nivel de detalle *i*</span><span class="sxs-lookup"><span data-stu-id="fc335-116">*x* - D texture image at level of detail *i*</span></span> |
| <span data-ttu-id="fc335-117">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-117">Attribute group:</span></span> |                                              |
| <span data-ttu-id="fc335-118">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-118">Initial value:</span></span>   |                                              |
| <span data-ttu-id="fc335-119">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-119">Get command:</span></span>     | [<span data-ttu-id="fc335-120">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="fc335-120">**glGetTexImage**</span></span>](glgetteximage.md)       |



 

<span data-ttu-id="fc335-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>\_ancho de textura de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL\_TEXTURE\_WIDTH</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="fc335-122">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-122">Description:</span></span>     | <span data-ttu-id="fc335-123">*x*   -D *textura imagen*   de ancho</span><span class="sxs-lookup"><span data-stu-id="fc335-123">*x* - D texture image *i* 's width</span></span>                       |
| <span data-ttu-id="fc335-124">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-124">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="fc335-125">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-125">Initial value:</span></span>   | <span data-ttu-id="fc335-126">0</span><span class="sxs-lookup"><span data-stu-id="fc335-126">0</span></span>                                                        |
| <span data-ttu-id="fc335-127">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-127">Get command:</span></span>     | [<span data-ttu-id="fc335-128">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="fc335-128">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="fc335-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>\_alto de textura de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL\_TEXTURE\_HEIGHT</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="fc335-130">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-130">Description:</span></span>     | <span data-ttu-id="fc335-131">*x*   Alto de la imagen *de* textura-D  </span><span class="sxs-lookup"><span data-stu-id="fc335-131">*x* - D texture image *i* 's height</span></span>                      |
| <span data-ttu-id="fc335-132">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-132">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="fc335-133">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-133">Initial value:</span></span>   | <span data-ttu-id="fc335-134">0</span><span class="sxs-lookup"><span data-stu-id="fc335-134">0</span></span>                                                        |
| <span data-ttu-id="fc335-135">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-135">Get command:</span></span>     | [<span data-ttu-id="fc335-136">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="fc335-136">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="fc335-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>\_borde de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL\_TEXTURE\_BORDER</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="fc335-138">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-138">Description:</span></span>     | <span data-ttu-id="fc335-139">*x*   -D textura imagen *i*  </span><span class="sxs-lookup"><span data-stu-id="fc335-139">*x* - D texture image *i* 's border</span></span>                      |
| <span data-ttu-id="fc335-140">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-140">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="fc335-141">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-141">Initial value:</span></span>   | <span data-ttu-id="fc335-142">0</span><span class="sxs-lookup"><span data-stu-id="fc335-142">0</span></span>                                                        |
| <span data-ttu-id="fc335-143">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-143">Get command:</span></span>     | [<span data-ttu-id="fc335-144">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="fc335-144">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="fc335-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_componentes de textura de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL\_TEXTURE\_COMPONENTS</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="fc335-146">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-146">Description:</span></span>     | <span data-ttu-id="fc335-147">Componentes de imagen de textura</span><span class="sxs-lookup"><span data-stu-id="fc335-147">Texture image components</span></span>                                 |
| <span data-ttu-id="fc335-148">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-148">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="fc335-149">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-149">Initial value:</span></span>   | <span data-ttu-id="fc335-150">1</span><span class="sxs-lookup"><span data-stu-id="fc335-150">1</span></span>                                                        |
| <span data-ttu-id="fc335-151">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-151">Get command:</span></span>     | [<span data-ttu-id="fc335-152">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="fc335-152">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="fc335-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>\_color de \_ borde de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL\_TEXTURE\_BORDER\_COLOR</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="fc335-154">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-154">Description:</span></span>     | <span data-ttu-id="fc335-155">Color de borde de textura</span><span class="sxs-lookup"><span data-stu-id="fc335-155">Texture border color</span></span>                           |
| <span data-ttu-id="fc335-156">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-156">Attribute group:</span></span> | <span data-ttu-id="fc335-157">textura</span><span class="sxs-lookup"><span data-stu-id="fc335-157">texture</span></span>                                        |
| <span data-ttu-id="fc335-158">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-158">Initial value:</span></span>   | <span data-ttu-id="fc335-159">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="fc335-159">0, 0, 0, 0</span></span>                                     |
| <span data-ttu-id="fc335-160">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-160">Get command:</span></span>     | [<span data-ttu-id="fc335-161">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="fc335-161">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="fc335-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>\_ \_ filtro mínimo de textura de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL\_TEXTURE\_MIN\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="fc335-163">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-163">Description:</span></span>     | <span data-ttu-id="fc335-164">Texture minificación función)</span><span class="sxs-lookup"><span data-stu-id="fc335-164">Texture minification function</span></span>                  |
| <span data-ttu-id="fc335-165">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-165">Attribute group:</span></span> | <span data-ttu-id="fc335-166">textura</span><span class="sxs-lookup"><span data-stu-id="fc335-166">texture</span></span>                                        |
| <span data-ttu-id="fc335-167">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-167">Initial value:</span></span>   | <span data-ttu-id="fc335-168">el \_ \_ MIP \_ lineal más cercano de contabilidad</span><span class="sxs-lookup"><span data-stu-id="fc335-168">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>                    |
| <span data-ttu-id="fc335-169">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-169">Get command:</span></span>     | [<span data-ttu-id="fc335-170">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="fc335-170">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="fc335-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>\_filtro de textura de GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL\_TEXTURE\_MAG\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="fc335-172">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-172">Description:</span></span>     | <span data-ttu-id="fc335-173">Función de aumento de textura</span><span class="sxs-lookup"><span data-stu-id="fc335-173">Texture magnification function</span></span>                 |
| <span data-ttu-id="fc335-174">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-174">Attribute group:</span></span> | <span data-ttu-id="fc335-175">textura</span><span class="sxs-lookup"><span data-stu-id="fc335-175">texture</span></span>                                        |
| <span data-ttu-id="fc335-176">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-176">Initial value:</span></span>   | <span data-ttu-id="fc335-177">CONTABILIDAD \_ lineal</span><span class="sxs-lookup"><span data-stu-id="fc335-177">GL\_LINEAR</span></span>                                     |
| <span data-ttu-id="fc335-178">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-178">Get command:</span></span>     | [<span data-ttu-id="fc335-179">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="fc335-179">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="fc335-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>Ajuste de textura de GL \_ \_ \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL\_TEXTURE\_WRAP\_ *x*</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="fc335-181">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-181">Description:</span></span>     | <span data-ttu-id="fc335-182">Modo de ajuste de textura (*x*   es S o T)</span><span class="sxs-lookup"><span data-stu-id="fc335-182">Texture wrap mode (*x* is S or T)</span></span>              |
| <span data-ttu-id="fc335-183">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-183">Attribute group:</span></span> | <span data-ttu-id="fc335-184">textura</span><span class="sxs-lookup"><span data-stu-id="fc335-184">texture</span></span>                                        |
| <span data-ttu-id="fc335-185">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-185">Initial value:</span></span>   | <span data-ttu-id="fc335-186">repetición de GL \_</span><span class="sxs-lookup"><span data-stu-id="fc335-186">GL\_REPEAT</span></span>                                     |
| <span data-ttu-id="fc335-187">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-187">Get command:</span></span>     | [<span data-ttu-id="fc335-188">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="fc335-188">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="fc335-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>\_modo de textura del libro de contabilidad \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL\_TEXTURE\_ENV\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="fc335-190">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-190">Description:</span></span>     | <span data-ttu-id="fc335-191">Función de aplicación de textura</span><span class="sxs-lookup"><span data-stu-id="fc335-191">Texture application function</span></span>         |
| <span data-ttu-id="fc335-192">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-192">Attribute group:</span></span> | <span data-ttu-id="fc335-193">textura</span><span class="sxs-lookup"><span data-stu-id="fc335-193">texture</span></span>                              |
| <span data-ttu-id="fc335-194">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-194">Initial value:</span></span>   | <span data-ttu-id="fc335-195">\_modular GL</span><span class="sxs-lookup"><span data-stu-id="fc335-195">GL\_MODULATE</span></span>                         |
| <span data-ttu-id="fc335-196">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-196">Get command:</span></span>     | [<span data-ttu-id="fc335-197">**glGetTexEnviv**</span><span class="sxs-lookup"><span data-stu-id="fc335-197">**glGetTexEnviv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="fc335-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>\_color de textura de libro de contabilidad \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL\_TEXTURE\_ENV\_COLOR</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="fc335-199">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-199">Description:</span></span>     | <span data-ttu-id="fc335-200">Color del entorno de textura</span><span class="sxs-lookup"><span data-stu-id="fc335-200">Texture environment color</span></span>            |
| <span data-ttu-id="fc335-201">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-201">Attribute group:</span></span> | <span data-ttu-id="fc335-202">textura</span><span class="sxs-lookup"><span data-stu-id="fc335-202">texture</span></span>                              |
| <span data-ttu-id="fc335-203">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-203">Initial value:</span></span>   | <span data-ttu-id="fc335-204">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="fc335-204">0, 0, 0, 0</span></span>                           |
| <span data-ttu-id="fc335-205">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-205">Get command:</span></span>     | [<span data-ttu-id="fc335-206">**glGetTexEnvfv**</span><span class="sxs-lookup"><span data-stu-id="fc335-206">**glGetTexEnvfv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="fc335-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ Texture \_ gen \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL\_TEXTURE\_GEN\_ *x*</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="fc335-208">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-208">Description:</span></span>     | <span data-ttu-id="fc335-209">Texgen está habilitado (*x*   es S, T, R o Q)</span><span class="sxs-lookup"><span data-stu-id="fc335-209">Texgen is enabled (*x* is S, T, R, or Q)</span></span> |
| <span data-ttu-id="fc335-210">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-210">Attribute group:</span></span> | <span data-ttu-id="fc335-211">textura/habilitar</span><span class="sxs-lookup"><span data-stu-id="fc335-211">texture/enable</span></span>                           |
| <span data-ttu-id="fc335-212">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-212">Initial value:</span></span>   | <span data-ttu-id="fc335-213">CONTABILIDAD \_ falsa</span><span class="sxs-lookup"><span data-stu-id="fc335-213">GL\_FALSE</span></span>                                |
| <span data-ttu-id="fc335-214">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-214">Get command:</span></span>     | [<span data-ttu-id="fc335-215">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="fc335-215">**glIsEnabled**</span></span>](glisenabled.md)       |



 

<span data-ttu-id="fc335-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>\_plano de ojo de contabilidad \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL\_EYE\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="fc335-217">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-217">Description:</span></span>     | <span data-ttu-id="fc335-218">Coeficientes de ecuación del plano Texgen</span><span class="sxs-lookup"><span data-stu-id="fc335-218">Texgen plane equation coefficients</span></span>   |
| <span data-ttu-id="fc335-219">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-219">Attribute group:</span></span> | <span data-ttu-id="fc335-220">textura</span><span class="sxs-lookup"><span data-stu-id="fc335-220">texture</span></span>                              |
| <span data-ttu-id="fc335-221">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-221">Initial value:</span></span>   |                                      |
| <span data-ttu-id="fc335-222">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-222">Get command:</span></span>     | [<span data-ttu-id="fc335-223">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="fc335-223">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="fc335-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_plano del objeto GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL\_OBJECT\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="fc335-225">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-225">Description:</span></span>     | <span data-ttu-id="fc335-226">Coeficientes lineales del objeto Texgen</span><span class="sxs-lookup"><span data-stu-id="fc335-226">Texgen object linear coefficients</span></span>    |
| <span data-ttu-id="fc335-227">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-227">Attribute group:</span></span> | <span data-ttu-id="fc335-228">textura</span><span class="sxs-lookup"><span data-stu-id="fc335-228">texture</span></span>                              |
| <span data-ttu-id="fc335-229">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-229">Initial value:</span></span>   |                                      |
| <span data-ttu-id="fc335-230">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-230">Get command:</span></span>     | [<span data-ttu-id="fc335-231">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="fc335-231">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="fc335-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>\_modo de generación de texturas GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="fc335-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL\_TEXTURE\_GEN\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="fc335-233">Descripción:</span><span class="sxs-lookup"><span data-stu-id="fc335-233">Description:</span></span>     | <span data-ttu-id="fc335-234">Función usada para texgen</span><span class="sxs-lookup"><span data-stu-id="fc335-234">Function used for texgen</span></span>             |
| <span data-ttu-id="fc335-235">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="fc335-235">Attribute group:</span></span> | <span data-ttu-id="fc335-236">textura</span><span class="sxs-lookup"><span data-stu-id="fc335-236">texture</span></span>                              |
| <span data-ttu-id="fc335-237">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="fc335-237">Initial value:</span></span>   | <span data-ttu-id="fc335-238">\_ojo \_ lineal de contabilidad</span><span class="sxs-lookup"><span data-stu-id="fc335-238">GL\_EYE\_LINEAR</span></span>                      |
| <span data-ttu-id="fc335-239">Obtener comando:</span><span class="sxs-lookup"><span data-stu-id="fc335-239">Get command:</span></span>     | [<span data-ttu-id="fc335-240">**glGetTexGeniv**</span><span class="sxs-lookup"><span data-stu-id="fc335-240">**glGetTexGeniv**</span></span>](glgettexgen.md) |



 

</dd> </dl>

 

 




