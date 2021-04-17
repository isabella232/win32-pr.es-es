---
description: En esta sección se describen los sombreadores que se pueden usar para el modelo de secuencia programable.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programar una o más secuencias (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714720"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a><span data-ttu-id="468d9-103">Programar una o más secuencias (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="468d9-103">Programming One or More Streams (Direct3D 9)</span></span>

<span data-ttu-id="468d9-104">En esta sección se describen los sombreadores que se pueden usar para el modelo de secuencia programable.</span><span class="sxs-lookup"><span data-stu-id="468d9-104">This section describes shaders that can be used for the programmable stream model.</span></span>

## <a name="using-streams"></a><span data-ttu-id="468d9-105">Usar secuencias</span><span class="sxs-lookup"><span data-stu-id="468d9-105">Using Streams</span></span>

<span data-ttu-id="468d9-106">DirectX 8 presentó la noción de una secuencia para enlazar datos a registros de entrada para su uso por parte de los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="468d9-106">DirectX 8 introduced the notion of a stream to bind data to input registers for use by shaders.</span></span> <span data-ttu-id="468d9-107">Una secuencia es una matriz uniforme de datos de componentes, donde cada componente consta de uno o varios elementos que representan una sola entidad, como posición, normal, color, etc.</span><span class="sxs-lookup"><span data-stu-id="468d9-107">A stream is a uniform array of component data, where each component consists of one or more elements that represent a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="468d9-108">Los flujos permiten que los chips gráficos realicen un acceso directo a la memoria desde varios búferes de vértices en paralelo y también proporcionan una asignación más natural de los datos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="468d9-108">Streams enable graphic chips to perform a direct memory access from multiple vertex buffers in parallel and also provide a more natural mapping from application data.</span></span> <span data-ttu-id="468d9-109">También habilitan tritexture triviales frente a Multipass.</span><span class="sxs-lookup"><span data-stu-id="468d9-109">They also enable trivial multitexture versus multipass.</span></span> <span data-ttu-id="468d9-110">Piense en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="468d9-110">Think of it like this:</span></span>

-   <span data-ttu-id="468d9-111">Un vértice se compone de n flujos.</span><span class="sxs-lookup"><span data-stu-id="468d9-111">A vertex is composed of n streams.</span></span>
-   <span data-ttu-id="468d9-112">Un flujo se compone de elementos m.</span><span class="sxs-lookup"><span data-stu-id="468d9-112">A stream is composed of m elements.</span></span>
-   <span data-ttu-id="468d9-113">Un elemento es \[ posición, color, normal, coordenada de textura \] .</span><span class="sxs-lookup"><span data-stu-id="468d9-113">An element is \[position, color, normal, texture coordinate\].</span></span>

<span data-ttu-id="468d9-114">El método [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) enlaza un búfer de vértice a un flujo de datos de dispositivo, creando una asociación entre los datos de vértice y uno de varios puertos de flujo de datos que alimentan las funciones de procesamiento primitiva.</span><span class="sxs-lookup"><span data-stu-id="468d9-114">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="468d9-115">Las referencias reales a los datos de la secuencia no se producen hasta que se llama a un método de dibujo, como [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="468d9-115">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="468d9-116">La asignación de los elementos de vértice de entrada a los registros de entrada de vértices para los sombreadores de vértices programables se define en la declaración del sombreador, pero los elementos del vértice de entrada no tienen una semántica específica sobre su uso.</span><span class="sxs-lookup"><span data-stu-id="468d9-116">The mapping of the input vertex elements to the vertex input registers for programmable vertex shaders is defined in the shader declaration, but the input vertex elements do not have specific semantics about their use.</span></span> <span data-ttu-id="468d9-117">La interpretación de los elementos de vértice de entrada se programa mediante las instrucciones del sombreador.</span><span class="sxs-lookup"><span data-stu-id="468d9-117">The interpretation of the input vertex elements is programmed using the shader instructions.</span></span> <span data-ttu-id="468d9-118">La función de sombreador de vértices se define mediante una matriz de instrucciones que se aplican a cada vértice.</span><span class="sxs-lookup"><span data-stu-id="468d9-118">The vertex shader function is defined by an array of instructions that are applied to each vertex.</span></span> <span data-ttu-id="468d9-119">Los registros de salida de vértices se escriben explícitamente en, mediante instrucciones en la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="468d9-119">The vertex output registers are explicitly written to, using instructions in the shader function.</span></span>

<span data-ttu-id="468d9-120">En este debate, sin embargo, debe preocuparse de la asignación semántica de elementos a los registros y más preocupado por el motivo del uso de las secuencias y del problema que se resuelve mediante el uso de secuencias.</span><span class="sxs-lookup"><span data-stu-id="468d9-120">For this discussion, though, be less concerned with the semantic mapping of elements to registers and more concerned with the reason for using streams and what problem is solved by using streams.</span></span> <span data-ttu-id="468d9-121">La principal ventaja de las secuencias es que quitan los costos de datos de vértices previamente asociados con la multitexturización.</span><span class="sxs-lookup"><span data-stu-id="468d9-121">The main benefit of streams is that they remove the vertex data costs previously associated with multitexturing.</span></span> <span data-ttu-id="468d9-122">Antes de las secuencias, un usuario tenía que duplicar conjuntos de datos de vértices para controlar el caso de una sola y multitextura sin elementos de datos no usados, o bien transportar elementos de datos que no se utilizarían excepto en el caso de múltiples texturas.</span><span class="sxs-lookup"><span data-stu-id="468d9-122">Before streams, a user had to either duplicate vertex data sets to handle the single and multitexture case with no unused data elements, or carry data elements that would be unused except in the multitexture case.</span></span>

<span data-ttu-id="468d9-123">Este es un ejemplo del uso de dos conjuntos de datos de vértices, uno para la textura única y otro para la multitexturización.</span><span class="sxs-lookup"><span data-stu-id="468d9-123">Here is an example of using two sets of vertex data, one for single texture and one for multitexturing.</span></span>


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="468d9-124">La alternativa era tener un elemento de vértice único que contenía ambos conjuntos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="468d9-124">The alternative was to have a single vertex element that contained both sets of texture coordinates.</span></span>


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="468d9-125">Con estos datos de vértices, solo una copia de la posición y los datos de color se transfieren en memoria, a costa de llevar ambos conjuntos de coordenadas de textura para la representación, incluso en el caso de una sola textura.</span><span class="sxs-lookup"><span data-stu-id="468d9-125">With this vertex data, only one copy of the position and color data are carried in memory, at the expense of carrying both sets of texture coordinates around for rendering even in the single texture case.</span></span>

<span data-ttu-id="468d9-126">Ahora que la contrapartida es clara, las secuencias proporcionan una solución elegante para este dilema.</span><span class="sxs-lookup"><span data-stu-id="468d9-126">Now that the tradeoff is clear, streams provide an elegant fix to this dilemma.</span></span> <span data-ttu-id="468d9-127">Este es un conjunto de definiciones de vértices para admitir tres flujos: uno con posición y color, uno con el primer conjunto de coordenadas de textura y otro con el segundo conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="468d9-127">Here is a set of vertex definitions to support three streams: one with position and color, one with the first set of texture coordinates, and one with the second set of texture coordinates.</span></span>


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



<span data-ttu-id="468d9-128">La declaración de vértice sería la siguiente:</span><span class="sxs-lookup"><span data-stu-id="468d9-128">The vertex declaration would be as follows:</span></span>


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



<span data-ttu-id="468d9-129">Ahora cree el objeto de declaración de vértices y establézcalo como se muestra:</span><span class="sxs-lookup"><span data-stu-id="468d9-129">Now create the vertex declaration object and set it as shown:</span></span>


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a><span data-ttu-id="468d9-130">Ejemplos de combinaciones</span><span class="sxs-lookup"><span data-stu-id="468d9-130">Examples of Combinations</span></span>

### <a name="one-stream-diffuse-color"></a><span data-ttu-id="468d9-131">Color difuso de una secuencia</span><span class="sxs-lookup"><span data-stu-id="468d9-131">One Stream Diffuse Color</span></span>

<span data-ttu-id="468d9-132">La declaración de vértices y la configuración de secuencia para la representación de color difusa tendrían el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="468d9-132">The vertex declaration and stream settings for diffuse color rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a><span data-ttu-id="468d9-133">Dos flujos con color y textura</span><span class="sxs-lookup"><span data-stu-id="468d9-133">Two Streams with Color and Texture</span></span>

<span data-ttu-id="468d9-134">La declaración de vértices y la configuración de flujo para la representación de textura única tendrían el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="468d9-134">The vertex declaration and stream settings for single texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a><span data-ttu-id="468d9-135">Dos flujos con color y dos texturas</span><span class="sxs-lookup"><span data-stu-id="468d9-135">Two Streams with Color and two Textures</span></span>

<span data-ttu-id="468d9-136">La declaración de vértices y la configuración de flujo para la representación de varias texturas de dos texturas tendrían el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="468d9-136">The vertex declaration and stream settings for two-texture multi-texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



<span data-ttu-id="468d9-137">En cada caso, basta con la invocación de [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="468d9-137">In every case, the following [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) invocation suffices.</span></span>


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



<span data-ttu-id="468d9-138">Esto muestra la flexibilidad de las secuencias para resolver el problema de la duplicación de datos o la transmisión de datos redundante a través del bus (es decir, de desperdiciar ancho de banda).</span><span class="sxs-lookup"><span data-stu-id="468d9-138">This shows the flexibility of streams in solving the problem of data duplication/redundant data transmission across the bus (that is, of wasting bandwidth).</span></span>

## <a name="related-topics"></a><span data-ttu-id="468d9-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="468d9-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="468d9-140">Declaración de vértice</span><span class="sxs-lookup"><span data-stu-id="468d9-140">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
