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
# <a name="organizing-state-in-an-effect-direct3d-11"></a>Organización del estado de un efecto (Direct3D 11)

Con Direct3D 11, el estado del efecto para ciertas fases de canalización se organiza por estructuras. Estas son las estructuras:



| Estado de canalización | Estructura                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| Rasterización  | [**Descripción de D3D11 \_ rasterizador \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| Fusión de salida  | [**D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) Descripción de la [ **\_ Galería de \_ símbolos \_ de profundidad** de Blend y D3D11](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) |
| Sombreadores        | Consulte a continuación                                                                                                          |



 

En el caso de las fases del sombreador, donde el número de cambios de Estado debe ser más controlado por una aplicación, el estado se ha dividido en el estado de búfer constante, el estado de muestra, el estado de los recursos del sombreador y el estado de vista de acceso desordenado (para los sombreadores de píxeles y de cálculo). Esto permite que una aplicación que se ha diseñado cuidadosamente para actualizar solo el estado que está cambiando, lo que mejora el rendimiento al reducir la cantidad de datos que se deben pasar a la GPU.

¿Cómo se organiza el estado de la canalización en un efecto?

La respuesta es que el orden no importa. No es necesario que las variables globales se encuentren en la parte superior. Sin embargo, todos los ejemplos del SDK siguen el mismo orden, ya que se recomienda organizar los datos de la misma manera. Por lo tanto, se trata de una breve descripción de la ordenación de datos en los ejemplos del SDK de DirectX.

-   [Variables globales](#global-variables)
-   [Sombreadores](#shaders)
-   [Grupos, técnicas y pases](#groups-techniques-and-passes)

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



La sintaxis de las variables de efecto es más detallada en la [Sintaxis de variables de efectos (Direct3D 11)](d3d11-effect-variable-syntax.md). La sintaxis para los muestreadores de texturas de efectos es más detallada en el [tipo de muestra (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

## <a name="shaders"></a>Sombreadores

Los sombreadores son pequeños programas ejecutables. Puede pensar en los sombreadores como el estado del sombreador encapsulador, ya que el código de HLSL implementa la funcionalidad del sombreador. Los gráficos se canalizan hasta cinco tipos diferentes de sombreadores.

-   Sombreadores de vértices: operan en datos de vértices. Un vértice en produce un vértice.
-   Sombreadores de casco: operan en datos de revisión. Fase de punto de control: una invocación produce un punto de control; Para cada bifurcación y fases de combinación: una revisión produce una cantidad de datos constantes de revisión.
-   Sombreadores de dominio: operan en datos primitivos. Un primitivo puede producir 0, 1 o muchos primitivos.
-   Sombreadores de geometría: operan en datos primitivos. Un primitivo en puede producir 0, 1 o muchas primitivas.
-   Sombreadores de píxeles: operan en datos de píxeles. Un píxel en produce 1 píxel de salida (a menos que se represente el píxel de una representación).

La canalización del sombreador de cálculo usa un sombreador:

-   Sombreadores de cálculo: operan en cualquier tipo de datos. La salida es independiente del número de subprocesos.

Los sombreadores son funciones locales y siguen las reglas de función de estilo C. Cuando se compila un efecto, cada sombreador se compila y se almacena internamente un puntero a cada función de sombreador. Se devuelve una interfaz ID3D11Effect cuando la compilación se realiza correctamente. En este momento, el efecto compilado está en un formato intermedio.

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



La sintaxis de los sombreadores de efectos es más detallada en la sintaxis de la [función de efecto (Direct3D 11)](d3d11-effect-function-syntax.md).

## <a name="groups-techniques-and-passes"></a>Grupos, técnicas y pases

Un grupo es una colección de técnicas. Una técnica es una colección de pasos de representación (debe haber al menos un paso). Cada paso de efecto (que es similar en el ámbito a un solo paso en un bucle de representación) define el estado del sombreador y cualquier otro estado de canalización necesario para representar la geometría.

Los grupos son opcionales. Hay un único grupo sin nombre que engloba todas las técnicas globales. Todos los demás grupos deben tener nombre.

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



La sintaxis de los sombreadores de efectos es más detallada en la sintaxis de la [técnica de efectos (Direct3D 11)](d3d11-effect-technique-syntax.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 