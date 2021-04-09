---
title: función glMapGrid1d (GL. h)
description: Define una malla unidimensional. | función glMapGrid1d (GL. h)
ms.assetid: a0bc822e-dd98-4586-a322-2779e11f38ca
keywords:
- glMapGrid1d (función) OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b1900f5597e8c516100504ca7288137ed99ded
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914330"
---
# <a name="glmapgrid1d-function"></a><span data-ttu-id="8b4dd-105">glMapGrid1d función)</span><span class="sxs-lookup"><span data-stu-id="8b4dd-105">glMapGrid1d function</span></span>

<span data-ttu-id="8b4dd-106">Define una malla unidimensional.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b4dd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b4dd-107">Syntax</span></span>


```C++
void WINAPI glMapGrid1d(
   GLint    un,
   GLdouble u1,
   GLdouble u2
);
```



## <a name="parameters"></a><span data-ttu-id="8b4dd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b4dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b4dd-109">*un*</span><span class="sxs-lookup"><span data-stu-id="8b4dd-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="8b4dd-110">El número de particiones en el intervalo de intervalo de la cuadrícula \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="8b4dd-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="8b4dd-111">Este valor debe ser positivo.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="8b4dd-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="8b4dd-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="8b4dd-113">Valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros i = 0.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="8b4dd-114">*U2*</span><span class="sxs-lookup"><span data-stu-id="8b4dd-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="8b4dd-115">Un valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros i = un.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b4dd-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b4dd-116">Return value</span></span>

<span data-ttu-id="8b4dd-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b4dd-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8b4dd-118">Error codes</span></span>

<span data-ttu-id="8b4dd-119">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8b4dd-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="8b4dd-120">Name</span></span>                                                                                                  | <span data-ttu-id="8b4dd-121">Significado</span><span class="sxs-lookup"><span data-stu-id="8b4dd-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b4dd-122"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b4dd-122"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8b4dd-123">*Un* o *vn* no era positivo.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-123">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="8b4dd-124"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b4dd-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8b4dd-125">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8b4dd-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8b4dd-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b4dd-126">Remarks</span></span>

<span data-ttu-id="8b4dd-127">Use las funciones **glMapGrid** y [glEvalMesh](glevalmesh-functions.md) conjuntamente para generar y evaluar de forma eficaz una serie de valores de dominio de mapa con espaciado uniforme.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-127">Use the **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions togetherto efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="8b4dd-128">La función glEvalMesh se recorre a través del dominio entero de una cuadrícula de una o dos dimensiones, cuyo intervalo es el dominio de las asignaciones de evaluación especificadas por [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="8b4dd-128">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="8b4dd-129">Las funciones **glMapGrid1** y [**glMapGrid2**](glmapgrid2d.md) especifican las asignaciones de cuadrícula lineal entre las coordenadas de la cuadrícula de los enteros i (o i y j), a las coordenadas de mapa de evaluación de punto flotante u (o y v).</span><span class="sxs-lookup"><span data-stu-id="8b4dd-129">The **glMapGrid1** and [**glMapGrid2**](glmapgrid2d.md) functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="8b4dd-130">Vea [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md) para obtener información detallada sobre cómo se evalúan las coordenadas de y v.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-130">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="8b4dd-131">La función **glMapGrid1** especifica una asignación lineal única, de modo que la *coordenada de* la cuadrícula entera 0 se asigna exactamente a U1, y la coordenada de la cuadrícula de enteros es una asignada exactamente a *U2*.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-131">The **glMapGrid1** function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="8b4dd-132">Todas las *demás coordenadas de* la cuadrícula de enteros se asignan de manera que:</span><span class="sxs-lookup"><span data-stu-id="8b4dd-132">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="8b4dd-133">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="8b4dd-133">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="8b4dd-134">La función [**glMapGrid2**](glmapgrid2d.md) especifica dos asignaciones lineales de este tipo.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-134">The [**glMapGrid2**](glmapgrid2d.md) function specifies two such linear mappings.</span></span> <span data-ttu-id="8b4dd-135">Una cuadrícula de enteros de asignación coordina *i = 0* exactamente a *U1* y las coordenadas de la cuadrícula de enteros *i =* out exactamente a *U2*.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-135">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="8b4dd-136">La otra coordenada de la cuadrícula de enteros de Maps *j = 0* exactamente a *v1* y la coordenada de la cuadrícula de enteros *j = vn* exactamente a *V2*.</span><span class="sxs-lookup"><span data-stu-id="8b4dd-136">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="8b4dd-137">Las coordenadas i y j de otras cuadrículas de enteros se asignan de forma que</span><span class="sxs-lookup"><span data-stu-id="8b4dd-137">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="8b4dd-138">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="8b4dd-138">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="8b4dd-139">*v = j (V2 V1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="8b4dd-139">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="8b4dd-140">Las asignaciones especificadas por **glMapGrid** se usan de forma idéntica en [glEvalMesh](glevalmesh-functions.md) y [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="8b4dd-140">The mappings specified by **glMapGrid** are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="8b4dd-141">Las siguientes funciones recuperan información relacionada con **glMapGrid**:</span><span class="sxs-lookup"><span data-stu-id="8b4dd-141">The following functions retrieve information related to **glMapGrid**:</span></span>

<dl>

<span data-ttu-id="8b4dd-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="8b4dd-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="8b4dd-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP2 ( \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="8b4dd-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="8b4dd-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP1 \_ segmentos de cuadrícula de GL \_</span><span class="sxs-lookup"><span data-stu-id="8b4dd-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="8b4dd-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP2 ( \_ segmentos de cuadrícula de GL \_</span><span class="sxs-lookup"><span data-stu-id="8b4dd-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="8b4dd-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b4dd-146">Requirements</span></span>



| <span data-ttu-id="8b4dd-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b4dd-147">Requirement</span></span> | <span data-ttu-id="8b4dd-148">Value</span><span class="sxs-lookup"><span data-stu-id="8b4dd-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b4dd-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b4dd-149">Minimum supported client</span></span><br/> | <span data-ttu-id="8b4dd-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8b4dd-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8b4dd-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b4dd-151">Minimum supported server</span></span><br/> | <span data-ttu-id="8b4dd-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b4dd-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8b4dd-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b4dd-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b4dd-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b4dd-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8b4dd-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b4dd-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b4dd-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b4dd-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8b4dd-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b4dd-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b4dd-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b4dd-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b4dd-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b4dd-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b4dd-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8b4dd-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8b4dd-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8b4dd-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8b4dd-162">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="8b4dd-162">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="8b4dd-163">glEvalMesh</span><span class="sxs-lookup"><span data-stu-id="8b4dd-163">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="8b4dd-164">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="8b4dd-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="8b4dd-165">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="8b4dd-165">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="8b4dd-166">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="8b4dd-166">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





