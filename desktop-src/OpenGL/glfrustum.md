---
title: función glFrustum (GL. h)
description: La función glFrustum multiplica la matriz actual por una matriz de perspectiva.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- glFrustum (función) OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce67879ca20819713e61a9392bf77be2f15211d5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104565625"
---
# <a name="glfrustum-function"></a><span data-ttu-id="35b29-104">glFrustum función)</span><span class="sxs-lookup"><span data-stu-id="35b29-104">glFrustum function</span></span>

<span data-ttu-id="35b29-105">La función **glFrustum** multiplica la matriz actual por una matriz de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="35b29-105">The **glFrustum** function multiplies the current matrix by a perspective matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="35b29-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35b29-106">Syntax</span></span>


```C++
void WINAPI glFrustum(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="35b29-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35b29-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35b29-108">*salido*</span><span class="sxs-lookup"><span data-stu-id="35b29-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="35b29-109">La coordenada del plano de recorte izquierdo-vertical.</span><span class="sxs-lookup"><span data-stu-id="35b29-109">The coordinate for the left-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="35b29-110">*correcta*</span><span class="sxs-lookup"><span data-stu-id="35b29-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="35b29-111">Coordenada del plano de recorte vertical derecha.</span><span class="sxs-lookup"><span data-stu-id="35b29-111">The coordinate for the right-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="35b29-112">*descendente*</span><span class="sxs-lookup"><span data-stu-id="35b29-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="35b29-113">Coordenada del plano de recorte horizontal inferior.</span><span class="sxs-lookup"><span data-stu-id="35b29-113">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="35b29-114">*top*</span><span class="sxs-lookup"><span data-stu-id="35b29-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="35b29-115">Coordenada del plano de recorte horizontal inferior.</span><span class="sxs-lookup"><span data-stu-id="35b29-115">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="35b29-116">*zNear*</span><span class="sxs-lookup"><span data-stu-id="35b29-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="35b29-117">Distancias al plano de recorte más profundo.</span><span class="sxs-lookup"><span data-stu-id="35b29-117">The distances to the near-depth clipping plane.</span></span> <span data-ttu-id="35b29-118">Debe ser positivo.</span><span class="sxs-lookup"><span data-stu-id="35b29-118">Must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="35b29-119">*zFar*</span><span class="sxs-lookup"><span data-stu-id="35b29-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="35b29-120">Las distancias a los planos de recorte de profundidad.</span><span class="sxs-lookup"><span data-stu-id="35b29-120">The distances to the far-depth clipping planes.</span></span> <span data-ttu-id="35b29-121">Debe ser positivo.</span><span class="sxs-lookup"><span data-stu-id="35b29-121">Must be positive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35b29-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35b29-122">Return value</span></span>

<span data-ttu-id="35b29-123">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="35b29-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35b29-124">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="35b29-124">Error codes</span></span>

<span data-ttu-id="35b29-125">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="35b29-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="35b29-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="35b29-126">Name</span></span>                                                                                                  | <span data-ttu-id="35b29-127">Significado</span><span class="sxs-lookup"><span data-stu-id="35b29-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35b29-128"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35b29-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="35b29-129">*zNear* o *zFar* no postitive.</span><span class="sxs-lookup"><span data-stu-id="35b29-129">*zNear* or *zFar* was not postitive.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="35b29-130"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35b29-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="35b29-131">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="35b29-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="35b29-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35b29-132">Remarks</span></span>

<span data-ttu-id="35b29-133">La función **glFrustum** describe una matriz de perspectiva que genera una proyección en perspectiva.</span><span class="sxs-lookup"><span data-stu-id="35b29-133">The **glFrustum** function describes a perspective matrix that produces a perspective projection.</span></span> <span data-ttu-id="35b29-134">Los parámetros (*left*, *Bottom*, *zNear*) y (*right*, *Top*, *zNear*) especifican los puntos del plano de recorte cercano que se asignan a las esquinas inferior izquierda y superior derecha de la ventana, respectivamente, suponiendo que el ojo está ubicado en (0,0).</span><span class="sxs-lookup"><span data-stu-id="35b29-134">The (*left*, *bottom*, *zNear*) and (*right*, *top*, *zNear*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0,0,0).</span></span> <span data-ttu-id="35b29-135">El parámetro *zFar* especifica la ubicación del plano de recorte lejano.</span><span class="sxs-lookup"><span data-stu-id="35b29-135">The *zFar* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="35b29-136">Tanto *zNear* como *zFar* deben ser positivos.</span><span class="sxs-lookup"><span data-stu-id="35b29-136">Both *zNear* and *zFar* must be positive.</span></span> <span data-ttu-id="35b29-137">La matriz correspondiente se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="35b29-137">The corresponding matrix is shown in the following image.</span></span>

![Diagrama que muestra la matriz de perspectiva que genera una proyección en perspectiva.](images/frust01.png)![Ecuaciones que muestran la función glFrustum que describe una matriz de perspectiva.](images/frust02.png)

<span data-ttu-id="35b29-140">La función **glFrustum** multiplica la matriz actual por esta matriz, con el resultado que reemplaza la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="35b29-140">The **glFrustum** function multiplies the current matrix by this matrix, with the result replacing the current matrix.</span></span> <span data-ttu-id="35b29-141">Es decir, si M es la matriz actual y F es la matriz de perspectiva del frustum, **glFrustum** reemplaza a M por m F.</span><span class="sxs-lookup"><span data-stu-id="35b29-141">That is, if M is the current matrix and F is the frustum perspective matrix, then **glFrustum** replaces M with M   F.</span></span>

<span data-ttu-id="35b29-142">Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix**](glpopmatrix.md) para guardar y restaurar la pila de matriz actual.</span><span class="sxs-lookup"><span data-stu-id="35b29-142">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the current matrix stack.</span></span>

<span data-ttu-id="35b29-143">La precisión del búfer de profundidad se ve afectada por los valores especificados para *zNear* y *zFar*.</span><span class="sxs-lookup"><span data-stu-id="35b29-143">Depth-buffer precision is affected by the values specified for *zNear* and *zFar*.</span></span> <span data-ttu-id="35b29-144">Cuanto mayor sea la relación de *zFar* con *zNear* , más eficaz será el búfer de profundidad a la distinción entre superficies que están cerca unas de otras.</span><span class="sxs-lookup"><span data-stu-id="35b29-144">The greater the ratio of *zFar* to *zNear* is, the less effective the depth buffer will be at distinguishing between surfaces that are near each other.</span></span> <span data-ttu-id="35b29-145">Si</span><span class="sxs-lookup"><span data-stu-id="35b29-145">If</span></span>

![Ecuación que muestra la relación de lejos a near.](images/frust03.png)

<span data-ttu-id="35b29-147">se pierden aproximadamente los bits de *registro* 2 (*r*) de la precisión del búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="35b29-147">roughly *log* 2 (*r*) bits of depth buffer precision are lost.</span></span> <span data-ttu-id="35b29-148">Dado que *r* se aproxima al infinito como *zNear* se aproxima a cero, nunca debe establecer *zNear* en cero.</span><span class="sxs-lookup"><span data-stu-id="35b29-148">Because *r* approaches infinity as *zNear* approaches zero, you should never set *zNear* to zero.</span></span>

<span data-ttu-id="35b29-149">Las siguientes funciones recuperan información sobre **glFrustum**:</span><span class="sxs-lookup"><span data-stu-id="35b29-149">The following functions retrieve information about **glFrustum**:</span></span>

<span data-ttu-id="35b29-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="35b29-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="35b29-151">**glGet** con el argumento \_ MODELVIEW \_ matriz de contabilidad</span><span class="sxs-lookup"><span data-stu-id="35b29-151">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="35b29-152">**glGet** con el argumento \_ matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="35b29-152">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="35b29-153">**glGet** con el argumento \_ matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="35b29-153">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="35b29-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35b29-154">Requirements</span></span>



| <span data-ttu-id="35b29-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="35b29-155">Requirement</span></span> | <span data-ttu-id="35b29-156">Value</span><span class="sxs-lookup"><span data-stu-id="35b29-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35b29-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35b29-157">Minimum supported client</span></span><br/> | <span data-ttu-id="35b29-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="35b29-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="35b29-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35b29-159">Minimum supported server</span></span><br/> | <span data-ttu-id="35b29-160">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="35b29-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35b29-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35b29-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="35b29-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="35b29-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="35b29-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35b29-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="35b29-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35b29-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="35b29-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35b29-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35b29-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35b29-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35b29-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="35b29-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35b29-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="35b29-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="35b29-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="35b29-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="35b29-170">**glGet**</span><span class="sxs-lookup"><span data-stu-id="35b29-170">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="35b29-171">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="35b29-171">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="35b29-172">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="35b29-172">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="35b29-173">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="35b29-173">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="35b29-174">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="35b29-174">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="35b29-175">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="35b29-175">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="35b29-176">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="35b29-176">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





