---
title: función glNormal3f (GL. h)
description: Establece el vector normal actual. | función glNormal3f (GL. h)
ms.assetid: 8407996e-47fd-4c30-91f6-53d4341a1fca
keywords:
- glNormal3f (función) OpenGL
topic_type:
- apiref
api_name:
- glNormal3f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e83b874b1588ad8bd91da9e5c9f831062de9cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689795"
---
# <a name="glnormal3f-function"></a><span data-ttu-id="fde01-105">glNormal3f función)</span><span class="sxs-lookup"><span data-stu-id="fde01-105">glNormal3f function</span></span>

<span data-ttu-id="fde01-106">Establece el vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="fde01-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde01-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fde01-107">Syntax</span></span>


```C++
void WINAPI glNormal3f(
   GLfloat nx,
   GLfloat ny,
   GLfloat nz
);
```



## <a name="parameters"></a><span data-ttu-id="fde01-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fde01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde01-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="fde01-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="fde01-110">Especifica la coordenada x del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="fde01-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="fde01-111">*1002*</span><span class="sxs-lookup"><span data-stu-id="fde01-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="fde01-112">Especifica la coordenada y del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="fde01-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="fde01-113">*Zelanda*</span><span class="sxs-lookup"><span data-stu-id="fde01-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="fde01-114">Especifica la coordenada z del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="fde01-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde01-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fde01-115">Return value</span></span>

<span data-ttu-id="fde01-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fde01-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fde01-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fde01-117">Remarks</span></span>

<span data-ttu-id="fde01-118">La normal actual se establece en las coordenadas especificadas siempre que se llama a la función **glNormal3f** .</span><span class="sxs-lookup"><span data-stu-id="fde01-118">The current normal is set to the given coordinates whenever you call the **glNormal3f** function.</span></span>

<span data-ttu-id="fde01-119">Los argumentos byte, Short o Integer se convierten al formato de punto flotante con una asignación lineal que asigna el valor entero representable más positivo a 1,0 y el valor entero representable más negativo a-1,0.</span><span class="sxs-lookup"><span data-stu-id="fde01-119">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="fde01-120">Las normales especificadas mediante **glNormal3f** no necesitan tener una longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="fde01-120">Normals specified by using **glNormal3f** need not have unit length.</span></span> <span data-ttu-id="fde01-121">Si la normalización está habilitada, las normales especificadas con **glNormal3f** se normalizan después de la transformación.</span><span class="sxs-lookup"><span data-stu-id="fde01-121">If normalization is enabled, then normals specified with **glNormal3f** are normalized after transformation.</span></span> <span data-ttu-id="fde01-122">Puede controlar la normalización mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento libro de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="fde01-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="fde01-123">De forma predeterminada, la normalización está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="fde01-123">By default, normalization is disabled.</span></span> <span data-ttu-id="fde01-124">Puede actualizar la normal actual en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="fde01-124">You can update the current normal at any time.</span></span> <span data-ttu-id="fde01-125">En concreto, puede llamar a **glNormal3f** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fde01-125">In particular, you can call **glNormal3f** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="fde01-126">Las siguientes funciones recuperan información relacionada con **glNormal3f**:</span><span class="sxs-lookup"><span data-stu-id="fde01-126">The following functions retrieve information related to **glNormal3f**:</span></span>

<span data-ttu-id="fde01-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ actual \_ normal</span><span class="sxs-lookup"><span data-stu-id="fde01-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="fde01-128">[**glIsEnable**](glisenabled.md) con el argumento \_ normalizar libro de contabilidad</span><span class="sxs-lookup"><span data-stu-id="fde01-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="fde01-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fde01-129">Requirements</span></span>



| <span data-ttu-id="fde01-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fde01-130">Requirement</span></span> | <span data-ttu-id="fde01-131">Value</span><span class="sxs-lookup"><span data-stu-id="fde01-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fde01-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fde01-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fde01-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fde01-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fde01-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fde01-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fde01-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fde01-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fde01-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fde01-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde01-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde01-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fde01-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fde01-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="fde01-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fde01-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fde01-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fde01-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fde01-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fde01-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fde01-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="fde01-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde01-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fde01-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fde01-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="fde01-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="fde01-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fde01-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fde01-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="fde01-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="fde01-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="fde01-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="fde01-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="fde01-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





