---
title: función gluDisk (GLU. h)
description: La función gluDisk dibuja un disco.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- gluDisk (función) OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079340"
---
# <a name="gludisk-function"></a><span data-ttu-id="ebfc2-104">gluDisk función)</span><span class="sxs-lookup"><span data-stu-id="ebfc2-104">gluDisk function</span></span>

<span data-ttu-id="ebfc2-105">La función **gluDisk** dibuja un disco.</span><span class="sxs-lookup"><span data-stu-id="ebfc2-105">The **gluDisk** function draws a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebfc2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebfc2-106">Syntax</span></span>


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a><span data-ttu-id="ebfc2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebfc2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebfc2-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="ebfc2-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="ebfc2-109">El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="ebfc2-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ebfc2-110">*innerRadius*</span><span class="sxs-lookup"><span data-stu-id="ebfc2-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="ebfc2-111">El radio interno del disco (puede ser cero).</span><span class="sxs-lookup"><span data-stu-id="ebfc2-111">The inner radius of the disk (may be zero).</span></span>

</dd> <dt>

<span data-ttu-id="ebfc2-112">*outerRadius*</span><span class="sxs-lookup"><span data-stu-id="ebfc2-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="ebfc2-113">Radio exterior del disco.</span><span class="sxs-lookup"><span data-stu-id="ebfc2-113">The outer radius of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="ebfc2-114">*segmento*</span><span class="sxs-lookup"><span data-stu-id="ebfc2-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="ebfc2-115">Número de subdivisiones alrededor del eje z.</span><span class="sxs-lookup"><span data-stu-id="ebfc2-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="ebfc2-116">*bucles*</span><span class="sxs-lookup"><span data-stu-id="ebfc2-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="ebfc2-117">El número de anillos concéntricos sobre el origen en el que se subdivide el disco.</span><span class="sxs-lookup"><span data-stu-id="ebfc2-117">The number of concentric rings about the origin into which the disk is subdivided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebfc2-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebfc2-118">Return value</span></span>

<span data-ttu-id="ebfc2-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ebfc2-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebfc2-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebfc2-120">Remarks</span></span>

<span data-ttu-id="ebfc2-121">La función **gluDisk** representa un disco en el plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="ebfc2-121">The **gluDisk** function renders a disk on the *z* = 0 plane.</span></span> <span data-ttu-id="ebfc2-122">El disco tiene un radio de *outerRadius* y contiene un orificio circular concéntrico con un radio de *innerRadius*.</span><span class="sxs-lookup"><span data-stu-id="ebfc2-122">The disk has a radius of *outerRadius*, and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="ebfc2-123">Si *innerRadius* es 0, no se genera ningún hueco.</span><span class="sxs-lookup"><span data-stu-id="ebfc2-123">If *innerRadius* is 0, then no hole is generated.</span></span> <span data-ttu-id="ebfc2-124">El disco se subdivide alrededor del eje z en segmentos (por ejemplo, segmentos de pizza) y también sobre el eje z en anillos (como se especifica en *segmentos* y *bucles*, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="ebfc2-124">The disk is subdivided around the z-axis into slices (like pizza slices) and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="ebfc2-125">Con respecto a la orientación, se considera que el lado *z* positivo del disco está *fuera* de (vea [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="ebfc2-125">With respect to orientation, the positive *z*-side of the disk is considered to be *outside* (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="ebfc2-126">Esto significa que si la orientación se establece en GLU \_ fuera de, cualquier punto normal generado a lo largo del eje z positivo.</span><span class="sxs-lookup"><span data-stu-id="ebfc2-126">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="ebfc2-127">Si la texturización está activada (con [**gluQuadricTexture**](gluquadrictexture.md)), las coordenadas de textura se generan de forma lineal , de modo que  =  *outerRadius* de r, el valor de (*r*, 0,0) es (1, 0,5); en (0, *r*, 0) es (0,5, 1); en (-*r*, 0,0) es (0, 0,5) y en (0,-*r*, 0) es (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="ebfc2-127">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)), texture coordinates are generated linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (-*r*, 0, 0) it is (0, 0.5); and at (0, -*r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebfc2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebfc2-128">Requirements</span></span>



| <span data-ttu-id="ebfc2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebfc2-129">Requirement</span></span> | <span data-ttu-id="ebfc2-130">Value</span><span class="sxs-lookup"><span data-stu-id="ebfc2-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ebfc2-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebfc2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ebfc2-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ebfc2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ebfc2-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebfc2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ebfc2-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ebfc2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ebfc2-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebfc2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebfc2-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebfc2-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ebfc2-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ebfc2-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="ebfc2-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebfc2-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ebfc2-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ebfc2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebfc2-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebfc2-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebfc2-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebfc2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebfc2-142">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="ebfc2-142">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="ebfc2-143">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="ebfc2-143">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="ebfc2-144">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="ebfc2-144">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="ebfc2-145">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="ebfc2-145">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="ebfc2-146">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="ebfc2-146">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="ebfc2-147">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="ebfc2-147">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





