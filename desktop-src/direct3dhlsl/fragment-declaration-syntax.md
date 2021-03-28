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
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a>Sintaxis de declaración de fragmentos (Direct3D 9 HLSL)

Cada función de Microsoft High Level Shader Language (HLSL) se puede convertir en un fragmento de sombreador con la adición de una declaración de fragmento.

## <a name="syntax"></a>Sintaxis


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



donde:



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fragmentKeyword   | Palabra clave required. Pixelfragment o vertexfragment.                                                                                                                                                                                             |
| FragmentName      | Cadena de texto ASCII que especifica el nombre del fragmento compilado.                                                                                                                                                                                       |
| compilar \_ fragmento | Palabra clave required.                                                                                                                                                                                                                                     |
| shaderProfile     | Modelo de sombreador con el que se va a realizar la compilación. Cualquier perfil de sombreador de vértices válido (vea [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) o el perfil del sombreador de píxeles (consulte [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)). |
| Nombrefunción ()    | El nombre de la función de sombreador, seguido de paréntesis.                                                                                                                                                                                                    |



 

Los parámetros de fragmento compartidos se marcan agregando un \_ prefijo "r" a su semántica.


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



En este ejemplo, la semántica de r \_ PosWorld y r \_ NormalWorld identifica que estos dos parámetros son parámetros compartidos entre otros fragmentos.

> [!Note]  
> Fragment linker era una tecnología de Microsoft Direct3D 9 en D3DX 9. Fragment linker era una herramienta (Flink.exe), una API de D3DX 9 y una mejora de HLSL. Fragment linker se quitó de la versión del SDK de DirectX 2009 de agosto. Fragment linker nunca se aplica a Microsoft Direct3D 10, Microsoft Direct3D 10,1 o Microsoft Direct3D 11.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 