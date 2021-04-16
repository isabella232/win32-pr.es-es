---
description: La escritura de un efecto requiere que entienda la sintaxis de los efectos y genere la información de estado necesaria. Puede Agregar el estado del sombreador, la textura y el estado del muestrario, y todo el estado de la canalización que la aplicación requiera en un efecto.
ms.assetid: 361dd260-526a-4484-8dc9-3857874e5023
title: Escribir un efecto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0f456c5a2bce66f782b4da7d426de5c86bbb33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686285"
---
# <a name="writing-an-effect-direct3d-9"></a>Escribir un efecto (Direct3D 9)

La escritura de un efecto requiere que entienda la sintaxis de los efectos y genere la información de estado necesaria. Puede Agregar el estado del sombreador, la textura y el estado del muestrario, y todo el estado de la canalización que la aplicación requiera en un efecto.

La sintaxis del efecto se detalla en el [formato de efecto (Direct3D 9)](dx9-graphics-reference-effects-file-format.md). Un efecto se encapsula normalmente en un archivo de efectos (. FX), pero también se puede escribir como una cadena de texto en una aplicación.

## <a name="effect-example"></a>Ejemplo de efecto

Los efectos contienen tres tipos de estado: el estado del sombreador, la textura y el estado del muestrario, y el estado de la canalización. Este es un ejemplo de un efecto del [ejemplo BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx):


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

-   El estado del sombreador, que es todo el estado asociado con el sombreador de vértices y el sombreador de píxeles. Esto se define mediante las funciones de sombreador de vértices y píxeles, las variables globales que requieran y sus estructuras de datos de entrada y salida, que se enumeran aquí:

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

    

-   Estado de muestra y textura, que son las variables globales para el objeto de textura y el objeto de muestra:

    ```
    texture g_MeshTexture;              // Color texture for mesh

    sampler MeshTextureSampler = 
    sampler_state
    {
       ...
    };
    ```

    

-   El otro estado del efecto. En este ejemplo no se usa explícitamente ningún otro estado de efecto. Si lo hubiera, sería la técnica dentro del paso al que se aplicó:

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

    

## <a name="effects-contain-one-or-more-techniques-and-passes"></a>Los efectos contienen una o más técnicas y pases

Las opciones de representación de efectos se controlan agregando técnicas y pasadas.

Los efectos se pueden crear con pasos adicionales para facilitar efectos de representación más complejos. Una técnica admite un número arbitrario de pasos:


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



Las técnicas y los pasos pueden tener nombres arbitrarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos](effects.md)
</dt> </dl>

 

 



