---
title: función glLoadMatrixf (GL. h)
description: La función glLoadMatrixf reemplaza la matriz actual por una matriz arbitraria. | función glLoadMatrixf (GL. h)
ms.assetid: 6e1337b0-d1e7-4002-a561-d959d7f70942
keywords:
- glLoadMatrixf (función) OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0c54f4f7f7255b2dde724cf018d57fab6cf3e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670114"
---
# <a name="glloadmatrixf-function"></a><span data-ttu-id="63932-105">glLoadMatrixf función)</span><span class="sxs-lookup"><span data-stu-id="63932-105">glLoadMatrixf function</span></span>

<span data-ttu-id="63932-106">Las funciones [**glLoadMatrixd**](glloadmatrixd.md) y **glLoadMatrixf** reemplazan la matriz actual por una matriz arbitraria.</span><span class="sxs-lookup"><span data-stu-id="63932-106">The [**glLoadMatrixd**](glloadmatrixd.md) and **glLoadMatrixf** functions replace the current matrix with an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="63932-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63932-107">Syntax</span></span>


```C++
void WINAPI glLoadMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a><span data-ttu-id="63932-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63932-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63932-109">*m*</span><span class="sxs-lookup"><span data-stu-id="63932-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="63932-110">Puntero a una matriz de 4x4 almacenada en el orden principal de columna como 16 valores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="63932-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63932-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63932-111">Return value</span></span>

<span data-ttu-id="63932-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="63932-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63932-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="63932-113">Error codes</span></span>

<span data-ttu-id="63932-114">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="63932-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="63932-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="63932-115">Name</span></span>                                                                                                  | <span data-ttu-id="63932-116">Significado</span><span class="sxs-lookup"><span data-stu-id="63932-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63932-117"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63932-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="63932-118">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="63932-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="63932-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63932-119">Remarks</span></span>

<span data-ttu-id="63932-120">La función **glLoadMatrix** reemplaza la matriz actual por la especificada en *m*.</span><span class="sxs-lookup"><span data-stu-id="63932-120">The **glLoadMatrix** function replaces the current matrix with the one specified in *m*.</span></span> <span data-ttu-id="63932-121">La matriz actual es la matriz de proyección, la matriz de MODELVIEW o la matriz de textura, determinada por el modo de matriz actual (vea [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="63932-121">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="63932-122">El parámetro *m* apunta a una matriz 4x4 de valores de punto flotante de precisión sencilla o de precisión doble almacenados en el orden de la columna principal.</span><span class="sxs-lookup"><span data-stu-id="63932-122">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="63932-123">Es decir, la matriz se almacena como se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="63932-123">That is, the matrix is stored as shown in the following image.</span></span>

![Diagrama que muestra la matriz 4x4 a la que apunta el parámetro m.](images/load02.png)

<span data-ttu-id="63932-125">Las siguientes funciones recuperan información relacionada con **glLoadMatrix**:</span><span class="sxs-lookup"><span data-stu-id="63932-125">The following functions retrieve information related to **glLoadMatrix**:</span></span>

<span data-ttu-id="63932-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="63932-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="63932-127">**glGet** con el argumento \_ MODELVIEW \_ matriz de contabilidad</span><span class="sxs-lookup"><span data-stu-id="63932-127">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="63932-128">**glGet** con el argumento \_ matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="63932-128">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="63932-129">**glGet** con el argumento \_ matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="63932-129">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="63932-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63932-130">Requirements</span></span>



| <span data-ttu-id="63932-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="63932-131">Requirement</span></span> | <span data-ttu-id="63932-132">Value</span><span class="sxs-lookup"><span data-stu-id="63932-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63932-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63932-133">Minimum supported client</span></span><br/> | <span data-ttu-id="63932-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="63932-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="63932-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63932-135">Minimum supported server</span></span><br/> | <span data-ttu-id="63932-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63932-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63932-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63932-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="63932-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="63932-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="63932-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63932-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="63932-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63932-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="63932-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63932-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63932-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63932-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63932-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="63932-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63932-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="63932-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="63932-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="63932-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="63932-146">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="63932-146">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="63932-147">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="63932-147">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="63932-148">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="63932-148">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="63932-149">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="63932-149">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





