---
title: función glNormal3iv (GL. h)
description: Establece el vector normal actual. | función glNormal3iv (GL. h)
ms.assetid: cf50e801-a34c-43bd-b7eb-facb84a6472d
keywords:
- glNormal3iv (función) OpenGL
topic_type:
- apiref
api_name:
- glNormal3iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5629a12d6c388da2aa133fbe72177646b4f95d63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003728"
---
# <a name="glnormal3iv-function"></a><span data-ttu-id="95611-105">glNormal3iv función)</span><span class="sxs-lookup"><span data-stu-id="95611-105">glNormal3iv function</span></span>

<span data-ttu-id="95611-106">Establece el vector normal actual.</span><span class="sxs-lookup"><span data-stu-id="95611-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="95611-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95611-107">Syntax</span></span>


```C++
void WINAPI glNormal3iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="95611-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95611-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95611-109">*v*</span><span class="sxs-lookup"><span data-stu-id="95611-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="95611-110">Puntero a una matriz de tres elementos: las coordenadas x, y y z de la nueva normal actual.</span><span class="sxs-lookup"><span data-stu-id="95611-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95611-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95611-111">Return value</span></span>

<span data-ttu-id="95611-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="95611-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95611-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95611-113">Remarks</span></span>

<span data-ttu-id="95611-114">La normal actual se establece en las coordenadas especificadas siempre que se llama a la función **glNormal3iv**.</span><span class="sxs-lookup"><span data-stu-id="95611-114">The current normal is set to the given coordinates whenever you call the **glNormal3iv** function.</span></span>

<span data-ttu-id="95611-115">Los argumentos byte, Short o Integer se convierten al formato de punto flotante con una asignación lineal que asigna el valor entero representable más positivo a 1,0 y el valor entero representable más negativo a-1,0.</span><span class="sxs-lookup"><span data-stu-id="95611-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="95611-116">Las normales especificadas mediante **glNormal3iv** no necesitan tener una longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="95611-116">Normals specified by using **glNormal3iv** need not have unit length.</span></span> <span data-ttu-id="95611-117">Si la normalización está habilitada, las normales especificadas con **glNormal3iv** se normalizan después de la transformación.</span><span class="sxs-lookup"><span data-stu-id="95611-117">If normalization is enabled, then normals specified with **glNormal3iv** are normalized after transformation.</span></span> <span data-ttu-id="95611-118">Puede controlar la normalización mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento libro de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="95611-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="95611-119">De forma predeterminada, la normalización está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="95611-119">By default, normalization is disabled.</span></span> <span data-ttu-id="95611-120">Puede actualizar la normal actual en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="95611-120">You can update the current normal at any time.</span></span> <span data-ttu-id="95611-121">En concreto, puede llamar a **glNormal3iv** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="95611-121">In particular, you can call **glNormal3iv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="95611-122">Las siguientes funciones recuperan información relacionada con **glNormal3iv**:</span><span class="sxs-lookup"><span data-stu-id="95611-122">The following functions retrieve information related to **glNormal3iv**:</span></span>

<span data-ttu-id="95611-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ actual \_ normal</span><span class="sxs-lookup"><span data-stu-id="95611-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="95611-124">[**glIsEnable**](glisenabled.md) con el argumento \_ normalizar libro de contabilidad</span><span class="sxs-lookup"><span data-stu-id="95611-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="95611-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95611-125">Requirements</span></span>



| <span data-ttu-id="95611-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="95611-126">Requirement</span></span> | <span data-ttu-id="95611-127">Value</span><span class="sxs-lookup"><span data-stu-id="95611-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95611-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95611-128">Minimum supported client</span></span><br/> | <span data-ttu-id="95611-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="95611-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="95611-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95611-130">Minimum supported server</span></span><br/> | <span data-ttu-id="95611-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="95611-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95611-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95611-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="95611-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="95611-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="95611-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95611-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="95611-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95611-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="95611-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95611-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95611-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95611-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95611-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="95611-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95611-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="95611-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="95611-140">**glColor**</span><span class="sxs-lookup"><span data-stu-id="95611-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="95611-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="95611-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="95611-142">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="95611-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="95611-143">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="95611-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="95611-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="95611-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





