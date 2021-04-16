---
title: función glNormal3bv (GL. h)
description: Establece el vector normal actual. | función glNormal3bv (GL. h)
ms.assetid: 1d9be974-93c9-45ac-89f1-92c14ff1c242
keywords:
- glNormal3bv (función) OpenGL
topic_type:
- apiref
api_name:
- glNormal3bv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d758c1768425ecb736096d59a49133ff4c8918c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689797"
---
# <a name="glnormal3bv-function"></a><span data-ttu-id="cc903-105">glNormal3bv función)</span><span class="sxs-lookup"><span data-stu-id="cc903-105">glNormal3bv function</span></span>

<span data-ttu-id="cc903-106">Establece el vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="cc903-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc903-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc903-107">Syntax</span></span>


```C++
void WINAPI glNormal3bv(
   const GLbyte *v
);
```



## <a name="parameters"></a><span data-ttu-id="cc903-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc903-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc903-109">*v*</span><span class="sxs-lookup"><span data-stu-id="cc903-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="cc903-110">Puntero a una matriz de tres elementos: las coordenadas x, y y z de la nueva normal actual.</span><span class="sxs-lookup"><span data-stu-id="cc903-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc903-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc903-111">Return value</span></span>

<span data-ttu-id="cc903-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cc903-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc903-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc903-113">Remarks</span></span>

<span data-ttu-id="cc903-114">La normal actual se establece en las coordenadas especificadas siempre que se llama a la función **glNormal3bv**.</span><span class="sxs-lookup"><span data-stu-id="cc903-114">The current normal is set to the given coordinates whenever you call the **glNormal3bv** function.</span></span>

<span data-ttu-id="cc903-115">Los argumentos byte, Short o Integer se convierten al formato de punto flotante mediante una asignación lineal que asigna el valor entero representable más positivo a 1,0 y el valor entero representable más negativo a-1,0.</span><span class="sxs-lookup"><span data-stu-id="cc903-115">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="cc903-116">Las normales especificadas mediante **glNormal3bv** no necesitan tener una longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="cc903-116">Normals specified by using **glNormal3bv** need not have unit length.</span></span> <span data-ttu-id="cc903-117">Si se habilita la normalización, las normales especificadas mediante **glNormal3bv** se normalizan después de la transformación.</span><span class="sxs-lookup"><span data-stu-id="cc903-117">If normalization is enabled, then normals specified by using **glNormal3bv** are normalized after transformation.</span></span> <span data-ttu-id="cc903-118">Puede controlar la normalización mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento libro de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="cc903-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="cc903-119">De forma predeterminada, la normalización está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="cc903-119">By default, normalization is disabled.</span></span> <span data-ttu-id="cc903-120">Puede actualizar la normal actual en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="cc903-120">You can update the current normal any time.</span></span> <span data-ttu-id="cc903-121">En concreto, puede llamar a **glNormal3bv** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cc903-121">In particular, you can call **glNormal3bv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="cc903-122">Las siguientes funciones recuperan información relacionada con **glNormal3bv**:</span><span class="sxs-lookup"><span data-stu-id="cc903-122">The following functions retrieve information related to **glNormal3bv**:</span></span>

<span data-ttu-id="cc903-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ actual \_ normal</span><span class="sxs-lookup"><span data-stu-id="cc903-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="cc903-124">[**glIsEnable**](glisenabled.md) con el argumento \_ normalizar libro de contabilidad</span><span class="sxs-lookup"><span data-stu-id="cc903-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="cc903-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc903-125">Requirements</span></span>



| <span data-ttu-id="cc903-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc903-126">Requirement</span></span> | <span data-ttu-id="cc903-127">Value</span><span class="sxs-lookup"><span data-stu-id="cc903-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc903-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc903-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cc903-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cc903-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cc903-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc903-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cc903-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc903-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cc903-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc903-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc903-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc903-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cc903-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc903-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc903-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc903-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cc903-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc903-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc903-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc903-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc903-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc903-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc903-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cc903-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cc903-140">**glColor**</span><span class="sxs-lookup"><span data-stu-id="cc903-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="cc903-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cc903-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cc903-142">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="cc903-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="cc903-143">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="cc903-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="cc903-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="cc903-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





