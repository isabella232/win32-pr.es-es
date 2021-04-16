---
title: función glGetTexLevelParameterfv (GL. h)
description: Las funciones glGetTexLevelParameterfv y glGetTexLevelParameteriv devuelven los valores de los parámetros de textura para un nivel de detalle específico. | función glGetTexLevelParameterfv (GL. h)
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- glGetTexLevelParameterfv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92f8b55b41d3538f116241a0401cedf643a5e55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670169"
---
# <a name="glgettexlevelparameterfv-function"></a><span data-ttu-id="e0aff-105">glGetTexLevelParameterfv función)</span><span class="sxs-lookup"><span data-stu-id="e0aff-105">glGetTexLevelParameterfv function</span></span>

<span data-ttu-id="e0aff-106">Las funciones **glGetTexLevelParameterfv** y [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) devuelven los valores de los parámetros de textura para un nivel de detalle específico.</span><span class="sxs-lookup"><span data-stu-id="e0aff-106">The **glGetTexLevelParameterfv** and [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) functions return texture parameter values for a specific level of detail.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0aff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0aff-107">Syntax</span></span>


```C++
void WINAPI glGetTexLevelParameterfv(
   GLenum  target,
   GLint   level,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="e0aff-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0aff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0aff-109">*Destino*</span><span class="sxs-lookup"><span data-stu-id="e0aff-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="e0aff-110">El nombre simbólico de la textura de destino: libro \_ \_ de contabilidad 1D, textura de contabilidad \_ 2D, textura de \_ \_ proxy de contabilidad \_ \_ 1D o textura de proxy de GL \_ \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="e0aff-110">The symbolic name of the target texture: either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="e0aff-111">*level*</span><span class="sxs-lookup"><span data-stu-id="e0aff-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="e0aff-112">El número de nivel de detalle de la imagen deseada.</span><span class="sxs-lookup"><span data-stu-id="e0aff-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="e0aff-113">El nivel 0 es el nivel de la imagen base.</span><span class="sxs-lookup"><span data-stu-id="e0aff-113">Level 0 is the base image level.</span></span> <span data-ttu-id="e0aff-114">*El nivel* *n* es la imagen de reducción del MIP.</span><span class="sxs-lookup"><span data-stu-id="e0aff-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="e0aff-115">*PName*</span><span class="sxs-lookup"><span data-stu-id="e0aff-115">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="e0aff-116">Nombre simbólico de un parámetro de textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-116">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="e0aff-117">Se aceptan los siguientes nombres de parámetro.</span><span class="sxs-lookup"><span data-stu-id="e0aff-117">The following parameter names are accepted.</span></span>



| <span data-ttu-id="e0aff-118">Value</span><span class="sxs-lookup"><span data-stu-id="e0aff-118">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="e0aff-119">Significado</span><span class="sxs-lookup"><span data-stu-id="e0aff-119">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <span data-ttu-id="e0aff-120"><dt>**\_ancho de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-120"><dt>**GL\_TEXTURE\_WIDTH**</dt></span></span> </dl>                                | <span data-ttu-id="e0aff-121">El parámetro *params* devuelve un valor único que contiene el ancho de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-121">The *params* parameter returns a single value containing the width of the texture image.</span></span> <span data-ttu-id="e0aff-122">Este valor incluye el borde de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-122">This value includes the border of the texture image.</span></span><br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <span data-ttu-id="e0aff-123"><dt>**\_alto de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-123"><dt>**GL\_TEXTURE\_HEIGHT**</dt></span></span> </dl>                             | <span data-ttu-id="e0aff-124">El parámetro *params* devuelve un valor único que contiene el alto de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-124">The *params* parameter returns a single value containing the height of the texture image.</span></span> <span data-ttu-id="e0aff-125">Este valor incluye el borde de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-125">This value includes the border of the texture image.</span></span><br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <span data-ttu-id="e0aff-126"><dt>**\_ \_ formato interno de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-126"><dt>**GL\_TEXTURE\_INTERNAL\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="e0aff-127">El parámetro *params* devuelve un valor único que describe el formato textura de la textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-127">The *params* parameter returns a single value which describes the texel format of the texture.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <span data-ttu-id="e0aff-128"><dt>**\_borde de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-128"><dt>**GL\_TEXTURE\_BORDER**</dt></span></span> </dl>                             | <span data-ttu-id="e0aff-129">El parámetro *params* devuelve un valor único: el ancho, en píxeles, del borde de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-129">The *params* parameter returns a single value: the width in pixels of the border of the texture image.</span></span><br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <span data-ttu-id="e0aff-130"><dt>**\_ \_ tamaño rojo de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-130"><dt>**GL\_TEXTURE\_RED\_SIZE**</dt></span></span> </dl>                      | <span data-ttu-id="e0aff-131">La resolución de almacenamiento interna del componente rojo de un textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-131">The internal storage resolution of the red component of a texel.</span></span> <span data-ttu-id="e0aff-132">La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="e0aff-132">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <span data-ttu-id="e0aff-133"><dt>**\_ \_ tamaño verde de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-133"><dt>**GL\_TEXTURE\_GREEN\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="e0aff-134">La resolución de almacenamiento interna del componente verde de un textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-134">The internal storage resolution of the green component of a texel.</span></span> <span data-ttu-id="e0aff-135">La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="e0aff-135">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <span data-ttu-id="e0aff-136"><dt>**\_ \_ tamaño azul de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-136"><dt>**GL\_TEXTURE\_BLUE\_SIZE**</dt></span></span> </dl>                   | <span data-ttu-id="e0aff-137">La resolución de almacenamiento interna del componente azul de un textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-137">The internal storage resolution of the blue component of a texel.</span></span> <span data-ttu-id="e0aff-138">La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="e0aff-138">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <span data-ttu-id="e0aff-139"><dt>**\_ \_ tamaño alfa de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-139"><dt>**GL\_TEXTURE\_ALPHA\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="e0aff-140">La resolución de almacenamiento interna del componente alfa de un textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-140">The internal storage resolution of the alpha component of a texel.</span></span> <span data-ttu-id="e0aff-141">La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="e0aff-141">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <span data-ttu-id="e0aff-142"><dt>**\_tamaño de \_ luminancia de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-142"><dt>**GL\_TEXTURE\_LUMINANCE\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="e0aff-143">La resolución de almacenamiento interna del componente de luminancia de un textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-143">The internal storage resolution of the luminance component of a texel.</span></span> <span data-ttu-id="e0aff-144">La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="e0aff-144">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <span data-ttu-id="e0aff-145"><dt>**\_tamaño de \_ intensidad de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-145"><dt>**GL\_TEXTURE\_INTENSITY\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="e0aff-146">La resolución de almacenamiento interna del componente de intensidad de un textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-146">The internal storage resolution of the intensity component of a texel.</span></span> <span data-ttu-id="e0aff-147">La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="e0aff-147">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <span data-ttu-id="e0aff-148"><dt>**\_componentes de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-148"><dt>**GL\_TEXTURE\_COMPONENTS**</dt></span></span> </dl>                 | <span data-ttu-id="e0aff-149">El parámetro *params* devuelve un valor único: el número de componentes de la imagen de textura.</span><span class="sxs-lookup"><span data-stu-id="e0aff-149">The *params* parameter returns a single value: the number of components in the texture image.</span></span><br/>                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="e0aff-150">*params*</span><span class="sxs-lookup"><span data-stu-id="e0aff-150">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="e0aff-151">Devuelve los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="e0aff-151">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0aff-152">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0aff-152">Return value</span></span>

<span data-ttu-id="e0aff-153">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e0aff-153">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e0aff-154">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e0aff-154">Error codes</span></span>

<span data-ttu-id="e0aff-155">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="e0aff-155">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e0aff-156">Nombre</span><span class="sxs-lookup"><span data-stu-id="e0aff-156">Name</span></span>                                                                                                  | <span data-ttu-id="e0aff-157">Significado</span><span class="sxs-lookup"><span data-stu-id="e0aff-157">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0aff-158"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-158"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e0aff-159">el *destino* o *PName* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="e0aff-159">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="e0aff-160"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-160"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="e0aff-161">el *nivel* es menor que cero o mayor que el *registro* 2 *(Max)*, donde *Max* es el valor devuelto del \_ tamaño de textura Max GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e0aff-161">*level* is less than zero or greater than *log* 2 *(max)*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="e0aff-162"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-162"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e0aff-163">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e0aff-163">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e0aff-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0aff-164">Remarks</span></span>

<span data-ttu-id="e0aff-165">La función **glGetTexLevelParameter** devuelve los valores de *parámetro Texture de los parámetros para* un valor de nivel de detalle específico, especificado como *nivel*.</span><span class="sxs-lookup"><span data-stu-id="e0aff-165">The **glGetTexLevelParameter** function returns in *params* texture parameter values for a specific level-of-detail value, specified as *level*.</span></span> <span data-ttu-id="e0aff-166">El parámetro de *destino* define la textura de destino, ya sea GL \_ Texture \_ 1D, GL \_ Texture \_ 2D, GL \_ proxy \_ Texture \_ 1D o la \_ \_ textura de proxy GL \_ 2D para especificar una texturización unidimensional o bidimensional.</span><span class="sxs-lookup"><span data-stu-id="e0aff-166">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="e0aff-167">El parámetro *PName* especifica el parámetro de textura cuyo valor o valores se devolverán.</span><span class="sxs-lookup"><span data-stu-id="e0aff-167">The *pname* parameter specifies the texture parameter whose value or values will be returned.</span></span>

<span data-ttu-id="e0aff-168">Si se genera un error, no se realiza ningún cambio en el contenido de los *parámetros*.</span><span class="sxs-lookup"><span data-stu-id="e0aff-168">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0aff-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0aff-169">Requirements</span></span>



| <span data-ttu-id="e0aff-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0aff-170">Requirement</span></span> | <span data-ttu-id="e0aff-171">Value</span><span class="sxs-lookup"><span data-stu-id="e0aff-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0aff-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0aff-172">Minimum supported client</span></span><br/> | <span data-ttu-id="e0aff-173">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e0aff-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e0aff-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0aff-174">Minimum supported server</span></span><br/> | <span data-ttu-id="e0aff-175">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e0aff-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0aff-176">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0aff-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0aff-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e0aff-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0aff-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="e0aff-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e0aff-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0aff-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0aff-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0aff-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0aff-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0aff-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0aff-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e0aff-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e0aff-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e0aff-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e0aff-185">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="e0aff-185">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="e0aff-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="e0aff-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="e0aff-187">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="e0aff-187">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="e0aff-188">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="e0aff-188">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





