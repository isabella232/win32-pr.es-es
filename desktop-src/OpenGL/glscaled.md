---
title: función glScaled (GL. h)
description: Las funciones glScaled y glScalef multiplican la matriz actual por una matriz de escala general. | función glScaled (GL. h)
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- glScaled (función) OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2655924f5716e142832882441066d4772d0e63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104552093"
---
# <a name="glscaled-function"></a><span data-ttu-id="984e3-105">glScaled función)</span><span class="sxs-lookup"><span data-stu-id="984e3-105">glScaled function</span></span>

<span data-ttu-id="984e3-106">Las funciones **glScaled** y [**glScalef**](glscalef.md) multiplican la matriz actual por una matriz de escala general.</span><span class="sxs-lookup"><span data-stu-id="984e3-106">The **glScaled** and [**glScalef**](glscalef.md) functions multiply the current matrix by a general scaling matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="984e3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="984e3-107">Syntax</span></span>


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="984e3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="984e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="984e3-109">*x*</span><span class="sxs-lookup"><span data-stu-id="984e3-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="984e3-110">Factores de escala a lo largo del eje *x* .</span><span class="sxs-lookup"><span data-stu-id="984e3-110">Scale factors along the *x* axis.</span></span>

</dd> <dt>

<span data-ttu-id="984e3-111">*y*</span><span class="sxs-lookup"><span data-stu-id="984e3-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="984e3-112">Factores de escala a lo largo del eje *y* .</span><span class="sxs-lookup"><span data-stu-id="984e3-112">Scale factors along the *y* axis.</span></span>

</dd> <dt>

<span data-ttu-id="984e3-113">*z*</span><span class="sxs-lookup"><span data-stu-id="984e3-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="984e3-114">Factores de escala a lo largo del eje *z* .</span><span class="sxs-lookup"><span data-stu-id="984e3-114">Scale factors along the *z* axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="984e3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="984e3-115">Return value</span></span>

<span data-ttu-id="984e3-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="984e3-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="984e3-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="984e3-117">Error codes</span></span>

<span data-ttu-id="984e3-118">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="984e3-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="984e3-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="984e3-119">Name</span></span>                                                                                                  | <span data-ttu-id="984e3-120">Significado</span><span class="sxs-lookup"><span data-stu-id="984e3-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="984e3-121"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="984e3-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="984e3-122">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="984e3-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="984e3-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="984e3-123">Remarks</span></span>

<span data-ttu-id="984e3-124">La función **glScaled** genera una escala general a lo largo de los ejes *x*, *y* y *z* .</span><span class="sxs-lookup"><span data-stu-id="984e3-124">The **glScaled** function produces a general scaling along the *x*, *y*, and *z* axes.</span></span> <span data-ttu-id="984e3-125">Los tres argumentos indican los factores de escala deseados a lo largo de cada uno de los tres ejes.</span><span class="sxs-lookup"><span data-stu-id="984e3-125">The three arguments indicate the desired scale factors along each of the three axes.</span></span> <span data-ttu-id="984e3-126">La matriz resultante es</span><span class="sxs-lookup"><span data-stu-id="984e3-126">The resulting matrix is</span></span>

![Diagrama que muestra la matriz de factores de escala a lo largo de los ejes x, y y z.](images/scale01.png)

<span data-ttu-id="984e3-128">La matriz actual (vea [**glMatrixMode**](glmatrixmode.md)) se multiplica por esta matriz de escala, con el producto que reemplaza la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="984e3-128">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this scale matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="984e3-129">Es decir, si M es la matriz actual y S es la matriz de escala, M se reemplaza por M S.</span><span class="sxs-lookup"><span data-stu-id="984e3-129">That is, if M is the current matrix and S is the scale matrix, then M is replaced with M   S.</span></span>

<span data-ttu-id="984e3-130">Si el modo de matriz es \_ MODELVIEW de GL o \_ proyección de contabilidad, se escalan todos los objetos dibujados después de **glScaled** .</span><span class="sxs-lookup"><span data-stu-id="984e3-130">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glScaled** is called are scaled.</span></span> <span data-ttu-id="984e3-131">Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix**](glpopmatrix.md) para guardar y restaurar el sistema de coordenadas sin escala.</span><span class="sxs-lookup"><span data-stu-id="984e3-131">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unscaled coordinate system.</span></span>

<span data-ttu-id="984e3-132">Si se aplican factores de escala distintos de 1,0 a la matriz de MODELVIEW y la iluminación está habilitada, la normalización automática de las normales también debe estar habilitada ([**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento normalizar libro de contabilidad \_ ).</span><span class="sxs-lookup"><span data-stu-id="984e3-132">If scale factors other than 1.0 are applied to the modelview matrix and lighting is enabled, automatic normalization of normals should probably also be enabled ([**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_NORMALIZE).</span></span>

<span data-ttu-id="984e3-133">Las siguientes funciones recuperan información relacionada con **glScaled**:</span><span class="sxs-lookup"><span data-stu-id="984e3-133">The following functions retrieve information related to **glScaled**:</span></span>

<span data-ttu-id="984e3-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="984e3-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="984e3-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MODELVIEW \_ matriz de contabilidad</span><span class="sxs-lookup"><span data-stu-id="984e3-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="984e3-136">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="984e3-136">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="984e3-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="984e3-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="984e3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="984e3-138">Requirements</span></span>



| <span data-ttu-id="984e3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="984e3-139">Requirement</span></span> | <span data-ttu-id="984e3-140">Value</span><span class="sxs-lookup"><span data-stu-id="984e3-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="984e3-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="984e3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="984e3-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="984e3-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="984e3-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="984e3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="984e3-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="984e3-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="984e3-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="984e3-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="984e3-146"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="984e3-146"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="984e3-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="984e3-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="984e3-148"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="984e3-148"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="984e3-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="984e3-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="984e3-150"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="984e3-150"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="984e3-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="984e3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="984e3-152">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="984e3-152">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="984e3-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="984e3-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="984e3-154">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="984e3-154">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="984e3-155">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="984e3-155">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="984e3-156">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="984e3-156">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="984e3-157">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="984e3-157">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="984e3-158">**glRotated**</span><span class="sxs-lookup"><span data-stu-id="984e3-158">**glRotated**</span></span>](glrotated.md)
</dt> <dt>

[<span data-ttu-id="984e3-159">**glRotatef**</span><span class="sxs-lookup"><span data-stu-id="984e3-159">**glRotatef**</span></span>](glrotatef.md)
</dt> <dt>

[<span data-ttu-id="984e3-160">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="984e3-160">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





