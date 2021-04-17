---
title: función gluCylinder (GLU. h)
description: La función gluCylinder dibuja un cilindro.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- gluCylinder (función) OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666031"
---
# <a name="glucylinder-function"></a><span data-ttu-id="1f953-104">gluCylinder función)</span><span class="sxs-lookup"><span data-stu-id="1f953-104">gluCylinder function</span></span>

<span data-ttu-id="1f953-105">La función **gluCylinder** dibuja un cilindro.</span><span class="sxs-lookup"><span data-stu-id="1f953-105">The **gluCylinder** function draws a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f953-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f953-106">Syntax</span></span>


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="1f953-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f953-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f953-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="1f953-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="1f953-109">El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="1f953-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1f953-110">*baseRadius*</span><span class="sxs-lookup"><span data-stu-id="1f953-110">*baseRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="1f953-111">Radio del cilindro en *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="1f953-111">The radius of the cylinder at *z* = 0.</span></span>

</dd> <dt>

<span data-ttu-id="1f953-112">*Radio*</span><span class="sxs-lookup"><span data-stu-id="1f953-112">*topRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="1f953-113">Radio del cilindro en el alto de *z*  =  .</span><span class="sxs-lookup"><span data-stu-id="1f953-113">The radius of the cylinder at *z* = *height*.</span></span>

</dd> <dt>

<span data-ttu-id="1f953-114">*height*</span><span class="sxs-lookup"><span data-stu-id="1f953-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="1f953-115">Alto del cilindro.</span><span class="sxs-lookup"><span data-stu-id="1f953-115">The height of the cylinder.</span></span>

</dd> <dt>

<span data-ttu-id="1f953-116">*segmento*</span><span class="sxs-lookup"><span data-stu-id="1f953-116">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="1f953-117">Número de subdivisiones alrededor del eje z.</span><span class="sxs-lookup"><span data-stu-id="1f953-117">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="1f953-118">*pilas*</span><span class="sxs-lookup"><span data-stu-id="1f953-118">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="1f953-119">Número de subdivisiones a lo largo del eje z.</span><span class="sxs-lookup"><span data-stu-id="1f953-119">The number of subdivisions along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f953-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f953-120">Return value</span></span>

<span data-ttu-id="1f953-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1f953-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f953-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f953-122">Remarks</span></span>

<span data-ttu-id="1f953-123">La función **gluCylinder** dibuja un cilindro orientado a lo largo del eje z.</span><span class="sxs-lookup"><span data-stu-id="1f953-123">The **gluCylinder** function draws a cylinder oriented along the z-axis.</span></span> <span data-ttu-id="1f953-124">La base del cilindro se coloca en *z* = 0 y la parte superior en la   =  *altura* z.</span><span class="sxs-lookup"><span data-stu-id="1f953-124">The base of the cylinder is placed at *z* = 0, and the top at *z* = *height*.</span></span> <span data-ttu-id="1f953-125">Al igual que una esfera, un cilindro se subdivide alrededor del eje z en segmentos y a lo largo del eje z en pilas.</span><span class="sxs-lookup"><span data-stu-id="1f953-125">Like a sphere, a cylinder is subdivided around the z-axis into slices, and along the z-axis into stacks.</span></span>

<span data-ttu-id="1f953-126">Tenga en cuenta que si el valor de *RADIUS* es cero, esta rutina generará un cono.</span><span class="sxs-lookup"><span data-stu-id="1f953-126">Note that if *topRadius* is set to zero, then this routine will generate a cone.</span></span>

<span data-ttu-id="1f953-127">Si la orientación se establece en GLU \_ fuera de (con [**gluQuadricOrientation**](gluquadricorientation.md)), cualquier normal generado apunta al eje z.</span><span class="sxs-lookup"><span data-stu-id="1f953-127">If the orientation is set to GLU\_OUTSIDE (with [**gluQuadricOrientation**](gluquadricorientation.md)), then any generated normals point away from the z-axis.</span></span> <span data-ttu-id="1f953-128">De lo contrario, apuntan hacia el eje z.</span><span class="sxs-lookup"><span data-stu-id="1f953-128">Otherwise, they point toward the z-axis.</span></span>

<span data-ttu-id="1f953-129">Si la texturización está activada (con [**gluQuadricTexture**](gluquadrictexture.md)): se generan coordenadas de textura para que *t* se rango linealmente de 0,0 a *z* = 0 a 1,0 a  =  *altura* z; y *s* va de 0,0 en el eje y positivo, a 0,25 en el eje x positivo, a 0,5 en el eje y positivo, a 0,75 en el eje x negativo y de nuevo a 1,0 en el eje y positivo.</span><span class="sxs-lookup"><span data-stu-id="1f953-129">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)): texture coordinates are generated so that *t* ranges linearly from 0.0 at *z* = 0 to 1.0 at *z* = *height*; and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f953-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f953-130">Requirements</span></span>



| <span data-ttu-id="1f953-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f953-131">Requirement</span></span> | <span data-ttu-id="1f953-132">Value</span><span class="sxs-lookup"><span data-stu-id="1f953-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1f953-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f953-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1f953-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1f953-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1f953-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f953-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1f953-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1f953-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1f953-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f953-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f953-138"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f953-138"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1f953-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f953-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f953-140"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f953-140"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1f953-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f953-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f953-142"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f953-142"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f953-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f953-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f953-144">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="1f953-144">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="1f953-145">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="1f953-145">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="1f953-146">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="1f953-146">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="1f953-147">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="1f953-147">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="1f953-148">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="1f953-148">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="1f953-149">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="1f953-149">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





