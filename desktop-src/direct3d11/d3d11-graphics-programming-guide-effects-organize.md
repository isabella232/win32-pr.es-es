---
title: Organización del estado de un efecto (Direct3D 11)
description: Con Direct3D 11, el estado del efecto para ciertas fases de canalización se organiza por estructuras.
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a0523dd8abdabde29a5485b8d3b1e6d13b9429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997104"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a><span data-ttu-id="a6ee6-103">Organización del estado de un efecto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="a6ee6-103">Organizing State in an Effect (Direct3D 11)</span></span>

<span data-ttu-id="a6ee6-104">Con Direct3D 11, el estado del efecto para ciertas fases de canalización se organiza por estructuras.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-104">With Direct3D 11, effect state for certain pipeline stages is organized by structures.</span></span> <span data-ttu-id="a6ee6-105">Estas son las estructuras:</span><span class="sxs-lookup"><span data-stu-id="a6ee6-105">Here are the structures:</span></span>



| <span data-ttu-id="a6ee6-106">Estado de canalización</span><span class="sxs-lookup"><span data-stu-id="a6ee6-106">Pipeline State</span></span> | <span data-ttu-id="a6ee6-107">Estructura</span><span class="sxs-lookup"><span data-stu-id="a6ee6-107">Structure</span></span>                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ee6-108">Rasterización</span><span class="sxs-lookup"><span data-stu-id="a6ee6-108">Rasterization</span></span>  | [<span data-ttu-id="a6ee6-109">**Descripción de D3D11 \_ rasterizador \_**</span><span class="sxs-lookup"><span data-stu-id="a6ee6-109">**D3D11\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| <span data-ttu-id="a6ee6-110">Fusión de salida</span><span class="sxs-lookup"><span data-stu-id="a6ee6-110">Output Merger</span></span>  | <span data-ttu-id="a6ee6-111">[**D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) Descripción de la [ **\_ Galería de \_ símbolos \_ de profundidad** de Blend y D3D11](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="a6ee6-111">[**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) and [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span> |
| <span data-ttu-id="a6ee6-112">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="a6ee6-112">Shaders</span></span>        | <span data-ttu-id="a6ee6-113">Consulte a continuación</span><span class="sxs-lookup"><span data-stu-id="a6ee6-113">See below</span></span>                                                                                                          |



 

<span data-ttu-id="a6ee6-114">En el caso de las fases del sombreador, donde el número de cambios de Estado debe ser más controlado por una aplicación, el estado se ha dividido en el estado de búfer constante, el estado de muestra, el estado de los recursos del sombreador y el estado de vista de acceso desordenado (para los sombreadores de píxeles y de cálculo).</span><span class="sxs-lookup"><span data-stu-id="a6ee6-114">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, shader resource state, and unordered access view state (for pixel and compute shaders).</span></span> <span data-ttu-id="a6ee6-115">Esto permite que una aplicación que se ha diseñado cuidadosamente para actualizar solo el estado que está cambiando, lo que mejora el rendimiento al reducir la cantidad de datos que se deben pasar a la GPU.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-115">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="a6ee6-116">¿Cómo se organiza el estado de la canalización en un efecto?</span><span class="sxs-lookup"><span data-stu-id="a6ee6-116">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="a6ee6-117">La respuesta es que el orden no importa.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-117">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="a6ee6-118">No es necesario que las variables globales se encuentren en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-118">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="a6ee6-119">Sin embargo, todos los ejemplos del SDK siguen el mismo orden, ya que se recomienda organizar los datos de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-119">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="a6ee6-120">Por lo tanto, se trata de una breve descripción de la ordenación de datos en los ejemplos del SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-120">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="a6ee6-121">Variables globales</span><span class="sxs-lookup"><span data-stu-id="a6ee6-121">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="a6ee6-122">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="a6ee6-122">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="a6ee6-123">Grupos, técnicas y pases</span><span class="sxs-lookup"><span data-stu-id="a6ee6-123">Groups, Techniques, and Passes</span></span>](#groups-techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="a6ee6-124">Variables globales</span><span class="sxs-lookup"><span data-stu-id="a6ee6-124">Global Variables</span></span>

<span data-ttu-id="a6ee6-125">Al igual que la práctica estándar de C, las variables globales se declaran en primer lugar, en la parte superior del archivo.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-125">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="a6ee6-126">A menudo, se trata de variables que inicializará una aplicación y que, a continuación, se usarán en un efecto.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-126">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="a6ee6-127">A veces se inicializan y nunca cambian, otras veces se actualizan cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-127">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="a6ee6-128">Al igual que las reglas de ámbito de la función de C, las variables de efecto que se declaran fuera del ámbito de las funciones de efecto son visibles a lo largo del efecto; cualquier variable declarada dentro de una función Effect solo es visible dentro de esa función.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-128">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="a6ee6-129">Este es un ejemplo de las variables declaradas en BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-129">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix


// Texture samplers
SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};
```



<span data-ttu-id="a6ee6-130">La sintaxis de las variables de efecto es más detallada en la [Sintaxis de variables de efectos (Direct3D 11)](d3d11-effect-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="a6ee6-130">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 11)](d3d11-effect-variable-syntax.md).</span></span> <span data-ttu-id="a6ee6-131">La sintaxis para los muestreadores de texturas de efectos es más detallada en el [tipo de muestra (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span><span class="sxs-lookup"><span data-stu-id="a6ee6-131">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

## <a name="shaders"></a><span data-ttu-id="a6ee6-132">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="a6ee6-132">Shaders</span></span>

<span data-ttu-id="a6ee6-133">Los sombreadores son pequeños programas ejecutables.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-133">Shaders are small executable programs.</span></span> <span data-ttu-id="a6ee6-134">Puede pensar en los sombreadores como el estado del sombreador encapsulador, ya que el código de HLSL implementa la funcionalidad del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-134">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="a6ee6-135">Los gráficos se canalizan hasta cinco tipos diferentes de sombreadores.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-135">The graphics pipeline up to five different kinds of shaders.</span></span>

-   <span data-ttu-id="a6ee6-136">Sombreadores de vértices: operan en datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-136">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="a6ee6-137">Un vértice en produce un vértice.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-137">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="a6ee6-138">Sombreadores de casco: operan en datos de revisión.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-138">Hull shaders - Operate on patch data.</span></span> <span data-ttu-id="a6ee6-139">Fase de punto de control: una invocación produce un punto de control; Para cada bifurcación y fases de combinación: una revisión produce una cantidad de datos constantes de revisión.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-139">Control Point Phase: one invocation yields one control point; For each Fork and Join Phases: one patch yields some amount of patch constant data.</span></span>
-   <span data-ttu-id="a6ee6-140">Sombreadores de dominio: operan en datos primitivos.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-140">Domain shaders - Operate on primitive data.</span></span> <span data-ttu-id="a6ee6-141">Un primitivo puede producir 0, 1 o muchos primitivos.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-141">One primitive may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="a6ee6-142">Sombreadores de geometría: operan en datos primitivos.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-142">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="a6ee6-143">Un primitivo en puede producir 0, 1 o muchas primitivas.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-143">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="a6ee6-144">Sombreadores de píxeles: operan en datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-144">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="a6ee6-145">Un píxel en produce 1 píxel de salida (a menos que se represente el píxel de una representación).</span><span class="sxs-lookup"><span data-stu-id="a6ee6-145">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="a6ee6-146">La canalización del sombreador de cálculo usa un sombreador:</span><span class="sxs-lookup"><span data-stu-id="a6ee6-146">The compute shader pipeline uses one shader:</span></span>

-   <span data-ttu-id="a6ee6-147">Sombreadores de cálculo: operan en cualquier tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-147">Compute shaders - Operate on any kind of data.</span></span> <span data-ttu-id="a6ee6-148">La salida es independiente del número de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-148">The output is independent of the number of threads.</span></span>

<span data-ttu-id="a6ee6-149">Los sombreadores son funciones locales y siguen las reglas de función de estilo C.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-149">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="a6ee6-150">Cuando se compila un efecto, cada sombreador se compila y se almacena internamente un puntero a cada función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-150">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="a6ee6-151">Se devuelve una interfaz ID3D11Effect cuando la compilación se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-151">An ID3D11Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="a6ee6-152">En este momento, el efecto compilado está en un formato intermedio.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-152">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="a6ee6-153">Para obtener más información sobre los sombreadores compilados, debe usar la reflexión del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-153">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="a6ee6-154">Esto es esencialmente como pedir al Runtime que descompile los sombreadores y devolver información sobre el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-154">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
 
    ....    
    
    return Output;    
}


struct PS_OUTPUT
{
    float4 RGBColor : SV_Target;  // Pixel color
};

PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    ....

    return Output;
}
```



<span data-ttu-id="a6ee6-155">La sintaxis de los sombreadores de efectos es más detallada en la sintaxis de la [función de efecto (Direct3D 11)](d3d11-effect-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="a6ee6-155">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 11)](d3d11-effect-function-syntax.md).</span></span>

## <a name="groups-techniques-and-passes"></a><span data-ttu-id="a6ee6-156">Grupos, técnicas y pases</span><span class="sxs-lookup"><span data-stu-id="a6ee6-156">Groups, Techniques, and Passes</span></span>

<span data-ttu-id="a6ee6-157">Un grupo es una colección de técnicas.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-157">A group is a collection of techniques.</span></span> <span data-ttu-id="a6ee6-158">Una técnica es una colección de pasos de representación (debe haber al menos un paso).</span><span class="sxs-lookup"><span data-stu-id="a6ee6-158">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="a6ee6-159">Cada paso de efecto (que es similar en el ámbito a un solo paso en un bucle de representación) define el estado del sombreador y cualquier otro estado de canalización necesario para representar la geometría.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-159">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="a6ee6-160">Los grupos son opcionales.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-160">Groups are optional.</span></span> <span data-ttu-id="a6ee6-161">Hay un único grupo sin nombre que engloba todas las técnicas globales.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-161">There is a single, unnamed group which encompasses all global techniques.</span></span> <span data-ttu-id="a6ee6-162">Todos los demás grupos deben tener nombre.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-162">All other groups must be named.</span></span>

<span data-ttu-id="a6ee6-163">Este es un ejemplo de una técnica (que incluye una pasada) de BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="a6ee6-163">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}

fxgroup g0
{
    technique11 RunComputeShader
    {
        pass P0
        {
            SetComputeShader( CompileShader( cs_5_0, CS() ) );
        }
    }
}

```



<span data-ttu-id="a6ee6-164">La sintaxis de los sombreadores de efectos es más detallada en la sintaxis de la [técnica de efectos (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="a6ee6-164">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6ee6-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6ee6-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6ee6-166">Efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="a6ee6-166">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 