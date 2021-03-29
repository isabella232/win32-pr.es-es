---
title: función gluEndCurve (GLU. h)
description: Las funciones gluBeginCurve y gluEndCurve delimitan una definición de curva B-spline racional (NURBS) no uniforme. | función gluEndCurve (GLU. h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- gluEndCurve (función) OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49f6c0c08bf31135ca82e87d2093ef3b57197955
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678727"
---
# <a name="gluendcurve-function"></a><span data-ttu-id="f139d-105">gluEndCurve función)</span><span class="sxs-lookup"><span data-stu-id="f139d-105">gluEndCurve function</span></span>

<span data-ttu-id="f139d-106">Las funciones [**gluBeginCurve**](glubegincurve.md) y **gluEndCurve** delimitan una definición de curva B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme.</span><span class="sxs-lookup"><span data-stu-id="f139d-106">The [**gluBeginCurve**](glubegincurve.md) and **gluEndCurve** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f139d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f139d-107">Syntax</span></span>


```C++
void WINAPI gluEndCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="f139d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f139d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f139d-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="f139d-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="f139d-110">El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="f139d-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f139d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f139d-111">Return value</span></span>

<span data-ttu-id="f139d-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f139d-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f139d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f139d-113">Remarks</span></span>

<span data-ttu-id="f139d-114">Use [**gluBeginCurve**](glubegincurve.md) para marcar el inicio de una definición de curva NURBS.</span><span class="sxs-lookup"><span data-stu-id="f139d-114">Use [**gluBeginCurve**](glubegincurve.md) to mark the beginning of a NURBS curve definition.</span></span> <span data-ttu-id="f139d-115">Después de llamar a **gluBeginCurve**, realice una o varias llamadas a [**gluNurbsCurve**](glunurbscurve.md) para definir los atributos de la curva.</span><span class="sxs-lookup"><span data-stu-id="f139d-115">After calling **gluBeginCurve**, make one or more calls to [**gluNurbsCurve**](glunurbscurve.md) to define the attributes of the curve.</span></span> <span data-ttu-id="f139d-116">Exactamente una de las llamadas a **gluNurbsCurve** debe tener un tipo de curva de GL \_ MAP1 \_ Vertex \_ 3 o GL \_ MAP1 \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="f139d-116">Exactly one of the calls to **gluNurbsCurve** must have a curve type of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4.</span></span> <span data-ttu-id="f139d-117">Para marcar el final de la definición de curva NURBS, llame a **gluEndCurve**.</span><span class="sxs-lookup"><span data-stu-id="f139d-117">To mark the end of the NURBS curve definition, call **gluEndCurve**.</span></span>

<span data-ttu-id="f139d-118">Los evaluadores de OpenGL se utilizan para representar la curva NURBS como una serie de segmentos de línea.</span><span class="sxs-lookup"><span data-stu-id="f139d-118">OpenGL evaluators are used to render the NURBS curve as a series of line segments.</span></span> <span data-ttu-id="f139d-119">El estado del evaluador se conserva durante la representación con [**glPushAttrib**](glpushattrib.md) (el bit de evaluación de GL \_ \_ ) y [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="f139d-119">Evaluator state is preserved during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT ) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="f139d-120">Para obtener información sobre exactamente el estado que estas llamadas conservan, vea **glPushAttrib**.</span><span class="sxs-lookup"><span data-stu-id="f139d-120">For information on exactly what state these calls preserve, see **glPushAttrib**.</span></span>

## <a name="examples"></a><span data-ttu-id="f139d-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f139d-121">Examples</span></span>

<span data-ttu-id="f139d-122">Las siguientes funciones representan una curva NURBS con texturas con normalidad; las coordenadas de textura y las normales también se especifican como curvas NURBS:</span><span class="sxs-lookup"><span data-stu-id="f139d-122">The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:</span></span>

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
```

## <a name="requirements"></a><span data-ttu-id="f139d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f139d-123">Requirements</span></span>



| <span data-ttu-id="f139d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f139d-124">Requirement</span></span> | <span data-ttu-id="f139d-125">Value</span><span class="sxs-lookup"><span data-stu-id="f139d-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f139d-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f139d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f139d-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f139d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f139d-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f139d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f139d-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f139d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f139d-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f139d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f139d-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f139d-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f139d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f139d-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="f139d-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f139d-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f139d-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f139d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f139d-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f139d-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f139d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f139d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f139d-137">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="f139d-137">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="f139d-138">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="f139d-138">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="f139d-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="f139d-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="f139d-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="f139d-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="f139d-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="f139d-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





