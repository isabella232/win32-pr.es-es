---
title: función glClear (GL. h)
description: La función glClear borra los búferes de los valores preestablecidos.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- glClear (función) OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db935e46c65c42976024a8afbb98028294710c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676785"
---
# <a name="glclear-function"></a><span data-ttu-id="16924-104">glClear función)</span><span class="sxs-lookup"><span data-stu-id="16924-104">glClear function</span></span>

<span data-ttu-id="16924-105">La función **glClear** borra los búferes de los valores preestablecidos.</span><span class="sxs-lookup"><span data-stu-id="16924-105">The **glClear** function clears buffers to preset values.</span></span>

## <a name="syntax"></a><span data-ttu-id="16924-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16924-106">Syntax</span></span>


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="16924-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16924-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16924-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="16924-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="16924-109">Operadores OR bit a bit de las máscaras que indican los búferes que se van a borrar.</span><span class="sxs-lookup"><span data-stu-id="16924-109">Bitwise OR operators of masks that indicate the buffers to be cleared.</span></span> <span data-ttu-id="16924-110">Las cuatro máscaras son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="16924-110">The four masks are as follows.</span></span>



| <span data-ttu-id="16924-111">Value</span><span class="sxs-lookup"><span data-stu-id="16924-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="16924-112">Significado</span><span class="sxs-lookup"><span data-stu-id="16924-112">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <span data-ttu-id="16924-113"><dt>**\_bit de \_ búfer de color de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16924-113"><dt>**GL\_COLOR\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="16924-114">Búferes habilitados actualmente para la escritura de color.</span><span class="sxs-lookup"><span data-stu-id="16924-114">The buffers currently enabled for color writing.</span></span><br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <span data-ttu-id="16924-115"><dt>**\_bit de \_ búfer de profundidad de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16924-115"><dt>**GL\_DEPTH\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="16924-116">Búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="16924-116">The depth buffer.</span></span><br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <span data-ttu-id="16924-117"><dt>**\_bit de \_ búfer de acumulación de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16924-117"><dt>**GL\_ACCUM\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="16924-118">Búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="16924-118">The accumulation buffer.</span></span><br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <span data-ttu-id="16924-119"><dt>**\_bit de \_ búfer de estarcido GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16924-119"><dt>**GL\_STENCIL\_BUFFER\_BIT**</dt></span></span> </dl> | <span data-ttu-id="16924-120">Búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="16924-120">The stencil buffer.</span></span><br/>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16924-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16924-121">Return value</span></span>

<span data-ttu-id="16924-122">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="16924-122">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="16924-123">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="16924-123">Error codes</span></span>

<span data-ttu-id="16924-124">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="16924-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="16924-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="16924-125">Name</span></span>                                                                                                  | <span data-ttu-id="16924-126">Significado</span><span class="sxs-lookup"><span data-stu-id="16924-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="16924-127"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16924-127"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="16924-128">Cualquier otro bit que no sea los cuatro bits definidos se estableció en *Mask*.</span><span class="sxs-lookup"><span data-stu-id="16924-128">Any bit other than the four defined bits was set in *mask*.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="16924-129"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16924-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="16924-130">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="16924-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="16924-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16924-131">Remarks</span></span>

<span data-ttu-id="16924-132">La función **glClear** establece el área Bitplane de la ventana en valores previamente seleccionados por [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)y [**glClearAccum**](glclearaccum.md).</span><span class="sxs-lookup"><span data-stu-id="16924-132">The **glClear** function sets the bitplane area of the window to values previously selected by [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), and [**glClearAccum**](glclearaccum.md).</span></span> <span data-ttu-id="16924-133">Puede borrar varios búferes de color simultáneamente seleccionando más de un búfer a la vez mediante [**glDrawBuffer**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="16924-133">You can clear multiple color buffers simultaneously by selecting more than one buffer at a time using [**glDrawBuffer**](gldrawbuffer.md).</span></span>

<span data-ttu-id="16924-134">La prueba de propiedad de píxeles, la prueba de tijera, la interpolación y el writemasks de búfer afectan al funcionamiento de **glClear**.</span><span class="sxs-lookup"><span data-stu-id="16924-134">The pixel-ownership test, the scissor test, dithering, and the buffer writemasks affect the operation of **glClear**.</span></span> <span data-ttu-id="16924-135">El cuadro de tijera delimita la región borrada.</span><span class="sxs-lookup"><span data-stu-id="16924-135">The scissor box bounds the cleared region.</span></span> <span data-ttu-id="16924-136">La función **glClear** omite la función alfa, la función Blend, la operación lógica, el estarcido, la asignación de textura y el almacenamiento en búfer *z*.</span><span class="sxs-lookup"><span data-stu-id="16924-136">The **glClear** function ignores the alpha function, blend function, logical operation, stenciling, texture mapping, and *z*-buffering.</span></span>

<span data-ttu-id="16924-137">La función **glClear** toma un solo argumento (*Mask*) que es la operación OR bit a bit de varios valores que indican qué búfer se va a borrar.</span><span class="sxs-lookup"><span data-stu-id="16924-137">The **glClear** function takes a single argument (*mask*) that is the bitwise OR of several values indicating which buffer is to be cleared.</span></span>

<span data-ttu-id="16924-138">El valor en el que se borra cada búfer depende de la configuración del valor sin cifrar para ese búfer.</span><span class="sxs-lookup"><span data-stu-id="16924-138">The value to which each buffer is cleared depends on the setting of the clear value for that buffer.</span></span>

<span data-ttu-id="16924-139">Si no hay ningún búfer, una llamada a **glClear** dirigida a ese búfer no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="16924-139">If a buffer is not present, a **glClear** call directed at that buffer has no effect.</span></span>

<span data-ttu-id="16924-140">Las siguientes funciones recuperan información relacionada con **glClear**:</span><span class="sxs-lookup"><span data-stu-id="16924-140">The following functions retrieve information related to **glClear**:</span></span>

<span data-ttu-id="16924-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ valor Clear acumulado de GL \_</span><span class="sxs-lookup"><span data-stu-id="16924-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="16924-142">**glGet** con valor de profundidad de GL de argumento \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="16924-142">**glGet** with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

<span data-ttu-id="16924-143">**glGet** con el argumento \_ \_ valor sin formato de índice de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="16924-143">**glGet** with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="16924-144">**glGet** con el argumento \_ GL \_ color \_ valor sin formato</span><span class="sxs-lookup"><span data-stu-id="16924-144">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

<span data-ttu-id="16924-145">**glGet** con el argumento \_ GL \_ \_ valor sin formato de estarcido</span><span class="sxs-lookup"><span data-stu-id="16924-145">**glGet** with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="16924-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16924-146">Requirements</span></span>



| <span data-ttu-id="16924-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="16924-147">Requirement</span></span> | <span data-ttu-id="16924-148">Value</span><span class="sxs-lookup"><span data-stu-id="16924-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16924-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16924-149">Minimum supported client</span></span><br/> | <span data-ttu-id="16924-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="16924-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="16924-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16924-151">Minimum supported server</span></span><br/> | <span data-ttu-id="16924-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="16924-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="16924-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16924-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="16924-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="16924-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="16924-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16924-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="16924-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16924-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="16924-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="16924-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16924-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16924-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16924-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="16924-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16924-160">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="16924-160">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="16924-161">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="16924-161">**glClearColor**</span></span>](glclearcolor.md)
</dt> <dt>

[<span data-ttu-id="16924-162">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="16924-162">**glClearDepth**</span></span>](glcleardepth.md)
</dt> <dt>

[<span data-ttu-id="16924-163">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="16924-163">**glClearIndex**</span></span>](glclearindex.md)
</dt> <dt>

[<span data-ttu-id="16924-164">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="16924-164">**glClearStencil**</span></span>](glclearstencil.md)
</dt> <dt>

[<span data-ttu-id="16924-165">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="16924-165">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="16924-166">**glGet**</span><span class="sxs-lookup"><span data-stu-id="16924-166">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="16924-167">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="16924-167">**glScissor**</span></span>](glscissor.md)
</dt> </dl>

 

 





