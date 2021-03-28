---
title: Usar la fase Input-Assembler sin búferes
description: No es necesario crear y enlazar búferes si los sombreadores no requieren búferes. Esta sección contiene un ejemplo de sombreadores de vértices y píxeles simples que dibujan un solo triángulo.
ms.assetid: 84d24494-f2cb-4ca1-84fd-635e20f2c9ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3aa4c63176d184e1e67349149bd1f4044159e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983638"
---
# <a name="using-the-input-assembler-stage-without-buffers"></a><span data-ttu-id="5fe70-104">Usar la fase Input-Assembler sin búferes</span><span class="sxs-lookup"><span data-stu-id="5fe70-104">Using the Input-Assembler Stage without Buffers</span></span>

<span data-ttu-id="5fe70-105">No es necesario crear y enlazar búferes si los sombreadores no requieren búferes.</span><span class="sxs-lookup"><span data-stu-id="5fe70-105">Creating and binding buffers is not necessary if your shaders don't require buffers.</span></span> <span data-ttu-id="5fe70-106">Esta sección contiene un ejemplo de sombreadores de vértices y píxeles simples que dibujan un solo triángulo.</span><span class="sxs-lookup"><span data-stu-id="5fe70-106">This section contains an example of simple vertex and pixel shaders that draw a single triangle.</span></span>

-   [<span data-ttu-id="5fe70-107">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5fe70-107">Vertex Shader</span></span>](#vertex-shader)
-   [<span data-ttu-id="5fe70-108">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5fe70-108">Pixel Shader</span></span>](#pixel-shader)
-   [<span data-ttu-id="5fe70-109">Técnica</span><span class="sxs-lookup"><span data-stu-id="5fe70-109">Technique</span></span>](#technique)
-   [<span data-ttu-id="5fe70-110">Código de aplicación</span><span class="sxs-lookup"><span data-stu-id="5fe70-110">Application Code</span></span>](#application-code)
-   [<span data-ttu-id="5fe70-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5fe70-111">Related topics</span></span>](#related-topics)

## <a name="vertex-shader"></a><span data-ttu-id="5fe70-112">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5fe70-112">Vertex Shader</span></span>

<span data-ttu-id="5fe70-113">Por ejemplo, podría declarar un sombreador de vértices que cree sus propios vértices.</span><span class="sxs-lookup"><span data-stu-id="5fe70-113">For example, you could declare a vertex shader that creates its own vertices.</span></span>


```
struct VSIn
{
    uint vertexId : SV_VertexID;
};

struct VSOut
{
    float4 pos : SV_Position;
    float4 color : color;
};

VSOut VSmain(VSIn input)
{
    VSOut output;
    
    if (input.vertexId == 0)
        output.pos = float4(0.0, 0.5, 0.5, 1.0);
    else if (input.vertexId == 2)
        output.pos = float4(0.5, -0.5, 0.5, 1.0);
    else if (input.vertexId == 1)
        output.pos = float4(-0.5, -0.5, 0.5, 1.0);
    
    output.color = clamp(output.pos, 0, 1);
    
    return output;
}
```



## <a name="pixel-shader"></a><span data-ttu-id="5fe70-114">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5fe70-114">Pixel Shader</span></span>


```
// NoBuffer.fx
// Copyright (c) 2004 Microsoft Corporation. All rights reserved.
//

struct PSIn
{
    float4 pos : SV_Position;
    linear float4 color : color;
};

struct PSOut
{
    float4 color : SV_Target;
};


PSOut PSmain(PSIn input)
{
    PSOut output;
    
    output.color = input.color;
    
    return output;
}
```



## <a name="technique"></a><span data-ttu-id="5fe70-115">Técnica</span><span class="sxs-lookup"><span data-stu-id="5fe70-115">Technique</span></span>

<span data-ttu-id="5fe70-116">Una técnica es una colección de pasos de representación (debe haber al menos un paso).</span><span class="sxs-lookup"><span data-stu-id="5fe70-116">A technique is a collection of rendering passes (there must be at least one pass).</span></span>


```
VertexShader vsCompiled = CompileShader( vs_4_0, VSmain() );

technique10 t0
{
    pass p0
    {
        SetVertexShader( vsCompiled );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PSmain() ));
    }  
}
```



## <a name="application-code"></a><span data-ttu-id="5fe70-117">Código de aplicación</span><span class="sxs-lookup"><span data-stu-id="5fe70-117">Application Code</span></span>


```
m_pD3D11Device->IASetInputLayout( NULL );

m_pD3D11Device->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
    
ID3DX11EffectTechnique * pTech = NULL;
pTech = m_pEffect->GetTechniqueByIndex(0);
pTech->GetPassByIndex(iPass)->Apply(0);

m_pD3D11Device->Draw( 3, 0 );
```



## <a name="related-topics"></a><span data-ttu-id="5fe70-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5fe70-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fe70-119">Introducción con la fase de Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="5fe70-119">Getting Started with the Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> </dl>

 

 




