---
title: función glOrtho (GL. h)
description: La función glOrtho multiplica la matriz actual por una matriz ortográfica.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- glOrtho (función) OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46abbb0edd2dfc7fc51aaf7fa6519dc5367b109c
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104569741"
---
# <a name="glortho-function"></a><span data-ttu-id="68b17-104">glOrtho función)</span><span class="sxs-lookup"><span data-stu-id="68b17-104">glOrtho function</span></span>

<span data-ttu-id="68b17-105">La función **glOrtho** multiplica la matriz actual por una matriz ortográfica.</span><span class="sxs-lookup"><span data-stu-id="68b17-105">The **glOrtho** function multiplies the current matrix by an orthographic matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b17-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68b17-106">Syntax</span></span>


```C++
void WINAPI glOrtho(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="68b17-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68b17-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68b17-108">*salido*</span><span class="sxs-lookup"><span data-stu-id="68b17-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="68b17-109">Coordenadas del plano de recorte vertical izquierdo.</span><span class="sxs-lookup"><span data-stu-id="68b17-109">The coordinates for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="68b17-110">*correcta*</span><span class="sxs-lookup"><span data-stu-id="68b17-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="68b17-111">Coordenadas del plano de recorte vertical derecho.</span><span class="sxs-lookup"><span data-stu-id="68b17-111">The coordinates for theright vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="68b17-112">*descendente*</span><span class="sxs-lookup"><span data-stu-id="68b17-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="68b17-113">Coordenadas del plano de recorte horizontal inferior.</span><span class="sxs-lookup"><span data-stu-id="68b17-113">The coordinates for the bottom horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="68b17-114">*top*</span><span class="sxs-lookup"><span data-stu-id="68b17-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="68b17-115">Coordenadas para los planes de recorte horizontal superior.</span><span class="sxs-lookup"><span data-stu-id="68b17-115">The coordinates for the top horizontal clipping plans.</span></span>

</dd> <dt>

<span data-ttu-id="68b17-116">*zNear*</span><span class="sxs-lookup"><span data-stu-id="68b17-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="68b17-117">Las distancias al plano de recorte de profundidad más cercana.</span><span class="sxs-lookup"><span data-stu-id="68b17-117">The distances to the nearer depth clipping plane.</span></span> <span data-ttu-id="68b17-118">Esta distancia es negativa si el plano va a estar detrás del visor.</span><span class="sxs-lookup"><span data-stu-id="68b17-118">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> <dt>

<span data-ttu-id="68b17-119">*zFar*</span><span class="sxs-lookup"><span data-stu-id="68b17-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="68b17-120">Las distancias al plano de recorte de profundidad más lejano.</span><span class="sxs-lookup"><span data-stu-id="68b17-120">The distances to the farther depth clipping plane.</span></span> <span data-ttu-id="68b17-121">Esta distancia es negativa si el plano va a estar detrás del visor.</span><span class="sxs-lookup"><span data-stu-id="68b17-121">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68b17-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68b17-122">Return value</span></span>

<span data-ttu-id="68b17-123">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="68b17-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68b17-124">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="68b17-124">Error codes</span></span>

<span data-ttu-id="68b17-125">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="68b17-125">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="68b17-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="68b17-126">Name</span></span>                                                                                                  | <span data-ttu-id="68b17-127">Significado</span><span class="sxs-lookup"><span data-stu-id="68b17-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68b17-128"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68b17-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="68b17-129">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="68b17-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="68b17-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68b17-130">Remarks</span></span>

<span data-ttu-id="68b17-131">La función **glOrtho** describe una matriz de perspectiva que genera una proyección paralela.</span><span class="sxs-lookup"><span data-stu-id="68b17-131">The **glOrtho** function describes a perspective matrix that produces a parallel projection.</span></span> <span data-ttu-id="68b17-132">Los parámetros (*izquierda*, *inferior*, *Near*) y (*derecho*, *superior*, *Near*) especifican los puntos del plano de recorte cercano que se asignan a las esquinas inferior izquierda y superior derecha de la ventana, respectivamente, suponiendo que el ojo está ubicado en (0,0).</span><span class="sxs-lookup"><span data-stu-id="68b17-132">The (*left*, *bottom*, *near*) and (*right*, *top*, *near*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0, 0, 0).</span></span> <span data-ttu-id="68b17-133">El parámetro *Far* especifica la ubicación del plano de recorte lejano.</span><span class="sxs-lookup"><span data-stu-id="68b17-133">The *far* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="68b17-134">Tanto *zNear* como *zFar* pueden ser positivos o negativos.</span><span class="sxs-lookup"><span data-stu-id="68b17-134">Both *zNear* and *zFar* can be either positive or negative.</span></span> <span data-ttu-id="68b17-135">La matriz correspondiente se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="68b17-135">The corresponding matrix is shown in the following image.</span></span>

![Diagrama que muestra la matriz de perspectiva que describe la función glOrtho.](images/ortho1.png)

<span data-ttu-id="68b17-137">where</span><span class="sxs-lookup"><span data-stu-id="68b17-137">where</span></span>

![Ecuaciones que describen la matriz de perspectiva.](images/ortho2.png)

<span data-ttu-id="68b17-139">Esta matriz multiplica la matriz actual con el resultado que reemplaza la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="68b17-139">The current matrix is multiplied by this matrix with the result replacing the current matrix.</span></span> <span data-ttu-id="68b17-140">Es decir, si M es la matriz actual y O es la matriz Ortho, M se reemplaza por M O.</span><span class="sxs-lookup"><span data-stu-id="68b17-140">That is, if M is the current matrix and O is the ortho matrix, then M is replaced with M   O.</span></span>

<span data-ttu-id="68b17-141">Use [**glPushMatrix**](glpushmatrix.md) y **glPopMatrix** para guardar y restaurar la pila de matriz actual.</span><span class="sxs-lookup"><span data-stu-id="68b17-141">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the current matrix stack.</span></span> <span data-ttu-id="68b17-142">Use [**glMatrixMode**](glmatrixmode.md) para establecer la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="68b17-142">Use [**glMatrixMode**](glmatrixmode.md) to set the current matrix.</span></span>

<span data-ttu-id="68b17-143">Las siguientes funciones recuperan información relacionada con **glOrtho**:</span><span class="sxs-lookup"><span data-stu-id="68b17-143">The following functions retrieve information related to **glOrtho**:</span></span>

<span data-ttu-id="68b17-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="68b17-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="68b17-145">**glGet** con el argumento \_ MODELVIEW \_ matriz de contabilidad</span><span class="sxs-lookup"><span data-stu-id="68b17-145">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="68b17-146">**glGet** con el argumento \_ matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="68b17-146">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="68b17-147">**glGet** con el argumento \_ matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="68b17-147">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="68b17-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68b17-148">Requirements</span></span>



| <span data-ttu-id="68b17-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b17-149">Requirement</span></span> | <span data-ttu-id="68b17-150">Value</span><span class="sxs-lookup"><span data-stu-id="68b17-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68b17-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68b17-151">Minimum supported client</span></span><br/> | <span data-ttu-id="68b17-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68b17-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="68b17-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68b17-153">Minimum supported server</span></span><br/> | <span data-ttu-id="68b17-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68b17-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68b17-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68b17-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="68b17-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="68b17-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="68b17-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68b17-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="68b17-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68b17-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="68b17-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68b17-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68b17-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68b17-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68b17-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="68b17-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b17-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="68b17-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="68b17-163">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="68b17-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="68b17-164">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="68b17-164">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="68b17-165">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="68b17-165">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="68b17-166">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="68b17-166">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="68b17-167">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="68b17-167">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="68b17-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="68b17-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





