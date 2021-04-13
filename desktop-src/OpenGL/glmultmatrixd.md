---
title: función glMultMatrixd (GL. h)
description: La función glMultMatrixd multiplica la matriz actual por una matriz arbitraria. | función glMultMatrixd (GL. h)
ms.assetid: 1f6cf4e4-e7bd-470c-b1f4-b9ccc1fb756e
keywords:
- glMultMatrixd (función) OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24993fe5873be0af8713e3d127b86a7c593cd82
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362356"
---
# <a name="glmultmatrixd-function"></a><span data-ttu-id="bbc1b-105">glMultMatrixd función)</span><span class="sxs-lookup"><span data-stu-id="bbc1b-105">glMultMatrixd function</span></span>

<span data-ttu-id="bbc1b-106">Las funciones **glMultMatrixd** y [**glMultMatrixf**](glmultmatrixf.md) multiplican la matriz actual por una matriz arbitraria.</span><span class="sxs-lookup"><span data-stu-id="bbc1b-106">The **glMultMatrixd** and [**glMultMatrixf**](glmultmatrixf.md) functions multiply the current matrix by an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc1b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbc1b-107">Syntax</span></span>


```C++
void WINAPI glMultMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a><span data-ttu-id="bbc1b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bbc1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbc1b-109">*m*</span><span class="sxs-lookup"><span data-stu-id="bbc1b-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="bbc1b-110">Puntero a una matriz de 4x4 almacenada en el orden principal de columna como 16 valores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="bbc1b-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbc1b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbc1b-111">Return value</span></span>

<span data-ttu-id="bbc1b-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bbc1b-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bbc1b-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="bbc1b-113">Error codes</span></span>

<span data-ttu-id="bbc1b-114">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="bbc1b-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bbc1b-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="bbc1b-115">Name</span></span>                                                                                                  | <span data-ttu-id="bbc1b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="bbc1b-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bbc1b-117"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bbc1b-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bbc1b-118">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="bbc1b-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bbc1b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbc1b-119">Remarks</span></span>

<span data-ttu-id="bbc1b-120">La función **glMultMatrix** multiplica la matriz actual por la especificada en *m*.</span><span class="sxs-lookup"><span data-stu-id="bbc1b-120">The **glMultMatrix** function multiplies the current matrix by the one specified in *m*.</span></span> <span data-ttu-id="bbc1b-121">Es decir, si M es la matriz actual y T es la matriz que se pasa a **glMultMatrix**, m se reemplaza por m T.</span><span class="sxs-lookup"><span data-stu-id="bbc1b-121">That is, if M is the current matrix and T is the matrix passed to **glMultMatrix**, then M is replaced with M   T.</span></span>

<span data-ttu-id="bbc1b-122">La matriz actual es la matriz de proyección, la matriz de MODELVIEW o la matriz de textura, determinada por el modo de matriz actual (vea [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="bbc1b-122">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="bbc1b-123">El parámetro *m* apunta a una matriz 4x4 de valores de punto flotante de precisión sencilla o de precisión doble almacenados en el orden de la columna principal.</span><span class="sxs-lookup"><span data-stu-id="bbc1b-123">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="bbc1b-124">Es decir, la matriz se almacena como se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="bbc1b-124">That is, the matrix is stored as shown in the following image.</span></span>

![! [Diagrama que muestra la matriz de 4x4 a la que apunta el parámetro m.]](images/multi01.png)

<span data-ttu-id="bbc1b-126">Las siguientes funciones recuperan información relacionada con **glMultMatrix**:</span><span class="sxs-lookup"><span data-stu-id="bbc1b-126">The following functions retrieve information related to **glMultMatrix**:</span></span>

<span data-ttu-id="bbc1b-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="bbc1b-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="bbc1b-128">**glGet** con el argumento \_ MODELVIEW \_ matriz de contabilidad</span><span class="sxs-lookup"><span data-stu-id="bbc1b-128">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="bbc1b-129">**glGet** con el argumento \_ matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="bbc1b-129">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="bbc1b-130">**glGet** con el argumento \_ matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="bbc1b-130">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc1b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbc1b-131">Requirements</span></span>



| <span data-ttu-id="bbc1b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbc1b-132">Requirement</span></span> | <span data-ttu-id="bbc1b-133">Value</span><span class="sxs-lookup"><span data-stu-id="bbc1b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc1b-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbc1b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc1b-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bbc1b-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bbc1b-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbc1b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc1b-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bbc1b-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bbc1b-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbc1b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbc1b-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbc1b-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bbc1b-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bbc1b-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="bbc1b-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbc1b-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bbc1b-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bbc1b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbc1b-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbc1b-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbc1b-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbc1b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc1b-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bbc1b-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bbc1b-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bbc1b-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bbc1b-147">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="bbc1b-147">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="bbc1b-148">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="bbc1b-148">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="bbc1b-149">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="bbc1b-149">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="bbc1b-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="bbc1b-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





