---
title: función gluPwlCurve (GLU. h)
description: La función gluPwlCurve describe una curva de recorte B-spline racional no uniforme (NURBS) a trozos lineal.
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- gluPwlCurve (función) OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666041"
---
# <a name="glupwlcurve-function"></a><span data-ttu-id="c56a1-104">gluPwlCurve función)</span><span class="sxs-lookup"><span data-stu-id="c56a1-104">gluPwlCurve function</span></span>

<span data-ttu-id="c56a1-105">La función **gluPwlCurve** describe una curva de recorte B-spline racional no uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)) a trozos lineal.</span><span class="sxs-lookup"><span data-stu-id="c56a1-105">The **gluPwlCurve** function describes a piecewise linear Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="c56a1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c56a1-106">Syntax</span></span>


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="c56a1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c56a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c56a1-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="c56a1-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="c56a1-109">El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="c56a1-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c56a1-110">*count*</span><span class="sxs-lookup"><span data-stu-id="c56a1-110">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="c56a1-111">Número de puntos de la curva.</span><span class="sxs-lookup"><span data-stu-id="c56a1-111">The number of points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="c56a1-112">*array*</span><span class="sxs-lookup"><span data-stu-id="c56a1-112">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="c56a1-113">Una matriz que contiene los puntos de curva.</span><span class="sxs-lookup"><span data-stu-id="c56a1-113">An array containing the curve points.</span></span>

</dd> <dt>

<span data-ttu-id="c56a1-114">*STRI*</span><span class="sxs-lookup"><span data-stu-id="c56a1-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="c56a1-115">Desplazamiento (un número de valores de punto flotante de precisión sencilla) entre los puntos de la curva.</span><span class="sxs-lookup"><span data-stu-id="c56a1-115">The offset (a number of single-precision floating-point values) between points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="c56a1-116">*type*</span><span class="sxs-lookup"><span data-stu-id="c56a1-116">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="c56a1-117">Tipo de curva.</span><span class="sxs-lookup"><span data-stu-id="c56a1-117">The type of curve.</span></span> <span data-ttu-id="c56a1-118">Debe ser GLU \_ MAP1 \_ Trim \_ 2 o Glu \_ MAP1 \_ Trim \_ 3.</span><span class="sxs-lookup"><span data-stu-id="c56a1-118">Must be either GLU\_MAP1\_TRIM\_2 or GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c56a1-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c56a1-119">Return value</span></span>

<span data-ttu-id="c56a1-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c56a1-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c56a1-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c56a1-121">Remarks</span></span>

<span data-ttu-id="c56a1-122">La función **gluPwlCurve** describe una curva de recorte lineal a trozos para una superficie NURBS.</span><span class="sxs-lookup"><span data-stu-id="c56a1-122">The **gluPwlCurve** function describes a piecewise linear trimming curve for a NURBS surface.</span></span> <span data-ttu-id="c56a1-123">Una curva lineal a trozos consta de una lista de coordenadas de puntos en el espacio de parámetros para que se recorte la superficie NURBS.</span><span class="sxs-lookup"><span data-stu-id="c56a1-123">A piecewise linear curve consists of a list of coordinates of points in the parameter space for the NURBS surface to be trimmed.</span></span> <span data-ttu-id="c56a1-124">Estos puntos están conectados con segmentos de línea para formar una curva.</span><span class="sxs-lookup"><span data-stu-id="c56a1-124">These points are connected with line segments to form a curve.</span></span> <span data-ttu-id="c56a1-125">Si la curva es una aproximación a una curva real, los puntos deben ser lo suficientemente cercanos para que el trazado resultante aparezca curvado en la resolución usada en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c56a1-125">If the curve is an approximation to a real curve, the points should be close enough that the resulting path appears curved at the resolution used in the application.</span></span>

<span data-ttu-id="c56a1-126">Si *Type* es Glu \_ MAP1 \_ Trim \_ 2, describe una curva en el espacio de parámetros bidimensional (*u* y *v*).</span><span class="sxs-lookup"><span data-stu-id="c56a1-126">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="c56a1-127">Si es GLU \_ MAP1 \_ Trim \_ 3, describe una curva en el espacio de parámetros homogéneos bidimensionales (*u*, *v* y *w*).</span><span class="sxs-lookup"><span data-stu-id="c56a1-127">If it is GLU\_MAP1\_TRIM\_3, then it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="c56a1-128">Para obtener más información sobre las curvas de recorte, vea [**gluBeginTrim**](glubegintrim.md).</span><span class="sxs-lookup"><span data-stu-id="c56a1-128">For more information about trimming curves, see [**gluBeginTrim**](glubegintrim.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c56a1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c56a1-129">Requirements</span></span>



| <span data-ttu-id="c56a1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c56a1-130">Requirement</span></span> | <span data-ttu-id="c56a1-131">Value</span><span class="sxs-lookup"><span data-stu-id="c56a1-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c56a1-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c56a1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c56a1-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c56a1-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c56a1-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c56a1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c56a1-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c56a1-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c56a1-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c56a1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c56a1-137"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="c56a1-137"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="c56a1-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c56a1-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="c56a1-139"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c56a1-139"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c56a1-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c56a1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c56a1-141"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c56a1-141"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c56a1-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="c56a1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56a1-143">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="c56a1-143">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="c56a1-144">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="c56a1-144">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="c56a1-145">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="c56a1-145">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="c56a1-146">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="c56a1-146">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





