---
title: función glNormal3d (GL. h)
description: Establece el vector normal actual. | función glNormal3d (GL. h)
ms.assetid: d256aef0-3ad5-4e70-b1c8-6402434b1e67
keywords:
- glNormal3d (función) OpenGL
topic_type:
- apiref
api_name:
- glNormal3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ab158e298ff20cce635ab4002f38ca82fdaa2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083683"
---
# <a name="glnormal3d-function"></a><span data-ttu-id="ce6ce-105">glNormal3d función)</span><span class="sxs-lookup"><span data-stu-id="ce6ce-105">glNormal3d function</span></span>

<span data-ttu-id="ce6ce-106">Establece el vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce6ce-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce6ce-107">Syntax</span></span>


```C++
void WINAPI glNormal3d(
   GLdouble nx,
   GLdouble ny,
   GLdouble nz
);
```



## <a name="parameters"></a><span data-ttu-id="ce6ce-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce6ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce6ce-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="ce6ce-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="ce6ce-110">Especifica la coordenada x del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="ce6ce-111">*1002*</span><span class="sxs-lookup"><span data-stu-id="ce6ce-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="ce6ce-112">Especifica la coordenada y del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="ce6ce-113">*Zelanda*</span><span class="sxs-lookup"><span data-stu-id="ce6ce-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="ce6ce-114">Especifica la coordenada z del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce6ce-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce6ce-115">Return value</span></span>

<span data-ttu-id="ce6ce-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce6ce-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce6ce-117">Remarks</span></span>

<span data-ttu-id="ce6ce-118">La normal actual se establece en las coordenadas especificadas siempre que se llama a la función **glNormal3d**.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-118">The current normal is set to the given coordinates whenever you call the **glNormal3d** function.</span></span>

<span data-ttu-id="ce6ce-119">Los argumentos byte, Short o Integer se convierten al formato de punto flotante mediante una asignación lineal que asigna el valor entero representable más positivo a 1,0 y el valor entero representable más negativo a-1,0.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-119">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="ce6ce-120">Las normales especificadas mediante **glNormal3d** no necesitan tener una longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-120">Normals specified by using **glNormal3d** need not have unit length.</span></span> <span data-ttu-id="ce6ce-121">Si la normalización está habilitada, las normales especificadas con **glNormal3d** se normalizan después de la transformación.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-121">If normalization is enabled, then normals specified with **glNormal3d** are normalized after transformation.</span></span> <span data-ttu-id="ce6ce-122">Puede controlar la normalización mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento libro de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="ce6ce-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="ce6ce-123">De forma predeterminada, la normalización está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-123">By default, normalization is disabled.</span></span> <span data-ttu-id="ce6ce-124">Puede actualizar la normal actual en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-124">You can update the current normal at any time.</span></span> <span data-ttu-id="ce6ce-125">En concreto, puede llamar a **glNormal3d** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ce6ce-125">In particular, you can call **glNormal3d** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="ce6ce-126">Las siguientes funciones recuperan información relacionada con **glNormal3d**:</span><span class="sxs-lookup"><span data-stu-id="ce6ce-126">The following functions retrieve information related to **glNormal3d**:</span></span>

<span data-ttu-id="ce6ce-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ actual \_ normal</span><span class="sxs-lookup"><span data-stu-id="ce6ce-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="ce6ce-128">[**glIsEnable**](glisenabled.md) con el argumento \_ normalizar libro de contabilidad</span><span class="sxs-lookup"><span data-stu-id="ce6ce-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6ce-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce6ce-129">Requirements</span></span>



| <span data-ttu-id="ce6ce-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce6ce-130">Requirement</span></span> | <span data-ttu-id="ce6ce-131">Value</span><span class="sxs-lookup"><span data-stu-id="ce6ce-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6ce-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce6ce-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6ce-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ce6ce-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ce6ce-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce6ce-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6ce-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ce6ce-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce6ce-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce6ce-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce6ce-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce6ce-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ce6ce-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce6ce-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce6ce-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce6ce-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ce6ce-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ce6ce-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce6ce-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce6ce-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce6ce-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce6ce-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6ce-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ce6ce-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ce6ce-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="ce6ce-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="ce6ce-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ce6ce-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ce6ce-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="ce6ce-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="ce6ce-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="ce6ce-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="ce6ce-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="ce6ce-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





