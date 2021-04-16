---
title: función glAlphaFunc (GL. h)
description: La función glAlphaFunc permite que la aplicación establezca la función de prueba alfa.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- glAlphaFunc (función) OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686009"
---
# <a name="glalphafunc-function"></a><span data-ttu-id="c5cd2-104">glAlphaFunc función)</span><span class="sxs-lookup"><span data-stu-id="c5cd2-104">glAlphaFunc function</span></span>

<span data-ttu-id="c5cd2-105">La función **glAlphaFunc** permite que la aplicación establezca la función de prueba alfa.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-105">The **glAlphaFunc** function enables your application to set the alpha test function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5cd2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5cd2-106">Syntax</span></span>


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a><span data-ttu-id="c5cd2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5cd2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5cd2-108">*func*</span><span class="sxs-lookup"><span data-stu-id="c5cd2-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="c5cd2-109">Función de comparación alfa.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-109">The alpha comparison function.</span></span> <span data-ttu-id="c5cd2-110">A continuación se indican las constantes simbólicas aceptadas y su significado.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-110">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="c5cd2-111">Value</span><span class="sxs-lookup"><span data-stu-id="c5cd2-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="c5cd2-112">Significado</span><span class="sxs-lookup"><span data-stu-id="c5cd2-112">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="c5cd2-113"><dt>**GL \_ nunca**</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="c5cd2-114">Nunca pasa.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-114">Never passes.</span></span><br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="c5cd2-115"><dt>**CONTABILIDAD \_ inferior**</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="c5cd2-116">Pasa si el valor alfa de entrada es menor que el valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-116">Passes if the incoming alpha value is less than the reference value.</span></span><br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="c5cd2-117"><dt>**igual a GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-117"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="c5cd2-118">Pasa si el valor alfa entrante es igual al valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-118">Passes if the incoming alpha value is equal to the reference value.</span></span><br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="c5cd2-119"><dt>**GL \_ LEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-119"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="c5cd2-120">Pasa si el valor alfa entrante es menor o igual que el valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-120">Passes if the incoming alpha value is less than or equal to the reference value.</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="c5cd2-121"><dt>**LIBRO \_ superior**</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-121"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="c5cd2-122">Pasa si el valor alfa entrante es mayor que el valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-122">Passes if the incoming alpha value is greater than the reference value.</span></span><br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="c5cd2-123"><dt>**NOTEQUAL en GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-123"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="c5cd2-124">Pasa si el valor alfa entrante no es igual que el valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-124">Passes if the incoming alpha value is not equal to the reference value.</span></span><br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="c5cd2-125"><dt>**GL \_ GEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-125"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="c5cd2-126">Pasa si el valor alfa entrante es mayor o igual que el valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-126">Passes if the incoming alpha value is greater than or equal to the reference value.</span></span><br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="c5cd2-127"><dt>**GL \_ siempre**</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-127"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="c5cd2-128">Siempre pasa.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-128">Always passes.</span></span> <span data-ttu-id="c5cd2-129">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-129">This is the default.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="c5cd2-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="c5cd2-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="c5cd2-131">Valor de referencia con el que se comparan los valores alfa entrantes.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-131">The reference value to which incoming alpha values are compared.</span></span> <span data-ttu-id="c5cd2-132">Este valor se fija en el intervalo comprendido entre 0 y 1, donde 0 representa el valor alfa más bajo posible y 1 el valor más alto posible.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-132">This value is clamped to the range 0 through 1, where 0 represents the lowest possible alpha value and 1 the highest possible value.</span></span> <span data-ttu-id="c5cd2-133">La referencia predeterminada es 0.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-133">The default reference is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5cd2-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5cd2-134">Return value</span></span>

<span data-ttu-id="c5cd2-135">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c5cd2-136">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c5cd2-136">Error codes</span></span>

<span data-ttu-id="c5cd2-137">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c5cd2-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="c5cd2-138">Name</span></span>                                                                                                  | <span data-ttu-id="c5cd2-139">Significado</span><span class="sxs-lookup"><span data-stu-id="c5cd2-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5cd2-140"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c5cd2-141">*FUNC* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-141">*func* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="c5cd2-142"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c5cd2-143">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c5cd2-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c5cd2-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5cd2-144">Remarks</span></span>

<span data-ttu-id="c5cd2-145">La prueba alfa descarta los fragmentos según el resultado de una comparación entre los valores alfa de los fragmentos entrantes y un valor de referencia constante.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-145">The alpha test discards fragments depending on the outcome of a comparison between the incoming fragments' alpha values and a constant reference value.</span></span> <span data-ttu-id="c5cd2-146">La función **glAlphaFunc** especifica la función de referencia y de comparación.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-146">The **glAlphaFunc** function specifies the reference and comparison function.</span></span> <span data-ttu-id="c5cd2-147">La comparación solo se realiza si está habilitada la prueba alfa.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-147">The comparison is performed only if alpha testing is enabled.</span></span> <span data-ttu-id="c5cd2-148">(Para obtener más información sobre GL \_ ) La \_ prueba alfa, vea [**glEnable**](glenable.md)).</span><span class="sxs-lookup"><span data-stu-id="c5cd2-148">(For more information on GL\_ALPHA\_TEST, see [**glEnable**](glenable.md).)</span></span>

<span data-ttu-id="c5cd2-149">Los parámetros *FUNC* y *ref* especifican las condiciones en las que se dibuja el píxel.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-149">The *func* and *ref* parameters specify the conditions under which the pixel is drawn.</span></span> <span data-ttu-id="c5cd2-150">El valor alfa entrante se compara con *ref* mediante la función especificada por *FUNC*.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-150">The incoming alpha value is compared to *ref* using the function specified by *func*.</span></span> <span data-ttu-id="c5cd2-151">Si se pasa la comparación, se dibuja el fragmento entrante, condicional en las siguientes pruebas de estarcido y de búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-151">If the comparison passes, the incoming fragment is drawn, conditional on subsequent stencil and depth-buffer tests.</span></span> <span data-ttu-id="c5cd2-152">Si se produce un error en la comparación, no se realiza ningún cambio en el fotogramas en esa ubicación de píxeles.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-152">If the comparison fails, no change is made to the framebuffer at that pixel location.</span></span>

<span data-ttu-id="c5cd2-153">La función **glAlphaFunc** funciona en todas las escrituras de píxeles, incluidas las que resultan de la conversión de recorrido de puntos, líneas, polígonos y mapas de bits, así como de las operaciones de copia y dibujo de píxeles.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-153">The **glAlphaFunc** function operates on all pixel writes, including those resulting from the scan conversion of points, lines, polygons, and bitmaps, and from pixel draw and copy operations.</span></span> <span data-ttu-id="c5cd2-154">La función **glAlphaFunc** no afecta a las operaciones de borrado de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-154">The **glAlphaFunc** function does not affect screen clear operations.</span></span>

<span data-ttu-id="c5cd2-155">La prueba alfa solo se realiza en el modo RGBA.</span><span class="sxs-lookup"><span data-stu-id="c5cd2-155">Alpha testing is done only in RGBA mode.</span></span>

<span data-ttu-id="c5cd2-156">Las siguientes funciones recuperan información relacionada con la función **glAlphaFunc** :</span><span class="sxs-lookup"><span data-stu-id="c5cd2-156">The following functions retrieve information related to the **glAlphaFunc** function:</span></span>

<span data-ttu-id="c5cd2-157">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ FUNC Alpha test \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="c5cd2-157">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ALPHA\_TEST\_FUNC</span></span>

<span data-ttu-id="c5cd2-158">**glGet** con argumento referencia de prueba de GL \_ alpha \_ \_</span><span class="sxs-lookup"><span data-stu-id="c5cd2-158">**glGet** with argument GL\_ALPHA\_TEST\_REF</span></span>

<span data-ttu-id="c5cd2-159">[**glIsEnabled**](glisenabled.md) con el argumento \_ prueba de GL alpha \_</span><span class="sxs-lookup"><span data-stu-id="c5cd2-159">[**glIsEnabled**](glisenabled.md) with argument GL\_ALPHA\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="c5cd2-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5cd2-160">Requirements</span></span>



| <span data-ttu-id="c5cd2-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5cd2-161">Requirement</span></span> | <span data-ttu-id="c5cd2-162">Value</span><span class="sxs-lookup"><span data-stu-id="c5cd2-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5cd2-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5cd2-163">Minimum supported client</span></span><br/> | <span data-ttu-id="c5cd2-164">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c5cd2-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c5cd2-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5cd2-165">Minimum supported server</span></span><br/> | <span data-ttu-id="c5cd2-166">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5cd2-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c5cd2-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5cd2-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5cd2-168"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-168"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c5cd2-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5cd2-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="c5cd2-170"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-170"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c5cd2-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5cd2-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5cd2-172"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5cd2-172"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5cd2-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5cd2-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5cd2-174">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c5cd2-174">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c5cd2-175">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="c5cd2-175">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="c5cd2-176">**glClear**</span><span class="sxs-lookup"><span data-stu-id="c5cd2-176">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="c5cd2-177">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="c5cd2-177">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="c5cd2-178">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="c5cd2-178">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="c5cd2-179">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c5cd2-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c5cd2-180">**glGet**</span><span class="sxs-lookup"><span data-stu-id="c5cd2-180">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="c5cd2-181">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="c5cd2-181">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="c5cd2-182">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="c5cd2-182">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





