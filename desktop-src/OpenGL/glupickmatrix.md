---
title: función gluPickMatrix (GLU. h)
description: La función gluPickMatrix define una región de picking.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- gluPickMatrix (función) OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c54e62f82f52fedc7de7c7c4af1cd3ed1ccdf149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995905"
---
# <a name="glupickmatrix-function"></a><span data-ttu-id="52681-104">gluPickMatrix función)</span><span class="sxs-lookup"><span data-stu-id="52681-104">gluPickMatrix function</span></span>

<span data-ttu-id="52681-105">La función **gluPickMatrix** define una región de picking.</span><span class="sxs-lookup"><span data-stu-id="52681-105">The **gluPickMatrix** function defines a picking region.</span></span>

## <a name="syntax"></a><span data-ttu-id="52681-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52681-106">Syntax</span></span>


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="52681-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52681-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52681-108">*x*</span><span class="sxs-lookup"><span data-stu-id="52681-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="52681-109">La coordenada x de la ventana de una región de picking.</span><span class="sxs-lookup"><span data-stu-id="52681-109">The x window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="52681-110">*y*</span><span class="sxs-lookup"><span data-stu-id="52681-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="52681-111">La coordenada de la ventana y de una región de picking.</span><span class="sxs-lookup"><span data-stu-id="52681-111">The y window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="52681-112">*height*</span><span class="sxs-lookup"><span data-stu-id="52681-112">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="52681-113">Alto de la región de selección en coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="52681-113">The height of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="52681-114">*width*</span><span class="sxs-lookup"><span data-stu-id="52681-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="52681-115">Ancho de la región de selección en coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="52681-115">The width of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="52681-116">*encuadre*</span><span class="sxs-lookup"><span data-stu-id="52681-116">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="52681-117">La ventanilla actual (a partir de una llamada a [**glGetIntegerv**](glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="52681-117">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52681-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52681-118">Return value</span></span>

<span data-ttu-id="52681-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="52681-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52681-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52681-120">Remarks</span></span>

<span data-ttu-id="52681-121">La función **gluPickMatrix** crea una matriz de proyección que puede usar para restringir el dibujo a una región pequeña de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="52681-121">The **gluPickMatrix** function creates a projection matrix you can use to restrict drawing to a small region of the viewport.</span></span>

1.  <span data-ttu-id="52681-122">Use **gluPickMatrix** para restringir el dibujo a una región pequeña alrededor del cursor.</span><span class="sxs-lookup"><span data-stu-id="52681-122">Use **gluPickMatrix** to restrict drawing to a small region around the cursor.</span></span>
2.  <span data-ttu-id="52681-123">Escriba el modo de selección (con [**glRenderMode**](glrendermode.md)) y, a continuación, represente la escena.</span><span class="sxs-lookup"><span data-stu-id="52681-123">Enter selection mode (with [**glRenderMode**](glrendermode.md)), and then rerender the scene.</span></span>

    <span data-ttu-id="52681-124">Todos los primitivos que se habrían dibujado cerca del cursor se identifican y almacenan en el búfer de selección.</span><span class="sxs-lookup"><span data-stu-id="52681-124">All primitives that would have been drawn near the cursor are identified and stored in the selection buffer.</span></span>

<span data-ttu-id="52681-125">La matriz creada por **gluPickMatrix** se multiplica por la matriz actual como si se llamara a [**glMultMatrix**](glmultmatrix.md) con la matriz generada.</span><span class="sxs-lookup"><span data-stu-id="52681-125">The matrix created by **gluPickMatrix** is multiplied by the current matrix just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span>

1.  <span data-ttu-id="52681-126">Llame a [**glLoadIdentity**](glloadidentity.md) para cargar una matriz de identidad en la pila de la matriz de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="52681-126">Call [**glLoadIdentity**](glloadidentity.md) to load an identity matrix onto the perspective matrix stack.</span></span>
2.  <span data-ttu-id="52681-127">Llame a **gluPickMatrix**.</span><span class="sxs-lookup"><span data-stu-id="52681-127">Call **gluPickMatrix**.</span></span>
3.  <span data-ttu-id="52681-128">Llame a una función (como [**gluPerspective**](gluperspective.md)) para multiplicar la matriz de perspectiva por la matriz de picking.</span><span class="sxs-lookup"><span data-stu-id="52681-128">Call a function (such as [**gluPerspective**](gluperspective.md)) to multiply the perspective matrix by the pick matrix.</span></span>

<span data-ttu-id="52681-129">Al usar **gluPickMatrix** para elegir la spline B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme, tenga cuidado de desactivar la propiedad NURBS, Glu \_ \_ autoload \_ Matrix.</span><span class="sxs-lookup"><span data-stu-id="52681-129">When using **gluPickMatrix** to pick Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)), be careful to turn off the NURBS property, GLU\_AUTO\_LOAD\_MATRIX.</span></span> <span data-ttu-id="52681-130">Si \_ \_ \_ la matriz de carga automática de Glu no está desactivada, cualquier superficie de NURBS presentada se subdivide de manera diferente con la matriz de picking de cómo se subdividió sin la matriz de picking.</span><span class="sxs-lookup"><span data-stu-id="52681-130">If GLU\_AUTO\_LOAD\_MATRIX is not turned off, any NURBS surface rendered is subdivided differently with the pick matrix from how it was subdivided without the pick matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="52681-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="52681-131">Examples</span></span>

<span data-ttu-id="52681-132">Al representar una escena de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="52681-132">When rendering a scene as follows:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



<span data-ttu-id="52681-133">el código siguiente selecciona una parte de la ventanilla:</span><span class="sxs-lookup"><span data-stu-id="52681-133">the following code selects a portion of the viewport:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a><span data-ttu-id="52681-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52681-134">Requirements</span></span>



| <span data-ttu-id="52681-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="52681-135">Requirement</span></span> | <span data-ttu-id="52681-136">Value</span><span class="sxs-lookup"><span data-stu-id="52681-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52681-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52681-137">Minimum supported client</span></span><br/> | <span data-ttu-id="52681-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="52681-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="52681-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52681-139">Minimum supported server</span></span><br/> | <span data-ttu-id="52681-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="52681-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="52681-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52681-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="52681-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="52681-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="52681-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52681-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="52681-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52681-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="52681-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52681-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52681-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52681-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52681-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="52681-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52681-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="52681-148">**glGetIntegerv**</span></span>](glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="52681-149">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="52681-149">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="52681-150">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="52681-150">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="52681-151">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="52681-151">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="52681-152">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="52681-152">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





