---
description: La escritura de un efecto requiere que comprenda la sintaxis del efecto y genere la información de estado necesaria. Puede agregar el estado del sombreador, la textura y el muestreador, y todo el estado de canalización que la aplicación requiere en un efecto.
ms.assetid: 361dd260-526a-4484-8dc9-3857874e5023
title: Escribir un efecto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d625d09f57b68f6447982769d0ff4d4731e6aaaeff330b1cec639c4dffec8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068805"
---
# <a name="writing-an-effect-direct3d-9"></a>Escribir un efecto (Direct3D 9)

La escritura de un efecto requiere que comprenda la sintaxis del efecto y genere la información de estado necesaria. Puede agregar el estado del sombreador, la textura y el muestreador, y todo el estado de canalización que la aplicación requiere en un efecto.

La sintaxis del efecto se detalla en [El formato de efecto (Direct3D 9).](dx9-graphics-reference-effects-file-format.md) Normalmente, un efecto se encapsula en un archivo de efecto (.fx), pero también se puede escribir como una cadena de texto en una aplicación.

## <a name="effect-example"></a>Ejemplo de efecto

Los efectos contienen tres tipos de estado: estado del sombreador, estado de textura y muestra y estado de canalización. Este es un ejemplo de un efecto del [ejemplo BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx):


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

texture g_MeshTexture;              // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
// Texture samplers
sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};
struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
  
    float4 vAnimatedPos = vPos;
    
    // Animation the vertex based on time and the vertex's object space position
    if( bAnimate )
        vAnimatedPos += float4(vNormal, 0) * (sin(g_fTime+5.5)+0.5)*5;
    
    // Transform the position from object space to homogeneous projection space
    Output.Position = mul(vAnimatedPos, g_mWorldViewProjection);
    
    // Transform the normal from object space to world space    
    vNormalWorldSpace = normalize(mul(vNormal, (float3x3)g_mWorld));
    
    // Compute simple directional lighting equation
    float3 vTotalLightDiffuse = float3(0,0,0);
    for(int i=0; i < nNumLights; i++ )
        vTotalLightDiffuse += g_LightDiffuse[i] * max(0,dot(vNormalWorldSpace, g_LightDir[i]));
        
    Output.Diffuse.rgb = g_MaterialDiffuseColor * vTotalLightDiffuse + 
                         g_MaterialAmbientColor * g_LightAmbient;   
    Output.Diffuse.a = 1.0f; 
    
    // Just copy the texture coordinate through
    if( bTexture ) 
        Output.TextureUV = vTexCoord0; 
    else
        Output.TextureUV = 0; 
    
    return Output;    
}
struct PS_OUTPUT
{
    float4 RGBColor : COLOR0;  // Pixel color    
};
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_1_1 RenderScenePS( true ); 
    }
}
```



Este efecto contiene:

-   Estado del sombreador, que es todo el estado asociado al sombreador de vértices y al sombreador de píxeles. Esto se define mediante las funciones de sombreador de vértices y píxeles, las variables globales que necesiten y sus estructuras de datos de entrada y salida, que se enumeran aquí:

    ```
    struct VS_OUTPUT
    {  ...  };
    VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                             ...
    {  ...  }

    struct PS_OUTPUT
    {  ...  };
    PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                             uniform bool bTexture ) 
    {  ...  }
    ```

    

-   Estado de textura y muestreador, que son las variables globales para el objeto de textura y el objeto sampler:

    ```
    texture g_MeshTexture;              // Color texture for mesh

    sampler MeshTextureSampler = 
    sampler_state
    {
       ...
    };
    ```

    

-   El otro estado de efecto. No hay ningún otro estado de efecto que se utilice explícitamente en este ejemplo. Si lo hubiera, sería la técnica dentro del paso al que se aplicó:

    ```
    technique RenderSceneWithTexture1Light
    {
        pass P0
        {          
            // Any other effect state can be set here.

            VertexShader = compile vs_1_1 RenderSceneVS( 1, true, true );
            PixelShader  = compile ps_1_1 RenderScenePS( true ); 
        }
    }
    
    ```

    

## <a name="effects-contain-one-or-more-techniques-and-passes"></a>Los efectos contienen una o varias técnicas y pases

Las opciones de representación de efectos se controlan mediante la adición de técnicas y pases.

Los efectos se pueden crear con pases adicionales para facilitar efectos de representación más complejos. Una técnica admite un número arbitrario de pases:


```
technique T0
{
    pass P0
    { ... }

    pass P1
    { ... }

    ...

    pass Pn
    { ... }
}
```



Los efectos también se pueden crear con un número arbitrario de técnicas.


```
technique T0
{
    pass P0
    { ... }
}

technique T1
{
    pass P0
    { ... }

    pass P1
    { ... }
}

...

technique Tn
{
    pass P0
    { ... }
}

technique TVertexShaderOnly
{
    pass P0
    {
        VertexShader =
        asm
        {
         // assembly-language shader code goes here
         ...
        };
    }
}
```



Las técnicas y los pases pueden tener nombres arbitrarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos](effects.md)
</dt> </dl>

 

 



