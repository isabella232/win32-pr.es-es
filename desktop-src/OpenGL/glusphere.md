---
title: función gluSphere (GLU. h)
description: La función gluSphere dibuja una esfera.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- gluSphere (función) OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ff4833c705aae34fdb7830c264fee91414116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491908"
---
# <a name="glusphere-function"></a><span data-ttu-id="ea4f2-104">gluSphere función)</span><span class="sxs-lookup"><span data-stu-id="ea4f2-104">gluSphere function</span></span>

<span data-ttu-id="ea4f2-105">La función **gluSphere** dibuja una esfera.</span><span class="sxs-lookup"><span data-stu-id="ea4f2-105">The **gluSphere** function draws a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4f2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea4f2-106">Syntax</span></span>


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="ea4f2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea4f2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea4f2-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="ea4f2-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="ea4f2-109">El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="ea4f2-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ea4f2-110">*tórica*</span><span class="sxs-lookup"><span data-stu-id="ea4f2-110">*radius*</span></span> 
</dt> <dd>

<span data-ttu-id="ea4f2-111">Radio de la esfera.</span><span class="sxs-lookup"><span data-stu-id="ea4f2-111">The radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="ea4f2-112">*segmento*</span><span class="sxs-lookup"><span data-stu-id="ea4f2-112">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="ea4f2-113">Número de subdivisiones alrededor del eje z (similar a las líneas de longitud).</span><span class="sxs-lookup"><span data-stu-id="ea4f2-113">The number of subdivisions around the z-axis (similar to lines of longitude).</span></span>

</dd> <dt>

<span data-ttu-id="ea4f2-114">*pilas*</span><span class="sxs-lookup"><span data-stu-id="ea4f2-114">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="ea4f2-115">El número de subdivisiones a lo largo del eje z (similar a las líneas de la latitud).</span><span class="sxs-lookup"><span data-stu-id="ea4f2-115">The number of subdivisions along the z-axis (similar to lines of latitude).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea4f2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea4f2-116">Return value</span></span>

<span data-ttu-id="ea4f2-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ea4f2-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea4f2-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea4f2-118">Remarks</span></span>

<span data-ttu-id="ea4f2-119">La función **gluSphere** dibuja una esfera del radio determinado centrado alrededor del origen.</span><span class="sxs-lookup"><span data-stu-id="ea4f2-119">The **gluSphere** function draws a sphere of the given radius centered around the origin.</span></span> <span data-ttu-id="ea4f2-120">La esfera se subdivide alrededor del eje z en segmentos y a lo largo del eje z en pilas (similar a las líneas de longitud y latitud).</span><span class="sxs-lookup"><span data-stu-id="ea4f2-120">The sphere is subdivided around the z-axis into slices and along the z-axis into stacks (similar to lines of longitude and latitude).</span></span>

<span data-ttu-id="ea4f2-121">Si la orientación se establece en GLU \_ fuera de (con **gluQuadricOrientation**), cualquier normal generado apunta fuera del centro de la esfera.</span><span class="sxs-lookup"><span data-stu-id="ea4f2-121">If the orientation is set to GLU\_OUTSIDE (with **gluQuadricOrientation**), any normals generated point away from the center of the sphere.</span></span> <span data-ttu-id="ea4f2-122">De lo contrario, apuntan hacia el centro de la esfera.</span><span class="sxs-lookup"><span data-stu-id="ea4f2-122">Otherwise, they point toward the center of the sphere.</span></span>

<span data-ttu-id="ea4f2-123">Si la texturización está activada (con **gluQuadricTexture**): se generan coordenadas de textura para que *t* vaya de 0,0 a *z* =*-RADIUS* a 1,0 en radio *z*  =   (*t* aumenta linealmente a lo largo de las líneas longitudinales); y *s* van desde 0,0 en el eje y positivo hasta 0,25 en el eje x positivo, a 0,5 en el eje y negativo, a 0,75 en el eje x negativo y de nuevo a 1,0 en el eje y positivo.</span><span class="sxs-lookup"><span data-stu-id="ea4f2-123">If texturing is turned on (with **gluQuadricTexture**): texture coordinates are generated so that *t* ranges from 0.0 at *z* = -*radius* to 1.0 at *z* = *radius* (*t* increases linearly along longitudinal lines); and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea4f2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea4f2-124">Requirements</span></span>



| <span data-ttu-id="ea4f2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea4f2-125">Requirement</span></span> | <span data-ttu-id="ea4f2-126">Value</span><span class="sxs-lookup"><span data-stu-id="ea4f2-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4f2-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea4f2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4f2-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ea4f2-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ea4f2-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea4f2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4f2-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ea4f2-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ea4f2-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea4f2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea4f2-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea4f2-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ea4f2-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea4f2-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea4f2-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea4f2-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ea4f2-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea4f2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea4f2-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea4f2-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4f2-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea4f2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4f2-138">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="ea4f2-138">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="ea4f2-139">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="ea4f2-139">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="ea4f2-140">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="ea4f2-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="ea4f2-141">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="ea4f2-141">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="ea4f2-142">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="ea4f2-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="ea4f2-143">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="ea4f2-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





