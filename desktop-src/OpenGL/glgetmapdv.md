---
title: función glGetMapdv (GL. h)
description: Las funciones glGetMapdv, glGetMapfv y glGetMapiv devuelven parámetros de evaluador. | función glGetMapdv (GL. h)
ms.assetid: 3b4fc03b-ada4-4f4a-a234-fa6439f2e5c8
keywords:
- glGetMapdv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetMapdv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf7dd5104ce7a47b0d1215221c115a7191f4548
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689749"
---
# <a name="glgetmapdv-function"></a><span data-ttu-id="14be0-105">glGetMapdv función)</span><span class="sxs-lookup"><span data-stu-id="14be0-105">glGetMapdv function</span></span>

<span data-ttu-id="14be0-106">Las funciones **glGetMapdv**, [**glGetMapfv**](glgetmapfv.md)y [**glGetMapiv**](glgetmapiv.md) devuelven parámetros de evaluador.</span><span class="sxs-lookup"><span data-stu-id="14be0-106">The **glGetMapdv**, [**glGetMapfv**](glgetmapfv.md), and [**glGetMapiv**](glgetmapiv.md) functions return evaluator parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="14be0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14be0-107">Syntax</span></span>


```C++
void WINAPI glGetMapdv(
   GLenum   target,
   GLenum   query,
   GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="14be0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14be0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14be0-109">*Destino*</span><span class="sxs-lookup"><span data-stu-id="14be0-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="14be0-110">Nombre simbólico de un mapa.</span><span class="sxs-lookup"><span data-stu-id="14be0-110">The symbolic name of a map.</span></span> <span data-ttu-id="14be0-111">A continuación se indican los valores aceptados: GL \_ MAP1 \_ color \_ 4, GL \_ MAP1 \_ index, GL \_ MAP1 \_ normal, GL \_ MAP1 \_ Texture \_ coordenadas \_ 1, GL \_ MAP1 \_ Texture \_ coordenadas \_ 2, GL \_ MAP1 \_ Texture \_ coordenadas \_ 3, GL \_ MAP1 \_ Texture \_ \_ 4, GL \_ MAP1 \_ Vertex \_ 3, GL \_ MAP1 \_ Vertex \_ 4, GL \_ MAP2 ( \_ color \_ 4, GL \_ MAP2 ( \_ index, GL \_ MAP2 ( \_ normal, GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 1, GL MAP2 (Texture 3, GL MAP2 ( \_ \_ \_ \_ \_ \_ Texture \_ \_ 4, GL \_ MAP2 ( \_ Texture \_ \_ 4, GL \_ MAP2 (Texture \_ \_ y \_ \_ \_ GL MAP2 (.</span><span class="sxs-lookup"><span data-stu-id="14be0-111">The following are accepted values: GL\_MAP1\_COLOR\_4, GL\_MAP1\_INDEX, GL\_MAP1\_NORMAL, GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP1\_VERTEX\_3, GL\_MAP1\_VERTEX\_4, GL\_MAP2\_COLOR\_4, GL\_MAP2\_INDEX, GL\_MAP2\_NORMAL, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, GL\_MAP2\_TEXTURE\_COORD\_4, GL\_MAP2\_VERTEX\_3, and GL\_MAP2\_VERTEX\_4.</span></span>

</dd> <dt>

<span data-ttu-id="14be0-112">*consulta*</span><span class="sxs-lookup"><span data-stu-id="14be0-112">*query*</span></span> 
</dt> <dd>

<span data-ttu-id="14be0-113">Especifica el parámetro que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="14be0-113">Specifies which parameter to return.</span></span> <span data-ttu-id="14be0-114">Se aceptan los siguientes nombres simbólicos.</span><span class="sxs-lookup"><span data-stu-id="14be0-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="14be0-115">Value</span><span class="sxs-lookup"><span data-stu-id="14be0-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="14be0-116">Significado</span><span class="sxs-lookup"><span data-stu-id="14be0-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <span data-ttu-id="14be0-117"><dt>**GL \_ COEFF**</dt></span><span class="sxs-lookup"><span data-stu-id="14be0-117"><dt>**GL\_COEFF**</dt></span></span> </dl>    | <span data-ttu-id="14be0-118">El parámetro *v* devuelve los puntos de control de la función Evaluator.</span><span class="sxs-lookup"><span data-stu-id="14be0-118">The *v* parameter returns the control points for the evaluator function.</span></span> <span data-ttu-id="14be0-119">Los evaluadores unidimensionales devuelven puntos de control de *orden* y los evaluadores bidimensionales devuelven puntos de control *uorder* *x* *Vorder* .</span><span class="sxs-lookup"><span data-stu-id="14be0-119">One-dimensional evaluators return *order* control points, and two-dimensional evaluators return *uorder* *x* *vorder* control points.</span></span> <span data-ttu-id="14be0-120">Cada punto de control se compone de uno, dos, tres o cuatro valores de punto flotante de precisión simple o de punto flotante de precisión sencilla, dependiendo del tipo de evaluador.</span><span class="sxs-lookup"><span data-stu-id="14be0-120">Each control point consists of one, two, three, or four integer, single-precision floating-point, or double-precision floating-point values, depending on the type of the evaluator.</span></span> <span data-ttu-id="14be0-121">Los puntos de control bidimensionales se devuelven en orden principal de fila, incrementando rápidamente el índice de *uorder* y el índice de *Vorder* después de cada fila.</span><span class="sxs-lookup"><span data-stu-id="14be0-121">Two-dimensional control points are returned in row-major order, incrementing the *uorder* index quickly, and the *vorder* index after each row.</span></span> <span data-ttu-id="14be0-122">Los valores enteros, cuando se solicitan, se calculan Redondeando los valores de punto flotante internos a los valores enteros más cercanos.</span><span class="sxs-lookup"><span data-stu-id="14be0-122">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <span data-ttu-id="14be0-123"><dt>**orden de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14be0-123"><dt>**GL\_ORDER**</dt></span></span> </dl>    | <span data-ttu-id="14be0-124">El parámetro *v* devuelve el orden de la función evaluadora.</span><span class="sxs-lookup"><span data-stu-id="14be0-124">The *v* parameter returns the order of the evaluator function.</span></span> <span data-ttu-id="14be0-125">Los evaluadores unidimensionales devuelven un único valor, *Order*.</span><span class="sxs-lookup"><span data-stu-id="14be0-125">One-dimensional evaluators return a single value, *order*.</span></span> <span data-ttu-id="14be0-126">Los evaluadores bidimensionales devuelven dos valores, *uorder* y *Vorder*.</span><span class="sxs-lookup"><span data-stu-id="14be0-126">Two-dimensional evaluators return two values, *uorder* and *vorder*.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <span data-ttu-id="14be0-127"><dt>**dominio de contabilidad general \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14be0-127"><dt>**GL\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="14be0-128">El parámetro *v* devuelve los parámetros de asignación lineal de *u* y *v* .</span><span class="sxs-lookup"><span data-stu-id="14be0-128">The *v* parameter returns the linear *u* and *v* mapping parameters.</span></span> <span data-ttu-id="14be0-129">Los evaluadores unidimensionales devuelven dos valores, *u* 1 y *u* 2, según se especifica en [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="14be0-129">One-dimensional evaluators return two values, *u* 1 and *u* 2, as specified by [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="14be0-130">Los evaluadores bidimensionales devuelven cuatro valores (*U1*, *U2*, *v1* y *V2*), tal y como se especifica en [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="14be0-130">Two-dimensional evaluators return four values (*u1*, *u2*, *v1*, and *v2*) as specified by [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="14be0-131">Los valores enteros, cuando se solicitan, se calculan Redondeando los valores de punto flotante internos a los valores enteros más cercanos.</span><span class="sxs-lookup"><span data-stu-id="14be0-131">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="14be0-132">*v*</span><span class="sxs-lookup"><span data-stu-id="14be0-132">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="14be0-133">Devuelve los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="14be0-133">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14be0-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14be0-134">Return value</span></span>

<span data-ttu-id="14be0-135">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="14be0-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="14be0-136">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="14be0-136">Error codes</span></span>

<span data-ttu-id="14be0-137">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="14be0-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="14be0-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="14be0-138">Name</span></span>                                                                                                  | <span data-ttu-id="14be0-139">Significado</span><span class="sxs-lookup"><span data-stu-id="14be0-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14be0-140"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14be0-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="14be0-141">el *destino* o la *consulta* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="14be0-141">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="14be0-142"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14be0-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="14be0-143">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="14be0-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="14be0-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14be0-144">Remarks</span></span>

<span data-ttu-id="14be0-145">La función **glGetMap** devuelve los parámetros del evaluador.</span><span class="sxs-lookup"><span data-stu-id="14be0-145">The **glGetMap** function returns evaluator parameters.</span></span> <span data-ttu-id="14be0-146">(Las funciones **glMap1** y **glMap2** definen evaluadores). El parámetro de *destino* especifica un mapa, la *consulta* selecciona un parámetro específico y *v* apunta al almacenamiento donde se devolverán los valores.</span><span class="sxs-lookup"><span data-stu-id="14be0-146">(The **glMap1** and **glMap2** functions define evaluators.) The *target* parameter specifies a map, *query* selects a specific parameter, and *v* points to storage where the values will be returned.</span></span>

<span data-ttu-id="14be0-147">Los valores aceptables para el parámetro de *destino* se describen en [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="14be0-147">The acceptable values for the *target* parameter are described in [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="14be0-148">Si se genera un error, no se realiza ningún cambio en el contenido de *v*.</span><span class="sxs-lookup"><span data-stu-id="14be0-148">If an error is generated, no change is made to the contents of *v*.</span></span>

## <a name="requirements"></a><span data-ttu-id="14be0-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14be0-149">Requirements</span></span>



| <span data-ttu-id="14be0-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="14be0-150">Requirement</span></span> | <span data-ttu-id="14be0-151">Value</span><span class="sxs-lookup"><span data-stu-id="14be0-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14be0-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14be0-152">Minimum supported client</span></span><br/> | <span data-ttu-id="14be0-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="14be0-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14be0-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14be0-154">Minimum supported server</span></span><br/> | <span data-ttu-id="14be0-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14be0-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14be0-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14be0-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="14be0-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="14be0-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="14be0-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14be0-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="14be0-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14be0-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="14be0-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="14be0-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14be0-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14be0-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14be0-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="14be0-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14be0-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="14be0-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="14be0-164">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="14be0-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="14be0-165">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="14be0-165">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="14be0-166">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="14be0-166">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="14be0-167">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="14be0-167">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





