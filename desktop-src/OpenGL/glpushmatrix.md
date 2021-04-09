---
title: función glPushMatrix (GL. h)
description: Las funciones glPushMatrix y glPopMatrix envían y extraen la pila de matriz actual. | función glPushMatrix (GL. h)
ms.assetid: 97d8e644-50bb-4130-b6b7-d87df4468e73
keywords:
- glPushMatrix (función) OpenGL
topic_type:
- apiref
api_name:
- glPushMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee62b03e221f44db829a7167d642a766af8e129c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003651"
---
# <a name="glpushmatrix-function"></a><span data-ttu-id="eb366-105">glPushMatrix función)</span><span class="sxs-lookup"><span data-stu-id="eb366-105">glPushMatrix function</span></span>

<span data-ttu-id="eb366-106">Las funciones **glPushMatrix** y [**glPopMatrix**](glpopmatrix.md) envían y extraen la pila de matriz actual.</span><span class="sxs-lookup"><span data-stu-id="eb366-106">The **glPushMatrix** and [**glPopMatrix**](glpopmatrix.md) functions push and pop the current matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb366-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb366-107">Syntax</span></span>


```C++
void WINAPI glPushMatrix(void);
```



## <a name="parameters"></a><span data-ttu-id="eb366-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb366-108">Parameters</span></span>

<span data-ttu-id="eb366-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="eb366-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb366-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb366-110">Return value</span></span>

<span data-ttu-id="eb366-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="eb366-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eb366-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="eb366-112">Error codes</span></span>

<span data-ttu-id="eb366-113">Es un error insertar una pila de matriz completa o extraer una pila de matriz que contenga una sola matriz.</span><span class="sxs-lookup"><span data-stu-id="eb366-113">It is an error to push a full matrix stack, or to pop a matrix stack that contains only a single matrix.</span></span> <span data-ttu-id="eb366-114">En cualquier caso, se establece la marca de error y no se realiza ningún otro cambio en el estado de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="eb366-114">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="eb366-115">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="eb366-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="eb366-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb366-116">Name</span></span>                                                                                                  | <span data-ttu-id="eb366-117">Significado</span><span class="sxs-lookup"><span data-stu-id="eb366-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb366-118"><dt>**desbordamiento de la pila de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb366-118"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="eb366-119">Se llamó a la función mientras la pila de matriz actual estaba llena.</span><span class="sxs-lookup"><span data-stu-id="eb366-119">The function was called while the current matrix stack was full.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="eb366-120"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb366-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="eb366-121">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="eb366-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="eb366-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb366-122">Remarks</span></span>

<span data-ttu-id="eb366-123">Hay una pila de matrices para cada uno de los modos de matriz.</span><span class="sxs-lookup"><span data-stu-id="eb366-123">There is a stack of matrices for each of the matrix modes.</span></span> <span data-ttu-id="eb366-124">En \_ el modo GL MODELVIEW, la profundidad de la pila es al menos 32.</span><span class="sxs-lookup"><span data-stu-id="eb366-124">In GL\_MODELVIEW mode, the stack depth is at least 32.</span></span> <span data-ttu-id="eb366-125">En los otros dos modos, \_ proyección GL y \_ textura GL, la profundidad es al menos 2.</span><span class="sxs-lookup"><span data-stu-id="eb366-125">In the other two modes, GL\_PROJECTION and GL\_TEXTURE, the depth is at least 2.</span></span> <span data-ttu-id="eb366-126">La matriz actual en cualquier modo es la matriz de la parte superior de la pila para ese modo.</span><span class="sxs-lookup"><span data-stu-id="eb366-126">The current matrix in any mode is the matrix on the top of the stack for that mode.</span></span>

<span data-ttu-id="eb366-127">La función **glPushMatrix** empuja hacia abajo la pila de la matriz actual, duplicando la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="eb366-127">The **glPushMatrix** function pushes the current matrix stack down by one, duplicating the current matrix.</span></span> <span data-ttu-id="eb366-128">Es decir, después de una llamada a **glPushMatrix** , la matriz de la parte superior de la pila es idéntica a la que se encuentra debajo de ella.</span><span class="sxs-lookup"><span data-stu-id="eb366-128">That is, after a **glPushMatrix** call, the matrix on the top of the stack is identical to the one below it.</span></span> <span data-ttu-id="eb366-129">La función **glPopMatrix** extrae la pila de matriz actual, reemplazando la matriz actual por la que se encuentra debajo en la pila.</span><span class="sxs-lookup"><span data-stu-id="eb366-129">The **glPopMatrix** function pops the current matrix stack, replacing the current matrix with the one below it on the stack.</span></span> <span data-ttu-id="eb366-130">Inicialmente, cada una de las pilas contiene una matriz, una matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="eb366-130">Initially, each of the stacks contains one matrix, an identity matrix.</span></span>

<span data-ttu-id="eb366-131">Las siguientes funciones recuperan información relacionada con **glPushMatrix** y **glPopMatrix**:</span><span class="sxs-lookup"><span data-stu-id="eb366-131">The following functions retrieve information related to **glPushMatrix** and **glPopMatrix**:</span></span>

<span data-ttu-id="eb366-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="eb366-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="eb366-133">**glGet** con el argumento \_ MODELVIEW \_ matriz de contabilidad</span><span class="sxs-lookup"><span data-stu-id="eb366-133">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="eb366-134">**glGet** con el argumento \_ matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="eb366-134">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="eb366-135">**glGet** con el argumento \_ matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="eb366-135">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

<span data-ttu-id="eb366-136">**glGet** con el argumento GL MODELVIEW de la \_ \_ pila \_</span><span class="sxs-lookup"><span data-stu-id="eb366-136">**glGet** with argument GL\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="eb366-137">**glGet** con el argumento \_ profundidad de la pila de proyección GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="eb366-137">**glGet** with argument GL\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="eb366-138">**glGet** con el argumento \_ profundidad de la pila de textura de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="eb366-138">**glGet** with argument GL\_TEXTURE\_STACK\_DEPTH</span></span>

<span data-ttu-id="eb366-139">**glGet** con el argumento GL \_ Max MODELVIEW de la \_ \_ pila \_</span><span class="sxs-lookup"><span data-stu-id="eb366-139">**glGet** with argument GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="eb366-140">**glGet** con el argumento \_ profundidad de la \_ pila de proyección Max \_ \_</span><span class="sxs-lookup"><span data-stu-id="eb366-140">**glGet** with argument GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="eb366-141">**glGet** con el argumento \_ profundidad máxima de la \_ pila de textura de \_ GL \_</span><span class="sxs-lookup"><span data-stu-id="eb366-141">**glGet** with argument GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="eb366-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb366-142">Requirements</span></span>



| <span data-ttu-id="eb366-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb366-143">Requirement</span></span> | <span data-ttu-id="eb366-144">Value</span><span class="sxs-lookup"><span data-stu-id="eb366-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb366-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb366-145">Minimum supported client</span></span><br/> | <span data-ttu-id="eb366-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eb366-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="eb366-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb366-147">Minimum supported server</span></span><br/> | <span data-ttu-id="eb366-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eb366-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eb366-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb366-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb366-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb366-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="eb366-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb366-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb366-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb366-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="eb366-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb366-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb366-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb366-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb366-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb366-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb366-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="eb366-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="eb366-157">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="eb366-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="eb366-158">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="eb366-158">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="eb366-159">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="eb366-159">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="eb366-160">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="eb366-160">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="eb366-161">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="eb366-161">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="eb366-162">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="eb366-162">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="eb366-163">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="eb366-163">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="eb366-164">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="eb366-164">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="eb366-165">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="eb366-165">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="eb366-166">**glScale**</span><span class="sxs-lookup"><span data-stu-id="eb366-166">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="eb366-167">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="eb366-167">**glTranslate**</span></span>](gltranslate.md)
</dt> <dt>

[<span data-ttu-id="eb366-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="eb366-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





