---
title: función gluTessEndPolygon (GLU. h)
description: Las funciones gluTessBeginPolygon y gluTessEndPolygon delimitan una descripción de polígono. | función gluTessEndPolygon (GLU. h)
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
keywords:
- gluTessEndPolygon (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f9176e5bdb64dc0e3cd21bd42735e57b541b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689757"
---
# <a name="glutessendpolygon-function"></a><span data-ttu-id="1e17e-105">gluTessEndPolygon función)</span><span class="sxs-lookup"><span data-stu-id="1e17e-105">gluTessEndPolygon function</span></span>

<span data-ttu-id="1e17e-106">Las funciones [**gluTessBeginPolygon**](glutessbeginpolygon.md) y **gluTessEndPolygon** delimitan una descripción de polígono.</span><span class="sxs-lookup"><span data-stu-id="1e17e-106">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e17e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e17e-107">Syntax</span></span>


```C++
void WINAPI gluTessEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="1e17e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e17e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e17e-109">*tess*</span><span class="sxs-lookup"><span data-stu-id="1e17e-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="1e17e-110">Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="1e17e-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e17e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e17e-111">Return value</span></span>

<span data-ttu-id="1e17e-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1e17e-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e17e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e17e-113">Remarks</span></span>

<span data-ttu-id="1e17e-114">Las funciones [**gluTessBeginPolygon**](glutessbeginpolygon.md) y **gluTessEndPolygon** delimitan la definición de un polígono no convexo.</span><span class="sxs-lookup"><span data-stu-id="1e17e-114">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="1e17e-115">Dentro de cada par de gluTessEndPolygon de **gluTessBeginPolygon**  /   , incluya una o más llamadas a [**gluTessBeginContour**](glutessbegincontour.md).</span><span class="sxs-lookup"><span data-stu-id="1e17e-115">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="1e17e-116">Dentro de cada perfil, hay cero o más llamadas a [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="1e17e-116">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="1e17e-117">Los vértices especifican un perfil cerrado (el último vértice de cada contorno se vincula automáticamente al primero).</span><span class="sxs-lookup"><span data-stu-id="1e17e-117">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="1e17e-118">El parámetro de *\_ datos Polygon* es un puntero a una estructura de datos definida por el programador.</span><span class="sxs-lookup"><span data-stu-id="1e17e-118">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="1e17e-119">Si se especifican las devoluciones de llamada adecuadas (vea [*gluTessCallback*](glutess.md)), este puntero se devuelve a la función o funciones de devolución de llamada, lo que lo convierte en una manera cómoda de almacenar la información por polígono.</span><span class="sxs-lookup"><span data-stu-id="1e17e-119">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="1e17e-120">Cuando se llama a **gluTessEndPolygon**, el polígono es teselando y los triángulos resultantes se describen a través de las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="1e17e-120">When you call **gluTessEndPolygon**, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="1e17e-121">Para obtener descripciones de las funciones de devolución de llamada, vea [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="1e17e-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1e17e-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1e17e-122">Examples</span></span>

<span data-ttu-id="1e17e-123">A continuación se describe un cuadrangular con un orificio triangular:</span><span class="sxs-lookup"><span data-stu-id="1e17e-123">The following describes a quadrilateral with a triangular hole:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="1e17e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e17e-124">Requirements</span></span>



| <span data-ttu-id="1e17e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e17e-125">Requirement</span></span> | <span data-ttu-id="1e17e-126">Value</span><span class="sxs-lookup"><span data-stu-id="1e17e-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1e17e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e17e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1e17e-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1e17e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1e17e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e17e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1e17e-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e17e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1e17e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e17e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e17e-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e17e-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1e17e-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e17e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e17e-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e17e-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1e17e-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e17e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e17e-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e17e-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e17e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e17e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e17e-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="1e17e-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="1e17e-139">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="1e17e-139">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="1e17e-140">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="1e17e-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="1e17e-141">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="1e17e-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="1e17e-142">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="1e17e-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="1e17e-143">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="1e17e-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="1e17e-144">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="1e17e-144">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





