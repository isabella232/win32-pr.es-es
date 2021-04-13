---
title: función glLogicOp (GL. h)
description: La función glLogicOp especifica una operación de píxeles lógicos para la representación del índice de color.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- glLogicOp (función) OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535512"
---
# <a name="gllogicop-function"></a><span data-ttu-id="dfacd-104">glLogicOp función)</span><span class="sxs-lookup"><span data-stu-id="dfacd-104">glLogicOp function</span></span>

<span data-ttu-id="dfacd-105">La función **glLogicOp** especifica una operación de píxeles lógicos para la representación del índice de color.</span><span class="sxs-lookup"><span data-stu-id="dfacd-105">The **glLogicOp** function specifies a logical pixel operation for color index rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfacd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfacd-106">Syntax</span></span>


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a><span data-ttu-id="dfacd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dfacd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfacd-108">*Código*</span><span class="sxs-lookup"><span data-stu-id="dfacd-108">*opcode*</span></span> 
</dt> <dd>

<span data-ttu-id="dfacd-109">Una constante simbólica que selecciona una operación lógica.</span><span class="sxs-lookup"><span data-stu-id="dfacd-109">A symbolic constant that selects a logical operation.</span></span> <span data-ttu-id="dfacd-110">Los siguientes símbolos se aceptan donde s es igual al valor del bit de origen y d es el valor del bit de destino.</span><span class="sxs-lookup"><span data-stu-id="dfacd-110">The following symbols are accepted where s equals the value of the source bit and d is the value of the destination bit.</span></span>



| <span data-ttu-id="dfacd-111">Value</span><span class="sxs-lookup"><span data-stu-id="dfacd-111">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="dfacd-112">Significado</span><span class="sxs-lookup"><span data-stu-id="dfacd-112">Meaning</span></span>              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <span data-ttu-id="dfacd-113"><dt>**\_borrado de contabilidad**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-113"><dt>**GL\_CLEAR**</dt></span></span> </dl>                          | <span data-ttu-id="dfacd-114">0</span><span class="sxs-lookup"><span data-stu-id="dfacd-114">0</span></span><br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <span data-ttu-id="dfacd-115"><dt>**conjunto de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-115"><dt>**GL\_SET**</dt></span></span> </dl>                                | <span data-ttu-id="dfacd-116">1</span><span class="sxs-lookup"><span data-stu-id="dfacd-116">1</span></span><br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <span data-ttu-id="dfacd-117"><dt>**copia en GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-117"><dt>**GL\_COPY**</dt></span></span> </dl>                             | <span data-ttu-id="dfacd-118">s</span><span class="sxs-lookup"><span data-stu-id="dfacd-118">s</span></span><br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <span data-ttu-id="dfacd-119"><dt>**copia en contab \_ \_ invertida**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-119"><dt>**GL\_COPY\_INVERTED**</dt></span></span> </dl> | <span data-ttu-id="dfacd-120">! s</span><span class="sxs-lookup"><span data-stu-id="dfacd-120">!s</span></span><br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <span data-ttu-id="dfacd-121"><dt>**NOOP de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-121"><dt>**GL\_NOOP**</dt></span></span> </dl>                             | <span data-ttu-id="dfacd-122">d</span><span class="sxs-lookup"><span data-stu-id="dfacd-122">d</span></span><br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="dfacd-123"><dt>**inversión en contab \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-123"><dt>**GL\_INVERT**</dt></span></span> </dl>                       | <span data-ttu-id="dfacd-124">! d</span><span class="sxs-lookup"><span data-stu-id="dfacd-124">!d</span></span><br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <span data-ttu-id="dfacd-125"><dt>**GL \_ y**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-125"><dt>**GL\_AND**</dt></span></span> </dl>                                | <span data-ttu-id="dfacd-126">s & d</span><span class="sxs-lookup"><span data-stu-id="dfacd-126">s & d</span></span><br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <span data-ttu-id="dfacd-127"><dt>**CC \_ NAND**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-127"><dt>**GL\_NAND**</dt></span></span> </dl>                             | <span data-ttu-id="dfacd-128">! (s & d)</span><span class="sxs-lookup"><span data-stu-id="dfacd-128">!(s & d)</span></span><br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <span data-ttu-id="dfacd-129"><dt>**GL \_ o**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-129"><dt>**GL\_OR**</dt></span></span> </dl>                                   | <span data-ttu-id="dfacd-130">s \| d</span><span class="sxs-lookup"><span data-stu-id="dfacd-130">s \| d</span></span><br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <span data-ttu-id="dfacd-131"><dt>**GL \_ y**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-131"><dt>**GL\_NOR**</dt></span></span> </dl>                                | <span data-ttu-id="dfacd-132">! (s \| d)</span><span class="sxs-lookup"><span data-stu-id="dfacd-132">!(s \| d)</span></span><br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <span data-ttu-id="dfacd-133"><dt>**cont. de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-133"><dt>**GL\_XOR**</dt></span></span> </dl>                                | <span data-ttu-id="dfacd-134">s ^ d</span><span class="sxs-lookup"><span data-stu-id="dfacd-134">s ^ d</span></span><br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <span data-ttu-id="dfacd-135"><dt>**EQUIV. cont. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-135"><dt>**GL\_EQUIV**</dt></span></span> </dl>                          | <span data-ttu-id="dfacd-136">! (s ^ d)</span><span class="sxs-lookup"><span data-stu-id="dfacd-136">!(s ^ d)</span></span><br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <span data-ttu-id="dfacd-137"><dt>**GL \_ e \_ inverso**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-137"><dt>**GL\_AND\_REVERSE**</dt></span></span> </dl>       | <span data-ttu-id="dfacd-138">s &! d</span><span class="sxs-lookup"><span data-stu-id="dfacd-138">s & !d</span></span><br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <span data-ttu-id="dfacd-139"><dt>**GL \_ y \_ invertido**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-139"><dt>**GL\_AND\_INVERTED**</dt></span></span> </dl>    | <span data-ttu-id="dfacd-140">! s & d</span><span class="sxs-lookup"><span data-stu-id="dfacd-140">!s & d</span></span><br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <span data-ttu-id="dfacd-141"><dt>**GL \_ o \_ inverso**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-141"><dt>**GL\_OR\_REVERSE**</dt></span></span> </dl>          | <span data-ttu-id="dfacd-142">s \| ! d</span><span class="sxs-lookup"><span data-stu-id="dfacd-142">s \| !d</span></span><br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <span data-ttu-id="dfacd-143"><dt>**GL \_ o \_ invertido**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-143"><dt>**GL\_OR\_INVERTED**</dt></span></span> </dl>       | <span data-ttu-id="dfacd-144">! s \| d</span><span class="sxs-lookup"><span data-stu-id="dfacd-144">!s \| d</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfacd-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfacd-145">Return value</span></span>

<span data-ttu-id="dfacd-146">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dfacd-146">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dfacd-147">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="dfacd-147">Error codes</span></span>

<span data-ttu-id="dfacd-148">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="dfacd-148">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="dfacd-149">Nombre</span><span class="sxs-lookup"><span data-stu-id="dfacd-149">Name</span></span>                                                                                                  | <span data-ttu-id="dfacd-150">Significado</span><span class="sxs-lookup"><span data-stu-id="dfacd-150">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfacd-151"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-151"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="dfacd-152">*OpCode* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="dfacd-152">*opcode* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="dfacd-153"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="dfacd-154">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="dfacd-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dfacd-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfacd-155">Remarks</span></span>

<span data-ttu-id="dfacd-156">La función **glLogicOp** especifica una operación lógica que, cuando se habilita, se aplica entre el índice de color entrante y el índice de color en la ubicación correspondiente en fotogramas.</span><span class="sxs-lookup"><span data-stu-id="dfacd-156">The **glLogicOp** function specifies a logical operation that, when enabled, is applied between the incoming color index and the color index at the corresponding location in the framebuffer.</span></span> <span data-ttu-id="dfacd-157">La operación lógica está habilitada o deshabilitada con [**glEnable**](glenable.md) y **glDisable** con la constante simbólica de la lógica de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dfacd-157">The logical operation is enabled or disabled with [**glEnable**](glenable.md) and **glDisable** using the symbolic constant GL\_LOGIC\_OP.</span></span>

<span data-ttu-id="dfacd-158">El parámetro *OpCode* es una constante simbólica elegida en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="dfacd-158">The *opcode* parameter is a symbolic constant chosen from the list below.</span></span> <span data-ttu-id="dfacd-159">En la explicación de las operaciones lógicas, *s* representa el índice de color entrante y *d* representa el índice en fotogramas.</span><span class="sxs-lookup"><span data-stu-id="dfacd-159">In the explanation of the logical operations, *s* represents the incoming color index and *d* represents the index in the framebuffer.</span></span> <span data-ttu-id="dfacd-160">Se usan los operadores estándar de lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="dfacd-160">Standard C-language operators are used.</span></span> <span data-ttu-id="dfacd-161">Como sugieren estos operadores bit a bit, la operación lógica se aplica independientemente a cada par de bits de los índices de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="dfacd-161">As these bitwise operators suggest, the logical operation is applied independently to each bit pair of the source and destination indexes.</span></span>

<span data-ttu-id="dfacd-162">Las operaciones de píxeles lógicos no se aplican a los búferes de color RGBA.</span><span class="sxs-lookup"><span data-stu-id="dfacd-162">Logical pixel operations are not applied to RGBA color buffers.</span></span>

<span data-ttu-id="dfacd-163">Cuando se habilita más de un búfer de índice de color para dibujar, las operaciones lógicas se realizan por separado para cada búfer habilitado, utilizando el contenido de ese búfer para el índice de destino (vea [**glDrawBuffer**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="dfacd-163">When more than one color-index buffer is enabled for drawing, logical operations are done separately for each enabled buffer, using the contents of that buffer for the destination index (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span>

<span data-ttu-id="dfacd-164">El parámetro *OpCode* debe ser uno de los 16 valores aceptados.</span><span class="sxs-lookup"><span data-stu-id="dfacd-164">The *opcode* parameter must be one of the 16 accepted values.</span></span> <span data-ttu-id="dfacd-165">Otros valores producen un error.</span><span class="sxs-lookup"><span data-stu-id="dfacd-165">Other values result in an error.</span></span>

<span data-ttu-id="dfacd-166">Las siguientes funciones recuperan información relacionada con **glLogicOp**:</span><span class="sxs-lookup"><span data-stu-id="dfacd-166">The following functions retrieve information related to **glLogicOp**:</span></span>

<span data-ttu-id="dfacd-167">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de \_ OP \_ Logic de contabilidad de argumentos</span><span class="sxs-lookup"><span data-stu-id="dfacd-167">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LOGIC\_OP\_MODE</span></span>

<span data-ttu-id="dfacd-168">[**glIsEnabled**](glisenabled.md) con el argumento \_ OP lógica de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="dfacd-168">[**glIsEnabled**](glisenabled.md) with argument GL\_LOGIC\_OP</span></span>

## <a name="requirements"></a><span data-ttu-id="dfacd-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfacd-169">Requirements</span></span>



| <span data-ttu-id="dfacd-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfacd-170">Requirement</span></span> | <span data-ttu-id="dfacd-171">Value</span><span class="sxs-lookup"><span data-stu-id="dfacd-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfacd-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfacd-172">Minimum supported client</span></span><br/> | <span data-ttu-id="dfacd-173">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dfacd-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dfacd-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfacd-174">Minimum supported server</span></span><br/> | <span data-ttu-id="dfacd-175">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dfacd-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dfacd-176">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dfacd-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfacd-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="dfacd-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dfacd-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="dfacd-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dfacd-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dfacd-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfacd-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfacd-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfacd-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfacd-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfacd-183">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="dfacd-183">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="dfacd-184">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="dfacd-184">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="dfacd-185">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="dfacd-185">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="dfacd-186">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="dfacd-186">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="dfacd-187">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="dfacd-187">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="dfacd-188">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="dfacd-188">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="dfacd-189">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="dfacd-189">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="dfacd-190">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="dfacd-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





