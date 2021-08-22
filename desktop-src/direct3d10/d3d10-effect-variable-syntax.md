---
description: Una variable de efecto se declara con la sintaxis siguiente.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Sintaxis de variable de efecto (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2422ba2cebf18c72a14d621ef13a98700aefd2858169c6e96566b455ec21d2ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497715"
---
# <a name="effect-variable-syntax-direct3d-10"></a>Sintaxis de variable de efecto (Direct3D 10)

Una variable de efecto se declara con la sintaxis siguiente.

## <a name="syntax"></a>Syntax

*DataType* *VariableName:* \[ anotaciones *SemanticName* \]  <   >;



| Nombre         | Descripción                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Cualquier [tipo](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) básico [o de](../direct3dhlsl/dx-graphics-hlsl-to-type.md) textura.                                                                        |
| VariableName | Cadena ASCII que identifica de forma única el nombre de la variable de efecto.                                                                                                                   |
| SemanticName | Cadena ASCII que denota información adicional sobre cómo se debe usar una variable. Una semántica es una cadena ASCII que puede ser un valor del sistema predefinido o una cadena de usuario personalizado. |
| anotaciones  | Uno o varios fragmentos de información proporcionados por el usuario (metadatos) que el sistema de efectos omite. Para obtener información sobre la [sintaxis, vea Annotation Syntax (Direct3D 10) (Sintaxis de anotación [Direct3D 10]).](d3d10-effect-annotation-syntax.md)     |



 

Una variable de efecto que se declara fuera de todas las funciones se considera global en el ámbito; Las variables declaradas dentro de una función son locales para esa función.

## <a name="example"></a>Ejemplo

El [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa variables globales sin semántica para colores de material, propiedades de luz y matrices de transformación.

En este ejemplo se muestran las variables de efecto global.


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



En este ejemplo se muestran las variables de efecto que son locales para una función de sombreador.


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



En este ejemplo se muestran los parámetros de función que tienen semántica.


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



En este ejemplo se muestra cómo declarar una variable de textura.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



El muestreo de una textura se realiza con un muestreador de textura. Para configurar un sampler en un efecto, vea el [tipo de sampler](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](d3d10-effect-format.md)
</dt> </dl>

 

 
