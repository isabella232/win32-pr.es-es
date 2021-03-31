---
title: función glEvalMesh2 (GL. h)
description: Calcula una cuadrícula bidimensional de puntos o líneas.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- glEvalMesh2 (función) OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 531e9f1f6288116d052c728654cd2cf03f38550a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801652"
---
# <a name="glevalmesh2-function"></a><span data-ttu-id="55a38-104">glEvalMesh2 función)</span><span class="sxs-lookup"><span data-stu-id="55a38-104">glEvalMesh2 function</span></span>

<span data-ttu-id="55a38-105">Calcula una cuadrícula bidimensional de puntos o líneas.</span><span class="sxs-lookup"><span data-stu-id="55a38-105">Computes a two-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a38-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55a38-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a><span data-ttu-id="55a38-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55a38-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55a38-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="55a38-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="55a38-109">Valor que especifica si se va a calcular una malla bidimensional de puntos, líneas o polígonos.</span><span class="sxs-lookup"><span data-stu-id="55a38-109">A value that specifies whether to compute a two-dimensional mesh of points, lines, or polygons.</span></span> <span data-ttu-id="55a38-110">Se aceptan las siguientes constantes simbólicas: \_ punto de contabilidad, línea de libro de contabilidad \_ y relleno de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="55a38-110">The following symbolic constants are accepted: GL\_POINT, GL\_LINE, and GL\_FILL.</span></span>

</dd> <dt>

<span data-ttu-id="55a38-111">*I1*</span><span class="sxs-lookup"><span data-stu-id="55a38-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="55a38-112">El primer valor entero para la variable de dominio de cuadrícula i.</span><span class="sxs-lookup"><span data-stu-id="55a38-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="55a38-113">*I2*</span><span class="sxs-lookup"><span data-stu-id="55a38-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="55a38-114">El último valor entero para la variable de dominio de cuadrícula i.</span><span class="sxs-lookup"><span data-stu-id="55a38-114">The last integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="55a38-115">*j1*</span><span class="sxs-lookup"><span data-stu-id="55a38-115">*j1*</span></span> 
</dt> <dd>

<span data-ttu-id="55a38-116">El primer valor entero para la variable de dominio de cuadrícula j.</span><span class="sxs-lookup"><span data-stu-id="55a38-116">The first integer value for grid domain variable j.</span></span>

</dd> <dt>

<span data-ttu-id="55a38-117">*J2*</span><span class="sxs-lookup"><span data-stu-id="55a38-117">*j2*</span></span> 
</dt> <dd>

<span data-ttu-id="55a38-118">Último valor entero para la variable de dominio de cuadrícula j.</span><span class="sxs-lookup"><span data-stu-id="55a38-118">The last integer value for grid domain variable j.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55a38-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55a38-119">Return value</span></span>

<span data-ttu-id="55a38-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="55a38-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="55a38-121">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="55a38-121">Error codes</span></span>

<span data-ttu-id="55a38-122">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="55a38-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="55a38-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="55a38-123">Name</span></span>                                                                                                  | <span data-ttu-id="55a38-124">Significado</span><span class="sxs-lookup"><span data-stu-id="55a38-124">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55a38-125"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55a38-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="55a38-126">Indica que el *modo* no es un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="55a38-126">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="55a38-127"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55a38-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="55a38-128">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="55a38-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="55a38-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55a38-129">Remarks</span></span>

<span data-ttu-id="55a38-130">Use [**glMapGrid**](glmapgrid-functions.md) y [**glEvalMesh**](glevalmesh-functions.md) en tándem para generar y evaluar eficazmente una serie de valores de dominio de mapa con espaciado uniforme.</span><span class="sxs-lookup"><span data-stu-id="55a38-130">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="55a38-131">La función **glEvalMesh** se recorre a través del dominio entero de una cuadrícula de una o dos dimensiones, cuyo intervalo es el dominio de las asignaciones de evaluación especificadas por [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="55a38-131">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="55a38-132">El parámetro Mode determina si los vértices resultantes se conectan como puntos, líneas o polígonos rellenos.</span><span class="sxs-lookup"><span data-stu-id="55a38-132">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="55a38-133">En el caso bidimensional, **glEvalMesh2**, Let</span><span class="sxs-lookup"><span data-stu-id="55a38-133">In the two-dimensional case, **glEvalMesh2**, let</span></span>

<span data-ttu-id="55a38-134">?</span><span class="sxs-lookup"><span data-stu-id="55a38-134">?</span></span> <span data-ttu-id="55a38-135">u = (U2 U1)/n</span><span class="sxs-lookup"><span data-stu-id="55a38-135">u = (u2 u1)/n</span></span>

<span data-ttu-id="55a38-136">?</span><span class="sxs-lookup"><span data-stu-id="55a38-136">?</span></span> <span data-ttu-id="55a38-137">v = (V2 V1)/m,</span><span class="sxs-lookup"><span data-stu-id="55a38-137">v = (v2 v1)/m,</span></span>

<span data-ttu-id="55a38-138">donde n, U1, U2, m, V1 y V2 son los argumentos de la función [**glMapGrid2**](glmapgrid-functions.md) más reciente.</span><span class="sxs-lookup"><span data-stu-id="55a38-138">where n, u1, u2, m, v1, and v2 are the arguments to the most recent [**glMapGrid2**](glmapgrid-functions.md) function.</span></span> <span data-ttu-id="55a38-139">A continuación, si el *modo* es \_ relleno de contabilidad, **glEvalMesh2** es equivalente a:</span><span class="sxs-lookup"><span data-stu-id="55a38-139">Then, if *mode* is GL\_FILL, **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="55a38-140">para (j = J1; j < J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="55a38-140">for (j = j1; j < j2; j += 1)</span></span>

<span data-ttu-id="55a38-141">{</span><span class="sxs-lookup"><span data-stu-id="55a38-141">{</span></span>

<span data-ttu-id="55a38-142">[**glBegin**](glbegin.md)( \_ banda cuádruple de GL \_ );</span><span class="sxs-lookup"><span data-stu-id="55a38-142">[**glBegin**](glbegin.md)(GL\_QUAD\_STRIP);</span></span>

<span data-ttu-id="55a38-143">para (i = i1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="55a38-143">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="55a38-144">{</span><span class="sxs-lookup"><span data-stu-id="55a38-144">{</span></span>

<span data-ttu-id="55a38-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), j?</span><span class="sxs-lookup"><span data-stu-id="55a38-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , j ?</span></span> <span data-ttu-id="55a38-146">v + v1);</span><span class="sxs-lookup"><span data-stu-id="55a38-146">v + v1);</span></span>

<span data-ttu-id="55a38-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), (j + 1)?</span><span class="sxs-lookup"><span data-stu-id="55a38-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , (j+1) ?</span></span> <span data-ttu-id="55a38-148">v + v1);</span><span class="sxs-lookup"><span data-stu-id="55a38-148">v + v1);</span></span>

<span data-ttu-id="55a38-149">}</span><span class="sxs-lookup"><span data-stu-id="55a38-149">}</span></span>

<span data-ttu-id="55a38-150">[**glEnd**](glend.md)(); }</span><span class="sxs-lookup"><span data-stu-id="55a38-150">[**glEnd**](glend.md)( ); }</span></span>

<span data-ttu-id="55a38-151">Si el *modo* es \_ línea de contabilidad, una llamada a **glEvalMesh2** es equivalente a:</span><span class="sxs-lookup"><span data-stu-id="55a38-151">If *mode* is GL\_LINE, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="55a38-152">para (j = J1; j <= J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="55a38-152">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="55a38-153">{</span><span class="sxs-lookup"><span data-stu-id="55a38-153">{</span></span>

<span data-ttu-id="55a38-154">[**glBegin**](glbegin.md)(franja de línea de contabilidad \_ \_ );</span><span class="sxs-lookup"><span data-stu-id="55a38-154">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="55a38-155">para (i = i1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="55a38-155">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="55a38-156">{</span><span class="sxs-lookup"><span data-stu-id="55a38-156">{</span></span>

<span data-ttu-id="55a38-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="55a38-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="55a38-158">}</span><span class="sxs-lookup"><span data-stu-id="55a38-158">}</span></span>

<span data-ttu-id="55a38-159">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="55a38-159">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="55a38-160">}</span><span class="sxs-lookup"><span data-stu-id="55a38-160">}</span></span>

<span data-ttu-id="55a38-161">para (i = i1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="55a38-161">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="55a38-162">{</span><span class="sxs-lookup"><span data-stu-id="55a38-162">{</span></span>

<span data-ttu-id="55a38-163">[**glBegin**](glbegin.md)(franja de línea de contabilidad \_ \_ );</span><span class="sxs-lookup"><span data-stu-id="55a38-163">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="55a38-164">para (j = J1; j <= J1; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="55a38-164">for (j = j1; j <= j1; j += 1)</span></span>

<span data-ttu-id="55a38-165">{</span><span class="sxs-lookup"><span data-stu-id="55a38-165">{</span></span>

<span data-ttu-id="55a38-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="55a38-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="55a38-167">}</span><span class="sxs-lookup"><span data-stu-id="55a38-167">}</span></span>

<span data-ttu-id="55a38-168">glEnd( );</span><span class="sxs-lookup"><span data-stu-id="55a38-168">glEnd( );</span></span>

<span data-ttu-id="55a38-169">}</span><span class="sxs-lookup"><span data-stu-id="55a38-169">}</span></span>

<span data-ttu-id="55a38-170">Y, por último, si el *modo* es \_ el punto de contabilidad, una llamada a **glEvalMesh2** es equivalente a:</span><span class="sxs-lookup"><span data-stu-id="55a38-170">And finally, if *mode* is GL\_POINT, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="55a38-171">[**glBegin**](glbegin.md)(puntos de contabilidad \_ );</span><span class="sxs-lookup"><span data-stu-id="55a38-171">[**glBegin**](glbegin.md)(GL\_POINTS);</span></span>

<span data-ttu-id="55a38-172">para (j = J1; j <= J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="55a38-172">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="55a38-173">{</span><span class="sxs-lookup"><span data-stu-id="55a38-173">{</span></span>

<span data-ttu-id="55a38-174">para (i = i1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="55a38-174">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="55a38-175">{</span><span class="sxs-lookup"><span data-stu-id="55a38-175">{</span></span>

<span data-ttu-id="55a38-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="55a38-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="55a38-177">}</span><span class="sxs-lookup"><span data-stu-id="55a38-177">}</span></span>

<span data-ttu-id="55a38-178">}</span><span class="sxs-lookup"><span data-stu-id="55a38-178">}</span></span>

<span data-ttu-id="55a38-179">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="55a38-179">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="55a38-180">En los tres casos, los únicos requisitos numéricos absolutos son que si i = n, el valor calculado desde i? u + U1 es exactamente U2 y, si j = m, el valor calculado a partir de j? v + v1 es exactamente V2.</span><span class="sxs-lookup"><span data-stu-id="55a38-180">In all three cases, the only absolute numeric requirements are that if i = n, then the value computed from i? u + u1 is exactly u2, and if j = m, then the value computed from j? v + v1 is exactly v2.</span></span> <span data-ttu-id="55a38-181">Las siguientes funciones recuperan información relacionada con **glEvalMesh**:</span><span class="sxs-lookup"><span data-stu-id="55a38-181">The following functions retrieve information relating to **glEvalMesh**:</span></span>

<span data-ttu-id="55a38-182">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="55a38-182">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="55a38-183">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP2 ( \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="55a38-183">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="55a38-184">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP1 \_ segmentos de cuadrícula de GL \_</span><span class="sxs-lookup"><span data-stu-id="55a38-184">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="55a38-185">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP2 ( \_ segmentos de cuadrícula de GL \_</span><span class="sxs-lookup"><span data-stu-id="55a38-185">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="55a38-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55a38-186">Requirements</span></span>



| <span data-ttu-id="55a38-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="55a38-187">Requirement</span></span> | <span data-ttu-id="55a38-188">Value</span><span class="sxs-lookup"><span data-stu-id="55a38-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55a38-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55a38-189">Minimum supported client</span></span><br/> | <span data-ttu-id="55a38-190">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="55a38-190">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="55a38-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55a38-191">Minimum supported server</span></span><br/> | <span data-ttu-id="55a38-192">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55a38-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55a38-193">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55a38-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="55a38-194"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="55a38-194"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="55a38-195">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55a38-195">Library</span></span><br/>                  | <dl> <span data-ttu-id="55a38-196"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55a38-196"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="55a38-197">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55a38-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55a38-198"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a38-198"><dt>Opengl32.dll</dt></span></span> </dl> |



 

 





