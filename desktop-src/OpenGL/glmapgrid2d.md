---
title: función glMapGrid2d (GL. h)
description: Define una malla unidimensional. | función glMapGrid2d (GL. h)
ms.assetid: 5e5887d1-e137-434b-a1f3-b3f10d462823
keywords:
- glMapGrid2d (función) OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6992a904528cf961f27335e7241c50fbd14f058b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670113"
---
# <a name="glmapgrid2d-function"></a><span data-ttu-id="4f75c-105">glMapGrid2d función)</span><span class="sxs-lookup"><span data-stu-id="4f75c-105">glMapGrid2d function</span></span>

<span data-ttu-id="4f75c-106">Define una malla unidimensional.</span><span class="sxs-lookup"><span data-stu-id="4f75c-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f75c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f75c-107">Syntax</span></span>


```C++
void WINAPI glMapGrid2d(
   GLint    un,
   GLdouble u1,
   GLdouble u2,
   GLint    vn,
   GLdouble v1,
   GLdouble v2
);
```



## <a name="parameters"></a><span data-ttu-id="4f75c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f75c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f75c-109">*un*</span><span class="sxs-lookup"><span data-stu-id="4f75c-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="4f75c-110">El número de particiones en el intervalo de intervalo de la cuadrícula \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="4f75c-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="4f75c-111">Este valor debe ser positivo.</span><span class="sxs-lookup"><span data-stu-id="4f75c-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="4f75c-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="4f75c-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="4f75c-113">Valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros i = 0.</span><span class="sxs-lookup"><span data-stu-id="4f75c-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="4f75c-114">*U2*</span><span class="sxs-lookup"><span data-stu-id="4f75c-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="4f75c-115">Un valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros i = un.</span><span class="sxs-lookup"><span data-stu-id="4f75c-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> <dt>

<span data-ttu-id="4f75c-116">*vn*</span><span class="sxs-lookup"><span data-stu-id="4f75c-116">*vn*</span></span> 
</dt> <dd>

<span data-ttu-id="4f75c-117">El número de particiones en el intervalo de intervalo de la cuadrícula \[ v1, V2 \] .</span><span class="sxs-lookup"><span data-stu-id="4f75c-117">The number of partitions in the grid range interval \[v1, v2\].</span></span>

</dd> <dt>

<span data-ttu-id="4f75c-118">*v1*</span><span class="sxs-lookup"><span data-stu-id="4f75c-118">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="4f75c-119">Valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros j = 0.</span><span class="sxs-lookup"><span data-stu-id="4f75c-119">A value used as the mapping for integer grid domain value j = 0.</span></span>

</dd> <dt>

<span data-ttu-id="4f75c-120">*v2*</span><span class="sxs-lookup"><span data-stu-id="4f75c-120">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="4f75c-121">Valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros j = vn.</span><span class="sxs-lookup"><span data-stu-id="4f75c-121">A value used as the mapping for integer grid domain value j = vn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f75c-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f75c-122">Return value</span></span>

<span data-ttu-id="4f75c-123">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4f75c-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f75c-124">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4f75c-124">Error codes</span></span>

<span data-ttu-id="4f75c-125">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="4f75c-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4f75c-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="4f75c-126">Name</span></span>                                                                                                  | <span data-ttu-id="4f75c-127">Significado</span><span class="sxs-lookup"><span data-stu-id="4f75c-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f75c-128"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4f75c-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="4f75c-129">*Un* o *vn* no era positivo.</span><span class="sxs-lookup"><span data-stu-id="4f75c-129">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="4f75c-130"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4f75c-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4f75c-131">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4f75c-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4f75c-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f75c-132">Remarks</span></span>

<span data-ttu-id="4f75c-133">Las funciones **glMapGrid** y [glEvalMesh](glevalmesh-functions.md) se usan en conjunto para generar y evaluar eficazmente una serie de valores de dominio de mapa con espaciado uniforme.</span><span class="sxs-lookup"><span data-stu-id="4f75c-133">The **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="4f75c-134">La función glEvalMesh se recorre a través del dominio entero de una cuadrícula de una o dos dimensiones, cuyo intervalo es el dominio de las asignaciones de evaluación especificadas por [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="4f75c-134">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="4f75c-135">Las funciones [**glMapGrid1**](glmapgrid1d.md) y **glMapGrid2** especifican las asignaciones de cuadrícula lineal entre las coordenadas de la cuadrícula de los enteros i (o i y j), a las coordenadas de mapa de evaluación de punto flotante u (o y v).</span><span class="sxs-lookup"><span data-stu-id="4f75c-135">The [**glMapGrid1**](glmapgrid1d.md) and **glMapGrid2** functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="4f75c-136">Vea [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md) para obtener información detallada sobre cómo se evalúan las coordenadas de y v.</span><span class="sxs-lookup"><span data-stu-id="4f75c-136">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="4f75c-137">La función [**glMapGrid1**](glmapgrid1d.md) especifica una asignación lineal única, de modo que la *coordenada de* la cuadrícula entera 0 se asigna exactamente a U1, y la coordenada de la cuadrícula de enteros es una asignada exactamente a *U2*.</span><span class="sxs-lookup"><span data-stu-id="4f75c-137">The [**glMapGrid1**](glmapgrid1d.md) function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="4f75c-138">Todas las *demás coordenadas de* la cuadrícula de enteros se asignan de manera que:</span><span class="sxs-lookup"><span data-stu-id="4f75c-138">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="4f75c-139">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="4f75c-139">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="4f75c-140">La función **glMapGrid2** especifica dos asignaciones lineales de este tipo.</span><span class="sxs-lookup"><span data-stu-id="4f75c-140">The **glMapGrid2** function specifies two such linear mappings.</span></span> <span data-ttu-id="4f75c-141">Una cuadrícula de enteros de asignación coordina *i = 0* exactamente a *U1* y las coordenadas de la cuadrícula de enteros *i =* out exactamente a *U2*.</span><span class="sxs-lookup"><span data-stu-id="4f75c-141">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="4f75c-142">La otra coordenada de la cuadrícula de enteros de Maps *j = 0* exactamente a *v1* y la coordenada de la cuadrícula de enteros *j = vn* exactamente a *V2*.</span><span class="sxs-lookup"><span data-stu-id="4f75c-142">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="4f75c-143">Las coordenadas i y j de otras cuadrículas de enteros se asignan de forma que</span><span class="sxs-lookup"><span data-stu-id="4f75c-143">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="4f75c-144">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="4f75c-144">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="4f75c-145">*v = j (V2 V1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="4f75c-145">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="4f75c-146">Las asignaciones especificadas por [**glMapGrid**](glmapgrid1d.md) se usan de forma idéntica en [glEvalMesh](glevalmesh-functions.md) y [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="4f75c-146">The mappings specified by [**glMapGrid**](glmapgrid1d.md) are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="4f75c-147">Las siguientes funciones recuperan información relacionada con [**glMapGrid**](glmapgrid1d.md):</span><span class="sxs-lookup"><span data-stu-id="4f75c-147">The following functions retrieve information related to [**glMapGrid**](glmapgrid1d.md):</span></span>

<dl>

<span data-ttu-id="4f75c-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="4f75c-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="4f75c-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP2 ( \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="4f75c-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="4f75c-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP1 \_ segmentos de cuadrícula de GL \_</span><span class="sxs-lookup"><span data-stu-id="4f75c-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="4f75c-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP2 ( \_ segmentos de cuadrícula de GL \_</span><span class="sxs-lookup"><span data-stu-id="4f75c-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="4f75c-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f75c-152">Requirements</span></span>



| <span data-ttu-id="4f75c-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f75c-153">Requirement</span></span> | <span data-ttu-id="4f75c-154">Value</span><span class="sxs-lookup"><span data-stu-id="4f75c-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f75c-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f75c-155">Minimum supported client</span></span><br/> | <span data-ttu-id="4f75c-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4f75c-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4f75c-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f75c-157">Minimum supported server</span></span><br/> | <span data-ttu-id="4f75c-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4f75c-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f75c-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f75c-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f75c-160"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f75c-160"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4f75c-161">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f75c-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f75c-162"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f75c-162"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4f75c-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f75c-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f75c-164"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f75c-164"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f75c-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f75c-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f75c-166">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4f75c-166">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4f75c-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4f75c-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4f75c-168">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="4f75c-168">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="4f75c-169">glEvalMesh</span><span class="sxs-lookup"><span data-stu-id="4f75c-169">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="4f75c-170">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="4f75c-170">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="4f75c-171">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="4f75c-171">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="4f75c-172">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="4f75c-172">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





