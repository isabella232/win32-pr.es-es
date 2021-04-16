---
title: función gluTessBeginPolygon (GLU. h)
description: Las funciones gluTessBeginPolygon y gluTessEndPolygon delimitan una descripción de polígono. | función gluTessBeginPolygon (GLU. h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- gluTessBeginPolygon (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34fad4c620890df109449b9a222d3355041ac77f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670185"
---
# <a name="glutessbeginpolygon-function"></a><span data-ttu-id="3651b-105">gluTessBeginPolygon función)</span><span class="sxs-lookup"><span data-stu-id="3651b-105">gluTessBeginPolygon function</span></span>

<span data-ttu-id="3651b-106">Las funciones **gluTessBeginPolygon** y [**gluTessEndPolygon**](glutessendpolygon.md) delimitan una descripción de polígono.</span><span class="sxs-lookup"><span data-stu-id="3651b-106">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3651b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3651b-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a><span data-ttu-id="3651b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3651b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3651b-109">*tess*</span><span class="sxs-lookup"><span data-stu-id="3651b-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="3651b-110">Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="3651b-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="3651b-111">*datos de polígono \_*</span><span class="sxs-lookup"><span data-stu-id="3651b-111">*polygon\_data*</span></span> 
</dt> <dd>

<span data-ttu-id="3651b-112">Puntero a una estructura de datos de polígono definida por el programador.</span><span class="sxs-lookup"><span data-stu-id="3651b-112">A pointer to a programmer-defined polygon data structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3651b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3651b-113">Return value</span></span>

<span data-ttu-id="3651b-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3651b-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3651b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3651b-115">Remarks</span></span>

<span data-ttu-id="3651b-116">Las funciones **gluTessBeginPolygon** y [**gluTessEndPolygon**](glutessendpolygon.md) delimitan la definición de un polígono no convexo.</span><span class="sxs-lookup"><span data-stu-id="3651b-116">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="3651b-117">Dentro de cada par de gluTessEndPolygon de **gluTessBeginPolygon**  /   , incluya una o más llamadas a [**gluTessBeginContour**](glutessbegincontour.md).</span><span class="sxs-lookup"><span data-stu-id="3651b-117">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="3651b-118">Dentro de cada perfil, hay cero o más llamadas a [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="3651b-118">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="3651b-119">Los vértices especifican un perfil cerrado (el último vértice de cada contorno se vincula automáticamente al primero).</span><span class="sxs-lookup"><span data-stu-id="3651b-119">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="3651b-120">El parámetro de *\_ datos Polygon* es un puntero a una estructura de datos definida por el programador.</span><span class="sxs-lookup"><span data-stu-id="3651b-120">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="3651b-121">Si se especifican las devoluciones de llamada adecuadas (vea [*gluTessCallback*](glutess.md)), este puntero se devuelve a la función o funciones de devolución de llamada, lo que lo convierte en una manera cómoda de almacenar la información por polígono.</span><span class="sxs-lookup"><span data-stu-id="3651b-121">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="3651b-122">Cuando se llama a [**gluTessEndPolygon**](glutessendpolygon.md), el polígono es teselando y los triángulos resultantes se describen a través de las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="3651b-122">When you call [**gluTessEndPolygon**](glutessendpolygon.md), the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="3651b-123">Para obtener descripciones de las funciones de devolución de llamada, vea [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="3651b-123">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3651b-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3651b-124">Examples</span></span>

<span data-ttu-id="3651b-125">A continuación se describe un cuadrangular con un orificio triangular:</span><span class="sxs-lookup"><span data-stu-id="3651b-125">The following describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
```

## <a name="requirements"></a><span data-ttu-id="3651b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3651b-126">Requirements</span></span>



| <span data-ttu-id="3651b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3651b-127">Requirement</span></span> | <span data-ttu-id="3651b-128">Value</span><span class="sxs-lookup"><span data-stu-id="3651b-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3651b-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3651b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3651b-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3651b-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3651b-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3651b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3651b-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3651b-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3651b-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3651b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3651b-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="3651b-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="3651b-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3651b-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3651b-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3651b-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3651b-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3651b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3651b-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3651b-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3651b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="3651b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3651b-140">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="3651b-140">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="3651b-141">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="3651b-141">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="3651b-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="3651b-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="3651b-143">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="3651b-143">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="3651b-144">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="3651b-144">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="3651b-145">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="3651b-145">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="3651b-146">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="3651b-146">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





