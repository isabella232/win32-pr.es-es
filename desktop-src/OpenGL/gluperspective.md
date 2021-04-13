---
title: función gluPerspective (GLU. h)
description: La función gluPerspective configura una matriz de proyección en perspectiva.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- gluPerspective (función) OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf30fc7dc4c6ba5a56efd3def6a5a7178f81ed49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422510"
---
# <a name="gluperspective-function"></a><span data-ttu-id="23f6f-104">gluPerspective función)</span><span class="sxs-lookup"><span data-stu-id="23f6f-104">gluPerspective function</span></span>

<span data-ttu-id="23f6f-105">La función **gluPerspective** configura una matriz de proyección en perspectiva.</span><span class="sxs-lookup"><span data-stu-id="23f6f-105">The **gluPerspective** function sets up a perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f6f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23f6f-106">Syntax</span></span>


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="23f6f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23f6f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f6f-108">*fovy*</span><span class="sxs-lookup"><span data-stu-id="23f6f-108">*fovy*</span></span> 
</dt> <dd>

<span data-ttu-id="23f6f-109">Campo de ángulo de vista, en grados, en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="23f6f-109">The field of view angle, in degrees, in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="23f6f-110">*aspect*</span><span class="sxs-lookup"><span data-stu-id="23f6f-110">*aspect*</span></span> 
</dt> <dd>

<span data-ttu-id="23f6f-111">La relación de aspecto que determina el campo de la vista en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="23f6f-111">The aspect ratio that determines the field of view in the x-direction.</span></span> <span data-ttu-id="23f6f-112">La relación de aspecto es la proporción de *x* (ancho) a *y* (alto).</span><span class="sxs-lookup"><span data-stu-id="23f6f-112">The aspect ratio is the ratio of *x* (width) to *y* (height).</span></span>

</dd> <dt>

<span data-ttu-id="23f6f-113">*zNear*</span><span class="sxs-lookup"><span data-stu-id="23f6f-113">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="23f6f-114">Distancia desde el visor al plano de recorte cercano (siempre positivo).</span><span class="sxs-lookup"><span data-stu-id="23f6f-114">The distance from the viewer to the near clipping plane (always positive).</span></span>

</dd> <dt>

<span data-ttu-id="23f6f-115">*zFar*</span><span class="sxs-lookup"><span data-stu-id="23f6f-115">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="23f6f-116">Distancia desde el visor al plano de recorte lejano (siempre positivo).</span><span class="sxs-lookup"><span data-stu-id="23f6f-116">The distance from the viewer to the far clipping plane (always positive).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f6f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23f6f-117">Return value</span></span>

<span data-ttu-id="23f6f-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="23f6f-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23f6f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23f6f-119">Remarks</span></span>

<span data-ttu-id="23f6f-120">La función **gluPerspective** especifica un frustum de visualización en el sistema de coordenadas universal.</span><span class="sxs-lookup"><span data-stu-id="23f6f-120">The **gluPerspective** function specifies a viewing frustum into the world coordinate system.</span></span> <span data-ttu-id="23f6f-121">En general, la relación de aspecto de **gluPerspective** debe coincidir con la relación de aspecto de la ventanilla asociada.</span><span class="sxs-lookup"><span data-stu-id="23f6f-121">In general, the aspect ratio in **gluPerspective** should match the aspect ratio of the associated viewport.</span></span> <span data-ttu-id="23f6f-122">Por ejemplo, el *aspecto* = 2,0 significa que el ángulo de vista del visor es el doble de ancho en *x* que en *y*.</span><span class="sxs-lookup"><span data-stu-id="23f6f-122">For example, *aspect* = 2.0 means the viewer's angle of view is twice as wide in *x* as it is in *y*.</span></span> <span data-ttu-id="23f6f-123">Si la ventanilla es el doble de ancha que la de alta, se muestra la imagen sin distorsión.</span><span class="sxs-lookup"><span data-stu-id="23f6f-123">If the viewport is twice as wide as it is tall, it displays the image without distortion.</span></span>

<span data-ttu-id="23f6f-124">La matriz generada por **gluPerspective** se multiplica por la matriz actual, al igual que si se llamara a [**glMultMatrix**](glmultmatrix.md) con la matriz generada.</span><span class="sxs-lookup"><span data-stu-id="23f6f-124">The matrix generated by **gluPerspective** is multiplied by the current matrix, just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span> <span data-ttu-id="23f6f-125">Para cargar la matriz de perspectiva en la pila de matriz actual, preceda a la llamada a **gluPerspective** con una llamada a [**glLoadIdentity**](glloadidentity.md).</span><span class="sxs-lookup"><span data-stu-id="23f6f-125">To load the perspective matrix onto the current matrix stack instead, precede the call to **gluPerspective** with a call to [**glLoadIdentity**](glloadidentity.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23f6f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23f6f-126">Requirements</span></span>



| <span data-ttu-id="23f6f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="23f6f-127">Requirement</span></span> | <span data-ttu-id="23f6f-128">Value</span><span class="sxs-lookup"><span data-stu-id="23f6f-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23f6f-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23f6f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="23f6f-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="23f6f-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="23f6f-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23f6f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="23f6f-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="23f6f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="23f6f-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23f6f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="23f6f-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="23f6f-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="23f6f-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23f6f-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="23f6f-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23f6f-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="23f6f-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23f6f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23f6f-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23f6f-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23f6f-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="23f6f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f6f-140">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="23f6f-140">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="23f6f-141">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="23f6f-141">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="23f6f-142">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="23f6f-142">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="23f6f-143">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="23f6f-143">**gluOrtho2D**</span></span>](gluortho2d.md)
</dt> </dl>

 

 





