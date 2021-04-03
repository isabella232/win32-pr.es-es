---
title: función gluLookAt (GLU. h)
description: La función gluLookAt define una transformación de visualización.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- gluLookAt (función) OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5866f3c06ef6969c95eeef4b23fff7a4e7852eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905651"
---
# <a name="glulookat-function"></a><span data-ttu-id="eefc1-104">gluLookAt función)</span><span class="sxs-lookup"><span data-stu-id="eefc1-104">gluLookAt function</span></span>

<span data-ttu-id="eefc1-105">La función **gluLookAt** define una transformación de visualización.</span><span class="sxs-lookup"><span data-stu-id="eefc1-105">The **gluLookAt** function defines a viewing transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="eefc1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eefc1-106">Syntax</span></span>


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a><span data-ttu-id="eefc1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eefc1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eefc1-108">*eyex*</span><span class="sxs-lookup"><span data-stu-id="eefc1-108">*eyex*</span></span> 
</dt> <dd>

<span data-ttu-id="eefc1-109">Posición del punto de ojo.</span><span class="sxs-lookup"><span data-stu-id="eefc1-109">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="eefc1-110">*eyey*</span><span class="sxs-lookup"><span data-stu-id="eefc1-110">*eyey*</span></span> 
</dt> <dd>

<span data-ttu-id="eefc1-111">Posición del punto de ojo.</span><span class="sxs-lookup"><span data-stu-id="eefc1-111">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="eefc1-112">*eyez*</span><span class="sxs-lookup"><span data-stu-id="eefc1-112">*eyez*</span></span> 
</dt> <dd>

<span data-ttu-id="eefc1-113">Posición del punto de ojo.</span><span class="sxs-lookup"><span data-stu-id="eefc1-113">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="eefc1-114">*CenterX*</span><span class="sxs-lookup"><span data-stu-id="eefc1-114">*centerx*</span></span> 
</dt> <dd>

<span data-ttu-id="eefc1-115">Posición del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="eefc1-115">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="eefc1-116">*CenterY*</span><span class="sxs-lookup"><span data-stu-id="eefc1-116">*centery*</span></span> 
</dt> <dd>

<span data-ttu-id="eefc1-117">Posición del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="eefc1-117">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="eefc1-118">*centerz*</span><span class="sxs-lookup"><span data-stu-id="eefc1-118">*centerz*</span></span> 
</dt> <dd>

<span data-ttu-id="eefc1-119">Posición del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="eefc1-119">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="eefc1-120">*UPX*</span><span class="sxs-lookup"><span data-stu-id="eefc1-120">*upx*</span></span> 
</dt> <dd>

<span data-ttu-id="eefc1-121">Dirección del vector hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="eefc1-121">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="eefc1-122">*upy*</span><span class="sxs-lookup"><span data-stu-id="eefc1-122">*upy*</span></span> 
</dt> <dd>

<span data-ttu-id="eefc1-123">Dirección del vector hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="eefc1-123">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="eefc1-124">*upz*</span><span class="sxs-lookup"><span data-stu-id="eefc1-124">*upz*</span></span> 
</dt> <dd>

<span data-ttu-id="eefc1-125">Dirección del vector hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="eefc1-125">The direction of the up vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eefc1-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eefc1-126">Return value</span></span>

<span data-ttu-id="eefc1-127">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="eefc1-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eefc1-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eefc1-128">Remarks</span></span>

<span data-ttu-id="eefc1-129">La función **gluLookAt** crea una matriz de visualización derivada de un punto de vista, un punto de referencia que indica el centro de la escena y un vector hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="eefc1-129">The **gluLookAt** function creates a viewing matrix derived from an eye point, a reference point indicating the center of the scene, and an up vector.</span></span> <span data-ttu-id="eefc1-130">La matriz asigna el punto de referencia al eje z negativo y el punto de mira al origen, de modo que cuando se usa una matriz de proyección típica, el centro de la escena se asigna al centro de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="eefc1-130">The matrix maps the reference point to the negative z-axis and the eye point to the origin, so that when you use a typical projection matrix, the center of the scene maps to the center of the viewport.</span></span> <span data-ttu-id="eefc1-131">Del mismo modo, la dirección que describe el vector hacia arriba proyectado en el plano de visualización se asigna al eje y positivo para que apunte hacia arriba en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="eefc1-131">Similarly, the direction described by the up vector projected onto the viewing plane is mapped to the positive y-axis so that it points upward in the viewport.</span></span> <span data-ttu-id="eefc1-132">El vector hacia arriba no debe ser paralelo a la línea de visión desde el ojo hasta el punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="eefc1-132">The up vector must not be parallel to the line of sight from the eye to the reference point.</span></span>

<span data-ttu-id="eefc1-133">La matriz generada por **gluLookAt** postmultiplica la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="eefc1-133">The matrix generated by **gluLookAt** postmultiplies the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="eefc1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eefc1-134">Requirements</span></span>



| <span data-ttu-id="eefc1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="eefc1-135">Requirement</span></span> | <span data-ttu-id="eefc1-136">Value</span><span class="sxs-lookup"><span data-stu-id="eefc1-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eefc1-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eefc1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="eefc1-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eefc1-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="eefc1-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eefc1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="eefc1-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eefc1-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="eefc1-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eefc1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="eefc1-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="eefc1-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="eefc1-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eefc1-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="eefc1-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eefc1-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="eefc1-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eefc1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eefc1-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eefc1-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eefc1-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="eefc1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eefc1-148">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="eefc1-148">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="eefc1-149">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="eefc1-149">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





