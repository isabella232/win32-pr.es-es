---
title: función glNormal3b (GL. h)
description: Establece el vector normal actual. | función glNormal3b (GL. h)
ms.assetid: b6976143-bc9a-4766-9f7e-5380c3a24173
keywords:
- glNormal3b (función) OpenGL
topic_type:
- apiref
api_name:
- glNormal3b
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a09a92b718881670ed5625fd5aa94a23193cdd6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914326"
---
# <a name="glnormal3b-function"></a><span data-ttu-id="c492c-105">glNormal3b función)</span><span class="sxs-lookup"><span data-stu-id="c492c-105">glNormal3b function</span></span>

<span data-ttu-id="c492c-106">Establece el vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="c492c-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c492c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c492c-107">Syntax</span></span>


```C++
void WINAPI glNormal3b(
   GLbyte nx,
   GLbyte ny,
   GLbyte nz
);
```



## <a name="parameters"></a><span data-ttu-id="c492c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c492c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c492c-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="c492c-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="c492c-110">Especifica la coordenada x del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="c492c-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="c492c-111">*1002*</span><span class="sxs-lookup"><span data-stu-id="c492c-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="c492c-112">Especifica la coordenada y del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="c492c-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="c492c-113">*Zelanda*</span><span class="sxs-lookup"><span data-stu-id="c492c-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="c492c-114">Especifica la coordenada z del nuevo vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="c492c-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c492c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c492c-115">Return value</span></span>

<span data-ttu-id="c492c-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c492c-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c492c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c492c-117">Remarks</span></span>

<span data-ttu-id="c492c-118">La normal actual se establece en las coordenadas especificadas siempre que se llama a la función **glNormal3b** .</span><span class="sxs-lookup"><span data-stu-id="c492c-118">The current normal is set to the given coordinates whenever you call the **glNormal3b** function.</span></span>

<span data-ttu-id="c492c-119">Los argumentos byte, Short o Integer se convierten al formato de punto flotante mediante una asignación lineal que asigna el valor entero representable más positivo a 1,0 y el valor entero representable más negativo a-1,0.</span><span class="sxs-lookup"><span data-stu-id="c492c-119">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="c492c-120">No es necesario que las normales especificadas con **glNormal3b** tengan longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="c492c-120">Normals specified with **glNormal3b** need not have unit length.</span></span> <span data-ttu-id="c492c-121">Si la normalización está habilitada, las normales especificadas con **glNormal3b** se normalizan después de la transformación.</span><span class="sxs-lookup"><span data-stu-id="c492c-121">If normalization is enabled, then normals specified with **glNormal3b** are normalized after transformation.</span></span> <span data-ttu-id="c492c-122">Puede controlar la normalización mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento libro de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="c492c-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="c492c-123">De forma predeterminada, la normalización está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="c492c-123">By default, normalization is disabled.</span></span> <span data-ttu-id="c492c-124">Puede actualizar la normal actual en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="c492c-124">You can update the current normal at any time.</span></span> <span data-ttu-id="c492c-125">En concreto, puede llamar a **glNormal3b** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c492c-125">In particular, you can call **glNormal3b** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="c492c-126">Las siguientes funciones recuperan información relacionada con **glNormal3b**:</span><span class="sxs-lookup"><span data-stu-id="c492c-126">The following functions retrieve information related to **glNormal3b**:</span></span>

<span data-ttu-id="c492c-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ actual \_ normal</span><span class="sxs-lookup"><span data-stu-id="c492c-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="c492c-128">[**glIsEnable**](glisenabled.md) con el argumento \_ normalizar libro de contabilidad</span><span class="sxs-lookup"><span data-stu-id="c492c-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="c492c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c492c-129">Requirements</span></span>



| <span data-ttu-id="c492c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c492c-130">Requirement</span></span> | <span data-ttu-id="c492c-131">Value</span><span class="sxs-lookup"><span data-stu-id="c492c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c492c-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c492c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c492c-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c492c-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c492c-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c492c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c492c-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c492c-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c492c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c492c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c492c-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c492c-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c492c-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c492c-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="c492c-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c492c-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c492c-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c492c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c492c-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c492c-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c492c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="c492c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c492c-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c492c-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c492c-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="c492c-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="c492c-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c492c-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c492c-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="c492c-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="c492c-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="c492c-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="c492c-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="c492c-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





