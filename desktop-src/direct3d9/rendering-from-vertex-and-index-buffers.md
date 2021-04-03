---
description: Direct3D admite métodos de dibujo indexados y no indexados.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Representación de búferes de vértices y de índices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906438"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a><span data-ttu-id="9ea04-103">Representación de búferes de vértices y de índices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9ea04-103">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>

<span data-ttu-id="9ea04-104">Direct3D admite métodos de dibujo indexados y no indexados.</span><span class="sxs-lookup"><span data-stu-id="9ea04-104">Both indexed and nonindexed drawing methods are supported by Direct3D.</span></span> <span data-ttu-id="9ea04-105">Los métodos indizados usan un único conjunto de índices para todos los componentes de vértices.</span><span class="sxs-lookup"><span data-stu-id="9ea04-105">The indexed methods use a single set of indices for all vertex components.</span></span> <span data-ttu-id="9ea04-106">Los datos de vértice se almacenan en búferes de vértices y los datos de índice se almacenan en búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="9ea04-106">Vertex data is stored in vertex buffers, and index data is stored in index buffers.</span></span> <span data-ttu-id="9ea04-107">A continuación se enumeran algunos escenarios comunes para dibujar primitivos mediante el uso de búferes de vértices y de índices.</span><span class="sxs-lookup"><span data-stu-id="9ea04-107">Listed below are a few common scenarios for drawing primitives using vertex and index buffers.</span></span>

<span data-ttu-id="9ea04-108">En estos ejemplos se compara el uso de [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) y [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span><span class="sxs-lookup"><span data-stu-id="9ea04-108">These examples compare the use of [**IDirect3DDevice9::DrawPrimitive**](/windows/desktop/api) and [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span></span>

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a><span data-ttu-id="9ea04-109">Escenario 1: dibujar dos triángulos sin indexación</span><span class="sxs-lookup"><span data-stu-id="9ea04-109">Scenario 1: Drawing Two Triangles without Indexing</span></span>

<span data-ttu-id="9ea04-110">Supongamos que desea dibujar la cuádruple que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="9ea04-110">Let's say you want to draw the quad that is shown in the following illustration.</span></span>

![Ilustración de un cuadrado que consta de dos triángulos](images/dip-fig1.png)

<span data-ttu-id="9ea04-112">Si usa el tipo primitivo de la lista de triángulos para representar los dos triángulos, cada triángulo se almacenará como 3 vértices individuales, lo que dará lugar a un búfer de vértice similar a la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="9ea04-112">If you use the Triangle List primitive type to render the two triangles, each triangle will be stored as 3 individual vertices, resulting in a similar vertex buffer to the following illustration.</span></span>

![diagrama de un búfer de vértice que define tres vértices para dos triángulos](images/dip-fig2.png)

<span data-ttu-id="9ea04-114">La llamada de dibujo es muy sencilla; a partir de la ubicación 0 dentro del búfer de vértices, dibuje dos triángulos.</span><span class="sxs-lookup"><span data-stu-id="9ea04-114">The drawing call is very straightforward; starting at location 0 within the vertex buffer, draw two triangles.</span></span> <span data-ttu-id="9ea04-115">Si está habilitado el culling, el orden de los vértices será importante.</span><span class="sxs-lookup"><span data-stu-id="9ea04-115">If culling is enabled, the order of the vertices will be important.</span></span> <span data-ttu-id="9ea04-116">En este ejemplo se da por supuesto el estado de selección en el sentido contrario a las agujas del reloj, por lo que los triángulos visibles deben dibujarse en el orden del reloj.</span><span class="sxs-lookup"><span data-stu-id="9ea04-116">This example assumes the default counter-clockwise culling state, so visible triangles must be drawn in clockwise order.</span></span> <span data-ttu-id="9ea04-117">El tipo primitivo de la lista triangular simplemente Lee tres vértices en orden lineal desde el búfer para cada triángulo, por lo que esta llamada dibujará triángulos (0, 1, 2) y (3, 4, 5):</span><span class="sxs-lookup"><span data-stu-id="9ea04-117">The Triangle List primitive type simply reads three vertices in linear order from the buffer for each triangle, so this call will draw triangles (0, 1, 2) and (3, 4, 5):</span></span>


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a><span data-ttu-id="9ea04-118">Escenario 2: dibujar dos triángulos con indexación</span><span class="sxs-lookup"><span data-stu-id="9ea04-118">Scenario 2: Drawing Two Triangles with Indexing</span></span>

<span data-ttu-id="9ea04-119">Como observará, el búfer de vértices contiene datos duplicados en las ubicaciones 0 y 4, 2 y 5.</span><span class="sxs-lookup"><span data-stu-id="9ea04-119">As you'll notice, the vertex buffer contains duplicate data in locations 0 and 4, 2 and 5.</span></span> <span data-ttu-id="9ea04-120">Esto tiene sentido porque los dos triángulos comparten dos vértices comunes.</span><span class="sxs-lookup"><span data-stu-id="9ea04-120">That makes sense because the two triangles share two common vertices.</span></span> <span data-ttu-id="9ea04-121">Estos datos duplicados son excesivos y el búfer de vértices se puede comprimir mediante un búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="9ea04-121">This duplicate data is wasteful, and the vertex buffer can be compressed by using an index buffer.</span></span> <span data-ttu-id="9ea04-122">Un búfer de vértices más pequeño reduce la cantidad de datos de vértices que se deben enviar al adaptador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="9ea04-122">A smaller vertex buffer reduces the amount of vertex data that has to be sent to the graphics adapter.</span></span> <span data-ttu-id="9ea04-123">Incluso más importante, el uso de un búfer de índice permite que el adaptador almacene los vértices en una memoria caché de vértices. Si el primitivo que se está dibujando contiene un vértice usado recientemente, ese vértice se puede capturar desde la memoria caché en lugar de leerlo desde el búfer de vértices, lo que provoca un aumento de gran rendimiento.</span><span class="sxs-lookup"><span data-stu-id="9ea04-123">Even more importantly, using an index buffer allows the adapter to store vertices in a vertex cache; if the primitive being drawn contains a recently-used vertex, that vertex can be fetched from the cache instead of reading it from the vertex buffer, which results in a big performance increase.</span></span>

<span data-ttu-id="9ea04-124">Un búfer de índice ' índices ' en el búfer de vértices, por lo que cada vértice único debe almacenarse una sola vez en el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="9ea04-124">An index buffer 'indexes' into the vertex buffer so each unique vertex needs to be stored only once in the vertex buffer.</span></span> <span data-ttu-id="9ea04-125">En el diagrama siguiente se muestra un enfoque indizado en el escenario de dibujo anterior.</span><span class="sxs-lookup"><span data-stu-id="9ea04-125">The following diagram shows an indexed approach to the earlier drawing scenario.</span></span>

![diagrama de un búfer de índice para el búfer de vértices anterior](images/dip-fig3.png)

<span data-ttu-id="9ea04-127">El búfer de índice almacena los valores de índice de VB, que hacen referencia a un vértice determinado dentro del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="9ea04-127">The index buffer stores VB Index values, which reference a particular vertex within the vertex buffer.</span></span> <span data-ttu-id="9ea04-128">Un búfer de vértices se puede considerar como una matriz de vértices, por lo que el índice de VB es simplemente el índice en el búfer de vértices para el vértice de destino.</span><span class="sxs-lookup"><span data-stu-id="9ea04-128">A vertex buffer can be thought of as an array of vertices, so the VB Index is simply the index into the vertex buffer for the target vertex.</span></span> <span data-ttu-id="9ea04-129">Del mismo modo, un índice de IB es un índice en el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="9ea04-129">Similarly, an IB Index is an index into the index buffer.</span></span> <span data-ttu-id="9ea04-130">Esto puede resultar muy confuso si no tiene cuidado, por lo que debe asegurarse de que está claro en el vocabulario que se está usando: índice de valores de índice de VB en el búfer de vértices, IB index Values index en el búfer de índice y el propio búfer de índice almacena valores de índice de VB.</span><span class="sxs-lookup"><span data-stu-id="9ea04-130">This can get very confusing very quickly if you're not careful, so make sure you're clear on the vocabulary being used: VB Index values index into the vertex buffer, IB Index values index into the index buffer, and the index buffer itself stores VB Index values.</span></span>

<span data-ttu-id="9ea04-131">A continuación se muestra la llamada de dibujo.</span><span class="sxs-lookup"><span data-stu-id="9ea04-131">The drawing call is shown below.</span></span> <span data-ttu-id="9ea04-132">Los significados de todos los argumentos se describen en la longitud para el siguiente escenario de dibujo; por ahora, solo tenga en cuenta que esta llamada indica a Direct3D que represente una lista de triángulos que contiene dos triángulos, empezando en la ubicación 0 dentro del búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="9ea04-132">The meanings of all the arguments are discussed at length for the next drawing scenario; for now, just note that this call is again instructing Direct3D to render a triangle list containing two triangles, starting at location 0 within the index buffer.</span></span> <span data-ttu-id="9ea04-133">Esta llamada dibujará los mismos dos triángulos en el mismo orden que antes, lo que garantiza una orientación adecuada en el sentido de las agujas del reloj:</span><span class="sxs-lookup"><span data-stu-id="9ea04-133">This call will draw the same two triangles in the exact same order as before, ensuring a proper clockwise orientation:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a><span data-ttu-id="9ea04-134">Escenario 3: dibujo de un triángulo con indexación</span><span class="sxs-lookup"><span data-stu-id="9ea04-134">Scenario 3: Drawing One Triangle with Indexing</span></span>

<span data-ttu-id="9ea04-135">Imagine ahora que desea dibujar solo el segundo triángulo, pero desea usar el mismo búfer de vértices y el búfer de índice que se usan al dibujar el cuádruple completo, tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="9ea04-135">Pretend now that you want to draw only the second triangle, but you want to use the same vertex buffer and index buffer that are used when drawing the entire quad, as shown in the following diagram.</span></span>

![diagrama del búfer de índice y del búfer de vértice del segundo triángulo](images/dip-fig4.png)

<span data-ttu-id="9ea04-137">En esta llamada de dibujo, el primer índice de IB utilizado es 3; Este valor se denomina StartIndex.</span><span class="sxs-lookup"><span data-stu-id="9ea04-137">For this drawing call, the first IB Index used is 3; this value is called the StartIndex.</span></span> <span data-ttu-id="9ea04-138">El índice de VB más bajo utilizado es 0; Este valor se denomina MinIndex.</span><span class="sxs-lookup"><span data-stu-id="9ea04-138">The lowest VB Index used is 0; this value is called the MinIndex.</span></span> <span data-ttu-id="9ea04-139">Aunque solo se necesitan tres vértices para dibujar el triángulo, los tres vértices se distribuyen en cuatro ubicaciones adyacentes en el búfer de vértices. el número de ubicaciones dentro del bloque contiguo de memoria del búfer de vértices necesario para la llamada de dibujo se denomina NumVertices y se establecerá en 4 en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="9ea04-139">Even though only three vertices are required to draw the triangle, those three vertices are spread across four adjacent locations in the vertex buffer; the number of locations within the contiguous block of vertex buffer memory required for the drawing call is called NumVertices, and will be set to 4 in this call.</span></span> <span data-ttu-id="9ea04-140">Los valores MinIndex y NumVertices son simplemente sugerencias para ayudar a Direct3D a optimizar el acceso a la memoria durante el procesamiento de vértices de software y se pueden establecer simplemente para incluir todo el búfer de vértices en el precio del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="9ea04-140">The MinIndex and NumVertices values are really just hints to help Direct3D optimize memory access during software vertex processing, and could simply be set to include the entire vertex buffer at the price of performance.</span></span>

<span data-ttu-id="9ea04-141">Esta es la llamada de dibujo del caso de un solo triángulo; el significado del argumento BaseVertexIndex se explicará a continuación:</span><span class="sxs-lookup"><span data-stu-id="9ea04-141">Here is the drawing call for the single triangle case; the meaning of the BaseVertexIndex argument will be explained next:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a><span data-ttu-id="9ea04-142">Escenario 4: dibujo de un triángulo con índices de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="9ea04-142">Scenario 4: Drawing One Triangle with Offset Indexing</span></span>

<span data-ttu-id="9ea04-143">BaseVertexIndex es un valor que se agrega de forma eficaz a cada índice de VB almacenado en el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="9ea04-143">BaseVertexIndex is a value that's effectively added to every VB Index stored in the index buffer.</span></span> <span data-ttu-id="9ea04-144">Por ejemplo, si se hubiera pasado un valor de 50 para BaseVertexIndex durante la llamada anterior, esto sería lo mismo que usar el búfer de índice en el diagrama siguiente durante la llamada a DrawIndexedPrimitive:</span><span class="sxs-lookup"><span data-stu-id="9ea04-144">For example, if we had passed in a value of 50 for BaseVertexIndex during the previous call, that would functionally be the same as using the index buffer in the following diagram for the duration of the DrawIndexedPrimitive call:</span></span>

![diagrama de un búfer de índice con un valor de 50 para basevertexindex](images/dip-fig5.png)

<span data-ttu-id="9ea04-146">Este valor rara vez se establece en un valor distinto de 0, pero puede ser útil si desea desacoplar el búfer de índice del búfer de vértices: si al rellenar el búfer de índice para una malla determinada, la ubicación de la malla en el búfer de vértices no se conoce todavía, puede suponer que los vértices de la malla se encuentren al principio del búfer Cuando llega el momento de hacer la llamada a Draw, solo tiene que pasar la ubicación inicial real como BaseVertexIndex.</span><span class="sxs-lookup"><span data-stu-id="9ea04-146">This value is rarely set to anything other than 0, but can be useful if you want to decouple the index buffer from the vertex buffer: If when filling in the index buffer for a particular mesh the location of the mesh within the vertex buffer isn't yet known, you can simply pretend the mesh vertices will be located at the start of the vertex buffer; when it comes time to make the draw call, simply pass the actual starting location as the BaseVertexIndex.</span></span>

<span data-ttu-id="9ea04-147">Esta técnica también se puede usar al dibujar varias instancias de una malla mediante un búfer de índice único. por ejemplo, si el búfer de vértices contenía dos mallas con un orden de dibujo idéntico, pero con vértices ligeramente diferentes (quizás diferentes colores difusos o coordenadas de textura), ambas mallas podrían dibujarse usando valores diferentes para BaseVertexIndex.</span><span class="sxs-lookup"><span data-stu-id="9ea04-147">This technique can also be used when drawing multiple instances of a mesh using a single index buffer; for example, if the vertex buffer contained two meshes with identical draw order but slightly different vertices (perhaps different diffuse colors or texture coordinates), both meshes could be drawn by using different values for BaseVertexIndex.</span></span> <span data-ttu-id="9ea04-148">Tomando este concepto un paso más, podría usar un búfer de índice para dibujar varias instancias de una malla, cada una de ellas en un búfer de vértices diferente, simplemente recorriendo el búfer de vértices activo y ajustando el BaseVertexIndex según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9ea04-148">Taking this concept one step further, you could use one index buffer to draw multiple instances of a mesh, each contained in a different vertex buffer, simply by cycling which vertex buffer is active and adjusting the BaseVertexIndex as needed.</span></span> <span data-ttu-id="9ea04-149">Tenga en cuenta que el valor BaseVertexIndex también se agrega automáticamente al argumento MinIndex, que tiene sentido cuando se ve cómo se usa:</span><span class="sxs-lookup"><span data-stu-id="9ea04-149">Note that the BaseVertexIndex value is also automatically added to the MinIndex argument, which makes sense when you see how it's used:</span></span>

<span data-ttu-id="9ea04-150">Imagine ahora que deseamos dibujar solo el segundo triángulo de la cuádruple con el mismo búfer de índice que antes; sin embargo, se usa un búfer de vértices diferente en el que se encuentra el cuádruple en el índice de VB 50.</span><span class="sxs-lookup"><span data-stu-id="9ea04-150">Pretend now that we again want to draw only the second triangle of the quad using the same index buffer as before; however, a different vertex buffer is being used in which the quad is located at VB Index 50.</span></span> <span data-ttu-id="9ea04-151">El orden relativo de los vértices cuádruples permanece sin cambios, solo la ubicación inicial dentro del búfer de vértices es diferente.</span><span class="sxs-lookup"><span data-stu-id="9ea04-151">The relative order of the quad vertices remains unchanged, only the starting location within the vertex buffer is different.</span></span> <span data-ttu-id="9ea04-152">El búfer de índice y el búfer de vértice serían similares al diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="9ea04-152">The index buffer and vertex buffer would look like the following diagram.</span></span>

![diagrama del búfer de índice y del búfer de vértice con un índice de VB de 50](images/dip-fig6.png)

<span data-ttu-id="9ea04-154">Esta es la llamada a Draw adecuada; Tenga en cuenta que BaseVertexIndex es el único valor que ha cambiado en el escenario anterior:</span><span class="sxs-lookup"><span data-stu-id="9ea04-154">Here is the appropriate draw call; note that BaseVertexIndex is the only value which has changed from the previous scenario:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a><span data-ttu-id="9ea04-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9ea04-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ea04-156">Representación de primitivas</span><span class="sxs-lookup"><span data-stu-id="9ea04-156">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
