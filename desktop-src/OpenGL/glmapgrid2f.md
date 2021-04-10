---
title: función glMapGrid2f (GL. h)
description: Define una malla unidimensional. | función glMapGrid2f (GL. h)
ms.assetid: f9bc2b0c-dec5-4762-8c99-46546a81893e
keywords:
- glMapGrid2f (función) OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 087e42aa3d490ec605b4478d5691b256271268f5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279945"
---
# <a name="glmapgrid2f-function"></a><span data-ttu-id="0535a-105">glMapGrid2f función)</span><span class="sxs-lookup"><span data-stu-id="0535a-105">glMapGrid2f function</span></span>

<span data-ttu-id="0535a-106">Define una malla unidimensional.</span><span class="sxs-lookup"><span data-stu-id="0535a-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0535a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0535a-107">Syntax</span></span>


```C++
void WINAPI glMapGrid2f(
   GLint   un,
   GLfloat u1,
   GLfloat u2,
   GLint   vn,
   GLfloat v1,
   GLfloat v2
);
```



## <a name="parameters"></a><span data-ttu-id="0535a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0535a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0535a-109">*un*</span><span class="sxs-lookup"><span data-stu-id="0535a-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="0535a-110">El número de particiones en el intervalo de intervalo de la cuadrícula \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="0535a-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="0535a-111">Este valor debe ser positivo.</span><span class="sxs-lookup"><span data-stu-id="0535a-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="0535a-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="0535a-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="0535a-113">Valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros i = 0.</span><span class="sxs-lookup"><span data-stu-id="0535a-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="0535a-114">*U2*</span><span class="sxs-lookup"><span data-stu-id="0535a-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="0535a-115">Un valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros i = un.</span><span class="sxs-lookup"><span data-stu-id="0535a-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> <dt>

<span data-ttu-id="0535a-116">*vn*</span><span class="sxs-lookup"><span data-stu-id="0535a-116">*vn*</span></span> 
</dt> <dd>

<span data-ttu-id="0535a-117">El número de particiones en el intervalo de intervalo de la cuadrícula \[ v1, V2 \] .</span><span class="sxs-lookup"><span data-stu-id="0535a-117">The number of partitions in the grid range interval \[v1, v2\].</span></span>

</dd> <dt>

<span data-ttu-id="0535a-118">*v1*</span><span class="sxs-lookup"><span data-stu-id="0535a-118">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="0535a-119">Valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros j = 0.</span><span class="sxs-lookup"><span data-stu-id="0535a-119">A value used as the mapping for integer grid domain value j = 0.</span></span>

</dd> <dt>

<span data-ttu-id="0535a-120">*v2*</span><span class="sxs-lookup"><span data-stu-id="0535a-120">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="0535a-121">Valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros j = vn.</span><span class="sxs-lookup"><span data-stu-id="0535a-121">A value used as the mapping for integer grid domain value j = vn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0535a-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0535a-122">Return value</span></span>

<span data-ttu-id="0535a-123">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0535a-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0535a-124">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0535a-124">Error codes</span></span>

<span data-ttu-id="0535a-125">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="0535a-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0535a-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="0535a-126">Name</span></span>                                                                                                  | <span data-ttu-id="0535a-127">Significado</span><span class="sxs-lookup"><span data-stu-id="0535a-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0535a-128"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0535a-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="0535a-129">*Un* o *vn* no era positivo.</span><span class="sxs-lookup"><span data-stu-id="0535a-129">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="0535a-130"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0535a-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0535a-131">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="0535a-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0535a-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0535a-132">Remarks</span></span>

<span data-ttu-id="0535a-133">Las funciones **glMapGrid** y [glEvalMesh](glevalmesh-functions.md) se usan en conjunto para generar y evaluar eficazmente una serie de valores de dominio de mapa con espaciado uniforme.</span><span class="sxs-lookup"><span data-stu-id="0535a-133">The **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="0535a-134">La función glEvalMesh se recorre a través del dominio entero de una cuadrícula de una o dos dimensiones, cuyo intervalo es el dominio de las asignaciones de evaluación especificadas por [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="0535a-134">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="0535a-135">Las funciones [**glMapGrid1**](glmapgrid1d.md) y [**glMapGrid2**](glmapgrid2d.md) especifican las asignaciones de cuadrícula lineal entre las coordenadas de la cuadrícula de los enteros i (o i y j), a las coordenadas de mapa de evaluación de punto flotante u (o y v).</span><span class="sxs-lookup"><span data-stu-id="0535a-135">The [**glMapGrid1**](glmapgrid1d.md) and [**glMapGrid2**](glmapgrid2d.md) functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="0535a-136">Vea [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md) para obtener información detallada sobre cómo se evalúan las coordenadas de y v.</span><span class="sxs-lookup"><span data-stu-id="0535a-136">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="0535a-137">La función [**glMapGrid1**](glmapgrid1d.md) especifica una asignación lineal única, de modo que la *coordenada de* la cuadrícula entera 0 se asigna exactamente a U1, y la coordenada de la cuadrícula de enteros es una asignada exactamente a *U2*.</span><span class="sxs-lookup"><span data-stu-id="0535a-137">The [**glMapGrid1**](glmapgrid1d.md) function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="0535a-138">Todas las *demás coordenadas de* la cuadrícula de enteros se asignan de manera que:</span><span class="sxs-lookup"><span data-stu-id="0535a-138">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="0535a-139">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="0535a-139">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="0535a-140">La función [**glMapGrid2**](glmapgrid2d.md) especifica dos asignaciones lineales de este tipo.</span><span class="sxs-lookup"><span data-stu-id="0535a-140">The [**glMapGrid2**](glmapgrid2d.md) function specifies two such linear mappings.</span></span> <span data-ttu-id="0535a-141">Una cuadrícula de enteros de asignación coordina *i = 0* exactamente a *U1* y las coordenadas de la cuadrícula de enteros *i =* out exactamente a *U2*.</span><span class="sxs-lookup"><span data-stu-id="0535a-141">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="0535a-142">La otra coordenada de la cuadrícula de enteros de Maps *j = 0* exactamente a *v1* y la coordenada de la cuadrícula de enteros *j = vn* exactamente a *V2*.</span><span class="sxs-lookup"><span data-stu-id="0535a-142">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="0535a-143">Las coordenadas i y j de otras cuadrículas de enteros se asignan de forma que</span><span class="sxs-lookup"><span data-stu-id="0535a-143">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="0535a-144">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="0535a-144">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="0535a-145">*v = j (V2 V1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="0535a-145">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="0535a-146">Las asignaciones especificadas por [**glMapGrid**](glmapgrid1d.md) se usan de forma idéntica en [glEvalMesh](glevalmesh-functions.md) y [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="0535a-146">The mappings specified by [**glMapGrid**](glmapgrid1d.md) are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="0535a-147">Las siguientes funciones recuperan información relacionada con [**glMapGrid**](glmapgrid1d.md):</span><span class="sxs-lookup"><span data-stu-id="0535a-147">The following functions retrieve information related to [**glMapGrid**](glmapgrid1d.md):</span></span>

<dl>

<span data-ttu-id="0535a-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="0535a-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="0535a-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP2 ( \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="0535a-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="0535a-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP1 \_ segmentos de cuadrícula de GL \_</span><span class="sxs-lookup"><span data-stu-id="0535a-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="0535a-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP2 ( \_ segmentos de cuadrícula de GL \_</span><span class="sxs-lookup"><span data-stu-id="0535a-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="0535a-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0535a-152">Requirements</span></span>



| <span data-ttu-id="0535a-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="0535a-153">Requirement</span></span> | <span data-ttu-id="0535a-154">Value</span><span class="sxs-lookup"><span data-stu-id="0535a-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0535a-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0535a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="0535a-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0535a-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0535a-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0535a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="0535a-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0535a-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0535a-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0535a-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="0535a-160"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0535a-160"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0535a-161">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0535a-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="0535a-162"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0535a-162"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0535a-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0535a-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0535a-164"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0535a-164"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0535a-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="0535a-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0535a-166">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0535a-166">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0535a-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0535a-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0535a-168">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="0535a-168">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="0535a-169">glEvalMesh</span><span class="sxs-lookup"><span data-stu-id="0535a-169">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="0535a-170">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="0535a-170">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="0535a-171">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="0535a-171">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="0535a-172">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="0535a-172">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





