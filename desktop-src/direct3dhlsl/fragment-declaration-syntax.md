---
title: Sintaxis de declaración de fragmentos (Direct3D 9 HLSL)
description: Cada función de Microsoft High Level Shader Language (HLSL) se puede convertir en un fragmento de sombreador con la adición de una declaración de fragmento.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98e609820e67cc3ede6c3e280f63513850fed364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077944"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="ca099-103">Sintaxis de declaración de fragmentos (Direct3D 9 HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca099-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="ca099-104">Cada función de Microsoft High Level Shader Language (HLSL) se puede convertir en un fragmento de sombreador con la adición de una declaración de fragmento.</span><span class="sxs-lookup"><span data-stu-id="ca099-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca099-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca099-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="ca099-106">donde:</span><span class="sxs-lookup"><span data-stu-id="ca099-106">where:</span></span>



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca099-107">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="ca099-107">fragmentKeyword</span></span>   | <span data-ttu-id="ca099-108">Palabra clave required.</span><span class="sxs-lookup"><span data-stu-id="ca099-108">Required keyword.</span></span> <span data-ttu-id="ca099-109">Pixelfragment o vertexfragment.</span><span class="sxs-lookup"><span data-stu-id="ca099-109">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="ca099-110">FragmentName</span><span class="sxs-lookup"><span data-stu-id="ca099-110">FragmentName</span></span>      | <span data-ttu-id="ca099-111">Cadena de texto ASCII que especifica el nombre del fragmento compilado.</span><span class="sxs-lookup"><span data-stu-id="ca099-111">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="ca099-112">compilar \_ fragmento</span><span class="sxs-lookup"><span data-stu-id="ca099-112">compile\_fragment</span></span> | <span data-ttu-id="ca099-113">Palabra clave required.</span><span class="sxs-lookup"><span data-stu-id="ca099-113">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="ca099-114">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="ca099-114">shaderProfile</span></span>     | <span data-ttu-id="ca099-115">Modelo de sombreador con el que se va a realizar la compilación.</span><span class="sxs-lookup"><span data-stu-id="ca099-115">The shader model to compile against.</span></span> <span data-ttu-id="ca099-116">Cualquier perfil de sombreador de vértices válido (vea [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) o el perfil del sombreador de píxeles (consulte [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span><span class="sxs-lookup"><span data-stu-id="ca099-116">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="ca099-117">Nombrefunción ()</span><span class="sxs-lookup"><span data-stu-id="ca099-117">FunctionName()</span></span>    | <span data-ttu-id="ca099-118">El nombre de la función de sombreador, seguido de paréntesis.</span><span class="sxs-lookup"><span data-stu-id="ca099-118">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="ca099-119">Los parámetros de fragmento compartidos se marcan agregando un \_ prefijo "r" a su semántica.</span><span class="sxs-lookup"><span data-stu-id="ca099-119">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



<span data-ttu-id="ca099-120">En este ejemplo, la semántica de r \_ PosWorld y r \_ NormalWorld identifica que estos dos parámetros son parámetros compartidos entre otros fragmentos.</span><span class="sxs-lookup"><span data-stu-id="ca099-120">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="ca099-121">Fragment linker era una tecnología de Microsoft Direct3D 9 en D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="ca099-121">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="ca099-122">Fragment linker era una herramienta (Flink.exe), una API de D3DX 9 y una mejora de HLSL.</span><span class="sxs-lookup"><span data-stu-id="ca099-122">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="ca099-123">Fragment linker se quitó de la versión del SDK de DirectX 2009 de agosto.</span><span class="sxs-lookup"><span data-stu-id="ca099-123">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="ca099-124">Fragment linker nunca se aplica a Microsoft Direct3D 10, Microsoft Direct3D 10,1 o Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="ca099-124">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ca099-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca099-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca099-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca099-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 