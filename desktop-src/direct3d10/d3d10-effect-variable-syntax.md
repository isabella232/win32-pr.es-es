---
description: Una variable de efecto se declara con la sintaxis siguiente.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Sintaxis de las variables de efectos (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423368"
---
# <a name="effect-variable-syntax-direct3d-10"></a>Sintaxis de las variables de efectos (Direct3D 10)

Una variable de efecto se declara con la sintaxis siguiente.

## <a name="syntax"></a>Sintaxis

*DataType* *VariableName* \[ : *SemanticName* \]  <  *Annotations* >;



| Nombre         | Descripción                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Cualquier tipo [básico](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) o de [textura](../direct3dhlsl/dx-graphics-hlsl-to-type.md) .                                                                        |
| VariableName | Cadena ASCII que identifica de forma única el nombre de la variable de efecto.                                                                                                                   |
| SemanticName | Cadena ASCII que denota información adicional sobre cómo se debe usar una variable. Una semántica es una cadena ASCII que puede ser un valor de sistema predefinido o una cadena de usuario personalizado. |
| Anotaciones  | Una o más partes de la información proporcionada por el usuario (metadatos) que el sistema de efectos omite. Para ver la sintaxis, vea [Sintaxis de anotación (Direct3D 10)](d3d10-effect-annotation-syntax.md).     |



 

Una variable de efecto que se declara fuera de todas las funciones, se considera global en el ámbito; las variables declaradas dentro de una función son locales para esa función.

## <a name="example"></a>Ejemplo

El [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa variables globales sin semántica para los colores de materiales, las propiedades de luz y las matrices de transformación.

En este ejemplo se muestran las variables de efectos globales.


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



El muestreo de una textura se realiza con una muestra de textura. Para configurar una muestra en un efecto, vea el [tipo de muestra](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](d3d10-effect-format.md)
</dt> </dl>

 

 
