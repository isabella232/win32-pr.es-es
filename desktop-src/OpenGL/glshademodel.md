---
title: función glShadeModel (GL. h)
description: La función glShadeModel selecciona el sombreado plano o suave.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- glShadeModel (función) OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676715"
---
# <a name="glshademodel-function"></a><span data-ttu-id="9be54-104">glShadeModel función)</span><span class="sxs-lookup"><span data-stu-id="9be54-104">glShadeModel function</span></span>

<span data-ttu-id="9be54-105">La función **glShadeModel** selecciona el sombreado plano o suave.</span><span class="sxs-lookup"><span data-stu-id="9be54-105">The **glShadeModel** function selects flat or smooth shading.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be54-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9be54-106">Syntax</span></span>


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="9be54-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9be54-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9be54-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="9be54-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="9be54-109">Un valor simbólico que representa una técnica de sombreado.</span><span class="sxs-lookup"><span data-stu-id="9be54-109">A symbolic value representing a shading technique.</span></span> <span data-ttu-id="9be54-110">Los valores aceptados son contabilidad \_ plana y contabilidad \_ suave.</span><span class="sxs-lookup"><span data-stu-id="9be54-110">Accepted values are GL\_FLAT and GL\_SMOOTH.</span></span> <span data-ttu-id="9be54-111">El valor predeterminado es GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="9be54-111">The default is GL\_SMOOTH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9be54-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9be54-112">Return value</span></span>

<span data-ttu-id="9be54-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9be54-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9be54-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9be54-114">Error codes</span></span>

<span data-ttu-id="9be54-115">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="9be54-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9be54-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9be54-116">Name</span></span>                                                                                                  | <span data-ttu-id="9be54-117">Significado</span><span class="sxs-lookup"><span data-stu-id="9be54-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9be54-118"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9be54-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9be54-119">el *modo* era un valor distinto de GL \_ Glat o GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="9be54-119">*mode* was a value other than GL\_GLAT or GL\_SMOOTH.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="9be54-120"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9be54-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9be54-121">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9be54-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9be54-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9be54-122">Remarks</span></span>

<span data-ttu-id="9be54-123">Los primitivos de OpenGL pueden tener un sombreado plano o suave.</span><span class="sxs-lookup"><span data-stu-id="9be54-123">OpenGL primitives can have either flat or smooth shading.</span></span> <span data-ttu-id="9be54-124">El sombreado suave, el valor predeterminado, hace que los colores calculados de los vértices se interpolen a medida que se rasteriza la primitiva, normalmente asignando distintos colores a cada fragmento de píxel resultante.</span><span class="sxs-lookup"><span data-stu-id="9be54-124">Smooth shading, the default, causes the computed colors of vertices to be interpolated as the primitive is rasterized, typically assigning different colors to each resulting pixel fragment.</span></span> <span data-ttu-id="9be54-125">El sombreado plano selecciona el color calculado de un solo vértice y lo asigna a todos los fragmentos de píxeles generados mediante la rasterización de un solo primitivo.</span><span class="sxs-lookup"><span data-stu-id="9be54-125">Flat shading selects the computed color of just one vertex and assigns it to all the pixel fragments generated by rasterizing a single primitive.</span></span> <span data-ttu-id="9be54-126">En cualquier caso, el color calculado de un vértice es el resultado de la iluminación, si está habilitada la iluminación o es el color actual en el momento en que se especificó el vértice, si la iluminación está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="9be54-126">In either case, the computed color of a vertex is the result of lighting, if lighting is enabled, or it is the current color at the time the vertex was specified, if lighting is disabled.</span></span>

<span data-ttu-id="9be54-127">No se distinguen los sombreados planos y suaves en los puntos.</span><span class="sxs-lookup"><span data-stu-id="9be54-127">Flat and smooth shading are indistinguishable for points.</span></span> <span data-ttu-id="9be54-128">Contando los vértices y los primitivos de uno, a partir del momento en que se emite [**glBegin**](glbegin.md) , cada segmento de línea con sombra plana *i* recibe el color calculado del vértice *i* + 1, su segundo vértice.</span><span class="sxs-lookup"><span data-stu-id="9be54-128">Counting vertices and primitives from one, starting when [**glBegin**](glbegin.md) is issued, each flat-shaded line segment *i* is given the computed color of vertex *i* + 1, its second vertex.</span></span> <span data-ttu-id="9be54-129">Contando de forma similar a una, cada polígono con sombra plana recibe el color calculado del vértice mostrado en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9be54-129">Counting similarly from one, each flat-shaded polygon is given the computed color of the vertex listed in the following table.</span></span> <span data-ttu-id="9be54-130">Este es el último vértice para especificar el polígono en todos los casos excepto en polígonos únicos, donde el primer vértice especifica el color de sombra plana.</span><span class="sxs-lookup"><span data-stu-id="9be54-130">This is the last vertex to specify the polygon in all cases except single polygons, where the first vertex specifies the flat-shaded color.</span></span>



| <span data-ttu-id="9be54-131">Tipo primitivo de Polygon i</span><span class="sxs-lookup"><span data-stu-id="9be54-131">Primitive type of polygon i</span></span> | <span data-ttu-id="9be54-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="9be54-132">Vertex</span></span>   |
|-----------------------------|----------|
| <span data-ttu-id="9be54-133">Un solo Polígono (*I*= 1)</span><span class="sxs-lookup"><span data-stu-id="9be54-133">Single polygon (*I*=1)</span></span>      | <span data-ttu-id="9be54-134">1</span><span class="sxs-lookup"><span data-stu-id="9be54-134">1</span></span>        |
| <span data-ttu-id="9be54-135">Franja de triángulo</span><span class="sxs-lookup"><span data-stu-id="9be54-135">Triangle strip</span></span>              | <span data-ttu-id="9be54-136">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="9be54-136">*i* + 2</span></span>  |
| <span data-ttu-id="9be54-137">Ventilador de triángulo</span><span class="sxs-lookup"><span data-stu-id="9be54-137">Triangle fan</span></span>                | <span data-ttu-id="9be54-138">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="9be54-138">*i* + 2</span></span>  |
| <span data-ttu-id="9be54-139">Triángulo independiente</span><span class="sxs-lookup"><span data-stu-id="9be54-139">Independent triangle</span></span>        | <span data-ttu-id="9be54-140">3 *I*</span><span class="sxs-lookup"><span data-stu-id="9be54-140">3 *I*</span></span>     |
| <span data-ttu-id="9be54-141">Banda cuádruple</span><span class="sxs-lookup"><span data-stu-id="9be54-141">Quad strip</span></span>                  | <span data-ttu-id="9be54-142">2 *i* + 2</span><span class="sxs-lookup"><span data-stu-id="9be54-142">2 *i* + 2</span></span> |
| <span data-ttu-id="9be54-143">Cuádruple independiente</span><span class="sxs-lookup"><span data-stu-id="9be54-143">Independent quad</span></span>            | <span data-ttu-id="9be54-144">4 *I*</span><span class="sxs-lookup"><span data-stu-id="9be54-144">4 *I*</span></span>     |



 

<span data-ttu-id="9be54-145">Los sombreados planos y suaves se especifican mediante **glShadeModel** con el *modo* establecido en GL \_ plano y GL \_ Smooth, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9be54-145">Flat and smooth shading are specified by **glShadeModel** with *mode* set to GL\_FLAT and GL\_SMOOTH, respectively.</span></span>

<span data-ttu-id="9be54-146">La siguiente función recupera información relacionada con **glShadeModel**:</span><span class="sxs-lookup"><span data-stu-id="9be54-146">The following function retrieves information related to **glShadeModel**:</span></span>

<span data-ttu-id="9be54-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ modelo de SOMBREAdo de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="9be54-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SHADE\_MODEL</span></span>

## <a name="requirements"></a><span data-ttu-id="9be54-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9be54-148">Requirements</span></span>



| <span data-ttu-id="9be54-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="9be54-149">Requirement</span></span> | <span data-ttu-id="9be54-150">Value</span><span class="sxs-lookup"><span data-stu-id="9be54-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9be54-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9be54-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9be54-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9be54-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9be54-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9be54-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9be54-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9be54-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9be54-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9be54-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="9be54-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9be54-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9be54-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9be54-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="9be54-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9be54-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9be54-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9be54-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9be54-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9be54-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9be54-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="9be54-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be54-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9be54-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9be54-163">**glColor**</span><span class="sxs-lookup"><span data-stu-id="9be54-163">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="9be54-164">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9be54-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9be54-165">**glLight**</span><span class="sxs-lookup"><span data-stu-id="9be54-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="9be54-166">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="9be54-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





