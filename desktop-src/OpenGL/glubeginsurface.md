---
title: función gluBeginSurface (GLU. h)
description: Las funciones gluBeginSurface y gluEndSurface delimitan una definición de superficie de la spline B-spline racional (NURBS) no uniforme. | función gluBeginSurface (GLU. h)
ms.assetid: 7189f05e-0c4d-4f82-8a82-a51fcc51b202
keywords:
- gluBeginSurface (función) OpenGL
topic_type:
- apiref
api_name:
- gluBeginSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd09030290f78fac987a52cddd977a502dda06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689742"
---
# <a name="glubeginsurface-function"></a><span data-ttu-id="be563-105">gluBeginSurface función)</span><span class="sxs-lookup"><span data-stu-id="be563-105">gluBeginSurface function</span></span>

<span data-ttu-id="be563-106">Las funciones **gluBeginSurface** y [**gluEndSurface**](gluendsurface.md) delimitan una definición de superficie de la spline B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme.</span><span class="sxs-lookup"><span data-stu-id="be563-106">The **gluBeginSurface** and [**gluEndSurface**](gluendsurface.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="be563-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be563-107">Syntax</span></span>


```C++
void WINAPI gluBeginSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="be563-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be563-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be563-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="be563-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="be563-110">El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="be563-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be563-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be563-111">Return value</span></span>

<span data-ttu-id="be563-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="be563-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be563-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be563-113">Remarks</span></span>

<span data-ttu-id="be563-114">Las funciones **gluBeginSurface** y **gluEndSurface** marcan el principio y el final de las definiciones de la superficie de NURBS, que se definen con llamadas a **gluNurbsSurface**.</span><span class="sxs-lookup"><span data-stu-id="be563-114">The **gluBeginSurface** and **gluEndSurface** functions mark the beginning and end of NURBS surface definitions, which are defined with calls to **gluNurbsSurface**.</span></span>

1.  <span data-ttu-id="be563-115">Llame a **gluBeginSurface** para marcar el inicio de una definición de superficie de NURBS.</span><span class="sxs-lookup"><span data-stu-id="be563-115">Call **gluBeginSurface** to mark the beginning of a NURBS surface definition.</span></span>
2.  <span data-ttu-id="be563-116">Realice una o varias llamadas a **gluNurbsSurface** para definir los atributos de la superficie.</span><span class="sxs-lookup"><span data-stu-id="be563-116">Make one or more calls to **gluNurbsSurface** to define the attributes of the surface.</span></span>

    <span data-ttu-id="be563-117">Exactamente una de estas llamadas a **gluNurbsSurface** debe tener un tipo de superficie de GL \_ MAP2 ( \_ Vertex \_ 3 o GL \_ MAP2 ( \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="be563-117">Exactly one of these calls to **gluNurbsSurface** must have a surface type of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4.</span></span>

3.  <span data-ttu-id="be563-118">Para marcar el final de la definición de la superficie de NURBS, llame a **gluEndSurface**.</span><span class="sxs-lookup"><span data-stu-id="be563-118">To mark the end of the NURBS surface definition, call **gluEndSurface**.</span></span>

<span data-ttu-id="be563-119">Las funciones [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md)y [**gluEndTrim**](gluendtrim.md) admiten el recorte de superficies NURBS.</span><span class="sxs-lookup"><span data-stu-id="be563-119">The [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md), and [**gluEndTrim**](gluendtrim.md) functions support trimming of NURBS surfaces.</span></span>

<span data-ttu-id="be563-120">Utilice los evaluadores de OpenGL para representar la superficie de NURBS como un conjunto de polígonos.</span><span class="sxs-lookup"><span data-stu-id="be563-120">Use OpenGL evaluators to render the NURBS surface as a set of polygons.</span></span> <span data-ttu-id="be563-121">Conservar el estado del evaluador durante la representación con [**glPushAttrib**](glpushattrib.md)(el bit de evaluación de GL \_ \_ ) y [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="be563-121">Preserve the evaluator state during rendering with [**glPushAttrib**](glpushattrib.md)(GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span>

## <a name="examples"></a><span data-ttu-id="be563-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="be563-122">Examples</span></span>

<span data-ttu-id="be563-123">Las siguientes funciones representan una superficie NURBS con texturas con normalidad; las coordenadas de textura y las normales también se describen como superficies NURBS:</span><span class="sxs-lookup"><span data-stu-id="be563-123">The following functions render a textured NURBS surface with normals; the texture coordinates and normals are also described as NURBS surfaces:</span></span>

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

## <a name="requirements"></a><span data-ttu-id="be563-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be563-124">Requirements</span></span>



| <span data-ttu-id="be563-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="be563-125">Requirement</span></span> | <span data-ttu-id="be563-126">Value</span><span class="sxs-lookup"><span data-stu-id="be563-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="be563-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be563-127">Minimum supported client</span></span><br/> | <span data-ttu-id="be563-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="be563-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="be563-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be563-129">Minimum supported server</span></span><br/> | <span data-ttu-id="be563-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="be563-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="be563-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be563-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="be563-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="be563-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="be563-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be563-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="be563-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be563-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="be563-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be563-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be563-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be563-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be563-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="be563-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be563-138">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="be563-138">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="be563-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="be563-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="be563-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="be563-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="be563-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="be563-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="be563-142">**gluNurbsSurface**</span><span class="sxs-lookup"><span data-stu-id="be563-142">**gluNurbsSurface**</span></span>](glunurbssurface.md)
</dt> <dt>

[<span data-ttu-id="be563-143">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="be563-143">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





