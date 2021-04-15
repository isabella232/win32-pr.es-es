---
title: función glStencilFunc (GL. h)
description: La función glStencilFunc establece la función y el valor de referencia para las pruebas de estarcido.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- glStencilFunc (función) OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4f9c0a5ec905ecb061ddb54984bf35ff8edc3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677005"
---
# <a name="glstencilfunc-function"></a><span data-ttu-id="b3aa9-104">glStencilFunc función)</span><span class="sxs-lookup"><span data-stu-id="b3aa9-104">glStencilFunc function</span></span>

<span data-ttu-id="b3aa9-105">La función **glStencilFunc** establece la función y el valor de referencia para las pruebas de estarcido.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-105">The **glStencilFunc** function sets the function and reference value for stencil testing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3aa9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3aa9-106">Syntax</span></span>


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="b3aa9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3aa9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3aa9-108">*func*</span><span class="sxs-lookup"><span data-stu-id="b3aa9-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="b3aa9-109">La función de prueba.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-109">The test function.</span></span> <span data-ttu-id="b3aa9-110">Los ocho tokens siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-110">The following eight tokens are valid.</span></span>



| <span data-ttu-id="b3aa9-111">Value</span><span class="sxs-lookup"><span data-stu-id="b3aa9-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="b3aa9-112">Significado</span><span class="sxs-lookup"><span data-stu-id="b3aa9-112">Meaning</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="b3aa9-113"><dt>**GL \_ nunca**</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="b3aa9-114">Siempre produce un error.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-114">Always fails.</span></span><br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="b3aa9-115"><dt>**CONTABILIDAD \_ inferior**</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="b3aa9-116">Pasa si (  &  *máscara* de referencia) < (máscara de *estarcido*  &  ).</span><span class="sxs-lookup"><span data-stu-id="b3aa9-116">Passes if (*ref* & *mask*) < (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="b3aa9-117"><dt>**GL \_ LEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-117"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="b3aa9-118">Pasa si (  &  *máscara* de referencia) = (máscara de *estarcido*  &  ).</span><span class="sxs-lookup"><span data-stu-id="b3aa9-118">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="b3aa9-119"><dt>**LIBRO \_ superior**</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-119"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="b3aa9-120">Pasa si (  &  *máscara* de referencia) > (máscara de *estarcido*  &  ).</span><span class="sxs-lookup"><span data-stu-id="b3aa9-120">Passes if (*ref* & *mask*) > (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="b3aa9-121"><dt>**GL \_ GEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-121"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="b3aa9-122">Pasa si (  &  *máscara* de referencia) = (máscara de *estarcido*  &  ).</span><span class="sxs-lookup"><span data-stu-id="b3aa9-122">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="b3aa9-123"><dt>**igual a GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-123"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="b3aa9-124">Pasa si (  &  *máscara* de referencia) = (máscara de *estarcido*  &  ).</span><span class="sxs-lookup"><span data-stu-id="b3aa9-124">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="b3aa9-125"><dt>**NOTEQUAL en GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-125"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="b3aa9-126">¿Pasa si (máscara de *referencia*  &  )?</span><span class="sxs-lookup"><span data-stu-id="b3aa9-126">Passes if (*ref* & *mask*) ?</span></span> <span data-ttu-id="b3aa9-127">(*Galería de símbolos*  &  *máscara*).</span><span class="sxs-lookup"><span data-stu-id="b3aa9-127">(*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="b3aa9-128"><dt>**GL \_ siempre**</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="b3aa9-129">Siempre pasa.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-129">Always passes.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="b3aa9-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="b3aa9-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="b3aa9-131">El valor de referencia para la prueba de estarcido.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-131">The reference value for the stencil test.</span></span> <span data-ttu-id="b3aa9-132">El parámetro *ref* está fijado al intervalo \[ 0, 2 *n* 1 \] , donde *n* es el número de bitplanes en el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-132">The *ref* parameter is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b3aa9-133">*mask*</span><span class="sxs-lookup"><span data-stu-id="b3aa9-133">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="b3aa9-134">Máscara que es **y** Ed con el valor de referencia y el valor de estarcido almacenado cuando se realiza la prueba.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-134">A mask that is **AND** ed with both the reference value and the stored stencil value when the test is done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3aa9-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3aa9-135">Return value</span></span>

<span data-ttu-id="b3aa9-136">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-136">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b3aa9-137">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b3aa9-137">Error codes</span></span>

<span data-ttu-id="b3aa9-138">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-138">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b3aa9-139">Nombre</span><span class="sxs-lookup"><span data-stu-id="b3aa9-139">Name</span></span>                                                                                                  | <span data-ttu-id="b3aa9-140">Significado</span><span class="sxs-lookup"><span data-stu-id="b3aa9-140">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3aa9-141"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-141"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b3aa9-142">*FUNC* no era uno de los ocho valores aceptados.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-142">*func* was not one of the eight accepted values.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="b3aa9-143"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-143"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b3aa9-144">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b3aa9-144">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b3aa9-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3aa9-145">Remarks</span></span>

<span data-ttu-id="b3aa9-146">La galería de símbolos, como el almacenamiento en búfer de *z*, habilita y deshabilita el dibujo en cada píxel.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-146">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="b3aa9-147">Dibuja en los planos de la galería de símbolos mediante primitivos de dibujo de OpenGL y, a continuación, representa geometría e imágenes mediante los planos de la galería de símbolos para enmascarar partes de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-147">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="b3aa9-148">La galería de símbolos se usa normalmente en algoritmos de representación de Multipass para lograr efectos especiales, como marcas, esquematización y representación de geometría sólida constructiva.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-148">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="b3aa9-149">La prueba de estarcido elimina condicionalmente un píxel según el resultado de una comparación entre el valor de referencia y el valor en el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-149">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the reference value and the value in the stencil buffer.</span></span> <span data-ttu-id="b3aa9-150">La prueba está habilitada por [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL de \_ estarcido \_ Test.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-150">The test is enabled by [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_STENCIL\_TEST.</span></span> <span data-ttu-id="b3aa9-151">Las acciones realizadas en función del resultado de la prueba de estarcido se especifican con [**glStencilOp**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="b3aa9-151">Actions taken based on the outcome of the stencil test are specified with [**glStencilOp**](glstencilop.md).</span></span>

<span data-ttu-id="b3aa9-152">El parámetro *FUNC* es una constante simbólica que determina la función de comparación de estarcido.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-152">The *func* parameter is a symbolic constant that determines the stencil comparison function.</span></span> <span data-ttu-id="b3aa9-153">Acepta uno de los ocho valores mostrados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-153">It accepts one of the eight values shown above.</span></span> <span data-ttu-id="b3aa9-154">El parámetro *ref* es un valor de referencia entero que se utiliza en la comparación de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-154">The *ref* parameter is an integer reference value that is used in the stencil comparison.</span></span> <span data-ttu-id="b3aa9-155">Se fija en el intervalo comprendido entre \[ 0 y 2 *n* 1 \] , donde *n* es el número de bitplanes en el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-155">It is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span> <span data-ttu-id="b3aa9-156">El parámetro *Mask* es bit **a bit y** Ed con el valor de referencia y el valor de estarcido almacenado, con los valores **y** Ed que participan en la comparación.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-156">The *mask* parameter is bitwise **AND** ed with both the reference value and the stored stencil value, with the **AND** ed values participating in the comparison.</span></span>

<span data-ttu-id="b3aa9-157">Si *cliché* representa el valor almacenado en la ubicación del búfer de estarcido correspondiente, la lista anterior muestra el efecto de cada función de comparación que se puede especificar mediante *FUNC*.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-157">If *stencil* represents the value stored in the corresponding stencil buffer location, the preceding list shows the effect of each comparison function that can be specified by *func*.</span></span> <span data-ttu-id="b3aa9-158">Solo si la comparación se realiza correctamente, el píxel pasa a la siguiente fase del proceso de rasterización (vea [**glStencilOp**](glstencilop.md)).</span><span class="sxs-lookup"><span data-stu-id="b3aa9-158">Only if the comparison succeeds is the pixel passed through to the next stage in the rasterization process (see [**glStencilOp**](glstencilop.md)).</span></span> <span data-ttu-id="b3aa9-159">Todas las pruebas tratan los valores de la *Galería de símbolos* como enteros sin signo en el intervalo de \[ 0, 2 *n* 1 \] , donde *n* es el número de bitplanes en el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-159">All tests treat *stencil* values as unsigned integers in the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

<span data-ttu-id="b3aa9-160">Inicialmente, la prueba de galería de símbolos está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-160">Initially, the stencil test is disabled.</span></span> <span data-ttu-id="b3aa9-161">Si no hay ningún búfer de estarcido, no se puede modificar la galería de símbolos y es como si la prueba de estarcido siempre se supera.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-161">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil test always passes.</span></span>

<span data-ttu-id="b3aa9-162">Las siguientes funciones recuperan información relacionada con **glStencilFunc**:</span><span class="sxs-lookup"><span data-stu-id="b3aa9-162">The following functions retrieve information related to **glStencilFunc**:</span></span>

<span data-ttu-id="b3aa9-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento de \_ estarcido GL \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="b3aa9-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FUNC</span></span>

<span data-ttu-id="b3aa9-164">**glGet** con el argumento \_ \_ máscara de valor \_ de la galería de símbolos GL</span><span class="sxs-lookup"><span data-stu-id="b3aa9-164">**glGet** with argument GL\_STENCIL\_VALUE\_MASK</span></span>

<span data-ttu-id="b3aa9-165">**glGet** con el argumento \_ referencia de la galería de símbolos GL \_</span><span class="sxs-lookup"><span data-stu-id="b3aa9-165">**glGet** with argument GL\_STENCIL\_REF</span></span>

<span data-ttu-id="b3aa9-166">**glGet** con el argumento \_ bits de estarcido GL \_</span><span class="sxs-lookup"><span data-stu-id="b3aa9-166">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="b3aa9-167">[**glIsEnabled**](glisenabled.md) con el argumento, \_ prueba de estarcido GL \_</span><span class="sxs-lookup"><span data-stu-id="b3aa9-167">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="b3aa9-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3aa9-168">Requirements</span></span>



| <span data-ttu-id="b3aa9-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3aa9-169">Requirement</span></span> | <span data-ttu-id="b3aa9-170">Value</span><span class="sxs-lookup"><span data-stu-id="b3aa9-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3aa9-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3aa9-171">Minimum supported client</span></span><br/> | <span data-ttu-id="b3aa9-172">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b3aa9-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b3aa9-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3aa9-173">Minimum supported server</span></span><br/> | <span data-ttu-id="b3aa9-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b3aa9-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3aa9-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3aa9-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3aa9-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b3aa9-177">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3aa9-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3aa9-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3aa9-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3aa9-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3aa9-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa9-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3aa9-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3aa9-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3aa9-182">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="b3aa9-182">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="b3aa9-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b3aa9-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b3aa9-184">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="b3aa9-184">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="b3aa9-185">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="b3aa9-185">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="b3aa9-186">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="b3aa9-186">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="b3aa9-187">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b3aa9-187">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b3aa9-188">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="b3aa9-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="b3aa9-189">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="b3aa9-189">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="b3aa9-190">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="b3aa9-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





