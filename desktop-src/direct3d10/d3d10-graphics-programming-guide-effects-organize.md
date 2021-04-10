---
description: 'Con Direct3D 10, el estado del efecto para ciertas fases de canalización se organiza mediante las siguientes estructuras:'
ms.assetid: 674ed278-102c-43da-a6bf-58e084df151e
title: Organización del estado de un efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79cbea90c4d42d0a24ec7e35815616bf6698f72f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152936"
---
# <a name="organizing-state-in-an-effect-direct3d-10"></a><span data-ttu-id="d8d20-103">Organización del estado de un efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d8d20-103">Organizing State in an Effect (Direct3D 10)</span></span>

<span data-ttu-id="d8d20-104">Con Direct3D 10, el estado del efecto para ciertas fases de canalización se organiza mediante las siguientes estructuras:</span><span class="sxs-lookup"><span data-stu-id="d8d20-104">With Direct3D 10, effect state for certain pipeline stages is organized by the following structures:</span></span>



| <span data-ttu-id="d8d20-105">Estado de canalización</span><span class="sxs-lookup"><span data-stu-id="d8d20-105">Pipeline State</span></span>  | <span data-ttu-id="d8d20-106">Estructura</span><span class="sxs-lookup"><span data-stu-id="d8d20-106">Structure</span></span>                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d20-107">Ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="d8d20-107">Input Assembler</span></span> | [<span data-ttu-id="d8d20-108">**\_Descripción del \_ elemento de entrada D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="d8d20-108">**D3D10\_INPUT\_ELEMENT\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| <span data-ttu-id="d8d20-109">Rasterización</span><span class="sxs-lookup"><span data-stu-id="d8d20-109">Rasterization</span></span>   | [<span data-ttu-id="d8d20-110">**Descripción de D3D10 \_ rasterizador \_**</span><span class="sxs-lookup"><span data-stu-id="d8d20-110">**D3D10\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| <span data-ttu-id="d8d20-111">Fusión de salida</span><span class="sxs-lookup"><span data-stu-id="d8d20-111">Output Merger</span></span>   | <span data-ttu-id="d8d20-112">[**D3D10 \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) Descripción de la [ **\_ Galería de \_ símbolos \_ de profundidad** de Blend y D3D10](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="d8d20-112">[**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) and [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |



 

<span data-ttu-id="d8d20-113">En el caso de las fases del sombreador, en las que el número de cambios de Estado debe ser más controlado por una aplicación, el estado se ha dividido en el estado del búfer constante, el estado del muestrario y el estado del recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8d20-113">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, and shader resource state.</span></span> <span data-ttu-id="d8d20-114">Esto permite que una aplicación que se ha diseñado cuidadosamente para actualizar solo el estado que está cambiando, lo que mejora el rendimiento al reducir la cantidad de datos que se deben pasar a la GPU.</span><span class="sxs-lookup"><span data-stu-id="d8d20-114">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="d8d20-115">¿Cómo se organiza el estado de la canalización en un efecto?</span><span class="sxs-lookup"><span data-stu-id="d8d20-115">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="d8d20-116">La respuesta es que el orden no importa.</span><span class="sxs-lookup"><span data-stu-id="d8d20-116">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="d8d20-117">No es necesario que las variables globales se encuentren en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="d8d20-117">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="d8d20-118">Sin embargo, todos los ejemplos del SDK siguen el mismo orden, ya que se recomienda organizar los datos de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="d8d20-118">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="d8d20-119">Por lo tanto, se trata de una breve descripción de la ordenación de datos en los ejemplos del SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="d8d20-119">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="d8d20-120">Variables globales</span><span class="sxs-lookup"><span data-stu-id="d8d20-120">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="d8d20-121">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="d8d20-121">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="d8d20-122">Técnicas y pases</span><span class="sxs-lookup"><span data-stu-id="d8d20-122">Techniques and Passes</span></span>](#techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="d8d20-123">Variables globales</span><span class="sxs-lookup"><span data-stu-id="d8d20-123">Global Variables</span></span>

<span data-ttu-id="d8d20-124">Al igual que la práctica estándar de C, las variables globales se declaran en primer lugar, en la parte superior del archivo.</span><span class="sxs-lookup"><span data-stu-id="d8d20-124">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="d8d20-125">A menudo, se trata de variables que inicializará una aplicación y que, a continuación, se usarán en un efecto.</span><span class="sxs-lookup"><span data-stu-id="d8d20-125">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="d8d20-126">A veces se inicializan y nunca cambian, otras veces se actualizan cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="d8d20-126">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="d8d20-127">Al igual que las reglas de ámbito de la función de C, las variables de efecto que se declaran fuera del ámbito de las funciones de efecto son visibles a lo largo del efecto; cualquier variable declarada dentro de una función Effect solo es visible dentro de esa función.</span><span class="sxs-lookup"><span data-stu-id="d8d20-127">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="d8d20-128">Este es un ejemplo de las variables declaradas en BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="d8d20-128">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


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



<span data-ttu-id="d8d20-129">La sintaxis de las variables de efecto es más detallada en la [Sintaxis de variables de efecto (Direct3D 10)](d3d10-effect-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="d8d20-129">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 10)](d3d10-effect-variable-syntax.md).</span></span> <span data-ttu-id="d8d20-130">La sintaxis para los muestreadores de texturas de efectos es más detallada en el [tipo de muestra (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="d8d20-130">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="shaders"></a><span data-ttu-id="d8d20-131">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="d8d20-131">Shaders</span></span>

<span data-ttu-id="d8d20-132">Los sombreadores son pequeños programas ejecutables.</span><span class="sxs-lookup"><span data-stu-id="d8d20-132">Shaders are small executable programs.</span></span> <span data-ttu-id="d8d20-133">Puede pensar en los sombreadores como el estado del sombreador encapsulador, ya que el código de HLSL implementa la funcionalidad del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8d20-133">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="d8d20-134">La canalización usa tres tipos diferentes de sombreadores.</span><span class="sxs-lookup"><span data-stu-id="d8d20-134">The pipeline uses three different kinds of shaders.</span></span>

-   <span data-ttu-id="d8d20-135">Sombreadores de vértices: operan en datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="d8d20-135">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="d8d20-136">Un vértice en produce un vértice.</span><span class="sxs-lookup"><span data-stu-id="d8d20-136">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="d8d20-137">Sombreadores de geometría: operan en datos primitivos.</span><span class="sxs-lookup"><span data-stu-id="d8d20-137">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="d8d20-138">Un primitivo en puede producir 0, 1 o muchas primitivas.</span><span class="sxs-lookup"><span data-stu-id="d8d20-138">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="d8d20-139">Sombreadores de píxeles: operan en datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="d8d20-139">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="d8d20-140">Un píxel en produce 1 píxel de salida (a menos que se represente el píxel de una representación).</span><span class="sxs-lookup"><span data-stu-id="d8d20-140">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="d8d20-141">Los sombreadores son funciones locales y siguen las reglas de función de estilo C.</span><span class="sxs-lookup"><span data-stu-id="d8d20-141">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="d8d20-142">Cuando se compila un efecto, cada sombreador se compila y se almacena internamente un puntero a cada función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8d20-142">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="d8d20-143">Se devuelve una interfaz ID3D10Effect cuando la compilación se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8d20-143">An ID3D10Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="d8d20-144">En este momento, el efecto compilado está en un formato intermedio.</span><span class="sxs-lookup"><span data-stu-id="d8d20-144">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="d8d20-145">Para obtener más información sobre los sombreadores compilados, debe usar la reflexión del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8d20-145">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="d8d20-146">Esto es esencialmente como pedir al Runtime que descompile los sombreadores y devolver información sobre el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8d20-146">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


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



<span data-ttu-id="d8d20-147">La sintaxis de los sombreadores de efectos es más detallada en la sintaxis de la [función de efecto (Direct3D 10)](d3d10-effect-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="d8d20-147">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 10)](d3d10-effect-function-syntax.md).</span></span>

## <a name="techniques-and-passes"></a><span data-ttu-id="d8d20-148">Técnicas y pases</span><span class="sxs-lookup"><span data-stu-id="d8d20-148">Techniques and Passes</span></span>

<span data-ttu-id="d8d20-149">Una técnica es una colección de pasos de representación (debe haber al menos un paso).</span><span class="sxs-lookup"><span data-stu-id="d8d20-149">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="d8d20-150">Cada paso de efecto (que es similar en el ámbito a un solo paso en un bucle de representación) define el estado del sombreador y cualquier otro estado de canalización necesario para representar la geometría.</span><span class="sxs-lookup"><span data-stu-id="d8d20-150">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="d8d20-151">Este es un ejemplo de una técnica (que incluye una pasada) de BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="d8d20-151">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


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
```



<span data-ttu-id="d8d20-152">La sintaxis de los sombreadores de efectos es más detallada en la sintaxis de la [técnica de efectos (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="d8d20-152">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8d20-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8d20-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8d20-154">Efectos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d8d20-154">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
