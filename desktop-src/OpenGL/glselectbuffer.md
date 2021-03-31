---
title: función glSelectBuffer (GL. h)
description: La función glSelectBuffer establece un búfer para los valores del modo de selección.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- glSelectBuffer (función) OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801178"
---
# <a name="glselectbuffer-function"></a><span data-ttu-id="48263-104">glSelectBuffer función)</span><span class="sxs-lookup"><span data-stu-id="48263-104">glSelectBuffer function</span></span>

<span data-ttu-id="48263-105">La función **glSelectBuffer** establece un búfer para los valores del modo de selección.</span><span class="sxs-lookup"><span data-stu-id="48263-105">The **glSelectBuffer** function establishes a buffer for selection mode values.</span></span>

## <a name="syntax"></a><span data-ttu-id="48263-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48263-106">Syntax</span></span>


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="48263-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48263-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48263-108">*size*</span><span class="sxs-lookup"><span data-stu-id="48263-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="48263-109">Tamaño del *búfer*.</span><span class="sxs-lookup"><span data-stu-id="48263-109">The size of *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="48263-110">*búfer*</span><span class="sxs-lookup"><span data-stu-id="48263-110">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="48263-111">Devuelve los datos de la selección.</span><span class="sxs-lookup"><span data-stu-id="48263-111">Returns the selection data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48263-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48263-112">Return value</span></span>

<span data-ttu-id="48263-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="48263-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="48263-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="48263-114">Error codes</span></span>

<span data-ttu-id="48263-115">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="48263-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="48263-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="48263-116">Name</span></span>                                                                                                  | <span data-ttu-id="48263-117">Significado</span><span class="sxs-lookup"><span data-stu-id="48263-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48263-118"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="48263-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="48263-119">*el tamaño* era negativo.</span><span class="sxs-lookup"><span data-stu-id="48263-119">*size* was negative.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="48263-120"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="48263-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="48263-121">Se llamó a la función mientras que el modo de representación era GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="48263-121">The function was called while the render mode was GL\_SELECT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="48263-122"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="48263-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="48263-123">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="48263-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="48263-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48263-124">Remarks</span></span>

<span data-ttu-id="48263-125">La función **glSelectBuffer** tiene dos parámetros: *buffer* es un puntero a una matriz de enteros sin signo y *size* indica el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="48263-125">The **glSelectBuffer** function has two parameters: *buffer* is a pointer to an array of unsigned integers, and *size* indicates the size of the array.</span></span> <span data-ttu-id="48263-126">El parámetro *buffer* devuelve valores de la pila de nombres (consulte [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) cuando el modo de representación es GL \_ Select (vea [**glRenderMode**](glrendermode.md)).</span><span class="sxs-lookup"><span data-stu-id="48263-126">The *buffer* parameter returns values from the name stack (see [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) when the rendering mode is GL\_SELECT (see [**glRenderMode**](glrendermode.md)).</span></span> <span data-ttu-id="48263-127">Se debe emitir la función **glSelectBuffer** antes de que esté habilitado el modo de selección, y no debe emitirse mientras el modo de representación sea Select de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="48263-127">The **glSelectBuffer** function must be issued before selection mode is enabled, and it must not be issued while the rendering mode is GL\_SELECT.</span></span>

<span data-ttu-id="48263-128">Un programador utiliza la selección para determinar qué primitivas se dibujan en alguna región de una ventana.</span><span class="sxs-lookup"><span data-stu-id="48263-128">Selection is used by a programmer to determine which primitives are drawn into some region of a window.</span></span> <span data-ttu-id="48263-129">La región se define mediante las matrices MODELVIEW y Perspective actuales.</span><span class="sxs-lookup"><span data-stu-id="48263-129">The region is defined by the current modelview and perspective matrices.</span></span>

<span data-ttu-id="48263-130">En el modo de selección, no se generan fragmentos de píxeles desde la rasterización.</span><span class="sxs-lookup"><span data-stu-id="48263-130">In selection mode, no pixel fragments are produced from rasterization.</span></span> <span data-ttu-id="48263-131">En su lugar, si una primitiva forma una intersección con el volumen de clip definido por el frustum de visualización y los planos de recorte definidos por el usuario, este primitivo provocará un acierto de la selección.</span><span class="sxs-lookup"><span data-stu-id="48263-131">Instead, if a primitive intersects the clip volume defined by the viewing frustum and the user-defined clipping planes, this primitive causes a selection hit.</span></span> <span data-ttu-id="48263-132">(Con polígonos, no se produce ninguna interrupción si se selecciona el polígono). Cuando se realiza un cambio en la pila de nombres, o cuando se llama a [**glRenderMode**](glrendermode.md) , se copia un registro de aciertos en el *búfer* si se ha producido algún acierto desde el último evento de este tipo (un cambio en la pila de nombres o una llamada a **glRenderMode** ).</span><span class="sxs-lookup"><span data-stu-id="48263-132">(With polygons, no hit occurs if the polygon is culled.) When a change is made to the name stack, or when [**glRenderMode**](glrendermode.md) is called, a hit record is copied to *buffer* if any hits have occurred since the last such event (either a name stack change or a **glRenderMode** call).</span></span> <span data-ttu-id="48263-133">El registro de aciertos consta del número de nombres en la pila de nombres en el momento del evento; seguido de los valores de profundidad máximo y mínimo de todos los vértices que se alcanzaron desde el evento anterior; seguido del nombre de la pila de nombres, el nombre de la parte inferior en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="48263-133">The hit record consists of the number of names in the name stack at the time of the event; followed by the minimum and maximum depth values of all vertices that hit since the previous event; followed by the name stack contents, bottom name first.</span></span>

<span data-ttu-id="48263-134">Los valores devueltos de profundidad se asignan de modo que el valor entero sin signo más grande se corresponde con la profundidad de coordenadas de la ventana 1,0 y cero corresponde a profundidad de coordenadas de la ventana 0,0.</span><span class="sxs-lookup"><span data-stu-id="48263-134">Returned depth values are mapped such that the largest unsigned integer value corresponds to window coordinate depth 1.0, and zero corresponds to window coordinate depth 0.0.</span></span>

<span data-ttu-id="48263-135">Un índice interno en el *búfer* se restablece en cero siempre que se especifica el modo de selección.</span><span class="sxs-lookup"><span data-stu-id="48263-135">An internal index into *buffer* is reset to zero whenever selection mode is entered.</span></span> <span data-ttu-id="48263-136">Cada vez que se copia un registro de aciertos en el *búfer*, el índice se incrementa para apuntar a la celda que se encuentra justo después del final del bloque de namesthat, a la siguiente celda disponible.</span><span class="sxs-lookup"><span data-stu-id="48263-136">Each time a hit record is copied into *buffer*, the index is incremented to point to the cell just past the end of the block of namesthat is, to the next available cell.</span></span> <span data-ttu-id="48263-137">Si el registro de aciertos es mayor que el número de ubicaciones restantes en el *búfer*, se copian tantos datos como quepan y se establece la marca de desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="48263-137">If the hit record is larger than the number of remaining locations in *buffer*, as much data as can fit is copied, and the overflow flag is set.</span></span> <span data-ttu-id="48263-138">Si la pila de nombres está vacía cuando se copia un registro de aciertos, dicho registro consta de cero seguido de los valores de profundidad mínimo y máximo.</span><span class="sxs-lookup"><span data-stu-id="48263-138">If the name stack is empty when a hit record is copied, that record consists of zero followed by the minimum and maximum depth values.</span></span>

<span data-ttu-id="48263-139">El modo de selección se termina llamando a **glRenderMode** con un argumento distinto de GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="48263-139">Selection mode is exited by calling **glRenderMode** with an argument other than GL\_SELECT.</span></span> <span data-ttu-id="48263-140">Siempre que se llama a **glRenderMode** mientras el modo de representación es GL \_ Select, devuelve el número de registros de aciertos copiados en el *búfer*, restablece la marca de desbordamiento y el puntero del búfer de selección e inicializa la pila de nombres para que esté vacía.</span><span class="sxs-lookup"><span data-stu-id="48263-140">Whenever **glRenderMode** is called while the render mode is GL\_SELECT, it returns the number of hit records copied to *buffer*, resets the overflow flag and the selection buffer pointer, and initializes the name stack to be empty.</span></span> <span data-ttu-id="48263-141">Si se estableció el bit de desbordamiento cuando se llamó a **glRenderMode** , se devuelve un número de registros de aciertos negativos.</span><span class="sxs-lookup"><span data-stu-id="48263-141">If the overflow bit was set when **glRenderMode** was called, a negative hit record count is returned.</span></span>

<span data-ttu-id="48263-142">El contenido del *búfer* no está definido hasta que se llame a [**glRenderMode**](glrendermode.md) con un argumento distinto de \_ la selección de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="48263-142">The contents of *buffer* are undefined until [**glRenderMode**](glrendermode.md) is called with an argument other than GL\_SELECT.</span></span>

<span data-ttu-id="48263-143">Las primitivas de **glBegin** / **glEnd** y las llamadas a [**glRasterPos**](glrasterpos-functions.md) pueden dar lugar a aciertos.</span><span class="sxs-lookup"><span data-stu-id="48263-143">The **glBegin**/**glEnd** primitives and calls to [**glRasterPos**](glrasterpos-functions.md) can result in hits.</span></span>

<span data-ttu-id="48263-144">La siguiente función recupera información relacionada con **glSelectBuffer**:</span><span class="sxs-lookup"><span data-stu-id="48263-144">The following function retrieves information related to **glSelectBuffer**:</span></span>

<span data-ttu-id="48263-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento de profundidad de la pila de nombre del libro \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="48263-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="48263-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48263-146">Requirements</span></span>



| <span data-ttu-id="48263-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="48263-147">Requirement</span></span> | <span data-ttu-id="48263-148">Value</span><span class="sxs-lookup"><span data-stu-id="48263-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48263-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48263-149">Minimum supported client</span></span><br/> | <span data-ttu-id="48263-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="48263-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="48263-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48263-151">Minimum supported server</span></span><br/> | <span data-ttu-id="48263-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="48263-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48263-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48263-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="48263-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="48263-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="48263-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48263-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="48263-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48263-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="48263-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48263-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48263-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48263-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48263-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="48263-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48263-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="48263-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="48263-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="48263-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="48263-162">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="48263-162">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="48263-163">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="48263-163">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="48263-164">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="48263-164">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="48263-165">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="48263-165">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="48263-166">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="48263-166">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





