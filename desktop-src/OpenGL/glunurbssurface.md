---
title: función gluNurbsSurface (GLU. h)
description: La función gluNurbsSurface define la forma de una superficie no uniforme B-spline racional (NURBS).
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- gluNurbsSurface (función) OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c784741eded406a49bba90f67544a406ab024a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995906"
---
# <a name="glunurbssurface-function"></a><span data-ttu-id="1efc5-104">gluNurbsSurface función)</span><span class="sxs-lookup"><span data-stu-id="1efc5-104">gluNurbsSurface function</span></span>

<span data-ttu-id="1efc5-105">La función **gluNurbsSurface** define la forma de una superficie no uniforme B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="1efc5-105">The **gluNurbsSurface** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1efc5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1efc5-106">Syntax</span></span>


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="1efc5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1efc5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1efc5-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="1efc5-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="1efc5-109">El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="1efc5-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1efc5-110">*recuento de sknot \_*</span><span class="sxs-lookup"><span data-stu-id="1efc5-110">*sknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="1efc5-111">Número de nudos en la dirección de *u* paramétrica.</span><span class="sxs-lookup"><span data-stu-id="1efc5-111">The number of knots in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="1efc5-112">*sknot*</span><span class="sxs-lookup"><span data-stu-id="1efc5-112">*sknot*</span></span> 
</dt> <dd>

<span data-ttu-id="1efc5-113">Una matriz de valores de *sknot de \_ recuento* de nondecreasing en la dirección *u* paramétrica.</span><span class="sxs-lookup"><span data-stu-id="1efc5-113">An array of *sknot\_count* nondecreasing knot values in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="1efc5-114">*recuento de tknot \_*</span><span class="sxs-lookup"><span data-stu-id="1efc5-114">*tknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="1efc5-115">Número de nudos en la dirección de *v* paramétrica.</span><span class="sxs-lookup"><span data-stu-id="1efc5-115">The number of knots in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="1efc5-116">*tknot*</span><span class="sxs-lookup"><span data-stu-id="1efc5-116">*tknot*</span></span> 
</dt> <dd>

<span data-ttu-id="1efc5-117">Una matriz de valores de *tknot de \_ recuento* de nondecreasing en la dirección *v* paramétrica.</span><span class="sxs-lookup"><span data-stu-id="1efc5-117">An array of *tknot\_count* nondecreasing knot values in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="1efc5-118">*\_intervalo s*</span><span class="sxs-lookup"><span data-stu-id="1efc5-118">*s\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="1efc5-119">Desplazamiento (como número de valores únicos de precisionfloating) entre los puntos de control sucesivos de la dirección *u* paramétrica de *ctlarray*.</span><span class="sxs-lookup"><span data-stu-id="1efc5-119">The offset (as a number of single precisionfloating-point values) between successive control points in the parametric *u* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="1efc5-120">*\_intervalo t*</span><span class="sxs-lookup"><span data-stu-id="1efc5-120">*t\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="1efc5-121">Desplazamiento (en valores únicos de punto precisionfloating) entre los puntos de control sucesivos de la dirección *v* paramétrica en *ctlarray*.</span><span class="sxs-lookup"><span data-stu-id="1efc5-121">The offset (in single precisionfloating-point values) between successive control points in the parametric *v* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="1efc5-122">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="1efc5-122">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="1efc5-123">Una matriz que contiene los puntos de control para la superficie de NURBS.</span><span class="sxs-lookup"><span data-stu-id="1efc5-123">An array containing control points for the NURBS surface.</span></span> <span data-ttu-id="1efc5-124">Los desplazamientos entre los puntos de control sucesivos de las direcciones de *u* y *v* paramétricas se proporcionan mediante el *\_ STRIDE* y el *\_ paso t*.</span><span class="sxs-lookup"><span data-stu-id="1efc5-124">The offsets between successive control points in the parametric *u* and *v* directions are given by *s\_stride* and *t\_stride*.</span></span>

</dd> <dt>

<span data-ttu-id="1efc5-125">*sorder*</span><span class="sxs-lookup"><span data-stu-id="1efc5-125">*sorder*</span></span> 
</dt> <dd>

<span data-ttu-id="1efc5-126">El orden de la superficie NURBS en la dirección *u* paramétrica.</span><span class="sxs-lookup"><span data-stu-id="1efc5-126">The order of the NURBS surface in the parametric *u* direction.</span></span> <span data-ttu-id="1efc5-127">El orden es uno más que el grado; por lo tanto, una superficie cúbica en *u* tiene un orden *u* de 4.</span><span class="sxs-lookup"><span data-stu-id="1efc5-127">The order is one more than the degree, hence a surface that is cubic in *u* has a *u* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="1efc5-128">*torder*</span><span class="sxs-lookup"><span data-stu-id="1efc5-128">*torder*</span></span> 
</dt> <dd>

<span data-ttu-id="1efc5-129">El orden de la superficie NURBS en la dirección *v* paramétrica.</span><span class="sxs-lookup"><span data-stu-id="1efc5-129">The order of the NURBS surface in the parametric *v* direction.</span></span> <span data-ttu-id="1efc5-130">El orden es uno más que el grado; por lo tanto, una superficie cúbica en *v* tiene un orden *v* de 4.</span><span class="sxs-lookup"><span data-stu-id="1efc5-130">The order is one more than the degree, hence a surface that is cubic in *v* has a *v* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="1efc5-131">*type*</span><span class="sxs-lookup"><span data-stu-id="1efc5-131">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="1efc5-132">Tipo de la superficie.</span><span class="sxs-lookup"><span data-stu-id="1efc5-132">The type of the surface.</span></span> <span data-ttu-id="1efc5-133">El parámetro de *tipo* puede ser cualquiera de los tipos de evaluador bidimensionales válidos (como GL \_ MAP2 ( \_ Vertex \_ 3 o GL \_ MAP2 ( \_ color \_ 4).</span><span class="sxs-lookup"><span data-stu-id="1efc5-133">The *type* parameter can be any of the valid two-dimensional evaluator types (such as GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_COLOR\_4).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1efc5-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1efc5-134">Return value</span></span>

<span data-ttu-id="1efc5-135">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1efc5-135">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1efc5-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1efc5-136">Remarks</span></span>

<span data-ttu-id="1efc5-137">Use **gluNurbsSurface** en una definición de superficie de NURBS para describir la forma de una superficie NURBS (antes de cualquier recorte).</span><span class="sxs-lookup"><span data-stu-id="1efc5-137">Use **gluNurbsSurface** within a NURBS surface definition to describe the shape of a NURBS surface (before any trimming).</span></span> <span data-ttu-id="1efc5-138">Para marcar el inicio de una definición de superficie de NURBS, utilice la función [**gluBeginSurface**](glubeginsurface.md) .</span><span class="sxs-lookup"><span data-stu-id="1efc5-138">To mark the beginning of a NURBS surface definition, use the [**gluBeginSurface**](glubeginsurface.md) function.</span></span> <span data-ttu-id="1efc5-139">Para marcar el final de una definición de superficie de NURBS, utilice la función [**gluEndSurface**](gluendsurface.md) .</span><span class="sxs-lookup"><span data-stu-id="1efc5-139">To mark the end of a NURBS surface definition, use the [**gluEndSurface**](gluendsurface.md) function.</span></span> <span data-ttu-id="1efc5-140">Llame a **gluNurbsSurface** solo en una definición de Surface de NURBS.</span><span class="sxs-lookup"><span data-stu-id="1efc5-140">Call **gluNurbsSurface** within a NURBS surface definition only.</span></span>

<span data-ttu-id="1efc5-141">Las coordenadas de posición, textura y color se asocian con una superficie presentando cada una de ellas como un **gluNurbsSurface** independiente entre un par de gluEndSurface de **gluBeginSurface** /  .</span><span class="sxs-lookup"><span data-stu-id="1efc5-141">You associate positional, texture, and color coordinates with a surface by presenting each as a separate **gluNurbsSurface** between a **gluBeginSurface**/**gluEndSurface** pair.</span></span> <span data-ttu-id="1efc5-142">Dentro de un solo par de gluEndSurface de **gluBeginSurface** /  , solo puede hacer una llamada a **gluNurbsSurface** para los datos de color, posición y textura.</span><span class="sxs-lookup"><span data-stu-id="1efc5-142">Within a single **gluBeginSurface**/**gluEndSurface** pair, you can make only one call to **gluNurbsSurface** for color, position, and texture data.</span></span> <span data-ttu-id="1efc5-143">Realice exactamente una llamada para describir la posición de la superficie (un *tipo* de GL \_ MAP2 ( \_ Vertex \_ 3 o GL \_ MAP2 ( \_ Vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="1efc5-143">Make exactly one call to describe the position of the surface (a *type* of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4).</span></span>

<span data-ttu-id="1efc5-144">Puede recortar una superficie NURBS mediante las funciones [**gluNurbsCurve**](glunurbscurve.md) y [**gluPwlCurve**](glupwlcurve.md) entre las llamadas a [**gluBeginTrim**](glubegintrim.md) y [**gluEndTrim**](gluendtrim.md).</span><span class="sxs-lookup"><span data-stu-id="1efc5-144">You can trim a NURBS surface by using the [**gluNurbsCurve**](glunurbscurve.md) and [**gluPwlCurve**](glupwlcurve.md) functions between calls to [**gluBeginTrim**](glubegintrim.md) and [**gluEndTrim**](gluendtrim.md).</span></span>

<span data-ttu-id="1efc5-145">Un **gluNurbsSurface** con *sknotr \_* nudos en los nudos de la dirección *u* y *tknot \_ Count* en la dirección *v* con los pedidos *sorder* y *torder* debe tener (*sknot \_ Count*  - *sorder*) multipied por (*tknot \_ Count*  - *torder*) puntos de control.</span><span class="sxs-lookup"><span data-stu-id="1efc5-145">A **gluNurbsSurface** with *sknot\_count* knots in the *u* direction and *tknot\_count* knots in the *v* direction with orders *sorder* and *torder* must have (*sknot\_count* -*sorder*) multipied by (*tknot\_count* -*torder*) control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="1efc5-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1efc5-146">Requirements</span></span>



| <span data-ttu-id="1efc5-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="1efc5-147">Requirement</span></span> | <span data-ttu-id="1efc5-148">Value</span><span class="sxs-lookup"><span data-stu-id="1efc5-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1efc5-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1efc5-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1efc5-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1efc5-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1efc5-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1efc5-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1efc5-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1efc5-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1efc5-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1efc5-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="1efc5-154"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="1efc5-154"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1efc5-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1efc5-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="1efc5-156"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1efc5-156"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1efc5-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1efc5-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1efc5-158"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1efc5-158"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1efc5-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="1efc5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1efc5-160">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="1efc5-160">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="1efc5-161">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="1efc5-161">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="1efc5-162">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="1efc5-162">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="1efc5-163">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="1efc5-163">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="1efc5-164">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="1efc5-164">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="1efc5-165">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="1efc5-165">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="1efc5-166">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="1efc5-166">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





