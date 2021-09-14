---
title: Sintaxis de declaración de fragmento (DIRECT3D 9 HLSL)
description: Cada función del Lenguaje de sombreador de alto nivel (HLSL) de Microsoft se puede convertir en un fragmento de sombreador con la adición de una declaración de fragmento.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 60ac1153ff3491bc904f4f759f6653cb4243adff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361584"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a>Sintaxis de declaración de fragmento (DIRECT3D 9 HLSL)

Cada función del Lenguaje de sombreador de alto nivel (HLSL) de Microsoft se puede convertir en un fragmento de sombreador con la adición de una declaración de fragmento.

## <a name="syntax"></a>Sintaxis


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



donde:



| Value                  | Descripción                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fragmentKeyword   | Palabra clave Required. Pixelfragment o vertexfragment.                                                                                                                                                                                             |
| FragmentName      | Cadena de texto ASCII que especifica el nombre del fragmento compilado.                                                                                                                                                                                       |
| fragmento de \_ compilación | Palabra clave Required.                                                                                                                                                                                                                                     |
| shaderProfile     | Modelo de sombreador con el que se compilará. Cualquier perfil válido de sombreador de vértices (vea [**D3DXGetVertexShaderProfile)**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)o perfil de sombreador de píxeles (vea [**D3DXGetPixelShaderProfile).**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile) |
| FunctionName()    | Nombre de la función de sombreador, seguido de paréntesis.                                                                                                                                                                                                    |



 

Los parámetros de fragmento compartido se marcan mediante la adición de un prefijo \_ 'r' a su semántica.


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



En este ejemplo, la semántica de r PosWorld y r NormalWorld identifica que estos dos parámetros son parámetros \_ \_ compartidos entre otros fragmentos.

> [!Note]  
> El vinculador de fragmentos era una tecnología de Microsoft Direct3D 9 en D3DX 9. El vinculador de fragmentos era una herramienta (Flink.exe), una API D3DX 9 y una mejora de HLSL. El vinculador de fragmentos se ha eliminado a partir de la versión del SDK de DirectX de agosto de 2009. El vinculador de fragmentos nunca se aplicó a Microsoft Direct3D 10, Microsoft Direct3D 10.1 o Microsoft Direct3D 11.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
