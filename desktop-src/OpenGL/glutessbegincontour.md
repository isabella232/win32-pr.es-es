---
title: función gluTessBeginContour (GLU. h)
description: Las funciones gluTessBeginContour y gluTessEndContour delimitan una descripción de perfil. | función gluTessBeginContour (GLU. h)
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- gluTessBeginContour (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28efc96c977e5e0483b4f3d87e9ce840b985cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689788"
---
# <a name="glutessbegincontour-function"></a><span data-ttu-id="f600f-105">gluTessBeginContour función)</span><span class="sxs-lookup"><span data-stu-id="f600f-105">gluTessBeginContour function</span></span>

<span data-ttu-id="f600f-106">Las funciones **gluTessBeginContour** y [**gluTessEndContour**](glutessendcontour.md) delimitan una descripción de perfil.</span><span class="sxs-lookup"><span data-stu-id="f600f-106">The **gluTessBeginContour** and [**gluTessEndContour**](glutessendcontour.md) functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f600f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f600f-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="f600f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f600f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f600f-109">*tess*</span><span class="sxs-lookup"><span data-stu-id="f600f-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="f600f-110">Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="f600f-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f600f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f600f-111">Return value</span></span>

<span data-ttu-id="f600f-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f600f-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f600f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f600f-113">Remarks</span></span>

<span data-ttu-id="f600f-114">Las funciones **gluTessBeginContour** y [**gluTessEndPolygon**](glutessendpolygon.md) delimitan la definición de un contorno de polígono.</span><span class="sxs-lookup"><span data-stu-id="f600f-114">The **gluTessBeginContour** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="f600f-115">Dentro de cada par de gluTessEndPolygon de **gluTessBeginContour** /  , puede haber cero o más llamadas a [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="f600f-115">Within each **gluTessBeginContour**/**gluTessEndPolygon** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="f600f-116">Los vértices especifican un perfil cerrado (el último vértice de cada contorno se vincula automáticamente al primero).</span><span class="sxs-lookup"><span data-stu-id="f600f-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="f600f-117">Solo puede llamar a **gluTessBeginContour** entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) y **gluTessEndPolygon**.</span><span class="sxs-lookup"><span data-stu-id="f600f-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f600f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f600f-118">Requirements</span></span>



| <span data-ttu-id="f600f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f600f-119">Requirement</span></span> | <span data-ttu-id="f600f-120">Value</span><span class="sxs-lookup"><span data-stu-id="f600f-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f600f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f600f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f600f-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f600f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f600f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f600f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f600f-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f600f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f600f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f600f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f600f-126"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f600f-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f600f-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f600f-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f600f-128"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f600f-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f600f-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f600f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f600f-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f600f-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f600f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f600f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f600f-132">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="f600f-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="f600f-133">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="f600f-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="f600f-134">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="f600f-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="f600f-135">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="f600f-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="f600f-136">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="f600f-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="f600f-137">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="f600f-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="f600f-138">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="f600f-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





