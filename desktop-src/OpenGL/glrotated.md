---
title: función glRotated (GL. h)
description: La función glRotated multiplica la matriz actual por una matriz de rotación.
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
keywords:
- glRotated (función) OpenGL
topic_type:
- apiref
api_name:
- glRotated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d0678e9da6f0b68047708f45fda1c9da66d8139
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535416"
---
# <a name="glrotated-function"></a><span data-ttu-id="e80c2-104">glRotated función)</span><span class="sxs-lookup"><span data-stu-id="e80c2-104">glRotated function</span></span>

<span data-ttu-id="e80c2-105">La función **glRotated** multiplica la matriz actual por una matriz de rotación.</span><span class="sxs-lookup"><span data-stu-id="e80c2-105">The **glRotated** function multiplies the current matrix by a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e80c2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e80c2-106">Syntax</span></span>


```C++
void WINAPI glRotated(
   GLdouble angle,
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="e80c2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e80c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e80c2-108">*angle*</span><span class="sxs-lookup"><span data-stu-id="e80c2-108">*angle*</span></span> 
</dt> <dd>

<span data-ttu-id="e80c2-109">Ángulo de rotación, en grados.</span><span class="sxs-lookup"><span data-stu-id="e80c2-109">The angle of rotation, in degrees.</span></span>

</dd> <dt>

<span data-ttu-id="e80c2-110">*x*</span><span class="sxs-lookup"><span data-stu-id="e80c2-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="e80c2-111">Coordenada *x* de un vector.</span><span class="sxs-lookup"><span data-stu-id="e80c2-111">The *x* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="e80c2-112">*y*</span><span class="sxs-lookup"><span data-stu-id="e80c2-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="e80c2-113">Coordenada *y* de un vector.</span><span class="sxs-lookup"><span data-stu-id="e80c2-113">The *y* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="e80c2-114">*z*</span><span class="sxs-lookup"><span data-stu-id="e80c2-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="e80c2-115">Coordenada *z* de un vector.</span><span class="sxs-lookup"><span data-stu-id="e80c2-115">The *z* coordinate of a vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e80c2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e80c2-116">Return value</span></span>

<span data-ttu-id="e80c2-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e80c2-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e80c2-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e80c2-118">Error codes</span></span>

<span data-ttu-id="e80c2-119">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="e80c2-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e80c2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e80c2-120">Name</span></span>                                                                                                  | <span data-ttu-id="e80c2-121">Significado</span><span class="sxs-lookup"><span data-stu-id="e80c2-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e80c2-122"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e80c2-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e80c2-123">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e80c2-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e80c2-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e80c2-124">Remarks</span></span>

<span data-ttu-id="e80c2-125">La función **glRotated** calcula una matriz que realiza un giro en sentido contrario de los grados *angulares* del vector desde el origen hasta el punto (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="e80c2-125">The **glRotated** function computes a matrix that performs a counterclockwise rotation of *angle* degrees about the vector from the origin through the point (*x*, *y*, *z*).</span></span>

<span data-ttu-id="e80c2-126">La matriz actual (vea [**glMatrixMode**](glmatrixmode.md)) se multiplica por esta matriz de rotación, donde el producto reemplaza la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="e80c2-126">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this rotation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="e80c2-127">Es decir, si M es la matriz actual y R es la matriz de traslación, M se reemplaza por M R.</span><span class="sxs-lookup"><span data-stu-id="e80c2-127">That is, if M is the current matrix and R is the translation matrix, then M is replaced with M   R.</span></span>

<span data-ttu-id="e80c2-128">Si el modo de matriz es \_ MODELVIEW de GL o \_ proyección de contabilidad, se giran todos los objetos dibujados después de **glRotated** .</span><span class="sxs-lookup"><span data-stu-id="e80c2-128">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glRotated** is called are rotated.</span></span> <span data-ttu-id="e80c2-129">Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix**](glpopmatrix.md) para guardar y restaurar el sistema de coordenadas sin girar.</span><span class="sxs-lookup"><span data-stu-id="e80c2-129">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unrotated coordinate system.</span></span>

<span data-ttu-id="e80c2-130">Las siguientes funciones recuperan información relacionada con **glRotated**:</span><span class="sxs-lookup"><span data-stu-id="e80c2-130">The following functions retrieve information related to **glRotated**:</span></span>

<span data-ttu-id="e80c2-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de representación de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="e80c2-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

<span data-ttu-id="e80c2-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="e80c2-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="e80c2-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MODELVIEW \_ matriz de contabilidad</span><span class="sxs-lookup"><span data-stu-id="e80c2-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="e80c2-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="e80c2-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="e80c2-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="e80c2-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="e80c2-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e80c2-136">Requirements</span></span>



| <span data-ttu-id="e80c2-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e80c2-137">Requirement</span></span> | <span data-ttu-id="e80c2-138">Value</span><span class="sxs-lookup"><span data-stu-id="e80c2-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e80c2-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e80c2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e80c2-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e80c2-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e80c2-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e80c2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e80c2-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e80c2-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e80c2-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e80c2-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e80c2-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e80c2-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e80c2-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e80c2-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="e80c2-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e80c2-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e80c2-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e80c2-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e80c2-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e80c2-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e80c2-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="e80c2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80c2-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e80c2-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e80c2-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e80c2-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e80c2-152">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="e80c2-152">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="e80c2-153">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="e80c2-153">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="e80c2-154">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="e80c2-154">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="e80c2-155">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="e80c2-155">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="e80c2-156">**glScale**</span><span class="sxs-lookup"><span data-stu-id="e80c2-156">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="e80c2-157">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="e80c2-157">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





