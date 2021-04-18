---
title: función gluPartialDisk (GLU. h)
description: La función gluPartialDisk dibuja un arco de un disco.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- gluPartialDisk (función) OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665915"
---
# <a name="glupartialdisk-function"></a><span data-ttu-id="84387-104">gluPartialDisk función)</span><span class="sxs-lookup"><span data-stu-id="84387-104">gluPartialDisk function</span></span>

<span data-ttu-id="84387-105">La función **gluPartialDisk** dibuja un arco de un disco.</span><span class="sxs-lookup"><span data-stu-id="84387-105">The **gluPartialDisk** function draws an arc of a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="84387-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84387-106">Syntax</span></span>


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a><span data-ttu-id="84387-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84387-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84387-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="84387-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="84387-109">Objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="84387-109">A quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="84387-110">*innerRadius*</span><span class="sxs-lookup"><span data-stu-id="84387-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="84387-111">Radio interior del disco parcial (puede ser cero).</span><span class="sxs-lookup"><span data-stu-id="84387-111">The inner radius of the partial disk (can be zero).</span></span>

</dd> <dt>

<span data-ttu-id="84387-112">*outerRadius*</span><span class="sxs-lookup"><span data-stu-id="84387-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="84387-113">Radio exterior del disco parcial.</span><span class="sxs-lookup"><span data-stu-id="84387-113">The outer radius of the partial disk.</span></span>

</dd> <dt>

<span data-ttu-id="84387-114">*segmento*</span><span class="sxs-lookup"><span data-stu-id="84387-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="84387-115">Número de subdivisiones alrededor del eje z.</span><span class="sxs-lookup"><span data-stu-id="84387-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="84387-116">*bucles*</span><span class="sxs-lookup"><span data-stu-id="84387-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="84387-117">El número de anillos concéntricos sobre el origen en el que se subdivide el disco parcial.</span><span class="sxs-lookup"><span data-stu-id="84387-117">The number of concentric rings about the origin into which the partial disk is subdivided.</span></span>

</dd> <dt>

<span data-ttu-id="84387-118">*startAngle*</span><span class="sxs-lookup"><span data-stu-id="84387-118">*startAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="84387-119">Ángulo inicial, en grados, de la parte del disco.</span><span class="sxs-lookup"><span data-stu-id="84387-119">The starting angle, in degrees, of the disk portion.</span></span>

</dd> <dt>

<span data-ttu-id="84387-120">*sweepAngle*</span><span class="sxs-lookup"><span data-stu-id="84387-120">*sweepAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="84387-121">Ángulo de barrido, en grados, de la parte del disco.</span><span class="sxs-lookup"><span data-stu-id="84387-121">The sweep angle, in degrees, of the disk portion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84387-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84387-122">Return value</span></span>

<span data-ttu-id="84387-123">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="84387-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="84387-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84387-124">Remarks</span></span>

<span data-ttu-id="84387-125">La función **gluPartialDisk** representa un disco parcial en el plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="84387-125">The **gluPartialDisk** function renders a partial disk on the *z* = 0 plane.</span></span> <span data-ttu-id="84387-126">Un disco parcial es similar a un disco completo, excepto en que solo se incluye el subconjunto del *disco desde la* entrada de la misma a la   +  *sweepAngle* (donde 0 grados se encuentra a lo largo del eje y positivo, 90 grados está a lo largo del eje x positivo, 180 grados se encuentra a lo largo del 270 eje y de la x negativo).</span><span class="sxs-lookup"><span data-stu-id="84387-126">A partial disk is similar to a full disk, except that only the subset of the disk from *startAngle* through *startAngle* + *sweepAngle* is included (where 0 degrees is along the positive y-axis, 90 degrees is along the positive x-axis, 180 degrees is along the negative y-axis, and 270 degrees is along the negative x-axis).</span></span>

<span data-ttu-id="84387-127">El disco parcial tiene un radio de *outerRadius* y contiene un orificio circular concéntrico con un radio de *innerRadius*.</span><span class="sxs-lookup"><span data-stu-id="84387-127">The partial disk has a radius of *outerRadius* and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="84387-128">Si *innerRadius* es cero, no se genera ningún hueco.</span><span class="sxs-lookup"><span data-stu-id="84387-128">If *innerRadius* is zero, then no hole is generated.</span></span> <span data-ttu-id="84387-129">El disco parcial se divide por el eje z en segmentos (por ejemplo, segmentos de pizza) y también sobre el eje z en anillos (como se especifica en *segmentos* y *bucles*, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="84387-129">The partial disk is subdivided around the z-axis into slices (like pizza slices), and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="84387-130">Con respecto a la orientación, se considera que el lado z positivo del disco parcial está fuera (vea [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="84387-130">With respect to orientation, the positive z-side of the partial disk is considered to be outside (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="84387-131">Esto significa que si la orientación se establece en GLU \_ fuera de, cualquier punto normal generado a lo largo del eje z positivo.</span><span class="sxs-lookup"><span data-stu-id="84387-131">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="84387-132">Si ha activado la texturización (con [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** genera coordenadas de textura de forma lineal, de modo que, donde *r*  =  *outerRadius*, el valor de (*r*, 0,0) es (1, 0,5); en (0, *r*, 0) es (0,5, 1); en (*r*, 0, 0) es (0, 0,5) y en (0, *r*, 0) es (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="84387-132">If you have turned on texturing (with [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** generates texture coordinates linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (*r*, 0, 0) it is (0, 0.5); and at (0, *r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="84387-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84387-133">Requirements</span></span>



| <span data-ttu-id="84387-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="84387-134">Requirement</span></span> | <span data-ttu-id="84387-135">Value</span><span class="sxs-lookup"><span data-stu-id="84387-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="84387-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84387-136">Minimum supported client</span></span><br/> | <span data-ttu-id="84387-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="84387-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="84387-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84387-138">Minimum supported server</span></span><br/> | <span data-ttu-id="84387-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="84387-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="84387-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84387-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="84387-141"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="84387-141"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="84387-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84387-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="84387-143"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84387-143"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="84387-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="84387-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84387-145"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84387-145"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84387-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="84387-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84387-147">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="84387-147">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="84387-148">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="84387-148">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="84387-149">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="84387-149">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="84387-150">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="84387-150">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="84387-151">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="84387-151">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="84387-152">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="84387-152">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





