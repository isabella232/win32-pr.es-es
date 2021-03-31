---
title: función glAccum (GL. h)
description: La función glAccum funciona en el búfer de acumulación.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- glAccum (función) OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802611"
---
# <a name="glaccum-function"></a><span data-ttu-id="5bb50-104">glAccum función)</span><span class="sxs-lookup"><span data-stu-id="5bb50-104">glAccum function</span></span>

<span data-ttu-id="5bb50-105">La función **glAccum** funciona en el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="5bb50-105">The **glAccum** function operates on the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb50-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bb50-106">Syntax</span></span>


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a><span data-ttu-id="5bb50-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bb50-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bb50-108">*operador*</span><span class="sxs-lookup"><span data-stu-id="5bb50-108">*op*</span></span> 
</dt> <dd>

<span data-ttu-id="5bb50-109">Operación de búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="5bb50-109">The accumulation buffer operation.</span></span> <span data-ttu-id="5bb50-110">Las constantes simbólicas aceptadas son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="5bb50-110">The accepted symbolic constants are as follows.</span></span>



| <span data-ttu-id="5bb50-111">Value</span><span class="sxs-lookup"><span data-stu-id="5bb50-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="5bb50-112">Significado</span><span class="sxs-lookup"><span data-stu-id="5bb50-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <span data-ttu-id="5bb50-113"><dt>**LIBRO \_ acumulado**</dt></span><span class="sxs-lookup"><span data-stu-id="5bb50-113"><dt>**GL\_ACCUM**</dt></span></span> </dl>    | <span data-ttu-id="5bb50-114">Obtiene R, G, B y un valor del búfer seleccionado actualmente para lectura (vea [**glReadBuffer**](glreadbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="5bb50-114">Obtains R, G, B, and A values from the buffer currently selected for reading (see [**glReadBuffer**](glreadbuffer.md)).</span></span> <span data-ttu-id="5bb50-115">Cada valor de componente se divide por 2 *n*  1, donde *n* es el número de bits asignados a cada componente de color en el búfer seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="5bb50-115">Each component value is divided by 2 *n*  1, where *n* is the number of bits allocated to each color component in the currently selected buffer.</span></span> <span data-ttu-id="5bb50-116">El resultado es un valor de punto flotante en el intervalo de \[ 0, 1 \] , que se multiplica por *valor* y se agrega al componente de píxel correspondiente en el búfer de acumulación, con lo que se actualiza el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="5bb50-116">The result is a floating-point value in the range \[0,1\], which is multiplied by *value* and added to the corresponding pixel component in the accumulation buffer, thereby updating the accumulation buffer.</span></span><br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <span data-ttu-id="5bb50-117"><dt>**carga en contab. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5bb50-117"><dt>**GL\_LOAD**</dt></span></span> </dl>       | <span data-ttu-id="5bb50-118">Similar a GL \_ acumulado, salvo que el valor actual en el búfer de acumulación no se utiliza en el cálculo del nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="5bb50-118">Similar to GL\_ACCUM, except that the current value in the accumulation buffer is not used in the calculation of the new value.</span></span> <span data-ttu-id="5bb50-119">Es decir, los valores R, G, B y a del búfer seleccionado actualmente se dividen entre 2 *n*  1, multiplicado por *valor* y, a continuación, se almacenan en la celda del búfer de acumulación correspondiente, sobrescribiendo el valor actual.</span><span class="sxs-lookup"><span data-stu-id="5bb50-119">That is, the R, G, B, and A values from the currently selected buffer are divided by 2 *n*  1, multiplied by *value*, and then stored in the corresponding accumulation buffer cell, overwriting the current value.</span></span><br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <span data-ttu-id="5bb50-120"><dt>**\_Agregar GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5bb50-120"><dt>**GL\_ADD**</dt></span></span> </dl>          | <span data-ttu-id="5bb50-121">Agrega *valor* a cada R, G, B y a en el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="5bb50-121">Adds *value* to each R, G, B, and A in the accumulation buffer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <span data-ttu-id="5bb50-122"><dt>**\_mult**</dt></span><span class="sxs-lookup"><span data-stu-id="5bb50-122"><dt>**GL\_MULT**</dt></span></span> </dl>       | <span data-ttu-id="5bb50-123">Multiplica cada R, G, B y A en el búfer de acumulación por *valor* y devuelve el componente escalado a su ubicación de búfer de acumulación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5bb50-123">Multiplies each R, G, B, and A in the accumulation buffer by *value* and returns the scaled component to its corresponding accumulation buffer location.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <span data-ttu-id="5bb50-124"><dt>**devolución de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5bb50-124"><dt>**GL\_RETURN**</dt></span></span> </dl> | <span data-ttu-id="5bb50-125">Transfiere los valores del búfer de acumulación al búfer de color o a los búferes seleccionados actualmente para escritura.</span><span class="sxs-lookup"><span data-stu-id="5bb50-125">Transfers accumulation buffer values to the color buffer or buffers currently selected for writing.</span></span> <span data-ttu-id="5bb50-126">Cada R, G, B y un componente se multiplica por *valor* y, a continuación, se multiplica por 2 *n*  1, se fija al rango \[ 0, 2 *n*  1 \] y se almacena en la celda del búfer de presentación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5bb50-126">Each R, G, B, and A component is multiplied by *value*, then multiplied by 2 *n*  1, clamped to the range \[0, 2 *n*  1 \], and stored in the corresponding display buffer cell.</span></span> <span data-ttu-id="5bb50-127">Las únicas operaciones de fragmento que se aplican a esta transferencia son la propiedad de píxeles, las tijeras, la interpolación y el color writemasks.</span><span class="sxs-lookup"><span data-stu-id="5bb50-127">The only fragment operations that are applied to this transfer are pixel ownership, scissor, dithering, and color writemasks.</span></span><br/>                                                                        |



 

</dd> <dt>

<span data-ttu-id="5bb50-128">*value*</span><span class="sxs-lookup"><span data-stu-id="5bb50-128">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="5bb50-129">Un valor de punto flotante que se usa en la operación de búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="5bb50-129">A floating-point value used in the accumulation buffer operation.</span></span> <span data-ttu-id="5bb50-130">El parámetro *OP* determina cómo se usa *Value* .</span><span class="sxs-lookup"><span data-stu-id="5bb50-130">The *op* parameter determines how *value* is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bb50-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bb50-131">Return value</span></span>

<span data-ttu-id="5bb50-132">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5bb50-132">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5bb50-133">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5bb50-133">Error codes</span></span>

<span data-ttu-id="5bb50-134">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="5bb50-134">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5bb50-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="5bb50-135">Name</span></span>                                                                                                  | <span data-ttu-id="5bb50-136">Significado</span><span class="sxs-lookup"><span data-stu-id="5bb50-136">Meaning</span></span>                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5bb50-137"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5bb50-137"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5bb50-138">*OP* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="5bb50-138">*op* was not an accepted value.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="5bb50-139"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5bb50-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5bb50-140">No había ningún búfer de acumulación o se llamó a la función **glAccum** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5bb50-140">There was no accumulation buffer or the function **glAccum** was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5bb50-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bb50-141">Remarks</span></span>

<span data-ttu-id="5bb50-142">El búfer de acumulación es un búfer de color de intervalo extendido.</span><span class="sxs-lookup"><span data-stu-id="5bb50-142">The accumulation buffer is an extended-range color buffer.</span></span> <span data-ttu-id="5bb50-143">Las imágenes no se representan en ella.</span><span class="sxs-lookup"><span data-stu-id="5bb50-143">Images are not rendered into it.</span></span> <span data-ttu-id="5bb50-144">En su lugar, las imágenes representadas en uno de los búferes de color se agregan al contenido del búfer de acumulación después de la representación.</span><span class="sxs-lookup"><span data-stu-id="5bb50-144">Rather, images rendered into one of the color buffers are added to the contents of the accumulation buffer after rendering.</span></span> <span data-ttu-id="5bb50-145">Puede crear efectos como el suavizado de contorno (de puntos, líneas y polígonos), el desenfoque de movimiento y la profundidad de campo mediante la acumulación de las imágenes generadas con matrices de transformación diferentes.</span><span class="sxs-lookup"><span data-stu-id="5bb50-145">You can create effects such as antialiasing (of points, lines, and polygons), motion blur, and depth of field by accumulating images generated with different transformation matrices.</span></span>

<span data-ttu-id="5bb50-146">Cada píxel del búfer de acumulación consta de valores rojo, verde, azul y alfa.</span><span class="sxs-lookup"><span data-stu-id="5bb50-146">Each pixel in the accumulation buffer consists of red, green, blue, and alpha values.</span></span> <span data-ttu-id="5bb50-147">El número de bits por componente en el búfer de acumulación depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="5bb50-147">The number of bits per component in the accumulation buffer depends on the implementation.</span></span> <span data-ttu-id="5bb50-148">Puede examinar este número llamando a [**glGetIntegerv**](glgetintegerv.md) cuatro veces, con los argumentos los bits de color rojo acumulados en la contabilidad, los bits verdes de la acumulación de contabilidad, los bits azules acumulados en el libro de contabilidad \_ y los \_ \_ \_ \_ \_ \_ \_ \_ \_ bits alfa acumulados en el libro superior \_ \_ , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5bb50-148">You can examine this number by calling [**glGetIntegerv**](glgetintegerv.md) four times, with the arguments GL\_ACCUM\_RED\_BITS, GL\_ACCUM\_GREEN\_BITS, GL\_ACCUM\_BLUE\_BITS, and GL\_ACCUM\_ALPHA\_BITS, respectively.</span></span> <span data-ttu-id="5bb50-149">Sin embargo, independientemente del número de bits por componente, el intervalo de valores almacenados por cada componente es \[ 1,? 1 \] .</span><span class="sxs-lookup"><span data-stu-id="5bb50-149">Regardless of the number of bits per component, however, the range of values stored by each component is \[ 1,?1\].</span></span> <span data-ttu-id="5bb50-150">Los píxeles del búfer de acumulación se asignan uno a uno con fotogramas píxeles.</span><span class="sxs-lookup"><span data-stu-id="5bb50-150">The accumulation buffer pixels are mapped one-to-one with framebuffer pixels.</span></span>

<span data-ttu-id="5bb50-151">La función **glAccum** funciona en el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="5bb50-151">The **glAccum** function operates on the accumulation buffer.</span></span> <span data-ttu-id="5bb50-152">El primer argumento, *OP*, es una constante simbólica que selecciona una operación de búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="5bb50-152">The first argument, *op*, is a symbolic constant that selects an accumulation buffer operation.</span></span> <span data-ttu-id="5bb50-153">El segundo argumento, *Value*, es un valor de punto flotante que se va a usar en esa operación.</span><span class="sxs-lookup"><span data-stu-id="5bb50-153">The second argument, *value*, is a floating-point value to be used in that operation.</span></span> <span data-ttu-id="5bb50-154">Se especifican cinco operaciones: \_ Amort, GL \_ upload, GL \_ Add, GL \_ MULT y GL \_ Return.</span><span class="sxs-lookup"><span data-stu-id="5bb50-154">Five operations are specified: GL\_ACCUM, GL\_LOAD, GL\_ADD, GL\_MULT, and GL\_RETURN.</span></span>

<span data-ttu-id="5bb50-155">Todas las operaciones de búfer de acumulación se limitan al área del cuadro de tijeras actual y se aplican de forma idéntica a los componentes rojo, verde, azul y alfa de cada píxel.</span><span class="sxs-lookup"><span data-stu-id="5bb50-155">All accumulation buffer operations are limited to the area of the current scissor box and are applied identically to the red, green, blue, and alpha components of each pixel.</span></span> <span data-ttu-id="5bb50-156">El contenido de un componente de píxel del búfer de acumulación no está definido si la operación **glAccum** da como resultado un valor fuera del intervalo de \[ 1 a 1 \] .</span><span class="sxs-lookup"><span data-stu-id="5bb50-156">The contents of an accumulation buffer pixel component are undefined if the **glAccum** operation results in a value outside the range \[ 1,1\].</span></span>

<span data-ttu-id="5bb50-157">Para borrar el búfer de acumulación, utilice la función [**glClearAccum**](glclearaccum.md) para especificar R, G, B y un valor para establecerlo en, y emita una función [**glClear**](glclear.md) con el búfer de acumulación habilitado.</span><span class="sxs-lookup"><span data-stu-id="5bb50-157">To clear the accumulation buffer, use the [**glClearAccum**](glclearaccum.md) function to specify R, G, B, and A values to set it to, and issue a [**glClear**](glclear.md) function with the accumulation buffer enabled.</span></span>

<span data-ttu-id="5bb50-158">Los píxeles que se encuentren en el cuadro tijeras actuales se actualizarán con cualquier operación de **glAccum** .</span><span class="sxs-lookup"><span data-stu-id="5bb50-158">Only those pixels within the current scissor box are updated by any **glAccum** operation.</span></span>

<span data-ttu-id="5bb50-159">Las siguientes funciones recuperan información relacionada con la función **glAccum** :</span><span class="sxs-lookup"><span data-stu-id="5bb50-159">The following functions retrieve information related to the **glAccum** function:</span></span>

<span data-ttu-id="5bb50-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ bytes rojos acumulados por el libro de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="5bb50-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_RED\_BITS</span></span>

<span data-ttu-id="5bb50-161">**glGet** con el argumento \_ los \_ \_ bits verdes del libro de contabilidad</span><span class="sxs-lookup"><span data-stu-id="5bb50-161">**glGet** with argument GL\_ACCUM\_GREEN\_BITS</span></span>

<span data-ttu-id="5bb50-162">**glGet** con los \_ \_ bits azules acumulados en el libro de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="5bb50-162">**glGet** with argument GL\_ACCUM\_BLUE\_BITS</span></span>

<span data-ttu-id="5bb50-163">**glGet** con el argumento \_ \_ bytes alfa acumulados en el libro de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="5bb50-163">**glGet** with argument GL\_ACCUM\_ALPHA\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="5bb50-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bb50-164">Requirements</span></span>



| <span data-ttu-id="5bb50-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bb50-165">Requirement</span></span> | <span data-ttu-id="5bb50-166">Value</span><span class="sxs-lookup"><span data-stu-id="5bb50-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb50-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bb50-167">Minimum supported client</span></span><br/> | <span data-ttu-id="5bb50-168">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5bb50-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5bb50-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bb50-169">Minimum supported server</span></span><br/> | <span data-ttu-id="5bb50-170">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5bb50-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5bb50-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bb50-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bb50-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bb50-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5bb50-173">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5bb50-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="5bb50-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bb50-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5bb50-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5bb50-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bb50-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bb50-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bb50-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bb50-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb50-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5bb50-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5bb50-179">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="5bb50-179">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="5bb50-180">**glClear**</span><span class="sxs-lookup"><span data-stu-id="5bb50-180">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="5bb50-181">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="5bb50-181">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="5bb50-182">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="5bb50-182">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="5bb50-183">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5bb50-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5bb50-184">**glGet**</span><span class="sxs-lookup"><span data-stu-id="5bb50-184">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="5bb50-185">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="5bb50-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="5bb50-186">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="5bb50-186">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="5bb50-187">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="5bb50-187">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="5bb50-188">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="5bb50-188">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="5bb50-189">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="5bb50-189">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="5bb50-190">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="5bb50-190">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="5bb50-191">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="5bb50-191">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





