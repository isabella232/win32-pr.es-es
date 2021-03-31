---
title: función gluQuadricOrientation (GLU. h)
description: La función gluQuadricOrientation especifica la orientación interior o externa para Quadrics.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- gluQuadricOrientation (función) OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05ffb1eeff199297943e678783731a26a38092a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800992"
---
# <a name="gluquadricorientation-function"></a><span data-ttu-id="5cd7b-104">gluQuadricOrientation función)</span><span class="sxs-lookup"><span data-stu-id="5cd7b-104">gluQuadricOrientation function</span></span>

<span data-ttu-id="5cd7b-105">La función **gluQuadricOrientation** especifica la orientación interior o externa para Quadrics.</span><span class="sxs-lookup"><span data-stu-id="5cd7b-105">The **gluQuadricOrientation** function specifies inside or outside orientation for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cd7b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5cd7b-106">Syntax</span></span>


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a><span data-ttu-id="5cd7b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5cd7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cd7b-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="5cd7b-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="5cd7b-109">El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="5cd7b-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5cd7b-110">*orientation*</span><span class="sxs-lookup"><span data-stu-id="5cd7b-110">*orientation*</span></span> 
</dt> <dd>

<span data-ttu-id="5cd7b-111">Orientación deseada.</span><span class="sxs-lookup"><span data-stu-id="5cd7b-111">The desired orientation.</span></span> <span data-ttu-id="5cd7b-112">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="5cd7b-112">The following values are valid.</span></span>



| <span data-ttu-id="5cd7b-113">Value</span><span class="sxs-lookup"><span data-stu-id="5cd7b-113">Value</span></span>                                                                                                                                                   | <span data-ttu-id="5cd7b-114">Significado</span><span class="sxs-lookup"><span data-stu-id="5cd7b-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <span data-ttu-id="5cd7b-115"><dt>**GLU \_ fuera**</dt></span><span class="sxs-lookup"><span data-stu-id="5cd7b-115"><dt>**GLU\_OUTSIDE**</dt></span></span> </dl> | <span data-ttu-id="5cd7b-116">Dibuje Quadrics con normales que señalen hacia afuera.</span><span class="sxs-lookup"><span data-stu-id="5cd7b-116">Draw quadrics with normals pointing outward.</span></span> <span data-ttu-id="5cd7b-117">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5cd7b-117">This is the default value.</span></span><br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <span data-ttu-id="5cd7b-118"><dt>**GLU \_ dentro de**</dt></span><span class="sxs-lookup"><span data-stu-id="5cd7b-118"><dt>**GLU\_INSIDE**</dt></span></span> </dl>    | <span data-ttu-id="5cd7b-119">Dibuje Quadrics con normales que señalen hacia adentro.</span><span class="sxs-lookup"><span data-stu-id="5cd7b-119">Draw quadrics with normals pointing inward.</span></span><br/>                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cd7b-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5cd7b-120">Return value</span></span>

<span data-ttu-id="5cd7b-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5cd7b-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cd7b-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cd7b-122">Remarks</span></span>

<span data-ttu-id="5cd7b-123">La función **gluQuadricOrientation** especifica qué tipo de orientación se desea para Quadrics representada con **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="5cd7b-123">The **gluQuadricOrientation** function specifies what kind of orientation is desired for quadrics rendered with **quadObject**.</span></span> <span data-ttu-id="5cd7b-124">La interpretación de hacia afuera y hacia adentro depende de la quadric que se está dibujando.</span><span class="sxs-lookup"><span data-stu-id="5cd7b-124">The interpretation of outward and inward depends on the quadric being drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cd7b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cd7b-125">Requirements</span></span>



| <span data-ttu-id="5cd7b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cd7b-126">Requirement</span></span> | <span data-ttu-id="5cd7b-127">Value</span><span class="sxs-lookup"><span data-stu-id="5cd7b-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5cd7b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cd7b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5cd7b-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5cd7b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5cd7b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cd7b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5cd7b-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5cd7b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5cd7b-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cd7b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cd7b-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cd7b-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="5cd7b-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5cd7b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="5cd7b-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5cd7b-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5cd7b-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5cd7b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cd7b-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cd7b-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cd7b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cd7b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cd7b-139">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="5cd7b-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="5cd7b-140">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="5cd7b-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="5cd7b-141">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="5cd7b-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="5cd7b-142">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="5cd7b-142">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





