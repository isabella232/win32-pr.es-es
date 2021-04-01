---
title: función gluTessCallback (GLU. h)
description: La función gluTessCallback define una devolución de llamada para un objeto de teselación.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- gluTessCallback (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997000"
---
# <a name="glutesscallback-function"></a><span data-ttu-id="aff51-104">gluTessCallback función)</span><span class="sxs-lookup"><span data-stu-id="aff51-104">gluTessCallback function</span></span>

<span data-ttu-id="aff51-105">La función **gluTessCallback** define una devolución de llamada para un objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="aff51-105">The **gluTessCallback** function defines a callback for a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff51-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aff51-106">Syntax</span></span>


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="aff51-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aff51-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aff51-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="aff51-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="aff51-109">Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="aff51-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="aff51-110">*cuales*</span><span class="sxs-lookup"><span data-stu-id="aff51-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="aff51-111">Devolución de llamada que se está definiendo.</span><span class="sxs-lookup"><span data-stu-id="aff51-111">The callback being defined.</span></span> <span data-ttu-id="aff51-112">Los valores siguientes son válidos: GLU \_ Tess \_ Begin, Glu \_ Tess \_ Begin \_ Data, GLU \_ Tess \_ Edge \_ Flag, Glu \_ Tess \_ Edge \_ Flag \_ Data, Glu \_ Tess \_ Vertex, GLU \_ Tess \_ Vertex \_ Data, Glu \_ Tess \_ End, Glu \_ Tess \_ End \_ Data, Glu \_ Tess \_ combine, Glu \_ Tess \_ combine \_ Data, Glu \_ Tess \_ error y Glu Tess \_ \_ error \_ Data.</span><span class="sxs-lookup"><span data-stu-id="aff51-112">The following values are valid: GLU\_TESS\_BEGIN, GLU\_TESS\_BEGIN\_DATA, GLU\_TESS\_EDGE\_FLAG, GLU\_TESS\_EDGE\_FLAG\_DATA, GLU\_TESS\_VERTEX, GLU\_TESS\_VERTEX\_DATA, GLU\_TESS\_END, GLU\_TESS\_END\_DATA, GLU\_TESS\_COMBINE, GLU\_TESS\_COMBINE\_DATA, GLU\_TESS\_ERROR, and GLU\_TESS\_ERROR\_DATA.</span></span>

<span data-ttu-id="aff51-113">Para obtener más información sobre estas devoluciones de llamada, vea la sección Comentarios siguiente.</span><span class="sxs-lookup"><span data-stu-id="aff51-113">For more information on these callbacks, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="aff51-114">*fn*</span><span class="sxs-lookup"><span data-stu-id="aff51-114">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="aff51-115">Función a la que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="aff51-115">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aff51-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aff51-116">Return value</span></span>

<span data-ttu-id="aff51-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="aff51-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aff51-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aff51-118">Remarks</span></span>

<span data-ttu-id="aff51-119">Use **gluTessCallback** para especificar una devolución de llamada que va a usar un objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="aff51-119">Use **gluTessCallback** to specify a callback to be used by a tessellation object.</span></span> <span data-ttu-id="aff51-120">Si la devolución de llamada especificada ya está definida, se reemplaza.</span><span class="sxs-lookup"><span data-stu-id="aff51-120">If the specified callback is already defined, then it is replaced.</span></span> <span data-ttu-id="aff51-121">Si *FN* es **null**, la devolución de llamada existente queda sin definir.</span><span class="sxs-lookup"><span data-stu-id="aff51-121">If *fn* is **NULL**, then the existing callback becomes undefined.</span></span>

<span data-ttu-id="aff51-122">El objeto de teselación utiliza estas devoluciones de llamada para describir cómo un polígono que se especifica se divide en triángulos.</span><span class="sxs-lookup"><span data-stu-id="aff51-122">The tessellation object uses these callbacks to describe how a polygon that you specify is broken into triangles.</span></span>

<span data-ttu-id="aff51-123">Hay dos versiones de cada devolución de llamada, una con datos de polígono que puede definir y otra sin.</span><span class="sxs-lookup"><span data-stu-id="aff51-123">There are two versions of each callback, one with polygon data that you can define and one without.</span></span> <span data-ttu-id="aff51-124">Si se especifican ambas versiones de una devolución de llamada determinada, se usará la devolución de llamada con los datos de polígono que especifique.</span><span class="sxs-lookup"><span data-stu-id="aff51-124">If both versions of a particular callback are specified, the callback with the polygon data you specify will be used.</span></span> <span data-ttu-id="aff51-125">El parámetro de *\_ datos Polygon* de [**gluTessBeginPolygon**](glutessbeginpolygon.md) es una copia del puntero que se especificó cuando se llamó a **gluTessBeginPolygon** .</span><span class="sxs-lookup"><span data-stu-id="aff51-125">The *polygon\_data* parameter of [**gluTessBeginPolygon**](glutessbeginpolygon.md) is a copy of the pointer that was specified when **gluTessBeginPolygon** was called.</span></span>

<span data-ttu-id="aff51-126">A continuación se indican las devoluciones de llamada válidas:</span><span class="sxs-lookup"><span data-stu-id="aff51-126">The following are valid callbacks:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff51-127">Devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="aff51-127">Callback</span></span></th>
<th><span data-ttu-id="aff51-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="aff51-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aff51-129">GLU_TESS_BEGIN</span><span class="sxs-lookup"><span data-stu-id="aff51-129">GLU_TESS_BEGIN</span></span></td>
<td><span data-ttu-id="aff51-130">La devolución de llamada de GLU_TESS_BEGIN se invoca como <a href="glbegin.md"><strong>glBegin</strong></a> para indicar el inicio de una primitiva (triángulo).</span><span class="sxs-lookup"><span data-stu-id="aff51-130">The GLU_TESS_BEGIN callback is invoked like <a href="glbegin.md"><strong>glBegin</strong></a> to indicate the start of a (triangle) primitive.</span></span> <span data-ttu-id="aff51-131">La función toma un único argumento de tipo <strong>GLenum</strong>.</span><span class="sxs-lookup"><span data-stu-id="aff51-131">The function takes a single argument of type <strong>GLenum</strong>.</span></span> <span data-ttu-id="aff51-132">Si establece la propiedad GLU_TESS_BOUNDARY_ONLY en GL_FALSE, el argumento se establece en GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP o GL_TRIANGLES.</span><span class="sxs-lookup"><span data-stu-id="aff51-132">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_FALSE, the argument is set to either GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP, or GL_TRIANGLES.</span></span> <span data-ttu-id="aff51-133">Si establece la propiedad GLU_TESS_BOUNDARY_ONLY en GL_TRUE, el argumento se establece en GL_LINE_LOOP.</span><span class="sxs-lookup"><span data-stu-id="aff51-133">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_TRUE, the argument is set to GL_LINE_LOOP.</span></span> <span data-ttu-id="aff51-134">El prototipo de función para esta devolución de llamada es el siguiente: <strong>void</strong> <strong>Begin</strong> ( <em>tipo</em><strong>GLenum</strong> );</span><span class="sxs-lookup"><span data-stu-id="aff51-134">The function prototype for this callback is as follows: <strong>void</strong> <strong>begin</strong> (<strong>GLenum</strong> <em>type</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff51-135">GLU_TESS_BEGIN_DATA</span><span class="sxs-lookup"><span data-stu-id="aff51-135">GLU_TESS_BEGIN_DATA</span></span></td>
<td><span data-ttu-id="aff51-136">GLU_TESS_BEGIN_DATA es igual que la devolución de llamada de GLU_TESS_BEGIN, salvo que toma un argumento de puntero adicional.</span><span class="sxs-lookup"><span data-stu-id="aff51-136">GLU_TESS_BEGIN_DATA is the same as the GLU_TESS_BEGIN callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="aff51-137">Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aff51-137">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="aff51-138">El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>beginData</strong> ( <em>tipo</em><strong>GLenum</strong> , <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="aff51-138">The function prototype for this callback is: <strong>void</strong> <strong>beginData</strong> (<strong>GLenum</strong> <em>type</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff51-139">GLU_TESS_EDGE_FLAG</span><span class="sxs-lookup"><span data-stu-id="aff51-139">GLU_TESS_EDGE_FLAG</span></span></td>
<td><span data-ttu-id="aff51-140">La devolución de llamada GLU_TESS_EDGE_FLAG es similar a <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aff51-140">The GLU_TESS_EDGE_FLAG callback is similar to <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>.</span></span> <span data-ttu-id="aff51-141">La función toma una única marca booleana que indica qué bordes se encuentran en el límite del polígono.</span><span class="sxs-lookup"><span data-stu-id="aff51-141">The function takes a single Boolean flag that indicates which edges lie on the polygon boundary.</span></span> <span data-ttu-id="aff51-142">Si la marca es GL_TRUE, cada vértice siguiente comienza un borde que se encuentra en el límite del polígono; es decir, un borde que separa una región interior de una exterior.</span><span class="sxs-lookup"><span data-stu-id="aff51-142">If the flag is GL_TRUE, then each vertex that follows begins an edge that lies on the polygon boundary; that is, an edge which separates an interior region from an exterior one.</span></span> <span data-ttu-id="aff51-143">Si la marca es GL_FALSE, cada vértice siguiente comienza un borde que se encuentra en el interior del polígono.</span><span class="sxs-lookup"><span data-stu-id="aff51-143">If the flag is GL_FALSE, then each vertex that follows begins an edge that lies in the polygon interior.</span></span> <span data-ttu-id="aff51-144">La devolución de llamada de GLU_TESS_EDGE_FLAG (si se define) se invoca antes de que se realice la primera devolución de llamada de vértice.</span><span class="sxs-lookup"><span data-stu-id="aff51-144">The GLU_TESS_EDGE_FLAG callback (if defined) is invoked before the first vertex callback is made.</span></span> <span data-ttu-id="aff51-145">Dado que los ventiladores de triángulo y las tiras de triángulos no admiten marcas de borde, la devolución de llamada de inicio no se llama con GL_TRIANGLE_FAN o GL_TRIANGLE_STRIP si se proporciona una devolución de llamada de marca perimetral.</span><span class="sxs-lookup"><span data-stu-id="aff51-145">Because triangle fans and triangle strips do not support edge flags, the begin callback is not called with GL_TRIANGLE_FAN or GL_TRIANGLE_STRIP if an edge flag callback is provided.</span></span> <span data-ttu-id="aff51-146">En su lugar, los ventiladores y las franjas se convierten en triángulos independientes.</span><span class="sxs-lookup"><span data-stu-id="aff51-146">Instead, the fans and strips are converted to independent triangles.</span></span> <span data-ttu-id="aff51-147">El prototipo de función para esta devolución de llamada es:</span><span class="sxs-lookup"><span data-stu-id="aff51-147">The function prototype for this callback is:</span></span><br/> <span data-ttu-id="aff51-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong></strong> <em>marca</em>GLboolean);</span><span class="sxs-lookup"><span data-stu-id="aff51-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong>GLboolean</strong> <em>flag</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff51-149">GLU_TESS_EDGE_FLAG_DATA</span><span class="sxs-lookup"><span data-stu-id="aff51-149">GLU_TESS_EDGE_FLAG_DATA</span></span></td>
<td><span data-ttu-id="aff51-150">La devolución de llamada de GLU_TESS_EDGE_FLAG_DATA es igual que la devolución de llamada de GLU_TESS_EDGE_FLAG, salvo que toma un argumento de puntero adicional.</span><span class="sxs-lookup"><span data-stu-id="aff51-150">The GLU_TESS_EDGE_FLAG_DATA callback is the same as the GLU_TESS_EDGE_FLAG callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="aff51-151">Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aff51-151">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="aff51-152">El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>edgeFlagData</strong> ( <em>marca</em><strong>GLboolean</strong> , <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="aff51-152">The function prototype for this callback is: <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>flag</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff51-153">GLU_TESS_VERTEX</span><span class="sxs-lookup"><span data-stu-id="aff51-153">GLU_TESS_VERTEX</span></span></td>
<td><span data-ttu-id="aff51-154">Se invoca la devolución de llamada de GLU_TESS_VERTEX entre las devoluciones de llamada Begin y end.</span><span class="sxs-lookup"><span data-stu-id="aff51-154">The GLU_TESS_VERTEX callback is invoked between the begin and end callbacks.</span></span> <span data-ttu-id="aff51-155">Es similar a glVertex y define los vértices de los triángulos creados por el proceso de teselación.</span><span class="sxs-lookup"><span data-stu-id="aff51-155">It is similar to glVertex , and it defines the vertexes of the triangles created by the tessellation process.</span></span> <span data-ttu-id="aff51-156">La función toma un puntero como único argumento.</span><span class="sxs-lookup"><span data-stu-id="aff51-156">The function takes a pointer as its only argument.</span></span> <span data-ttu-id="aff51-157">Este puntero es idéntico al puntero opaco que proporcionó al definir el vértice (vea <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="aff51-157">This pointer is identical to the opaque pointer that you provided when you defined the vertex (see <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>).</span></span> <span data-ttu-id="aff51-158">El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span><span class="sxs-lookup"><span data-stu-id="aff51-158">The function prototype for this callback is: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff51-159">GLU_TESS_VERTEX_DATA</span><span class="sxs-lookup"><span data-stu-id="aff51-159">GLU_TESS_VERTEX_DATA</span></span></td>
<td><span data-ttu-id="aff51-160">La GLU_TESS_VERTEX_DATA es igual que la devolución de llamada de GLU_TESS_VERTEX, salvo que toma un argumento de puntero adicional.</span><span class="sxs-lookup"><span data-stu-id="aff51-160">The GLU_TESS_VERTEX_DATA is the same as the GLU_TESS_VERTEX callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="aff51-161">Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aff51-161">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="aff51-162">El prototipo de función para esta devolución de llamada es: <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="aff51-162">The function prototype for this callback is: <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff51-163">GLU_TESS_END</span><span class="sxs-lookup"><span data-stu-id="aff51-163">GLU_TESS_END</span></span></td>
<td><span data-ttu-id="aff51-164">La devolución de llamada de GLU_TESS_END tiene el mismo propósito que <a href="glend.md"><strong>glEnd</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aff51-164">The GLU_TESS_END callback serves the same purpose as <a href="glend.md"><strong>glEnd</strong></a>.</span></span> <span data-ttu-id="aff51-165">Indica el final de un primitivo y no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="aff51-165">It indicates the end of a primitive, and it takes no arguments.</span></span> <span data-ttu-id="aff51-166">El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>End</strong> (<strong>void</strong>);</span><span class="sxs-lookup"><span data-stu-id="aff51-166">The function prototype for this callback is: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff51-167">GLU_TESS_END_DATA</span><span class="sxs-lookup"><span data-stu-id="aff51-167">GLU_TESS_END_DATA</span></span></td>
<td><span data-ttu-id="aff51-168">La devolución de llamada de GLU_TESS_END_DATA es igual que la devolución de llamada de GLU_TESS_END, salvo que toma un argumento de puntero adicional.</span><span class="sxs-lookup"><span data-stu-id="aff51-168">The GLU_TESS_END_DATA callback is the same as the GLU_TESS_END callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="aff51-169">Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aff51-169">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="aff51-170">El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="aff51-170">The function prototype for this callback is: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff51-171">GLU_TESS_COMBINE</span><span class="sxs-lookup"><span data-stu-id="aff51-171">GLU_TESS_COMBINE</span></span></td>
<td><span data-ttu-id="aff51-172">Llame a la GLU_TESS_COMBINE devolución de llamada para crear un nuevo vértice cuando la teselación detecta una intersección o para combinar características.</span><span class="sxs-lookup"><span data-stu-id="aff51-172">Call the GLU_TESS_COMBINE callback to create a new vertex when the tessellation detects an intersection, or to merge features.</span></span> <span data-ttu-id="aff51-173">La función toma cuatro argumentos: una matriz de tres elementos, cada uno de los cuales es de tipo Gldouble.</span><span class="sxs-lookup"><span data-stu-id="aff51-173">The function takes four arguments: An array of three elements, each of type Gldouble.</span></span><br/> <span data-ttu-id="aff51-174">Matriz de cuatro punteros.</span><span class="sxs-lookup"><span data-stu-id="aff51-174">An array of four pointers.</span></span><br/> <span data-ttu-id="aff51-175">Una matriz de cuatro elementos, cada uno de los cuales es de tipo GLfloat.</span><span class="sxs-lookup"><span data-stu-id="aff51-175">An array of four elements, each of type GLfloat.</span></span><br/> <span data-ttu-id="aff51-176">Puntero a un puntero.</span><span class="sxs-lookup"><span data-stu-id="aff51-176">A pointer to a pointer.</span></span><br/> <span data-ttu-id="aff51-177">El prototipo de función para esta devolución de llamada es:</span><span class="sxs-lookup"><span data-stu-id="aff51-177">The function prototype for this callback is:</span></span> <br/> <span data-ttu-id="aff51-178"><strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>  \*\* <em>outdata</em>);</span><span class="sxs-lookup"><span data-stu-id="aff51-178"><strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>);</span></span><br/> <span data-ttu-id="aff51-179">El vértice se define como una combinación lineal de hasta cuatro vértices existentes, almacenados en vertex_data.</span><span class="sxs-lookup"><span data-stu-id="aff51-179">The vertex is defined as a linear combination of up to four existing vertexes, stored in vertex_data.</span></span> <span data-ttu-id="aff51-180">Los coeficientes de la combinación lineal se proporcionan por peso; Estos pesos siempre suman a 1,0.</span><span class="sxs-lookup"><span data-stu-id="aff51-180">The coefficients of the linear combination are given by weight; these weights always sum to 1.0.</span></span> <span data-ttu-id="aff51-181">Todos los punteros de vértice son válidos aunque algunos de los pesos sean cero.</span><span class="sxs-lookup"><span data-stu-id="aff51-181">All vertex pointers are valid even when some of the weights are zero.</span></span> <span data-ttu-id="aff51-182">El parámetro coords proporciona la ubicación del nuevo vértice.</span><span class="sxs-lookup"><span data-stu-id="aff51-182">The coords parameter gives the location of the new vertex.</span></span><br/> <span data-ttu-id="aff51-183">Asigne otro vértice, interpole los parámetros con vertex_data y peso, y devuelva el nuevo puntero de vértice en outdata.</span><span class="sxs-lookup"><span data-stu-id="aff51-183">Allocate another vertex, interpolate parameters using vertex_data and weight, and return the new vertex pointer in outData.</span></span> <span data-ttu-id="aff51-184">Este identificador se proporciona durante las devoluciones de llamada de representación.</span><span class="sxs-lookup"><span data-stu-id="aff51-184">This handle is supplied during rendering callbacks.</span></span> <span data-ttu-id="aff51-185">Libere memoria después de llamar a <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aff51-185">Free the memory sometime after calling <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.</span></span><br/> <span data-ttu-id="aff51-186">Por ejemplo, si el polígono se encuentra en un plano arbitrario en un espacio tridimensional y asocia un color a cada vértice, la devolución de llamada de GLU_TESS_COMBINE podría ser similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="aff51-186">For example, if the polygon lies in an arbitrary plane in three-dimensional space, and you associate a color with each vertex, the GLU_TESS_COMBINE callback might look like the following:</span></span><br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
<span data-ttu-id="aff51-187">Cuando la teselación detecta una intersección, se debe definir el GLU_TESS_COMBINE o GLU_TESS_COMBINE_DATA devolución de llamada (vea a continuación) y debe escribir un puntero no<strong>nulo</strong> en dataOut.</span><span class="sxs-lookup"><span data-stu-id="aff51-187">When the tessellation detects an intersection, the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback (see below) must be defined, and must write a non-<strong>NULL</strong> pointer into dataOut.</span></span> <span data-ttu-id="aff51-188">En caso contrario, se produce el error GLU_TESS_NEED_COMBINE_CALLBACK y no se genera ninguna salida.</span><span class="sxs-lookup"><span data-stu-id="aff51-188">Otherwise the GLU_TESS_NEED_COMBINE_CALLBACK error occurs, and no output is generated.</span></span> <span data-ttu-id="aff51-189">(Este es el único error que se puede producir durante la representación y la teselación).</span><span class="sxs-lookup"><span data-stu-id="aff51-189">(This is the only error that can occur during tessellation and rendering.)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff51-190">GLU_TESS_COMBINE_DATA</span><span class="sxs-lookup"><span data-stu-id="aff51-190">GLU_TESS_COMBINE_DATA</span></span></td>
<td><span data-ttu-id="aff51-191">La devolución de llamada de GLU_TESS_COMBINE_DATA es igual que la devolución de llamada de GLU_TESS_COMBINE, salvo que toma un argumento de puntero adicional.</span><span class="sxs-lookup"><span data-stu-id="aff51-191">The GLU_TESS_COMBINE_DATA callback is the same as the GLU_TESS_COMBINE callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="aff51-192">Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aff51-192">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="aff51-193">El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \*<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>  \*\* <em>outdata</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="aff51-193">The function prototype for this callback is: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \*<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff51-194">GLU_TESS_ERROR</span><span class="sxs-lookup"><span data-stu-id="aff51-194">GLU_TESS_ERROR</span></span></td>
<td><span data-ttu-id="aff51-195">Se llama a la devolución de llamada de GLU_TESS_ERROR cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="aff51-195">The GLU_TESS_ERROR callback is called when an error is encountered.</span></span> <span data-ttu-id="aff51-196">El único argumento es de tipo <strong>GLenum</strong>; indica el error específico que se ha producido y está establecido en uno de los siguientes: GLU_TESS_MISSING_BEGIN_POLYGON</span><span class="sxs-lookup"><span data-stu-id="aff51-196">The one argument is of type <strong>GLenum</strong>; it indicates the specific error that occurred and is set to one of the following: GLU_TESS_MISSING_BEGIN_POLYGON</span></span><br/> <span data-ttu-id="aff51-197">GLU_TESS_MISSING_END_POLYGON</span><span class="sxs-lookup"><span data-stu-id="aff51-197">GLU_TESS_MISSING_END_POLYGON</span></span><br/> <span data-ttu-id="aff51-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="aff51-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span></span><br/> <span data-ttu-id="aff51-199">GLU_TESS_MISSING_END_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="aff51-199">GLU_TESS_MISSING_END_CONTOUR</span></span><br/> <span data-ttu-id="aff51-200">GLU_TESS_COORD_TOO_LARGE</span><span class="sxs-lookup"><span data-stu-id="aff51-200">GLU_TESS_COORD_TOO_LARGE</span></span><br/> <span data-ttu-id="aff51-201">GLU_TESS_NEED_COMBINE_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="aff51-201">GLU_TESS_NEED_COMBINE_CALLBACK</span></span><br/> <span data-ttu-id="aff51-202">Llame a gluErrorString para recuperar las cadenas de caracteres que describen estos errores.</span><span class="sxs-lookup"><span data-stu-id="aff51-202">Call gluErrorString to retrieve character strings describing these errors.</span></span> <span data-ttu-id="aff51-203">El prototipo de función para esta devolución de llamada es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="aff51-203">The function prototype for this callback is as follows:</span></span><br/> <span data-ttu-id="aff51-204"><strong></strong> <strong>error</strong> void (<strong>GLenum</strong> <em>errno</em>);</span><span class="sxs-lookup"><span data-stu-id="aff51-204"><strong>void</strong> <strong>error</strong> (<strong>GLenum</strong> <em>errno</em>);</span></span><br/> <span data-ttu-id="aff51-205">La biblioteca GLU se recupera de los cuatro primeros errores mediante la inserción de la llamada o llamadas que faltan.</span><span class="sxs-lookup"><span data-stu-id="aff51-205">The GLU library recovers from the first four errors by inserting the missing call or calls.</span></span> <span data-ttu-id="aff51-206">GLU_TESS_COORD_TOO_LARGE indica que alguna coordenada de vértices superó la constante predefinida GLU_TESS_MAX_COORD en el valor absoluto y que el valor se ha fijado.</span><span class="sxs-lookup"><span data-stu-id="aff51-206">GLU_TESS_COORD_TOO_LARGE indicates that some vertex coordinate exceeded the predefined constant GLU_TESS_MAX_COORD in absolute value, and that the value has been clamped.</span></span> <span data-ttu-id="aff51-207">(Los valores de las coordenadas deben ser lo suficientemente pequeños como para multiplicarlos sin desbordamiento). GLU_TESS_NEED_COMBINE_CALLBACK indica que la teselación detectó una intersección entre dos bordes en los datos de entrada y no se proporcionó la devolución de llamada de GLU_TESS_COMBINE o GLU_TESS_COMBINE_DATA.</span><span class="sxs-lookup"><span data-stu-id="aff51-207">(Coordinate values must be small enough that two can be multiplied together without overflow.) GLU_TESS_NEED_COMBINE_CALLBACK indicates that the tessellation detected an intersection between two edges in the input data, and the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback was not provided.</span></span> <span data-ttu-id="aff51-208">No se generará ninguna salida.</span><span class="sxs-lookup"><span data-stu-id="aff51-208">No output will be generated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff51-209">GLU_TESS_ERROR_DATA</span><span class="sxs-lookup"><span data-stu-id="aff51-209">GLU_TESS_ERROR_DATA</span></span></td>
<td><span data-ttu-id="aff51-210">La devolución de llamada de GLU_TESS_ERROR_DATA es igual que la devolución de llamada de GLU_TESS_ERROR, salvo que toma un argumento de puntero adicional.</span><span class="sxs-lookup"><span data-stu-id="aff51-210">The GLU_TESS_ERROR_DATA callback is the same as the GLU_TESS_ERROR callback, except that it takes an additional pointer argument.</span></span> <span data-ttu-id="aff51-211">Este puntero es idéntico al puntero opaco que se proporciona al llamar a <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aff51-211">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="aff51-212">El prototipo de función para esta devolución de llamada es: <strong>void</strong> <strong>datoserror</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="aff51-212">The function prototype for this callback is: <strong>void</strong> <strong>errorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="aff51-213">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aff51-213">Requirements</span></span>



| <span data-ttu-id="aff51-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="aff51-214">Requirement</span></span> | <span data-ttu-id="aff51-215">Value</span><span class="sxs-lookup"><span data-stu-id="aff51-215">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aff51-216">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aff51-216">Minimum supported client</span></span><br/> | <span data-ttu-id="aff51-217">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aff51-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="aff51-218">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aff51-218">Minimum supported server</span></span><br/> | <span data-ttu-id="aff51-219">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aff51-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aff51-220">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aff51-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="aff51-221"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff51-221"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="aff51-222">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aff51-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="aff51-223"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aff51-223"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aff51-224">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aff51-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aff51-225"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aff51-225"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff51-226">Vea también</span><span class="sxs-lookup"><span data-stu-id="aff51-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff51-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="aff51-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="aff51-228">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="aff51-228">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="aff51-229">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="aff51-229">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="aff51-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="aff51-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> <dt>

[<span data-ttu-id="aff51-231">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="aff51-231">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="aff51-232">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="aff51-232">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="aff51-233">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="aff51-233">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="aff51-234">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="aff51-234">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="aff51-235">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="aff51-235">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="aff51-236">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="aff51-236">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





