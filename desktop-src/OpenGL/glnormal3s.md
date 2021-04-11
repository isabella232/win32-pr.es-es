---
title: función glNormal3s (GL. h)
description: Establece el vector normal actual. | función glNormal3s (GL. h)
ms.assetid: 4fd98ad5-266d-4ef1-9c1f-2b5166ee65d7
keywords:
- glNormal3s (función) OpenGL
topic_type:
- apiref
api_name:
- glNormal3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7941fa4e2c4e5ef00a5a14ce1eb913fb22a1f58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280058"
---
# <a name="glnormal3s-function"></a><span data-ttu-id="aad59-105">glNormal3s función)</span><span class="sxs-lookup"><span data-stu-id="aad59-105">glNormal3s function</span></span>

<span data-ttu-id="aad59-106">Establece el vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="aad59-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="aad59-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aad59-107">Syntax</span></span>


```C++
void WINAPI glNormal3s(
   GLshort nx,
   GLshort ny,
   GLshort nz
);
```



## <a name="parameters"></a><span data-ttu-id="aad59-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aad59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aad59-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="aad59-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="aad59-110">Especifica la coordenada x del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="aad59-110">Specifies the x-coordinate of the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="aad59-111">*1002*</span><span class="sxs-lookup"><span data-stu-id="aad59-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="aad59-112">Especifica la coordenada y del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="aad59-112">Specifies the y-coordinate of the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="aad59-113">*Zelanda*</span><span class="sxs-lookup"><span data-stu-id="aad59-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="aad59-114">Especifica la coordenada z del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="aad59-114">Specifies the z-coordinate of the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aad59-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aad59-115">Return value</span></span>

<span data-ttu-id="aad59-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="aad59-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aad59-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aad59-117">Remarks</span></span>

<span data-ttu-id="aad59-118">La normal actual se establece en las coordenadas especificadas siempre que se llama a la función **glNormal3s**.</span><span class="sxs-lookup"><span data-stu-id="aad59-118">The current normal is set to the given coordinates whenever you call the **glNormal3s** function.</span></span>

<span data-ttu-id="aad59-119">Los argumentos byte, Short o Integer se convierten al formato de punto flotante con una asignación lineal que asigna el valor entero representable más positivo a 1,0 y el valor entero representable más negativo a-1,0.</span><span class="sxs-lookup"><span data-stu-id="aad59-119">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="aad59-120">Las normales especificadas mediante **glNormal3s** no necesitan tener una longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="aad59-120">Normals specified by using **glNormal3s** need not have unit length.</span></span> <span data-ttu-id="aad59-121">Si la normalización está habilitada, las normales especificadas con **glNormal3s** se normalizan después de la transformación.</span><span class="sxs-lookup"><span data-stu-id="aad59-121">If normalization is enabled, then normals specified with **glNormal3s** are normalized after transformation.</span></span> <span data-ttu-id="aad59-122">Puede controlar normalizationby con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento libro de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="aad59-122">You can control normalizationby using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="aad59-123">De forma predeterminada, la normalización está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="aad59-123">By default, normalization is disabled.</span></span> <span data-ttu-id="aad59-124">Puede actualizar la normal actual en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="aad59-124">You can update the current normal at any time.</span></span> <span data-ttu-id="aad59-125">En concreto, puede llamar a **glNormal3s** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="aad59-125">In particular, you can call **glNormal3s** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="aad59-126">Las siguientes funciones recuperan información relacionada con **glNormal3s**:</span><span class="sxs-lookup"><span data-stu-id="aad59-126">The following functions retrieve information related to **glNormal3s**:</span></span>

<span data-ttu-id="aad59-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ actual \_ normal</span><span class="sxs-lookup"><span data-stu-id="aad59-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="aad59-128">[**glIsEnable**](glisenabled.md) con el argumento \_ normalizar libro de contabilidad</span><span class="sxs-lookup"><span data-stu-id="aad59-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="aad59-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aad59-129">Requirements</span></span>



| <span data-ttu-id="aad59-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="aad59-130">Requirement</span></span> | <span data-ttu-id="aad59-131">Value</span><span class="sxs-lookup"><span data-stu-id="aad59-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aad59-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aad59-132">Minimum supported client</span></span><br/> | <span data-ttu-id="aad59-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aad59-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aad59-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aad59-134">Minimum supported server</span></span><br/> | <span data-ttu-id="aad59-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aad59-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aad59-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aad59-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="aad59-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="aad59-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="aad59-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aad59-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="aad59-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aad59-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aad59-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aad59-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aad59-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aad59-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aad59-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="aad59-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad59-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="aad59-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="aad59-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="aad59-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="aad59-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="aad59-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="aad59-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="aad59-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="aad59-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="aad59-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="aad59-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="aad59-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





