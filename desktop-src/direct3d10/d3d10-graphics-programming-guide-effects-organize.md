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
# <a name="organizing-state-in-an-effect-direct3d-10"></a>Organización del estado de un efecto (Direct3D 10)

Con Direct3D 10, el estado del efecto para ciertas fases de canalización se organiza mediante las siguientes estructuras:



| Estado de canalización  | Estructura                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| Ensamblador de entrada | [**\_Descripción del \_ elemento de entrada D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| Rasterización   | [**Descripción de D3D10 \_ rasterizador \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| Fusión de salida   | [**D3D10 \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) Descripción de la [ **\_ Galería de \_ símbolos \_ de profundidad** de Blend y D3D10](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |



 

En el caso de las fases del sombreador, en las que el número de cambios de Estado debe ser más controlado por una aplicación, el estado se ha dividido en el estado del búfer constante, el estado del muestrario y el estado del recurso de sombreador. Esto permite que una aplicación que se ha diseñado cuidadosamente para actualizar solo el estado que está cambiando, lo que mejora el rendimiento al reducir la cantidad de datos que se deben pasar a la GPU.

¿Cómo se organiza el estado de la canalización en un efecto?

La respuesta es que el orden no importa. No es necesario que las variables globales se encuentren en la parte superior. Sin embargo, todos los ejemplos del SDK siguen el mismo orden, ya que se recomienda organizar los datos de la misma manera. Por lo tanto, se trata de una breve descripción de la ordenación de datos en los ejemplos del SDK de DirectX.

-   [Variables globales](#global-variables)
-   [Sombreadores](#shaders)
-   [Técnicas y pases](#techniques-and-passes)

## <a name="global-variables"></a>Variables globales

Al igual que la práctica estándar de C, las variables globales se declaran en primer lugar, en la parte superior del archivo. A menudo, se trata de variables que inicializará una aplicación y que, a continuación, se usarán en un efecto. A veces se inicializan y nunca cambian, otras veces se actualizan cada fotograma. Al igual que las reglas de ámbito de la función de C, las variables de efecto que se declaran fuera del ámbito de las funciones de efecto son visibles a lo largo del efecto; cualquier variable declarada dentro de una función Effect solo es visible dentro de esa función.

Este es un ejemplo de las variables declaradas en BasicHLSL10. FX.


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



La sintaxis de las variables de efecto es más detallada en la [Sintaxis de variables de efecto (Direct3D 10)](d3d10-effect-variable-syntax.md). La sintaxis para los muestreadores de texturas de efectos es más detallada en el [tipo de muestra (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="shaders"></a>Sombreadores

Los sombreadores son pequeños programas ejecutables. Puede pensar en los sombreadores como el estado del sombreador encapsulador, ya que el código de HLSL implementa la funcionalidad del sombreador. La canalización usa tres tipos diferentes de sombreadores.

-   Sombreadores de vértices: operan en datos de vértices. Un vértice en produce un vértice.
-   Sombreadores de geometría: operan en datos primitivos. Un primitivo en puede producir 0, 1 o muchas primitivas.
-   Sombreadores de píxeles: operan en datos de píxeles. Un píxel en produce 1 píxel de salida (a menos que se represente el píxel de una representación).

Los sombreadores son funciones locales y siguen las reglas de función de estilo C. Cuando se compila un efecto, cada sombreador se compila y se almacena internamente un puntero a cada función de sombreador. Se devuelve una interfaz ID3D10Effect cuando la compilación se realiza correctamente. En este momento, el efecto compilado está en un formato intermedio.

Para obtener más información sobre los sombreadores compilados, debe usar la reflexión del sombreador. Esto es esencialmente como pedir al Runtime que descompile los sombreadores y devolver información sobre el código del sombreador.


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



La sintaxis de los sombreadores de efectos es más detallada en la sintaxis de la [función de efecto (Direct3D 10)](d3d10-effect-function-syntax.md).

## <a name="techniques-and-passes"></a>Técnicas y pases

Una técnica es una colección de pasos de representación (debe haber al menos un paso). Cada paso de efecto (que es similar en el ámbito a un solo paso en un bucle de representación) define el estado del sombreador y cualquier otro estado de canalización necesario para representar la geometría.

Este es un ejemplo de una técnica (que incluye una pasada) de BasicHLSL10. FX.


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



La sintaxis de los sombreadores de efectos es más detallada en la sintaxis de la [técnica de efectos (Direct3D 10)](d3d10-effect-technique-syntax.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
