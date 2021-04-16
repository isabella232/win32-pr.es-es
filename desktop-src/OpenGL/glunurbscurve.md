---
title: función gluNurbsCurve (GLU. h)
description: La función gluNurbsCurve define la forma de una curva no uniforme B-spline (NURBS).
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- gluNurbsCurve (función) OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676689"
---
# <a name="glunurbscurve-function"></a><span data-ttu-id="092e5-104">gluNurbsCurve función)</span><span class="sxs-lookup"><span data-stu-id="092e5-104">gluNurbsCurve function</span></span>

<span data-ttu-id="092e5-105">La función **gluNurbsCurve** define la forma de una curva no uniforme B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="092e5-105">The **gluNurbsCurve** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="092e5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="092e5-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="092e5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="092e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="092e5-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="092e5-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="092e5-109">El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="092e5-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="092e5-110">*nknots*</span><span class="sxs-lookup"><span data-stu-id="092e5-110">*nknots*</span></span> 
</dt> <dd>

<span data-ttu-id="092e5-111">Número de nudos en el *nodo*.</span><span class="sxs-lookup"><span data-stu-id="092e5-111">The number of knots in *knot*.</span></span> <span data-ttu-id="092e5-112">El parámetro *nknots* es igual al número de puntos de control más el orden.</span><span class="sxs-lookup"><span data-stu-id="092e5-112">The *nknots* parameter equals the number of control points plus the order.</span></span>

</dd> <dt>

<span data-ttu-id="092e5-113">*decremento*</span><span class="sxs-lookup"><span data-stu-id="092e5-113">*knot*</span></span> 
</dt> <dd>

<span data-ttu-id="092e5-114">Matriz de valores de nudos de *nknots* nondecreasing.</span><span class="sxs-lookup"><span data-stu-id="092e5-114">An array of *nknots* nondecreasing knot values.</span></span>

</dd> <dt>

<span data-ttu-id="092e5-115">*STRI*</span><span class="sxs-lookup"><span data-stu-id="092e5-115">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="092e5-116">Desplazamiento (como un número de valores de punto flotante de precisión sencilla) entre los puntos de control de curva sucesivos.</span><span class="sxs-lookup"><span data-stu-id="092e5-116">The offset (as a number of single-precision floating-point values) between successive curve control points.</span></span>

</dd> <dt>

<span data-ttu-id="092e5-117">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="092e5-117">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="092e5-118">Puntero a una matriz de puntos de control.</span><span class="sxs-lookup"><span data-stu-id="092e5-118">A pointer to an array of control points.</span></span> <span data-ttu-id="092e5-119">Las coordenadas deben coincidir con el *tipo*.</span><span class="sxs-lookup"><span data-stu-id="092e5-119">The coordinates must agree with *type*.</span></span>

</dd> <dt>

<span data-ttu-id="092e5-120">*order*</span><span class="sxs-lookup"><span data-stu-id="092e5-120">*order*</span></span> 
</dt> <dd>

<span data-ttu-id="092e5-121">El orden de la curva de NURBS.</span><span class="sxs-lookup"><span data-stu-id="092e5-121">The order of the NURBS curve.</span></span> <span data-ttu-id="092e5-122">El parámetro *Order* es igual a degree + 1; por lo tanto, una curva cúbica tiene un orden de 4.</span><span class="sxs-lookup"><span data-stu-id="092e5-122">The *order* parameter equals degree + 1; hence a cubic curve has an order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="092e5-123">*type*</span><span class="sxs-lookup"><span data-stu-id="092e5-123">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="092e5-124">Tipo de la curva.</span><span class="sxs-lookup"><span data-stu-id="092e5-124">The type of the curve.</span></span> <span data-ttu-id="092e5-125">Si esta curva se define dentro de un par [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) , el tipo puede ser cualquiera de los tipos de evaluador unidimensional válidos (como GL \_ MAP1 \_ Vertex \_ 3 o GL \_ MAP1 \_ color \_ 4).</span><span class="sxs-lookup"><span data-stu-id="092e5-125">If this curve is defined within a [**gluBeginCurve**](glubegincurve.md)/[**gluEndCurve**](gluendcurve.md) pair, then the type can be any of the valid one-dimensional evaluator types (such as GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_COLOR\_4).</span></span> <span data-ttu-id="092e5-126">Entre un par de [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md) , los únicos tipos válidos son Glu \_ MAP1 \_ Trim \_ 2 y Glu \_ MAP1 \_ Trim \_ 3.</span><span class="sxs-lookup"><span data-stu-id="092e5-126">Between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, the only valid types are GLU\_MAP1\_TRIM\_2 and GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="092e5-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="092e5-127">Return value</span></span>

<span data-ttu-id="092e5-128">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="092e5-128">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="092e5-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="092e5-129">Remarks</span></span>

<span data-ttu-id="092e5-130">Cuando **gluNurbsCurve** aparece entre un  / par de **gluEndCurve** gluBeginCurve, describe una curva que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="092e5-130">When **gluNurbsCurve** appears between a **gluBeginCurve**/**gluEndCurve** pair, it describes a curve to be rendered.</span></span> <span data-ttu-id="092e5-131">Para asociar coordenadas posicional, de textura y de color, presenta cada una de ellas como un **gluNurbsCurve** independiente entre un par de gluEndCurve de **gluBeginCurve** /  .</span><span class="sxs-lookup"><span data-stu-id="092e5-131">You associate positional, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** between a **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="092e5-132">No realice más de una llamada a **gluNurbsCurve** para los datos de color, posición y textura dentro de un solo par de  / **gluEndCurve** gluBeginCurve.</span><span class="sxs-lookup"><span data-stu-id="092e5-132">Do not make more than one call to **gluNurbsCurve** for color, position, and texture data within a single **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="092e5-133">Realice exactamente una llamada para describir la posición de la curva (un *tipo* de GL \_ MAP1 \_ Vertex \_ 3 o GL \_ MAP1 \_ Vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="092e5-133">Make exactly one call to describe the position of the curve (a *type* of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4).</span></span>

<span data-ttu-id="092e5-134">Cuando **gluNurbsCurve** aparece entre un [](glubegintrim.md) / par de [**gluEndTrim**](gluendtrim.md) gluBeginTrim, describe una curva de recorte en una superficie NURBS.</span><span class="sxs-lookup"><span data-stu-id="092e5-134">When **gluNurbsCurve** appears between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, it describes a trimming curve on a NURBS surface.</span></span> <span data-ttu-id="092e5-135">Si *Type* es Glu \_ MAP1 \_ Trim \_ 2, describe una curva en el espacio de parámetros bidimensional (*u* y *v*).</span><span class="sxs-lookup"><span data-stu-id="092e5-135">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="092e5-136">Si es GLU \_ MAP1 \_ Trim \_ 3, describe una curva en el espacio de parámetros homogéneos bidimensionales (*u*, *v* y *w*).</span><span class="sxs-lookup"><span data-stu-id="092e5-136">If it is GLU\_MAP1\_TRIM\_3, it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="092e5-137">Para obtener más información sobre las curvas de recorte, vea **gluBeginTrim**.</span><span class="sxs-lookup"><span data-stu-id="092e5-137">For more discussion about trimming curves, see **gluBeginTrim**.</span></span>

## <a name="examples"></a><span data-ttu-id="092e5-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="092e5-138">Examples</span></span>

<span data-ttu-id="092e5-139">Las siguientes funciones representan una curva NURBS con texturas con normalidad:</span><span class="sxs-lookup"><span data-stu-id="092e5-139">The following functions render a textured NURBS curve with normals:</span></span>

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj); 
```

## <a name="requirements"></a><span data-ttu-id="092e5-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="092e5-140">Requirements</span></span>



| <span data-ttu-id="092e5-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="092e5-141">Requirement</span></span> | <span data-ttu-id="092e5-142">Value</span><span class="sxs-lookup"><span data-stu-id="092e5-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="092e5-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="092e5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="092e5-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="092e5-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="092e5-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="092e5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="092e5-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="092e5-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="092e5-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="092e5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="092e5-148"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="092e5-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="092e5-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="092e5-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="092e5-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="092e5-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="092e5-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="092e5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="092e5-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="092e5-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="092e5-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="092e5-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="092e5-154">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="092e5-154">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="092e5-155">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="092e5-155">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="092e5-156">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="092e5-156">**gluEndCurve**</span></span>](gluendcurve.md)
</dt> <dt>

[<span data-ttu-id="092e5-157">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="092e5-157">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="092e5-158">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="092e5-158">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="092e5-159">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="092e5-159">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





