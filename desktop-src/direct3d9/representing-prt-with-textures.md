---
description: El ejemplo PRTDemo y el simulador PRTCmdLine incluidos en el SDK de DirectX representan vectores de transferencia en los vértices de una malla.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Representar PRT con texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4647cfc85451ede9507e007ed556a203a3cd890a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274784"
---
# <a name="representing-prt-with-textures-direct3d-9"></a><span data-ttu-id="f99e9-103">Representar PRT con texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f99e9-103">Representing PRT With Textures (Direct3D 9)</span></span>

<span data-ttu-id="f99e9-104">El ejemplo PRTDemo y el simulador PRTCmdLine incluidos en el SDK de DirectX representan vectores de transferencia en los vértices de una malla.</span><span class="sxs-lookup"><span data-stu-id="f99e9-104">The PRTDemo sample and PRTCmdLine simulator included in the DirectX SDK represent transfer vectors at the vertices of a mesh.</span></span> <span data-ttu-id="f99e9-105">Para representar la señal de PRT con precisión, esto puede requerir teselaciones que podrían no ser prácticas para los juegos actuales.</span><span class="sxs-lookup"><span data-stu-id="f99e9-105">In order to represent the PRT signal accurately, this can require tessellations that may be impractical for current games.</span></span> <span data-ttu-id="f99e9-106">Representar vectores de transferencia en mapas de textura es un enfoque alternativo que tiene el mismo costo de datos independiente de la complejidad de la malla.</span><span class="sxs-lookup"><span data-stu-id="f99e9-106">Representing transfer vectors in texture maps is an alternative approach that has the same data cost independent of mesh complexity.</span></span> <span data-ttu-id="f99e9-107">Hay varias maneras de generar mapas de textura vectoriales de transferencia mediante la biblioteca de D3DX PRT.</span><span class="sxs-lookup"><span data-stu-id="f99e9-107">There are several ways to generate transfer vector texture maps using the D3DX PRT Library.</span></span>

## <a name="precomputing-transfer-vectors"></a><span data-ttu-id="f99e9-108">Computación de vectores de transferencia</span><span class="sxs-lookup"><span data-stu-id="f99e9-108">Precomputing Transfer Vectors</span></span>

<span data-ttu-id="f99e9-109">Un enfoque sería modificar los ejemplos PRTDemo y PRTCmdLine para calcular un vector de transferencia en cada textura en una parametrización de una superficie.</span><span class="sxs-lookup"><span data-stu-id="f99e9-109">One approach would be to modify the PRTDemo and PRTCmdLine samples to compute a transfer vector at every texel in a parameterization of a surface.</span></span> <span data-ttu-id="f99e9-110">Para hacerlo:</span><span class="sxs-lookup"><span data-stu-id="f99e9-110">To do this:</span></span>

1.  <span data-ttu-id="f99e9-111">Modifique la llamada a [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) para extraer las coordenadas de textura de la malla (ExtractUVs debe ser **true**)</span><span class="sxs-lookup"><span data-stu-id="f99e9-111">Modify the call to [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) to extract texture coordinates from the mesh (ExtractUVs must be **TRUE**)</span></span>
2.  <span data-ttu-id="f99e9-112">Reemplace las llamadas a [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) por [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) con el mismo tamaño de textura.</span><span class="sxs-lookup"><span data-stu-id="f99e9-112">Replace [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) calls with [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) using the same texture size.</span></span>

<span data-ttu-id="f99e9-113">Todos los métodos de ID3DXPRTEngine funcionan con simulaciones por textura, excepto: ComputeBounceAdaptive, ComputeSSAdaptive, Compute y ComputeDirectLightingSHAdaptive.</span><span class="sxs-lookup"><span data-stu-id="f99e9-113">All ID3DXPRTEngine methods work with per-texel simulations except for: ComputeBounceAdaptive, ComputeSSAdaptive, ComputeSS, and ComputeDirectLightingSHAdaptive.</span></span> <span data-ttu-id="f99e9-114">Aunque la simulación de espacio de textura generará el resultado correcto, a menudo puede ser bastante lento, ya que lo más probable es que el cálculo de los vectores de transferencia a una alta densidad.</span><span class="sxs-lookup"><span data-stu-id="f99e9-114">While texture-space simulation will generate the correct result, it can often be fairly slow since it will most likely be computing transfer vectors at a high density.</span></span>

<span data-ttu-id="f99e9-115">Otro enfoque consiste en calcular una simulación de PRT adaptable por vértice (con coordenadas de textura que se usarán para los datos por textura) y, a continuación, llamar a [**ID3DXPRTEngine:: ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (mediante un búfer de salida creado con [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) en la resolución adecuada).</span><span class="sxs-lookup"><span data-stu-id="f99e9-115">Another approach is to compute an adaptive per-vertex PRT simulation (with texture coordinates that will be used for the per-texel data) and then call [**ID3DXPRTEngine::ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (using an output buffer created using [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) at the appropriate resolution).</span></span> <span data-ttu-id="f99e9-116">Esto funciona con toda la funcionalidad de D3DX PRT en el SDK y a menudo puede ser mucho más eficaz que calcular directamente un búfer de transferencia por textura.</span><span class="sxs-lookup"><span data-stu-id="f99e9-116">This works with all D3DX PRT functionality in the SDK and can often be much more efficient than directly computing a per-texel transfer buffer.</span></span>

## <a name="runtime-calculations"></a><span data-ttu-id="f99e9-117">Cálculos en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="f99e9-117">Runtime Calculations</span></span>

<span data-ttu-id="f99e9-118">Si se usa un solo clúster, los resultados se pueden filtrar y mapas MIP como cualquier otra textura y el sombreador de píxeles es idéntico al código del sombreador de vértices que se distribuye con PRTDemo.</span><span class="sxs-lookup"><span data-stu-id="f99e9-118">If a single cluster is used the results can be filtered and mip-mapped like any other texture and the pixel shader is identical to the vertex shader code that ships with PRTDemo.</span></span>

<span data-ttu-id="f99e9-119">Si la compresión genera varios clústeres, no se pueden filtrar o adquierer los datos porque los índices de agrupación en clústeres no son continuos.</span><span class="sxs-lookup"><span data-stu-id="f99e9-119">If compression generates multiple clusters, you cannot filter or mipmap the data because clustering indexes are not continuous.</span></span> <span data-ttu-id="f99e9-120">Estas son algunas alternativas para administrar datos en clúster múltiple:</span><span class="sxs-lookup"><span data-stu-id="f99e9-120">Here are some alternatives for handling multi-clustered data:</span></span>

-   <span data-ttu-id="f99e9-121">Realice todo el filtrado en el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="f99e9-121">Do all of the filtering yourself in the pixel shader.</span></span> <span data-ttu-id="f99e9-122">Desafortunadamente, esto generalmente no es práctico por motivos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f99e9-122">Unfortunately, this is generally impractical for performance reasons.</span></span>
-   <span data-ttu-id="f99e9-123">Si las texturas tienen texturas de baja resolución no asignadas a MIP (es decir, mapas ligeros), lo más probable es que solo calcule la iluminación directamente en el espacio de textura, donde no se producirá ningún filtrado y represente el objeto con una textura sombreada.</span><span class="sxs-lookup"><span data-stu-id="f99e9-123">If the textures are low resolution non mip-mapped textures (ie: light maps), it is most likely more efficient to just compute the lighting directly in texture space - where no filtering will occur, and render the object with a shaded texture.</span></span> <span data-ttu-id="f99e9-124">Es esencialmente un mapa dinámico de luz que se crea completamente en la GPU.</span><span class="sxs-lookup"><span data-stu-id="f99e9-124">This is essentially a dynamic light map that is created entirely on the GPU.</span></span>
-   <span data-ttu-id="f99e9-125">Si se usa un Atlas de textura (consulte [uso de UVAtlas (Direct3D 9)](using-uvatlas.md)), puede agrupar manualmente la escena con todos los vectores de transferencia de un componente conectado en el espacio de textura en el mismo clúster.</span><span class="sxs-lookup"><span data-stu-id="f99e9-125">If a texture atlas is used (see [Using UVAtlas (Direct3D 9)](using-uvatlas.md)), you could manually cluster the scene by having all transfer vectors in a connected component in texture space be in the same cluster.</span></span> <span data-ttu-id="f99e9-126">De este modo, puede filtrar la textura porque todos los textura a los que se tiene acceso estarán en el mismo clúster mediante la construcción.</span><span class="sxs-lookup"><span data-stu-id="f99e9-126">This way you can filter the texture because all texels accessed would be in the same cluster by construction.</span></span> <span data-ttu-id="f99e9-127">El identificador de clúster para una esfera determinada podría propagarse desde el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="f99e9-127">The cluster ID for a given face could be propagated from the vertex shader.</span></span>

<span data-ttu-id="f99e9-128">Los sombreadores de píxeles tienen muchos menos registros constantes que no se pueden indizar, por lo que el sombreador de píxeles es algo diferente que el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="f99e9-128">Pixel shaders have much fewer constant registers that cannot be indexed, so the pixel shader is somewhat different than the vertex shader.</span></span> <span data-ttu-id="f99e9-129">Almacenar el trabajo por clúster en una textura dinámica de baja resolución y usar cargas de textura sería la manera más eficaz de representar cuando se usan varios clústeres.</span><span class="sxs-lookup"><span data-stu-id="f99e9-129">Storing the per-cluster work in a low resolution dynamic texture and using texture loads would be the most efficient way to render when using multiple clusters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f99e9-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f99e9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f99e9-131">Transferencia Radiance precalculada</span><span class="sxs-lookup"><span data-stu-id="f99e9-131">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> <dt>

<span data-ttu-id="f99e9-132">[Ejemplo de demostración de PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="f99e9-132">[PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)</span></span>
</dt> <dt>

<span data-ttu-id="f99e9-133">[Simulador PRT (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="f99e9-133">[PRT Simulator (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 



