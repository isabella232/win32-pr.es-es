---
title: función gluBeginPolygon (GLU. h)
description: Las funciones gluBeginPolygon y gluEndPolygon delimitan una descripción de polígono. | función gluBeginPolygon (GLU. h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- gluBeginPolygon (función) OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60204e7d937b4686f3757b520c820886e168529e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670139"
---
# <a name="glubeginpolygon-function"></a><span data-ttu-id="ee49e-105">gluBeginPolygon función)</span><span class="sxs-lookup"><span data-stu-id="ee49e-105">gluBeginPolygon function</span></span>

<span data-ttu-id="ee49e-106">\[La función **gluBeginPolygon** está obsoleta y solo se proporciona por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="ee49e-106">\[The **gluBeginPolygon** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="ee49e-107">La función **gluBeginPolygon** se asigna a [**GluTessBeginPolygon**](glutessbeginpolygon.md) seguido de [**gluTessBeginContour**](glutessbegincontour.md).\]</span><span class="sxs-lookup"><span data-stu-id="ee49e-107">The **gluBeginPolygon** function is mapped to [**gluTessBeginPolygon**](glutessbeginpolygon.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="ee49e-108">Las funciones **gluBeginPolygon** y [**gluEndPolygon**](gluendpolygon.md) delimitan una descripción de polígono.</span><span class="sxs-lookup"><span data-stu-id="ee49e-108">The **gluBeginPolygon** and [**gluEndPolygon**](gluendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee49e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee49e-109">Syntax</span></span>


```C++
void WINAPI gluBeginPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="ee49e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee49e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee49e-111">*tess*</span><span class="sxs-lookup"><span data-stu-id="ee49e-111">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="ee49e-112">Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="ee49e-112">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee49e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee49e-113">Return value</span></span>

<span data-ttu-id="ee49e-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ee49e-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee49e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee49e-115">Remarks</span></span>

<span data-ttu-id="ee49e-116">Use **gluBeginPolygon** y **gluEndPolygon** para delimitar la definición de un polígono no convexo.</span><span class="sxs-lookup"><span data-stu-id="ee49e-116">Use **gluBeginPolygon** and **gluEndPolygon** to delimit the definition of a nonconvex polygon.</span></span>

1.  <span data-ttu-id="ee49e-117">Llame a **gluBeginPolygon**.</span><span class="sxs-lookup"><span data-stu-id="ee49e-117">Call **gluBeginPolygon**.</span></span>
2.  <span data-ttu-id="ee49e-118">Defina los contornos del polígono mediante una llamada a [**gluTessVertex**](glutessvertex.md) para cada vértice y [**gluNextContour**](glunextcontour.md) para iniciar cada nuevo contorno.</span><span class="sxs-lookup"><span data-stu-id="ee49e-118">Define the contours of the polygon by calling [**gluTessVertex**](glutessvertex.md) for each vertex and [**gluNextContour**](glunextcontour.md) to start each new contour.</span></span>
3.  <span data-ttu-id="ee49e-119">Llame a **gluEndPolygon** para indicar el final de la definición.</span><span class="sxs-lookup"><span data-stu-id="ee49e-119">Call **gluEndPolygon** to signal the end of the definition.</span></span>

    <span data-ttu-id="ee49e-120">Una vez que se llama a **gluEndPolygon** , el polígono se tesela y los triángulos resultantes se describen a través de las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="ee49e-120">Once **gluEndPolygon** is called, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="ee49e-121">Para obtener descripciones de las funciones de devolución de llamada, vea [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="ee49e-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ee49e-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ee49e-122">Examples</span></span>

<span data-ttu-id="ee49e-123">En el ejemplo siguiente se describe un cuadrangular con un orificio triangular:</span><span class="sxs-lookup"><span data-stu-id="ee49e-123">The following example describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
```

## <a name="requirements"></a><span data-ttu-id="ee49e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee49e-124">Requirements</span></span>



| <span data-ttu-id="ee49e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee49e-125">Requirement</span></span> | <span data-ttu-id="ee49e-126">Value</span><span class="sxs-lookup"><span data-stu-id="ee49e-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ee49e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee49e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ee49e-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ee49e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ee49e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee49e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ee49e-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ee49e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ee49e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee49e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee49e-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee49e-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ee49e-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee49e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee49e-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee49e-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ee49e-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ee49e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee49e-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee49e-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee49e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee49e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee49e-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="ee49e-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="ee49e-139">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="ee49e-139">**gluNextContour**</span></span>](glunextcontour.md)
</dt> <dt>

[<span data-ttu-id="ee49e-140">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="ee49e-140">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="ee49e-141">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="ee49e-141">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="ee49e-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="ee49e-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="ee49e-143">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="ee49e-143">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





