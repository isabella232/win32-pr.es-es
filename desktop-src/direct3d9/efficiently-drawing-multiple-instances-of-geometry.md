---
description: Dada una escena que contiene muchos objetos que usan la misma geometría, puede dibujar muchas instancias de esa geometría en distintas orientaciones, tamaños, colores, etc., con un rendimiento mucho mejor, reduciendo la cantidad de datos que necesita proporcionar al representador.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Dibujo eficaz de varias instancias de Geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906444"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a><span data-ttu-id="1e516-103">Dibujo eficaz de varias instancias de Geometry (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1e516-103">Efficiently Drawing Multiple Instances of Geometry (Direct3D 9)</span></span>

<span data-ttu-id="1e516-104">Dada una escena que contiene muchos objetos que usan la misma geometría, puede dibujar muchas instancias de esa geometría en distintas orientaciones, tamaños, colores, etc., con un rendimiento mucho mejor, reduciendo la cantidad de datos que necesita proporcionar al representador.</span><span class="sxs-lookup"><span data-stu-id="1e516-104">Given a scene that contains many objects that use the same geometry, you can draw many instances of that geometry at different orientations, sizes, colors, and so on with dramatically better performance by reducing the amount of data you need to supply to the renderer.</span></span>

<span data-ttu-id="1e516-105">Esto se puede lograr mediante el uso de dos técnicas: la primera para dibujar geometría indizada y la segunda para geometría no indizada.</span><span class="sxs-lookup"><span data-stu-id="1e516-105">This can be accomplished through the use of two techniques: the first for drawing indexed geometry and the second for non-indexed geometry.</span></span> <span data-ttu-id="1e516-106">Ambas técnicas usan dos búferes de vértices: uno para proporcionar datos de geometría y otro para proporcionar datos de instancia por objeto.</span><span class="sxs-lookup"><span data-stu-id="1e516-106">Both techniques use two vertex buffers: one to supply geometry data and one to supply per-object instance data.</span></span> <span data-ttu-id="1e516-107">Los datos de instancia pueden ser una gran variedad de información, como una transformación, datos de color o datos de iluminación, básicamente todo lo que se puede describir en una declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="1e516-107">The instance data can be a wide variety of information such as a transform, color data, or lighting data - basically anything that you can describe in a vertex declaration.</span></span> <span data-ttu-id="1e516-108">Dibujar muchas instancias de Geometry con estas técnicas puede reducir drásticamente la cantidad de datos que se envían al representador.</span><span class="sxs-lookup"><span data-stu-id="1e516-108">Drawing many instances of geometry with these techniques can dramatically reduce the amount of data sent to the renderer.</span></span>

-   [<span data-ttu-id="1e516-109">Dibujar geometría indizada</span><span class="sxs-lookup"><span data-stu-id="1e516-109">Drawing Indexed Geometry</span></span>](#drawing-indexed-geometry)
    -   [<span data-ttu-id="1e516-110">Comparación de rendimiento de geometría indizada</span><span class="sxs-lookup"><span data-stu-id="1e516-110">Indexed Geometry Performance Comparison</span></span>](#indexed-geometry-performance-comparison)
-   [<span data-ttu-id="1e516-111">Dibujo de geometría no indizada</span><span class="sxs-lookup"><span data-stu-id="1e516-111">Drawing Non-Indexed Geometry</span></span>](#drawing-non-indexed-geometry)
    -   [<span data-ttu-id="1e516-112">Comparación de rendimiento de geometría no indizada</span><span class="sxs-lookup"><span data-stu-id="1e516-112">Non-Indexed Geometry Performance Comparison</span></span>](#non-indexed-geometry-performance-comparison)
-   [<span data-ttu-id="1e516-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e516-113">Related topics</span></span>](#related-topics)

## <a name="drawing-indexed-geometry"></a><span data-ttu-id="1e516-114">Dibujar geometría indizada</span><span class="sxs-lookup"><span data-stu-id="1e516-114">Drawing Indexed Geometry</span></span>

<span data-ttu-id="1e516-115">El búfer de vértice contiene datos por vértice que se definen mediante una declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="1e516-115">The vertex buffer contains per-vertex data that is defined by a vertex declaration.</span></span> <span data-ttu-id="1e516-116">Supongamos que parte de cada vértice contiene datos de geometría y que parte de cada vértice contiene datos de instancia por objeto, tal y como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="1e516-116">Suppose that part of each vertex contains geometry data, and part of each vertex contains per-object instance data, as shown in the following diagram.</span></span>

![diagrama de un búfer de vértices para geometría indizada](images/drawingmultipleinstances.png)

<span data-ttu-id="1e516-118">Esta técnica requiere un dispositivo que admita el \_ modelo de sombreador de vértices 3 0.</span><span class="sxs-lookup"><span data-stu-id="1e516-118">This technique requires a device that supports the 3\_0 vertex shader model.</span></span> <span data-ttu-id="1e516-119">Esta técnica funciona con cualquier sombreador programable, pero no con la canalización de funciones fijas.</span><span class="sxs-lookup"><span data-stu-id="1e516-119">This technique works with any programmable shader but not with the fixed function pipeline.</span></span>

<span data-ttu-id="1e516-120">En el caso de los búferes de vértices mostrados anteriormente, estas son las declaraciones de búfer de vértice correspondientes:</span><span class="sxs-lookup"><span data-stu-id="1e516-120">For the vertex buffers shown above, here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="1e516-121">Estas declaraciones definen dos búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="1e516-121">These declarations define two vertex buffers.</span></span> <span data-ttu-id="1e516-122">La primera declaración (para la secuencia 0, indicada por los ceros de la columna 1) define los datos de geometría que se componen de: posición, normal, tangente, binormalización y datos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="1e516-122">The first declaration (for stream 0, indicated by the zeros in column 1) defines the geometry data which consists of: position, normal, tangent, binormal, and texture coordinate data.</span></span>

<span data-ttu-id="1e516-123">La segunda declaración (para la secuencia 1, indicada por las de la columna 1) define los datos de instancia por objeto.</span><span class="sxs-lookup"><span data-stu-id="1e516-123">The second declaration (for stream 1, indicated by the ones in column 1) defines the per-object instance data.</span></span> <span data-ttu-id="1e516-124">Cada instancia se define mediante números de punto flotante del componente 4 4 y un color de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="1e516-124">Each instance is defined by four four-component floating point numbers, and a four-component color.</span></span> <span data-ttu-id="1e516-125">Los primeros cuatro valores se pueden usar para inicializar una matriz 4x4, lo que significa que estos datos dimensionarán, posicionarán y girarán de forma exclusiva cada instancia de la geometría.</span><span class="sxs-lookup"><span data-stu-id="1e516-125">The first four values could be used to initialize a 4x4 matrix, which means that this data will uniquely size, position, and rotate each instance of the geometry.</span></span> <span data-ttu-id="1e516-126">Los primeros cuatro componentes usan una semántica de coordenadas de textura que, en este caso, significa "Esto es un número de cuatro componentes general".</span><span class="sxs-lookup"><span data-stu-id="1e516-126">The first four components use a texture coordinate semantic which, in this case, means "this is a general four-component number."</span></span> <span data-ttu-id="1e516-127">Cuando se usan datos arbitrarios en una declaración de vértice, se usa una semántica de coordenadas de textura para marcarlo.</span><span class="sxs-lookup"><span data-stu-id="1e516-127">When you use arbitrary data in a vertex declaration, use a texture coordinate semantic to mark it.</span></span> <span data-ttu-id="1e516-128">El último elemento de la secuencia se utiliza para los datos de color.</span><span class="sxs-lookup"><span data-stu-id="1e516-128">The last element in the stream is used for color data.</span></span> <span data-ttu-id="1e516-129">Esto se podría aplicar en el sombreador de vértices para asignar a cada instancia un color único.</span><span class="sxs-lookup"><span data-stu-id="1e516-129">This could be applied in the vertex shader to give each instance a unique color.</span></span>

<span data-ttu-id="1e516-130">Antes de la representación, debe llamar a [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) para enlazar las secuencias del búfer de vértices al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1e516-130">Before rendering, you need to call [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to bind the vertex buffer streams to the device.</span></span> <span data-ttu-id="1e516-131">Este es un ejemplo en el que se enlazan ambos búferes de vértice:</span><span class="sxs-lookup"><span data-stu-id="1e516-131">Here is an example that binds both vertex buffers:</span></span>


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="1e516-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) usa [D3DSTREAMSOURCE \_ INDEXEDDATA](other-direct3d-constants.md) para identificar los datos de geometría indexados.</span><span class="sxs-lookup"><span data-stu-id="1e516-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INDEXEDDATA](other-direct3d-constants.md) to identify the indexed geometry data.</span></span> <span data-ttu-id="1e516-133">En este caso, stream 0 contiene los datos indizados que describen la geometría del objeto.</span><span class="sxs-lookup"><span data-stu-id="1e516-133">In this case, stream 0 contains the indexed data that describes the object geometry.</span></span> <span data-ttu-id="1e516-134">Este valor se combina lógicamente con el número de instancias de la geometría que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="1e516-134">This value is logically combined with the number of instances of the geometry to draw.</span></span>

<span data-ttu-id="1e516-135">Tenga en cuenta que D3DSTREAMSOURCE \_ INDEXEDDATA y el número de instancias que se van a dibujar siempre se deben establecer en el flujo cero.</span><span class="sxs-lookup"><span data-stu-id="1e516-135">Note that D3DSTREAMSOURCE\_INDEXEDDATA and the number of instances to draw must always be set in stream zero.</span></span>

<span data-ttu-id="1e516-136">En la segunda llamada, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) usa [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) para identificar la secuencia que contiene los datos de la instancia.</span><span class="sxs-lookup"><span data-stu-id="1e516-136">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INSTANCEDATA](other-direct3d-constants.md) to identify the stream containing the instance data.</span></span> <span data-ttu-id="1e516-137">Este valor se combina lógicamente con 1 porque cada vértice contiene un conjunto de datos de instancia.</span><span class="sxs-lookup"><span data-stu-id="1e516-137">This value is logically combined with 1 since each vertex contains one set of instance data.</span></span>

<span data-ttu-id="1e516-138">Las dos últimas llamadas a [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) enlazan los punteros de búfer de vértices al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1e516-138">The last two calls to [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bind the vertex buffer pointers to the device.</span></span>

<span data-ttu-id="1e516-139">Cuando haya terminado de representar los datos de la instancia, asegúrese de restablecer la frecuencia del flujo de vértices a su estado predeterminado (que no usa la creación de instancias).</span><span class="sxs-lookup"><span data-stu-id="1e516-139">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state (which does not use instancing).</span></span> <span data-ttu-id="1e516-140">Dado que en este ejemplo se usan dos flujos, establezca ambos flujos como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="1e516-140">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a><span data-ttu-id="1e516-141">Comparación de rendimiento de geometría indizada</span><span class="sxs-lookup"><span data-stu-id="1e516-141">Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="1e516-142">Aunque no es posible realizar una conclusión única sobre el grado en que esta técnica puede reducir el tiempo de representación en cada aplicación, tenga en cuenta la diferencia en la cantidad de datos transmitidos en el tiempo de ejecución y el número de cambios de estado que se reducirán si usa la técnica de creación de instancias.</span><span class="sxs-lookup"><span data-stu-id="1e516-142">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime and the number of state changes that will be reduced if you use the instancing technique.</span></span> <span data-ttu-id="1e516-143">Esta secuencia de representación aprovecha las ventajas de dibujar varias instancias de la misma geometría:</span><span class="sxs-lookup"><span data-stu-id="1e516-143">This render sequence takes advantage of drawing multiple instances of the same geometry:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="1e516-144">Observe que el bucle de representación se llama una vez, los datos de geometría se transmiten una vez y n instancias se transmiten una vez.</span><span class="sxs-lookup"><span data-stu-id="1e516-144">Notice that the render loop is called once, the geometry data is streamed once, and n instances are streamed once.</span></span> <span data-ttu-id="1e516-145">Esta secuencia de representación siguiente es idéntica en la funcionalidad, pero no aprovecha las ventajas de la creación de instancias:</span><span class="sxs-lookup"><span data-stu-id="1e516-145">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="1e516-146">Observe que el bucle de representación completo está incluido en un segundo bucle para dibujar cada objeto.</span><span class="sxs-lookup"><span data-stu-id="1e516-146">Notice that the entire render loop is wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="1e516-147">Ahora los datos de geometría se transmiten en el representador n veces (en lugar de una vez) y cualquier estado de canalización también se puede establecer de forma redundante para cada objeto dibujado.</span><span class="sxs-lookup"><span data-stu-id="1e516-147">Now the geometry data is streamed into the renderer n times (instead of once) and any pipeline states may also be set redundantly for each object drawn.</span></span> <span data-ttu-id="1e516-148">Es muy probable que esta secuencia de representación sea mucho más lenta.</span><span class="sxs-lookup"><span data-stu-id="1e516-148">This render sequence is very likely to be significantly slower.</span></span> <span data-ttu-id="1e516-149">Observe también que los parámetros de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) no han cambiado entre los dos bucles de representación.</span><span class="sxs-lookup"><span data-stu-id="1e516-149">Notice also that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed between the two render loops.</span></span>

## <a name="drawing-non-indexed-geometry"></a><span data-ttu-id="1e516-150">Dibujo de geometría no indizada</span><span class="sxs-lookup"><span data-stu-id="1e516-150">Drawing Non-Indexed Geometry</span></span>

<span data-ttu-id="1e516-151">En el [dibujo de geometría indizada](#drawing-indexed-geometry), los búferes de vértices se configuraron para dibujar varias instancias de geometría indizada con mayor eficacia.</span><span class="sxs-lookup"><span data-stu-id="1e516-151">In [Drawing Indexed Geometry](#drawing-indexed-geometry), vertex buffers were configured to draw multiple instances of indexed geometry with greater efficiency.</span></span> <span data-ttu-id="1e516-152">También puede usar [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) para dibujar geometría no indizada.</span><span class="sxs-lookup"><span data-stu-id="1e516-152">You can also use [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to draw non-indexed geometry.</span></span> <span data-ttu-id="1e516-153">Esto requiere un diseño de búfer de vértices diferente y tiene distintas restricciones.</span><span class="sxs-lookup"><span data-stu-id="1e516-153">This requires a different vertex buffer layout and has different constraints.</span></span> <span data-ttu-id="1e516-154">Para dibujar geometría no indizada, prepare los búferes de vértices como el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="1e516-154">To draw non-indexed geometry, prepare your vertex buffers like the following diagram.</span></span>

![diagrama de un búfer de vértices para geometría no indizada](images/olderstyleinstancing.png)

<span data-ttu-id="1e516-156">Esta técnica no es compatible con la aceleración de hardware en cualquier dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1e516-156">This technique is not supported by hardware acceleration on any device.</span></span> <span data-ttu-id="1e516-157">Solo se admite en el procesamiento de vértices de software y solo funcionará con los sombreadores de [vs \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) .</span><span class="sxs-lookup"><span data-stu-id="1e516-157">It is only supported by software vertex processing and will work only with [vs\_3\_0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) shaders.</span></span>

<span data-ttu-id="1e516-158">Dado que esta técnica funciona con geometría no indizada, no hay ningún búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="1e516-158">Because this technique works with non-indexed geometry, there is no index buffer.</span></span> <span data-ttu-id="1e516-159">Como se muestra en el diagrama, el búfer de vértices que contiene Geometry contiene n copias de los datos de geometría.</span><span class="sxs-lookup"><span data-stu-id="1e516-159">As the diagram shows, the vertex buffer that contains geometry contains n copies of the geometry data.</span></span> <span data-ttu-id="1e516-160">Para cada instancia dibujada, los datos de geometría se leen desde el primer búfer de vértices y los datos de instancia se leen desde el segundo búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="1e516-160">For each instance drawn, the geometry data is read from the first vertex buffer and the instance data is read from the second vertex buffer.</span></span>

<span data-ttu-id="1e516-161">Estas son las declaraciones de búfer de vértice correspondientes:</span><span class="sxs-lookup"><span data-stu-id="1e516-161">Here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="1e516-162">Estas declaraciones son idénticas a las declaraciones realizadas en el ejemplo de geometría indizada.</span><span class="sxs-lookup"><span data-stu-id="1e516-162">These declarations are identical to the declarations made in the indexed geometry example.</span></span> <span data-ttu-id="1e516-163">Una vez más, la primera declaración (para Stream 0) define los datos de geometría y la segunda declaración (para Stream 1) define los datos de instancia por objeto.</span><span class="sxs-lookup"><span data-stu-id="1e516-163">Once again, the first declaration (for stream 0) defines the geometry data and the second declaration (for stream 1) defines the per-object instance data.</span></span> <span data-ttu-id="1e516-164">Al crear el primer búfer de vértices, asegúrese de cargarlo con el número de instancias de los datos de geometría que va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="1e516-164">When you create the first vertex buffer, be sure to load it with the number of instances of the geometry data that you will be drawing.</span></span>

<span data-ttu-id="1e516-165">Antes de la representación, debe configurar el divisor, que indica al tiempo de ejecución cómo dividir el primer búfer de vértices en n instancias.</span><span class="sxs-lookup"><span data-stu-id="1e516-165">Before rendering, you need to set up the divider which tells the runtime how to divide up the first vertex buffer into n instances.</span></span> <span data-ttu-id="1e516-166">A continuación, establezca el divisor con [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1e516-166">Then set the divider using [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) like this:</span></span>


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="1e516-167">La primera llamada a [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) indica que el flujo 0 contiene n instancias de los vértices m.</span><span class="sxs-lookup"><span data-stu-id="1e516-167">The first call to [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) says that stream 0 contains n instances of m vertices.</span></span> <span data-ttu-id="1e516-168">A continuación, [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) enlaza el flujo 0 al búfer de vértices de geometría.</span><span class="sxs-lookup"><span data-stu-id="1e516-168">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 0 to the geometry vertex buffer.</span></span>

<span data-ttu-id="1e516-169">En la segunda llamada, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifica la secuencia 1 como el origen de los datos de instancia.</span><span class="sxs-lookup"><span data-stu-id="1e516-169">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifies stream 1 as the source of the instance data.</span></span> <span data-ttu-id="1e516-170">El segundo parámetro es el número de vértices de cada objeto (m).</span><span class="sxs-lookup"><span data-stu-id="1e516-170">The second parameter is the number of vertices in each object (m).</span></span> <span data-ttu-id="1e516-171">Recuerde que el flujo de datos de instancia siempre se debe declarar como la segunda secuencia.</span><span class="sxs-lookup"><span data-stu-id="1e516-171">Remember that the instance data stream must always be declared as the second stream.</span></span> <span data-ttu-id="1e516-172">A continuación, [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) enlaza el flujo 1 al búfer de vértices que contiene los datos de instancia.</span><span class="sxs-lookup"><span data-stu-id="1e516-172">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 1 to the vertex buffer that contains the instance data.</span></span>

<span data-ttu-id="1e516-173">Cuando haya terminado de representar los datos de la instancia, asegúrese de restablecer la frecuencia del flujo de vértices a su estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1e516-173">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state.</span></span> <span data-ttu-id="1e516-174">Dado que en este ejemplo se usan dos flujos, establezca ambos flujos como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="1e516-174">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a><span data-ttu-id="1e516-175">Comparación de rendimiento de geometría no indizada</span><span class="sxs-lookup"><span data-stu-id="1e516-175">Non-Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="1e516-176">La principal ventaja de este estilo de creación de instancias es que se puede usar en geometría no indizada.</span><span class="sxs-lookup"><span data-stu-id="1e516-176">The major advantage of this instancing style is that it can be used on non-indexed geometry.</span></span> <span data-ttu-id="1e516-177">Aunque no es posible realizar una conclusión única sobre el grado en que esta técnica puede reducir el tiempo de representación en cada aplicación, tenga en cuenta la diferencia en la cantidad de datos transmitidos en el tiempo de ejecución y el número de cambios de estado que se reducirán para la siguiente secuencia de representación:</span><span class="sxs-lookup"><span data-stu-id="1e516-177">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime, and the number of state changes that will be reduced for the following render sequence:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="1e516-178">Observe que el bucle de representación se llama una vez.</span><span class="sxs-lookup"><span data-stu-id="1e516-178">Notice that the render loop is called once.</span></span> <span data-ttu-id="1e516-179">Los datos de geometría se transmiten una vez, aunque hay n instancias de la geometría que se transmite.</span><span class="sxs-lookup"><span data-stu-id="1e516-179">The geometry data is streamed once although there are n instances of the geometry being streamed.</span></span> <span data-ttu-id="1e516-180">Los datos del búfer de vértice de instancia se transmiten una vez.</span><span class="sxs-lookup"><span data-stu-id="1e516-180">The data from the instance vertex buffer is streamed once.</span></span> <span data-ttu-id="1e516-181">Esta secuencia de representación siguiente es idéntica en la funcionalidad, pero no aprovecha las ventajas de la creación de instancias:</span><span class="sxs-lookup"><span data-stu-id="1e516-181">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="1e516-182">Sin creación de instancias, el bucle de representación debe estar incluido en un segundo bucle para dibujar cada objeto.</span><span class="sxs-lookup"><span data-stu-id="1e516-182">Without instancing, the render loop needs to be wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="1e516-183">Al eliminar el segundo bucle de representación, debería esperar un mejor rendimiento debido a menos cambios en el estado de representación a los que se llama dentro del bucle.</span><span class="sxs-lookup"><span data-stu-id="1e516-183">By eliminating the second render loop, you should expect better performance due to fewer render state changes that are called inside the loop.</span></span>

<span data-ttu-id="1e516-184">En general, es razonable esperar que la técnica indizada ([dibujo de geometría indizada](#drawing-indexed-geometry)) funcione mejor que la técnica no indizada ([dibujo de geometría no indizada](#drawing-non-indexed-geometry)) porque la técnica indizada solo transmite una copia de los datos de geometría.</span><span class="sxs-lookup"><span data-stu-id="1e516-184">Overall, it is reasonable to expect the indexed technique ([Drawing Indexed Geometry](#drawing-indexed-geometry)) to perform better than the non-indexed technique ([Drawing Non-Indexed Geometry](#drawing-non-indexed-geometry)) because the indexed technique only streams one copy of the geometry data.</span></span> <span data-ttu-id="1e516-185">Observe que los parámetros de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) no han cambiado en ninguna de las secuencias de representación.</span><span class="sxs-lookup"><span data-stu-id="1e516-185">Notice that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed for any of the render sequences.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e516-186">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e516-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e516-187">Temas avanzados</span><span class="sxs-lookup"><span data-stu-id="1e516-187">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

<span data-ttu-id="1e516-188">[Ejemplo de creación de instancias](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="1e516-188">[Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
