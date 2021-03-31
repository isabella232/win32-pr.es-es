---
description: El modelo de sombreador de vértices 3,0 admite la búsqueda de texturas en el sombreador de vértices mediante la instrucción texldl-vs Texture Load.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Texturas de vértices en vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e8e7bbf7e1ae9764fe5b30647f318dfaeb3ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806518"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a><span data-ttu-id="bf568-103">Texturas de vértices en vs \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf568-103">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>

<span data-ttu-id="bf568-104">El modelo de sombreador de vértices 3,0 admite la búsqueda de texturas en el sombreador de vértices mediante la instrucción [texldl-vs](../direct3dhlsl/texldl---vs.md) Texture Load.</span><span class="sxs-lookup"><span data-stu-id="bf568-104">The vertex shader 3.0 model supports texture lookup in the vertex shader using the [texldl - vs](../direct3dhlsl/texldl---vs.md) texture load statement.</span></span> <span data-ttu-id="bf568-105">El motor de vértices contiene cuatro fases de muestra de textura, denominadas [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 y D3DVERTEXTEXTURESAMPLER3.</span><span class="sxs-lookup"><span data-stu-id="bf568-105">The vertex engine contains four texture sampler stages, named [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2, and D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="bf568-106">Se diferencian de las muestras de textura y muestra del mapa de desplazamiento en el motor de píxeles.</span><span class="sxs-lookup"><span data-stu-id="bf568-106">These are distinct from the displacement map sampler and texture samplers in the pixel engine.</span></span>

<span data-ttu-id="bf568-107">Para muestras de texturas establecidas en esas cuatro fases, puede usar el motor de vértices y programar las fases con el método [**CheckDeviceFormat**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="bf568-107">To sample textures set at those four stages, you can use the vertex engine and program the stages with the [**CheckDeviceFormat**](/windows/desktop/api) method.</span></span> <span data-ttu-id="bf568-108">Establezca texturas en esas fases mediante [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), con el índice de fase [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) a través de D3DVERTEXTEXTURESAMPLER3.</span><span class="sxs-lookup"><span data-stu-id="bf568-108">Set textures at those stages using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), with the stage index [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) through D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="bf568-109">Se ha introducido un nuevo registro en el sombreador de vértices, el registro de muestra (como en PS \_ 2 \_ 0), que representa la muestra de textura de vértices.</span><span class="sxs-lookup"><span data-stu-id="bf568-109">A new register has been introduced in the vertex shader, the sampler register (like in ps\_2\_0), which represents the vertex texture sampler.</span></span> <span data-ttu-id="bf568-110">Este registro debe definirse en el sombreador antes de usarlo.</span><span class="sxs-lookup"><span data-stu-id="bf568-110">This register needs to be defined in the shader before using it.</span></span>

<span data-ttu-id="bf568-111">Una aplicación puede consultar si se admite un formato como textura de vértice llamando a [**CheckDeviceFormat**](/windows/desktop/api) con [ \_ \_ VERTEXTEXTURE de consulta D3DUSAGE](d3dusage-query.md).</span><span class="sxs-lookup"><span data-stu-id="bf568-111">An application can query if a format is supported as a vertex texture by calling [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE](d3dusage-query.md).</span></span>

> [!Note]  
> <span data-ttu-id="bf568-112">Se trata de una marca de consulta para que no se acepte en ninguna función de Createxxx.</span><span class="sxs-lookup"><span data-stu-id="bf568-112">This is a query flag so it is not accepted in any Createxxx function.</span></span> <span data-ttu-id="bf568-113">Una textura de vértice creada en el grupo predeterminado se puede establecer como una textura de píxeles y viceversa.</span><span class="sxs-lookup"><span data-stu-id="bf568-113">A vertex texture created in the default pool can be set as a pixel texture and vice versa.</span></span> <span data-ttu-id="bf568-114">Sin embargo, para usar el procesamiento de vértices de software, se debe crear la textura de vértices en el grupo de medios (independientemente de si se trata de un dispositivo de modo mixto o de un dispositivo de procesamiento de vértices de software).</span><span class="sxs-lookup"><span data-stu-id="bf568-114">However, to use the software vertex processing, the vertex texture must be created in the scratch pool (no matter if it is a mixed-mode device or a software vertex processing device).</span></span>

 

<span data-ttu-id="bf568-115">La funcionalidad es idéntica a las texturas de píxeles, excepto para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bf568-115">The functionality is identical to the pixel textures, except for the following:</span></span>

-   <span data-ttu-id="bf568-116">No se admite el filtrado de texturas anisotrópico, por lo que D3DSAMP \_ MAXANISOTROPY se pasa por alto y \_ no se puede establecer D3DTEXF anisotrópico para ampliar o minimizar en estas fases.</span><span class="sxs-lookup"><span data-stu-id="bf568-116">Anisotropic texture filtering is not supported, hence D3DSAMP\_MAXANISOTROPY is ignored and D3DTEXF\_ANISOTROPIC cannot be set for magnify, or minify for these stages.</span></span>
-   <span data-ttu-id="bf568-117">La velocidad de la información de los cambios no está disponible; por lo tanto, la aplicación tiene que calcular el nivel de detalle y proporcionar esa información como un parámetro a [texldl-vs](../direct3dhlsl/texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="bf568-117">Rate of change information is not available, hence the application has to compute the level of detail and provide that information as a parameter to [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="bf568-118">Entre las restricciones se incluyen:</span><span class="sxs-lookup"><span data-stu-id="bf568-118">Restrictions include:</span></span>

-   <span data-ttu-id="bf568-119">Como en los sombreadores de píxeles, si se admiten las texturas de múltiples elementos, \_ se usa D3DSAMP ELEMENTINDEX para averiguar de qué elemento se va a muestrear.</span><span class="sxs-lookup"><span data-stu-id="bf568-119">As in pixel shaders, if multielement textures are supported, D3DSAMP\_ELEMENTINDEX is used to figure out which element to sample from.</span></span>
-   <span data-ttu-id="bf568-120">El estado D3DSAMP \_ DMAPOFFSET se omite en estas fases.</span><span class="sxs-lookup"><span data-stu-id="bf568-120">The state D3DSAMP\_DMAPOFFSET is ignored for these stages.</span></span>
-   <span data-ttu-id="bf568-121">Use [**CheckDeviceFormat**](/windows/desktop/api) con [D3DUSAGE \_ query \_ VERTEXTEXTURE "](d3dusage-query.md) para consultar una textura y ver si se puede usar como textura de vértice.</span><span class="sxs-lookup"><span data-stu-id="bf568-121">Use [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE"](d3dusage-query.md) to query a texture to see if it can be used as a vertex texture.</span></span>
-   <span data-ttu-id="bf568-122">VertexTextureFilterCaps indica qué tipo de filtros se permiten en los muestreadores de textura de vértices.</span><span class="sxs-lookup"><span data-stu-id="bf568-122">VertexTextureFilterCaps indicates what kind of filters are allowed at the vertex texture samplers.</span></span> <span data-ttu-id="bf568-123">[D3DPTFILTERCAPS \_ MINFANISOTROPIC](d3dptfiltercaps.md) y D3DPTFILTERCAPS \_ MAGFANISOTROPIC no se permiten.</span><span class="sxs-lookup"><span data-stu-id="bf568-123">[D3DPTFILTERCAPS\_MINFANISOTROPIC](d3dptfiltercaps.md) and D3DPTFILTERCAPS\_MAGFANISOTROPIC are disallowed.</span></span>

## <a name="sampling-stage-registers"></a><span data-ttu-id="bf568-124">Registros de fase de muestreo</span><span class="sxs-lookup"><span data-stu-id="bf568-124">Sampling Stage Registers</span></span>

<span data-ttu-id="bf568-125">Un registro de fase de muestreo identifica una unidad de muestreo que se puede utilizar en las instrucciones de carga de textura.</span><span class="sxs-lookup"><span data-stu-id="bf568-125">A sampling stage register identifies a sampling unit that can be used in texture load statements.</span></span> <span data-ttu-id="bf568-126">Una unidad de muestreo corresponde a la fase de muestreo de textura, encapsulando el estado específico del muestreo proporcionado en [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="bf568-126">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided in [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span>

<span data-ttu-id="bf568-127">Cada muestra identifica de forma única una superficie de textura única que se establece en la muestra correspondiente mediante [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="bf568-127">Each sampler uniquely identifies a single texture surface that is set to the corresponding sampler using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="bf568-128">Sin embargo, la misma superficie de textura se puede establecer en varios muestreadores.</span><span class="sxs-lookup"><span data-stu-id="bf568-128">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="bf568-129">En el momento de dibujar, no se puede establecer una textura simultáneamente como un destino de representación y una textura en una fase.</span><span class="sxs-lookup"><span data-stu-id="bf568-129">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="bf568-130">Dado \_ que vs 3 \_ 0 admite cuatro muestreadores, se pueden leer hasta cuatro superficies de textura desde en una sola fase del sombreador.</span><span class="sxs-lookup"><span data-stu-id="bf568-130">Because vs\_3\_0 supports four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="bf568-131">Un registro de muestra solo puede aparecer como un argumento en la instrucción de carga de textura: [texldl-vs](../direct3dhlsl/texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="bf568-131">A sampler register might appear only as an argument in the texture load statement: [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="bf568-132">En vs \_ 3 \_ 0, si utiliza una muestra, debe declararse al principio del programa del sombreador mediante la [DCL \_ samplerType (SM3-vs ASM)](../direct3dhlsl/dcl-samplertype---vs.md) (como en PS \_ 2 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="bf568-132">In vs\_3\_0, if you use a sampler, it must be declared at the beginning of the shader program, using the [dcl\_samplerType (sm3 - vs asm)](../direct3dhlsl/dcl-samplertype---vs.md) (as in ps\_2\_0).</span></span>

## <a name="software-processing"></a><span data-ttu-id="bf568-133">Procesamiento de software</span><span class="sxs-lookup"><span data-stu-id="bf568-133">Software Processing</span></span>

<span data-ttu-id="bf568-134">Esta característica se admitirá en el procesamiento de vértices de software.</span><span class="sxs-lookup"><span data-stu-id="bf568-134">This feature will be supported in software vertex processing.</span></span> <span data-ttu-id="bf568-135">Los tipos de filtro específicos admitidos se pueden comprobar llamando a [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) y comprobando VertexTextureFilterCaps.</span><span class="sxs-lookup"><span data-stu-id="bf568-135">The specific filter types supported can be checked by calling [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) and checking VertexTextureFilterCaps.</span></span> <span data-ttu-id="bf568-136">Todos los formatos de textura publicados se admitirán como texturas de vértice en el procesamiento de vértices de software.</span><span class="sxs-lookup"><span data-stu-id="bf568-136">All published texture formats will be supported as vertex textures in software vertex processing.</span></span>

<span data-ttu-id="bf568-137">Las aplicaciones pueden comprobar si se admite un formato de textura determinado en el modo de procesamiento de vértices de software llamando a [**CheckDeviceFormat**](/windows/desktop/api) y proporcionando (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) como uso.</span><span class="sxs-lookup"><span data-stu-id="bf568-137">Applications can check if a particular texture format is supported in the software vertex processing mode by calling [**CheckDeviceFormat**](/windows/desktop/api) and providing (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md)) as usage.</span></span> <span data-ttu-id="bf568-138">Todos los formatos se admiten para el procesamiento de vértices de software.</span><span class="sxs-lookup"><span data-stu-id="bf568-138">All formats are supported for software vertex processing.</span></span> <span data-ttu-id="bf568-139">El grupo temporal es necesario para el procesamiento de vértices de software.</span><span class="sxs-lookup"><span data-stu-id="bf568-139">The scratch pool is required for software vertex processing.</span></span>

## <a name="api-changes"></a><span data-ttu-id="bf568-140">Cambios de la API</span><span class="sxs-lookup"><span data-stu-id="bf568-140">API Changes</span></span>


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a><span data-ttu-id="bf568-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf568-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf568-142">Canalización de vértices</span><span class="sxs-lookup"><span data-stu-id="bf568-142">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
