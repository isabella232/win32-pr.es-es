---
title: función glStencilOp (GL. h)
description: La función glStencilOp establece las acciones de prueba de la galería de símbolos.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- glStencilOp (función) OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b23162f8606ed68dc90a0cb6debdcc903e0ccd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676873"
---
# <a name="glstencilop-function"></a><span data-ttu-id="14e84-104">glStencilOp función)</span><span class="sxs-lookup"><span data-stu-id="14e84-104">glStencilOp function</span></span>

<span data-ttu-id="14e84-105">La función **glStencilOp** establece las acciones de prueba de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="14e84-105">The **glStencilOp** function sets the stencil test actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e84-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14e84-106">Syntax</span></span>


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a><span data-ttu-id="14e84-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14e84-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e84-108">*puedan*</span><span class="sxs-lookup"><span data-stu-id="14e84-108">*fail*</span></span> 
</dt> <dd>

<span data-ttu-id="14e84-109">Acción que se realizará cuando se produzca un error en la prueba de estarcido.</span><span class="sxs-lookup"><span data-stu-id="14e84-109">The action to take when the stencil test fails.</span></span> <span data-ttu-id="14e84-110">Se aceptan las seis constantes simbólicas siguientes.</span><span class="sxs-lookup"><span data-stu-id="14e84-110">The following six symbolic constants are accepted.</span></span>



| <span data-ttu-id="14e84-111">Value</span><span class="sxs-lookup"><span data-stu-id="14e84-111">Value</span></span>                                                                                                                                                | <span data-ttu-id="14e84-112">Significado</span><span class="sxs-lookup"><span data-stu-id="14e84-112">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <span data-ttu-id="14e84-113"><dt>**mantenimiento de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14e84-113"><dt>**GL\_KEEP**</dt></span></span> </dl>          | <span data-ttu-id="14e84-114">Mantiene el valor actual.</span><span class="sxs-lookup"><span data-stu-id="14e84-114">Keeps the current value.</span></span><br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <span data-ttu-id="14e84-115"><dt>**GL \_ cero**</dt></span><span class="sxs-lookup"><span data-stu-id="14e84-115"><dt>**GL\_ZERO**</dt></span></span> </dl>          | <span data-ttu-id="14e84-116">Establece el valor del búfer de la galería de símbolos en cero.</span><span class="sxs-lookup"><span data-stu-id="14e84-116">Sets the stencil buffer value to zero.</span></span><br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <span data-ttu-id="14e84-117"><dt>**reemplazo de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14e84-117"><dt>**GL\_REPLACE**</dt></span></span> </dl> | <span data-ttu-id="14e84-118">Establece el valor del búfer de estarcido en *ref*, tal y como se especifica en **glStencilFunc**.</span><span class="sxs-lookup"><span data-stu-id="14e84-118">Sets the stencil buffer value to *ref*, as specified by **glStencilFunc**.</span></span><br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <span data-ttu-id="14e84-119"><dt>**INCR del libro de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14e84-119"><dt>**GL\_INCR**</dt></span></span> </dl>          | <span data-ttu-id="14e84-120">Incrementa el valor del búfer de estarcido actual.</span><span class="sxs-lookup"><span data-stu-id="14e84-120">Increments the current stencil buffer value.</span></span> <span data-ttu-id="14e84-121">Se fija en el valor sin signo máximo que se puede representar.</span><span class="sxs-lookup"><span data-stu-id="14e84-121">Clamps to the maximum representable unsigned value.</span></span><br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <span data-ttu-id="14e84-122"><dt>**GL \_ decr (**</dt></span><span class="sxs-lookup"><span data-stu-id="14e84-122"><dt>**GL\_DECR**</dt></span></span> </dl>          | <span data-ttu-id="14e84-123">Disminuye el valor del búfer de estarcido actual.</span><span class="sxs-lookup"><span data-stu-id="14e84-123">Decrements the current stencil buffer value.</span></span> <span data-ttu-id="14e84-124">Se fija en cero.</span><span class="sxs-lookup"><span data-stu-id="14e84-124">Clamps to zero.</span></span><br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="14e84-125"><dt>**inversión en contab \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14e84-125"><dt>**GL\_INVERT**</dt></span></span> </dl>    | <span data-ttu-id="14e84-126">Bit a bit invierte el valor del búfer de estarcido actual.</span><span class="sxs-lookup"><span data-stu-id="14e84-126">Bitwise inverts the current stencil buffer value.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="14e84-127">*zfail*</span><span class="sxs-lookup"><span data-stu-id="14e84-127">*zfail*</span></span> 
</dt> <dd>

<span data-ttu-id="14e84-128">Acción de estarcido cuando se supera la prueba de estarcido, pero se produce un error en la prueba de profundidad.</span><span class="sxs-lookup"><span data-stu-id="14e84-128">Stencil action when the stencil test passes, but the depth test fails.</span></span> <span data-ttu-id="14e84-129">Acepta las mismas constantes simbólicas que *Fail.*</span><span class="sxs-lookup"><span data-stu-id="14e84-129">Accepts the same symbolic constants as *fail.*</span></span>

</dd> <dt>

<span data-ttu-id="14e84-130">*zpass*</span><span class="sxs-lookup"><span data-stu-id="14e84-130">*zpass*</span></span> 
</dt> <dd>

<span data-ttu-id="14e84-131">Acción de estarcido cuando la prueba de estarcido y la prueba de profundidad superan o cuando se supera la prueba de estarcido y no hay ningún búfer de profundidad o la prueba de profundidad no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="14e84-131">Stencil action when both the stencil test and the depth test pass, or when the stencil test passes and either there is no depth buffer or depth testing is not enabled.</span></span> <span data-ttu-id="14e84-132">Acepta las mismas constantes simbólicas que *FAIL*.</span><span class="sxs-lookup"><span data-stu-id="14e84-132">Accepts the same symbolic constants as *fail*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e84-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14e84-133">Return value</span></span>

<span data-ttu-id="14e84-134">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="14e84-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="14e84-135">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="14e84-135">Error codes</span></span>

<span data-ttu-id="14e84-136">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="14e84-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="14e84-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="14e84-137">Name</span></span>                                                                                                  | <span data-ttu-id="14e84-138">Significado</span><span class="sxs-lookup"><span data-stu-id="14e84-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14e84-139"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14e84-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="14e84-140">*FAIL*, *zfail* o *ZPass* era cualquier valor distinto de los seis valores constantes definidos.</span><span class="sxs-lookup"><span data-stu-id="14e84-140">*fail*, *zfail*, or *zpass* was any value other than the six defined constant values.</span></span><br/>                                      |
| <dl> <span data-ttu-id="14e84-141"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14e84-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="14e84-142">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="14e84-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="14e84-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14e84-143">Remarks</span></span>

<span data-ttu-id="14e84-144">La galería de símbolos, como el almacenamiento en búfer de *z*, habilita y deshabilita el dibujo en cada píxel.</span><span class="sxs-lookup"><span data-stu-id="14e84-144">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="14e84-145">Dibuja en los planos de la galería de símbolos mediante primitivos de dibujo de OpenGL y, a continuación, representa geometría e imágenes mediante los planos de la galería de símbolos para enmascarar partes de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="14e84-145">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="14e84-146">La galería de símbolos se usa normalmente en algoritmos de representación de Multipass para lograr efectos especiales, como marcas, esquematización y representación de geometría sólida constructiva.</span><span class="sxs-lookup"><span data-stu-id="14e84-146">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="14e84-147">La prueba de estarcido elimina condicionalmente un píxel según el resultado de una comparación entre el valor del búfer de estarcido y un valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="14e84-147">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="14e84-148">La prueba se habilita con llamadas a [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL de \_ estarcido \_ Test y se controla con [**glStencilFunc**](glstencilfunc.md).</span><span class="sxs-lookup"><span data-stu-id="14e84-148">The test is enabled with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) calls with argument GL\_STENCIL\_TEST, and controlled with [**glStencilFunc**](glstencilfunc.md).</span></span>

<span data-ttu-id="14e84-149">La función **glStencilOp** toma tres argumentos que indican lo que sucede con el valor de estarcido almacenado mientras está habilitado el estarcido.</span><span class="sxs-lookup"><span data-stu-id="14e84-149">The **glStencilOp** function takes three arguments that indicate what happens to the stored stencil value while stenciling is enabled.</span></span> <span data-ttu-id="14e84-150">Si se produce un error en la prueba de estarcido, no se realiza ningún cambio en los búferes de color o de profundidad del píxel y se *produce un error* y se especifica lo que sucede con el contenido del búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="14e84-150">If the stencil test fails, no change is made to the pixel's color or depth buffers, and *fail* specifies what happens to the stencil buffer contents.</span></span>

<span data-ttu-id="14e84-151">Los valores de búfer de estarcido se tratan como enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="14e84-151">Stencil buffer values are treated as unsigned integers.</span></span> <span data-ttu-id="14e84-152">Cuando se incrementa y disminuye, los valores se fijan a 0 y 2 *n* 1, donde *n* es el valor devuelto por la consulta de los bits de la \_ Galería de símbolos GL \_ .</span><span class="sxs-lookup"><span data-stu-id="14e84-152">When incremented and decremented, values are clamped to 0 and 2 *n* 1, where *n* is the value returned by querying GL\_STENCIL\_BITS.</span></span>

<span data-ttu-id="14e84-153">Los otros dos argumentos de **glStencilOp** especifican las acciones de búfer de estarcido deben realizarse correctamente las pruebas de búfer de profundidad (*ZPass*) o Fail (*zfail*).</span><span class="sxs-lookup"><span data-stu-id="14e84-153">The other two arguments to **glStencilOp** specify stencil buffer actions should subsequent depth buffer tests succeed (*zpass*) or fail (*zfail*).</span></span> <span data-ttu-id="14e84-154">(Consulte [**glDepthFunc**](gldepthfunc.md)). Se especifican con las mismas seis constantes simbólicas que *producen un error*.</span><span class="sxs-lookup"><span data-stu-id="14e84-154">(See [**glDepthFunc**](gldepthfunc.md).) They are specified using the same six symbolic constants as *fail*.</span></span> <span data-ttu-id="14e84-155">Tenga en cuenta que *zfail* se omite cuando no hay ningún búfer de profundidad o cuando el búfer de profundidad no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="14e84-155">Note that *zfail* is ignored when there is no depth buffer, or when the depth buffer is not enabled.</span></span> <span data-ttu-id="14e84-156">En estos casos, *FAIL* y *ZPass* especifican la acción de estarcido cuando se produce un error en la prueba de estarcido y se pasan, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="14e84-156">In these cases, *fail* and *zpass* specify stencil action when the stencil test fails and passes, respectively.</span></span>

<span data-ttu-id="14e84-157">Inicialmente, la prueba de galería de símbolos está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="14e84-157">Initially the stencil test is disabled.</span></span> <span data-ttu-id="14e84-158">Si no hay ningún búfer de estarcido, no se puede realizar ninguna modificación en la galería de símbolos y es como si el estarcido probara siempre, independientemente de cualquier llamada a **glStencilOp**.</span><span class="sxs-lookup"><span data-stu-id="14e84-158">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil tests always pass, regardless of any call to **glStencilOp**.</span></span>

<span data-ttu-id="14e84-159">Las siguientes funciones recuperan información relacionada con **glStencilOp**:</span><span class="sxs-lookup"><span data-stu-id="14e84-159">The following functions retrieve information related to **glStencilOp**:</span></span>

<span data-ttu-id="14e84-160">error de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL de la \_ Galería de símbolos \_</span><span class="sxs-lookup"><span data-stu-id="14e84-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FAIL</span></span>

<span data-ttu-id="14e84-161">**glGet** con el argumento de la profundidad de la fase de estarcido de GL \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="14e84-161">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_PASS</span></span>

<span data-ttu-id="14e84-162"> error de profundidad de \_ paso de estarcido de glGet con el argumento \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="14e84-162">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_FAIL</span></span>

<span data-ttu-id="14e84-163">**glGet** con el argumento \_ bits de estarcido GL \_</span><span class="sxs-lookup"><span data-stu-id="14e84-163">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="14e84-164">[**glIsEnabled**](glisenabled.md) con el argumento, \_ prueba de estarcido GL \_</span><span class="sxs-lookup"><span data-stu-id="14e84-164">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="14e84-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14e84-165">Requirements</span></span>



| <span data-ttu-id="14e84-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="14e84-166">Requirement</span></span> | <span data-ttu-id="14e84-167">Value</span><span class="sxs-lookup"><span data-stu-id="14e84-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14e84-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14e84-168">Minimum supported client</span></span><br/> | <span data-ttu-id="14e84-169">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="14e84-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14e84-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14e84-170">Minimum supported server</span></span><br/> | <span data-ttu-id="14e84-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14e84-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14e84-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14e84-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="14e84-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="14e84-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="14e84-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14e84-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="14e84-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14e84-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="14e84-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="14e84-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14e84-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14e84-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14e84-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="14e84-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e84-179">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="14e84-179">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="14e84-180">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="14e84-180">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="14e84-181">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="14e84-181">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="14e84-182">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="14e84-182">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="14e84-183">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="14e84-183">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="14e84-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="14e84-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="14e84-185">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="14e84-185">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="14e84-186">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="14e84-186">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="14e84-187">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="14e84-187">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





