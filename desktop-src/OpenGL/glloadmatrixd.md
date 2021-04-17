---
title: función glLoadMatrixd (GL. h)
description: La función glLoadMatrixd reemplaza la matriz actual por una matriz arbitraria. | función glLoadMatrixd (GL. h)
ms.assetid: 66c499f7-3f55-4de2-b67b-5b775b5854e0
keywords:
- glLoadMatrixd (función) OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4715da159dff60024adb3c7331cbf03c7c3759ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689719"
---
# <a name="glloadmatrixd-function"></a><span data-ttu-id="13ed8-105">glLoadMatrixd función)</span><span class="sxs-lookup"><span data-stu-id="13ed8-105">glLoadMatrixd function</span></span>

<span data-ttu-id="13ed8-106">Las funciones **glLoadMatrixd** y [**glLoadMatrixf**](glloadmatrixf.md) reemplazan la matriz actual por una matriz arbitraria.</span><span class="sxs-lookup"><span data-stu-id="13ed8-106">The **glLoadMatrixd** and [**glLoadMatrixf**](glloadmatrixf.md) functions replace the current matrix with an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ed8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13ed8-107">Syntax</span></span>


```C++
void WINAPI glLoadMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a><span data-ttu-id="13ed8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13ed8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ed8-109">*m*</span><span class="sxs-lookup"><span data-stu-id="13ed8-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="13ed8-110">Puntero a una matriz de 4x4 almacenada en el orden principal de columna como 16 valores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="13ed8-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ed8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13ed8-111">Return value</span></span>

<span data-ttu-id="13ed8-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="13ed8-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="13ed8-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="13ed8-113">Error codes</span></span>

<span data-ttu-id="13ed8-114">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="13ed8-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="13ed8-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="13ed8-115">Name</span></span>                                                                                                  | <span data-ttu-id="13ed8-116">Significado</span><span class="sxs-lookup"><span data-stu-id="13ed8-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13ed8-117"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="13ed8-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="13ed8-118">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="13ed8-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="13ed8-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13ed8-119">Remarks</span></span>

<span data-ttu-id="13ed8-120">La función **glLoadMatrix** reemplaza la matriz actual por la especificada en *m*.</span><span class="sxs-lookup"><span data-stu-id="13ed8-120">The **glLoadMatrix** function replaces the current matrix with the one specified in *m*.</span></span> <span data-ttu-id="13ed8-121">La matriz actual es la matriz de proyección, la matriz de MODELVIEW o la matriz de textura, determinada por el modo de matriz actual (vea [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="13ed8-121">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="13ed8-122">El parámetro *m* apunta a una matriz 4x4 de valores de punto flotante de precisión sencilla o de precisión doble almacenados en el orden de la columna principal.</span><span class="sxs-lookup"><span data-stu-id="13ed8-122">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="13ed8-123">Es decir, la matriz se almacena como se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="13ed8-123">That is, the matrix is stored as shown in the following image.</span></span>

![Diagrama que muestra la matriz 4x4 a la que apunta el parámetro m.](images/load02.png)

<span data-ttu-id="13ed8-125">Las siguientes funciones recuperan información relacionada con **glLoadMatrix**:</span><span class="sxs-lookup"><span data-stu-id="13ed8-125">The following functions retrieve information related to **glLoadMatrix**:</span></span>

<span data-ttu-id="13ed8-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="13ed8-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="13ed8-127">**glGet** con el argumento \_ MODELVIEW \_ matriz de contabilidad</span><span class="sxs-lookup"><span data-stu-id="13ed8-127">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="13ed8-128">**glGet** con el argumento \_ matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="13ed8-128">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="13ed8-129">**glGet** con el argumento \_ matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="13ed8-129">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="13ed8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13ed8-130">Requirements</span></span>



| <span data-ttu-id="13ed8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="13ed8-131">Requirement</span></span> | <span data-ttu-id="13ed8-132">Value</span><span class="sxs-lookup"><span data-stu-id="13ed8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13ed8-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13ed8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="13ed8-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="13ed8-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="13ed8-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13ed8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="13ed8-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13ed8-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13ed8-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13ed8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="13ed8-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="13ed8-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="13ed8-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="13ed8-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="13ed8-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13ed8-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="13ed8-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13ed8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13ed8-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13ed8-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13ed8-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="13ed8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13ed8-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="13ed8-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="13ed8-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="13ed8-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="13ed8-146">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="13ed8-146">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="13ed8-147">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="13ed8-147">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="13ed8-148">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="13ed8-148">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="13ed8-149">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="13ed8-149">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





