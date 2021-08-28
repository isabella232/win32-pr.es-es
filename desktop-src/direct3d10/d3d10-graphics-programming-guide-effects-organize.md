---
description: 'Con Direct3D 10, el estado de efecto de determinadas fases de canalización se organiza mediante las estructuras siguientes:'
ms.assetid: 674ed278-102c-43da-a6bf-58e084df151e
title: Organización del estado en un efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0fdd4389ce4db34a64e4bc5e39f21998c90481d4a43a06244be2b231cca999
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753755"
---
# <a name="organizing-state-in-an-effect-direct3d-10"></a>Organización del estado en un efecto (Direct3D 10)

Con Direct3D 10, el estado de efecto de determinadas fases de canalización se organiza mediante las estructuras siguientes:



| Estado de canalización  | Estructura                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| Ensamblador de entrada | [**D3D10 \_ INPUT \_ ELEMENT \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| Rasterización   | [**D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| Fusión de salida   | [**D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) y [ **D3D10 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |



 

En las fases del sombreador, donde una aplicación debe controlar más el número de cambios de estado, el estado se ha dividido en estado de búfer constante, estado del muestreador y estado de recurso del sombreador. Esto permite que una aplicación diseñada cuidadosamente actualice solo el estado que está cambiando, lo que mejora el rendimiento al reducir la cantidad de datos que se deben pasar a la GPU.

¿Cómo se organiza el estado de la canalización en un efecto?

La respuesta es que el pedido no importa. Las variables globales no tienen que encontrarse en la parte superior. Sin embargo, todos los ejemplos del SDK siguen el mismo orden, ya que es una buena práctica organizar los datos de la misma manera. Por lo tanto, esta es una breve descripción de la ordenación de datos en los ejemplos del SDK de DirectX.

-   [Variables globales](#global-variables)
-   [Sombreadores](#shaders)
-   [Técnicas y pases](#techniques-and-passes)

## <a name="global-variables"></a>Variables globales

Al igual que la práctica estándar de C, las variables globales se declaran primero, en la parte superior del archivo. A menudo, se trata de variables que una aplicación inicializará y, a continuación, se usarán en un efecto. A veces se inicializan y nunca cambian, otras veces se actualizan en cada fotograma. Al igual que las reglas de ámbito de función de C, las variables de efecto declaradas fuera del ámbito de las funciones de efecto son visibles a lo largo del efecto; cualquier variable declarada dentro de una función de efecto solo es visible dentro de esa función.

Este es un ejemplo de las variables declaradas en BasicHLSL10.fx.


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



La sintaxis de las variables de efecto se detalla más detalladamente en [Sintaxis de variable de efecto (Direct3D 10).](d3d10-effect-variable-syntax.md) La sintaxis de los muestreadores de textura de efecto es más detallada en [Sampler Type (DirectX HLSL).](../direct3dhlsl/dx-graphics-hlsl-sampler.md)

## <a name="shaders"></a>Sombreadores

Los sombreadores son pequeños programas ejecutables. Puede pensar que los sombreadores encapsulan el estado del sombreador, ya que el código HLSL implementa la funcionalidad del sombreador. La canalización usa tres tipos diferentes de sombreadores.

-   Sombreadores de vértices: operan en datos de vértices. Un vértice de produce un vértice.
-   Sombreadores de geometría: funcionan con datos primitivos. Una primitiva de puede producir 0, 1 o muchas primitivas.
-   Sombreadores de píxeles: funcionan con datos de píxeles. Un píxel de produce 1 píxel de salida (a menos que el píxel se culte fuera de una representación).

Los sombreadores son funciones locales y siguen las reglas de función de estilo C. Cuando se compila un efecto, se compila cada sombreador y se almacena internamente un puntero a cada función de sombreador. Cuando la compilación se realiza correctamente, se devuelve una interfaz ID3D10Effect. En este momento, el efecto compilado está en un formato intermedio.

Para obtener más información sobre los sombreadores compilados, deberá usar la reflexión del sombreador. Esto es esencialmente como pedir al tiempo de ejecución que descompile los sombreadores y devolverle información sobre el código del sombreador.


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



La sintaxis de los sombreadores de efectos se detalla más detalladamente en Sintaxis de función [de efecto (Direct3D 10).](d3d10-effect-function-syntax.md)

## <a name="techniques-and-passes"></a>Técnicas y pases

Una técnica es una colección de pases de representación (debe haber al menos un paso). Cada paso de efecto (que es similar en el ámbito a un solo paso de un bucle de representación) define el estado del sombreador y cualquier otro estado de canalización necesario para representar la geometría.

Este es un ejemplo de una técnica (que incluye un paso) de BasicHLSL10.fx.


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



La sintaxis de los sombreadores de efectos se detalla más detalladamente en Sintaxis de técnica de [efecto (Direct3D 10).](d3d10-effect-technique-syntax.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
