---
title: función glBegin (GL. h)
description: Las funciones glBegin y glend delimitan los vértices de un primitivo o un grupo de primitivos similares. | función glBegin (GL. h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- glBegin (función) OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003638"
---
# <a name="glbegin-function"></a><span data-ttu-id="ef54a-105">glBegin función)</span><span class="sxs-lookup"><span data-stu-id="ef54a-105">glBegin function</span></span>

<span data-ttu-id="ef54a-106">Las funciones **glBegin** y [**glend**](glend.md) delimitan los vértices de un primitivo o un grupo de primitivos similares.</span><span class="sxs-lookup"><span data-stu-id="ef54a-106">The **glBegin** and [**glend**](glend.md) functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef54a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef54a-107">Syntax</span></span>


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="ef54a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef54a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef54a-109">*mode*</span><span class="sxs-lookup"><span data-stu-id="ef54a-109">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="ef54a-110">Primitivas o primitivas que se crearán a partir de los vértices presentados entre **glBegin** y los [**glend**](glend.md)posteriores.</span><span class="sxs-lookup"><span data-stu-id="ef54a-110">The primitive or primitives that will be created from vertices presented between **glBegin** and the subsequent [**glend**](glend.md).</span></span> <span data-ttu-id="ef54a-111">A continuación se indican las constantes simbólicas aceptadas y su significado:</span><span class="sxs-lookup"><span data-stu-id="ef54a-111">The following are accepted symbolic constants and their meanings:</span></span>



| <span data-ttu-id="ef54a-112">Value</span><span class="sxs-lookup"><span data-stu-id="ef54a-112">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="ef54a-113">Significado</span><span class="sxs-lookup"><span data-stu-id="ef54a-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <span data-ttu-id="ef54a-114"><dt>**puntos de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-114"><dt>**GL\_POINTS**</dt></span></span> </dl>                          | <span data-ttu-id="ef54a-115">Trata cada vértice como un único punto.</span><span class="sxs-lookup"><span data-stu-id="ef54a-115">Treats each vertex as a single point.</span></span> <span data-ttu-id="ef54a-116">El vértice *n* define el punto *n*.</span><span class="sxs-lookup"><span data-stu-id="ef54a-116">Vertex *n* defines point *n*.</span></span> <span data-ttu-id="ef54a-117">Se dibujan *N* puntos.</span><span class="sxs-lookup"><span data-stu-id="ef54a-117">*N* points are drawn.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <span data-ttu-id="ef54a-118"><dt>**líneas de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-118"><dt>**GL\_LINES**</dt></span></span> </dl>                             | <span data-ttu-id="ef54a-119">Trata cada par de vértices como un segmento de línea independiente.</span><span class="sxs-lookup"><span data-stu-id="ef54a-119">Treats each pair of vertices as an independent line segment.</span></span> <span data-ttu-id="ef54a-120">Los vértices *2N-1* y *2N* definen la línea *n*.</span><span class="sxs-lookup"><span data-stu-id="ef54a-120">Vertices *2n - 1* and *2n* define line *n*.</span></span> <span data-ttu-id="ef54a-121">Se dibujan *N/2* líneas.</span><span class="sxs-lookup"><span data-stu-id="ef54a-121">*N/2* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <span data-ttu-id="ef54a-122"><dt>**\_franja de línea de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-122"><dt>**GL\_LINE\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="ef54a-123">Dibuja un grupo conectado de segmentos de línea desde el primer vértice hasta el último.</span><span class="sxs-lookup"><span data-stu-id="ef54a-123">Draws a connected group of line segments from the first vertex to the last.</span></span> <span data-ttu-id="ef54a-124">Los vértices *n* y *n + 1* definen la línea *n*.</span><span class="sxs-lookup"><span data-stu-id="ef54a-124">Vertices *n* and *n+1* define line *n*.</span></span> <span data-ttu-id="ef54a-125">Se dibujan *N-1* líneas.</span><span class="sxs-lookup"><span data-stu-id="ef54a-125">*N - 1* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <span data-ttu-id="ef54a-126"><dt>**\_bucle de línea de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-126"><dt>**GL\_LINE\_LOOP**</dt></span></span> </dl>                | <span data-ttu-id="ef54a-127">Dibuja un grupo conectado de segmentos de línea desde el primer vértice hasta el último y después vuelve al primer.</span><span class="sxs-lookup"><span data-stu-id="ef54a-127">Draws a connected group of line segments from the first vertex to the last, then back to the first.</span></span> <span data-ttu-id="ef54a-128">Los vértices *n* y *n + 1* definen la línea *n*.</span><span class="sxs-lookup"><span data-stu-id="ef54a-128">Vertices *n* and *n + 1* define line *n*.</span></span> <span data-ttu-id="ef54a-129">La última línea, sin embargo, se define mediante los vértices *N* y *1*.</span><span class="sxs-lookup"><span data-stu-id="ef54a-129">The last line, however, is defined by vertices *N* and *1*.</span></span> <span data-ttu-id="ef54a-130">Se dibujan *N* líneas.</span><span class="sxs-lookup"><span data-stu-id="ef54a-130">*N* lines are drawn.</span></span><br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <span data-ttu-id="ef54a-131"><dt>**triángulos de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-131"><dt>**GL\_TRIANGLES**</dt></span></span> </dl>                 | <span data-ttu-id="ef54a-132">Trata cada tríptico de los vértices como un triángulo independiente.</span><span class="sxs-lookup"><span data-stu-id="ef54a-132">Treats each triplet of vertices as an independent triangle.</span></span> <span data-ttu-id="ef54a-133">Los vértices *3N-2*, *3N-1* y *3N* definen el triángulo *n*.</span><span class="sxs-lookup"><span data-stu-id="ef54a-133">Vertices *3n - 2*, *3n - 1*, and *3n* define triangle *n*.</span></span> <span data-ttu-id="ef54a-134">Se dibujan los triángulos *N/3* .</span><span class="sxs-lookup"><span data-stu-id="ef54a-134">*N/3* triangles are drawn.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <span data-ttu-id="ef54a-135"><dt>**\_franja de triángulo de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-135"><dt>**GL\_TRIANGLE\_STRIP**</dt></span></span> </dl> | <span data-ttu-id="ef54a-136">Dibuja un grupo de triángulos conectado.</span><span class="sxs-lookup"><span data-stu-id="ef54a-136">Draws a connected group of triangles.</span></span> <span data-ttu-id="ef54a-137">Se define un triángulo para cada vértice presentado después de los dos primeros vértices.</span><span class="sxs-lookup"><span data-stu-id="ef54a-137">One triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="ef54a-138">Para *n* impar, los vértices *n*, *n + 1* y *n + 2* definen el triángulo *n*.</span><span class="sxs-lookup"><span data-stu-id="ef54a-138">For odd *n*, vertices *n*, *n + 1*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="ef54a-139">Para incluso *n*, los vértices *n + 1*, *n* y *n + 2* definen el triángulo *n*.</span><span class="sxs-lookup"><span data-stu-id="ef54a-139">For even *n*, vertices *n + 1*, *n*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="ef54a-140">Se dibujan los triángulos *N-2* .</span><span class="sxs-lookup"><span data-stu-id="ef54a-140">*N - 2* triangles are drawn.</span></span><br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <span data-ttu-id="ef54a-141"><dt>**\_ventilador de triángulo GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-141"><dt>**GL\_TRIANGLE\_FAN**</dt></span></span> </dl>       | <span data-ttu-id="ef54a-142">Dibuja un grupo de triángulos conectado.</span><span class="sxs-lookup"><span data-stu-id="ef54a-142">Draws a connected group of triangles.</span></span> <span data-ttu-id="ef54a-143">se define un triángulo para cada vértice presentado después de los dos primeros vértices.</span><span class="sxs-lookup"><span data-stu-id="ef54a-143">one triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="ef54a-144">Los vértices *1*, *n + 1*, *n + 2* definen el triángulo *n*.</span><span class="sxs-lookup"><span data-stu-id="ef54a-144">Vertices *1*, *n + 1*, *n + 2* define triangle *n*.</span></span> <span data-ttu-id="ef54a-145">Se dibujan los triángulos *N-2* .</span><span class="sxs-lookup"><span data-stu-id="ef54a-145">*N - 2* triangles are drawn.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <span data-ttu-id="ef54a-146"><dt>**\_cuádruples de GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-146"><dt>**GL\_QUADS**</dt></span></span> </dl>                             | <span data-ttu-id="ef54a-147">Trata cada grupo de cuatro vértices como un cuadrangular independiente.</span><span class="sxs-lookup"><span data-stu-id="ef54a-147">Treats each group of four vertices as an independent quadrilateral.</span></span> <span data-ttu-id="ef54a-148">Los vértices *4N-3*, *4N-2*, *4N-1* y *4N* definen cuadrangular *n*.</span><span class="sxs-lookup"><span data-stu-id="ef54a-148">Vertices *4n - 3*, *4n - 2*, *4n - 1*, and *4n* define quadrilateral *n*.</span></span> <span data-ttu-id="ef54a-149">Se dibujan *N/4* quadrilaterals.</span><span class="sxs-lookup"><span data-stu-id="ef54a-149">*N/4* quadrilaterals are drawn.</span></span><br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <span data-ttu-id="ef54a-150"><dt>**\_banda cuádruple de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-150"><dt>**GL\_QUAD\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="ef54a-151">Dibuja un grupo conectado de quadrilaterals.</span><span class="sxs-lookup"><span data-stu-id="ef54a-151">Draws a connected group of quadrilaterals.</span></span> <span data-ttu-id="ef54a-152">Se define un cuadrangular para cada par de vértices presentados después del primer par.</span><span class="sxs-lookup"><span data-stu-id="ef54a-152">One quadrilateral is defined for each pair of vertices presented after the first pair.</span></span> <span data-ttu-id="ef54a-153">Los vértices *2N-1*, *2N*, *2N + 2* y *2N + 1* definen cuadrangular *n*.</span><span class="sxs-lookup"><span data-stu-id="ef54a-153">Vertices *2n - 1*, *2n*, *2n + 2*, and *2n + 1* define quadrilateral *n*.</span></span> <span data-ttu-id="ef54a-154">*N/2-1* quadrilaterals se dibujan.</span><span class="sxs-lookup"><span data-stu-id="ef54a-154">*N/2 - 1* quadrilaterals are drawn.</span></span> <span data-ttu-id="ef54a-155">Tenga en cuenta que el orden en que se usan los vértices para construir un cuadrangular a partir de datos de franja es diferente del que se usa con datos independientes.</span><span class="sxs-lookup"><span data-stu-id="ef54a-155">Note that the order in which vertices are used to construct a quadrilateral from strip data is different from that used with independent data.</span></span><br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <span data-ttu-id="ef54a-156"><dt>**Polígono de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-156"><dt>**GL\_POLYGON**</dt></span></span> </dl>                       | <span data-ttu-id="ef54a-157">Dibuja un solo polígono convexo.</span><span class="sxs-lookup"><span data-stu-id="ef54a-157">Draws a single, convex polygon.</span></span> <span data-ttu-id="ef54a-158">Los vértices *1* a *N* definen este polígono.</span><span class="sxs-lookup"><span data-stu-id="ef54a-158">Vertices *1* through *N* define this polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef54a-159">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef54a-159">Return value</span></span>

<span data-ttu-id="ef54a-160">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ef54a-160">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ef54a-161">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ef54a-161">Error codes</span></span>

<span data-ttu-id="ef54a-162">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="ef54a-162">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ef54a-163">Nombre</span><span class="sxs-lookup"><span data-stu-id="ef54a-163">Name</span></span>                                                                                                  | <span data-ttu-id="ef54a-164">Significado</span><span class="sxs-lookup"><span data-stu-id="ef54a-164">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef54a-165"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-165"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ef54a-166">el *modo* se estableció en un valor no aceptado.</span><span class="sxs-lookup"><span data-stu-id="ef54a-166">*mode* was set to an unaccepted value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="ef54a-167"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-167"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ef54a-168">Se llamó a una función que no sea [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md)o [**glCallLists**](glcalllists.md) entre **glBegin** y el [**glend**](glend.md)correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ef54a-168">A function other than [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md), or [**glCallLists**](glcalllists.md) was called between **glBegin** and the corresponding [**glend**](glend.md).</span></span> <span data-ttu-id="ef54a-169">Se llamó a la función **glend** antes de que se llamara al **glBegin** correspondiente, o bien se llamó a **glBegin** dentro de una secuencia **glBegin** / **glend** .</span><span class="sxs-lookup"><span data-stu-id="ef54a-169">The function **glend** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glend** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="ef54a-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef54a-170">Remarks</span></span>

<span data-ttu-id="ef54a-171">Las funciones **glBegin** y [**glend**](glend.md) delimitan los vértices que definen un primitivo o un grupo de primitivos similares.</span><span class="sxs-lookup"><span data-stu-id="ef54a-171">The **glBegin** and [**glend**](glend.md) functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="ef54a-172">La función **glBegin** acepta un solo argumento que especifica los diez primitivos que componen los vértices.</span><span class="sxs-lookup"><span data-stu-id="ef54a-172">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="ef54a-173">Tomando *n* como un recuento entero a partir de uno, y *n* como el número total de vértices especificado, las interpretaciones son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="ef54a-173">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="ef54a-174">Solo se puede usar un subconjunto de funciones de OpenGL entre **glBegin** y [**glend**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ef54a-174">You can use only a subset of OpenGL functions between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="ef54a-175">Las funciones que puede usar son:</span><span class="sxs-lookup"><span data-stu-id="ef54a-175">The functions you can use are:</span></span>

    [<span data-ttu-id="ef54a-176">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="ef54a-176">**glVertex**</span></span>](glvertex-functions.md)

     

    [<span data-ttu-id="ef54a-177">**glColor**</span><span class="sxs-lookup"><span data-stu-id="ef54a-177">**glColor**</span></span>](glcolor-functions.md)

     

    [<span data-ttu-id="ef54a-178">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="ef54a-178">**glIndex**</span></span>](glindex-functions.md)

     

    [<span data-ttu-id="ef54a-179">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="ef54a-179">**glNormal**</span></span>](glnormal-functions.md)

     

    [<span data-ttu-id="ef54a-180">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="ef54a-180">**glTexCoord**</span></span>](gltexcoord-functions.md)

     

    [<span data-ttu-id="ef54a-181">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="ef54a-181">**glEvalCoord**</span></span>](glevalcoord-functions.md)

     

    [<span data-ttu-id="ef54a-182">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="ef54a-182">**glEvalPoint**</span></span>](glevalpoint.md)

     

    [<span data-ttu-id="ef54a-183">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="ef54a-183">**glMaterial**</span></span>](glmaterial-functions.md)

     

    [<span data-ttu-id="ef54a-184">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="ef54a-184">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="ef54a-185">También puede usar [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) para ejecutar listas de presentación que incluyen solo las funciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="ef54a-185">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="ef54a-186">Si se llama a cualquier otra función de OpenGL entre **glBegin** y [**glend**](glend.md), se establece la marca de error y se omite la función.</span><span class="sxs-lookup"><span data-stu-id="ef54a-186">If any other OpenGL function is called between **glBegin** and [**glend**](glend.md), the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="ef54a-187">Independientemente del valor elegido para el *modo* en **glBegin**, no hay ningún límite en el número de vértices que puede definir entre **glBegin** y [**glend**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ef54a-187">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="ef54a-188">No se dibujan líneas, triángulos, quadrilaterals ni polígonos que se hayan especificado de una vez incompleta.</span><span class="sxs-lookup"><span data-stu-id="ef54a-188">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="ef54a-189">Resultados de especificación incompletos cuando se proporcionan muy pocos vértices para especificar incluso un único primitivo o cuando se especifica un múltiplo incorrecto de vértices.</span><span class="sxs-lookup"><span data-stu-id="ef54a-189">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="ef54a-190">Se omite el primitivo incompleto; se dibujan los primitivos completos.</span><span class="sxs-lookup"><span data-stu-id="ef54a-190">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="ef54a-191">La especificación mínima de los vértices para cada primitiva es:</span><span class="sxs-lookup"><span data-stu-id="ef54a-191">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="ef54a-192">Número mínimo de vértices</span><span class="sxs-lookup"><span data-stu-id="ef54a-192">Minimum number of vertices</span></span> | <span data-ttu-id="ef54a-193">Tipo de primitivo</span><span class="sxs-lookup"><span data-stu-id="ef54a-193">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="ef54a-194">1</span><span class="sxs-lookup"><span data-stu-id="ef54a-194">1</span></span>                          | <span data-ttu-id="ef54a-195">point</span><span class="sxs-lookup"><span data-stu-id="ef54a-195">point</span></span>             |
    | <span data-ttu-id="ef54a-196">2</span><span class="sxs-lookup"><span data-stu-id="ef54a-196">2</span></span>                          | <span data-ttu-id="ef54a-197">line</span><span class="sxs-lookup"><span data-stu-id="ef54a-197">line</span></span>              |
    | <span data-ttu-id="ef54a-198">3</span><span class="sxs-lookup"><span data-stu-id="ef54a-198">3</span></span>                          | <span data-ttu-id="ef54a-199">triangle</span><span class="sxs-lookup"><span data-stu-id="ef54a-199">triangle</span></span>          |
    | <span data-ttu-id="ef54a-200">4</span><span class="sxs-lookup"><span data-stu-id="ef54a-200">4</span></span>                          | <span data-ttu-id="ef54a-201">cuadrangular</span><span class="sxs-lookup"><span data-stu-id="ef54a-201">quadrilateral</span></span>     |
    | <span data-ttu-id="ef54a-202">3</span><span class="sxs-lookup"><span data-stu-id="ef54a-202">3</span></span>                          | <span data-ttu-id="ef54a-203">polygon</span><span class="sxs-lookup"><span data-stu-id="ef54a-203">polygon</span></span>           |

    

     

-   <span data-ttu-id="ef54a-204">Los modos que requieren un determinado múltiplo de vértices son \_ las líneas de libro de contabilidad (2), los \_ triángulos de contabilidad (3), los \_ cuatro cuádruples (4) y la \_ franja cuádruple de GL \_ (2).</span><span class="sxs-lookup"><span data-stu-id="ef54a-204">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef54a-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef54a-205">Requirements</span></span>



| <span data-ttu-id="ef54a-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef54a-206">Requirement</span></span> | <span data-ttu-id="ef54a-207">Value</span><span class="sxs-lookup"><span data-stu-id="ef54a-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef54a-208">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef54a-208">Minimum supported client</span></span><br/> | <span data-ttu-id="ef54a-209">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ef54a-209">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ef54a-210">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef54a-210">Minimum supported server</span></span><br/> | <span data-ttu-id="ef54a-211">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef54a-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef54a-212">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef54a-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef54a-213"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-213"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ef54a-214">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef54a-214">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef54a-215"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-215"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ef54a-216">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef54a-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef54a-217"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef54a-217"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef54a-218">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef54a-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef54a-219">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="ef54a-219">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="ef54a-220">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="ef54a-220">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="ef54a-221">**glColor**</span><span class="sxs-lookup"><span data-stu-id="ef54a-221">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="ef54a-222">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="ef54a-222">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="ef54a-223">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ef54a-223">**glEnd**</span></span>](/windows/desktop/OpenGL/glend)
</dt> <dt>

[<span data-ttu-id="ef54a-224">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="ef54a-224">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="ef54a-225">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="ef54a-225">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="ef54a-226">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="ef54a-226">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="ef54a-227">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="ef54a-227">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="ef54a-228">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="ef54a-228">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="ef54a-229">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="ef54a-229">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="ef54a-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="ef54a-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

