---
title: función gluTessNormal (GLU. h)
description: La función gluTessNormal especifica una normal para un polígono.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- gluTessNormal (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996999"
---
# <a name="glutessnormal-function"></a><span data-ttu-id="896c3-104">gluTessNormal función)</span><span class="sxs-lookup"><span data-stu-id="896c3-104">gluTessNormal function</span></span>

<span data-ttu-id="896c3-105">La función **gluTessNormal** especifica una normal para un polígono.</span><span class="sxs-lookup"><span data-stu-id="896c3-105">The **gluTessNormal** function specifies a normal for a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="896c3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="896c3-106">Syntax</span></span>


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a><span data-ttu-id="896c3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="896c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="896c3-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="896c3-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="896c3-109">Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="896c3-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="896c3-110">*x*</span><span class="sxs-lookup"><span data-stu-id="896c3-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="896c3-111">Componente de la coordenada x de un normal.</span><span class="sxs-lookup"><span data-stu-id="896c3-111">The x-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="896c3-112">*y*</span><span class="sxs-lookup"><span data-stu-id="896c3-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="896c3-113">Componente de la coordenada y de un normal.</span><span class="sxs-lookup"><span data-stu-id="896c3-113">The y-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="896c3-114">*z*</span><span class="sxs-lookup"><span data-stu-id="896c3-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="896c3-115">Componente de la coordenada z de un normal.</span><span class="sxs-lookup"><span data-stu-id="896c3-115">The z-coordinate component of a normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="896c3-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="896c3-116">Return value</span></span>

<span data-ttu-id="896c3-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="896c3-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="896c3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="896c3-118">Remarks</span></span>

<span data-ttu-id="896c3-119">La función **gluTessNormal** describe una normal para un polígono que defina.</span><span class="sxs-lookup"><span data-stu-id="896c3-119">The **gluTessNormal** function describes a normal for a polygon that you define.</span></span> <span data-ttu-id="896c3-120">Todos los datos de entrada se proyectan en un plano perpendicular a uno de los tres ejes de coordenadas antes de la teselación, y todos los triángulos de salida se orientan en sentido contrario a las agujas del reloj con respecto al normal.</span><span class="sxs-lookup"><span data-stu-id="896c3-120">All input data is projected onto a plane perpendicular to one of the three coordinate axes before tessellation, and all output triangles are oriented counterclockwise with respect to the normal.</span></span> <span data-ttu-id="896c3-121">(Para obtener orientación en el sentido de las agujas del reloj, invierta el signo del normal proporcionado).</span><span class="sxs-lookup"><span data-stu-id="896c3-121">(To obtain clockwise orientation, reverse the sign of the supplied normal).</span></span> <span data-ttu-id="896c3-122">Por ejemplo, si sabe que todos los polígonos se encuentran en el plano x-y, llame a **gluTessNormal**(tess, 0,0, 0,0, 1,0) antes de representar los polígonos.</span><span class="sxs-lookup"><span data-stu-id="896c3-122">For example, if you know that all polygons lie in the x-y plane, call **gluTessNormal**(tess, 0.0, 0.0, 1.0) before rendering any polygons.</span></span>

<span data-ttu-id="896c3-123">Si la normal proporcionada es (0,0, 0,0, 0,0) (el valor predeterminado), la normal se determina de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="896c3-123">If the supplied normal is (0.0, 0.0, 0.0) (the default value), the normal is determined as follows:</span></span>

1.  <span data-ttu-id="896c3-124">La dirección del normal, hasta su signo, se encuentra al ajustar un plano a los vértices, sin tener en cuenta cómo se conectan los vértices.</span><span class="sxs-lookup"><span data-stu-id="896c3-124">The direction of the normal, up to its sign, is found by fitting a plane to the vertexes, without regard to how the vertexes are connected.</span></span> <span data-ttu-id="896c3-125">Se espera que los datos de entrada se encuentren aproximadamente en el plano; de lo contrario, la proyección perpendicular a uno de los tres ejes de coordenadas puede cambiar la geometría de forma sustancial.</span><span class="sxs-lookup"><span data-stu-id="896c3-125">It is expected that the input data lies approximately in the plane; otherwise projection perpendicular to one of the three coordinate axes can change the geometry substantially.</span></span>
2.  <span data-ttu-id="896c3-126">El signo de la normal se elige de modo que la suma de las áreas con signo de todos los contornos de entrada no sea negativa (cuando un contorno en sentido contrario tenga un área positiva).</span><span class="sxs-lookup"><span data-stu-id="896c3-126">The sign of the normal is chosen so that the sum of the signed areas of all input contours is nonnegative (where a counterclockwise contour has positive area).</span></span>

<span data-ttu-id="896c3-127">La normal proporcionada se conserva hasta que otra llamada a **gluTessNormal** lo cambia.</span><span class="sxs-lookup"><span data-stu-id="896c3-127">The supplied normal persists until another call to **gluTessNormal** changes it.</span></span>

## <a name="requirements"></a><span data-ttu-id="896c3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="896c3-128">Requirements</span></span>



| <span data-ttu-id="896c3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="896c3-129">Requirement</span></span> | <span data-ttu-id="896c3-130">Value</span><span class="sxs-lookup"><span data-stu-id="896c3-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="896c3-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="896c3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="896c3-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="896c3-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="896c3-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="896c3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="896c3-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="896c3-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="896c3-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="896c3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="896c3-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="896c3-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="896c3-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="896c3-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="896c3-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="896c3-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="896c3-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="896c3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="896c3-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="896c3-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="896c3-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="896c3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="896c3-142">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="896c3-142">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="896c3-143">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="896c3-143">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="896c3-144">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="896c3-144">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> </dl>

 

 





