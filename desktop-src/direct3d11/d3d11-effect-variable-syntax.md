---
title: Sintaxis de las variables de efectos (Direct3D 11)
description: Una variable de efecto se declara con la sintaxis descrita en esta sección.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67710642060ffea642434ba2d23a77cec2fb8bc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487754"
---
# <a name="effect-variable-syntax-direct3d-11"></a>Sintaxis de las variables de efectos (Direct3D 11)

Una variable de efecto se declara con la sintaxis descrita en esta sección.

## <a name="syntax"></a>Sintaxis

Sintaxis básica:

*DataType* *VariableName* \[ *: SemanticName* \]  <  *Annotations*  >  \[ = InitialValue \] ;

Consulte [Sintaxis de variables (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) para ver la sintaxis completa.



| Nombre         | Descripción                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Cualquier vista de acceso [básica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [textura](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), sin ordenar, sombreador o tipo de bloque de estado.                            |
| VariableName | Cadena ASCII que identifica de forma única el nombre de la variable de efecto.                                                                                                                   |
| SemanticName | Cadena ASCII que denota información adicional sobre cómo se debe usar una variable. Una semántica es una cadena ASCII que puede ser un valor de sistema predefinido o una cadena de usuario personalizado. |
| Anotaciones  | Una o más partes de la información proporcionada por el usuario (metadatos) que el sistema de efectos omite. Para ver la sintaxis, vea [Sintaxis de anotación (Direct3D 11)](d3d11-effect-annotation-syntax.md).     |
| InitialValue | Valor predeterminado de la variable.                                                                                                                                                          |



 

Una variable de efecto que se declara fuera de todas las funciones, se considera global en el ámbito; las variables declaradas dentro de una función son locales para esa función.

## <a name="example"></a>Ejemplo

En este ejemplo se muestran variables numéricas de efectos globales.


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



En este ejemplo se muestra la declaración de una variable de textura global.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



El muestreo de una textura se realiza con una muestra de textura. Para configurar una muestra en un efecto, vea el [tipo de muestra](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

En este ejemplo se muestra la declaración de variables de vista de acceso no ordenada global.


```
RWStructuredBuffer<uint> bc : register(u2) < string name="bc"; >;
RWBuffer<uint> bRW;
struct S
{
   uint key;
   uint value;
};
AppendStructuredBuffer<S> asb : register(u5);
RWByteAddressBuffer rwbab : register(u1);
RWStructuredBuffer<uint> rwsb : register(u3);
RWTexture1D<float> rwt1d : register(u1);
RWTexture1DArray<uint> rwt1da : register(u4);
RWTexture2D<uint> rwt2d : register(u2);
RWTexture2DArray<uint> rwt2da : register(u6);
RWTexture3D<uint> rwt3d : register(u7); 
 This example illustrates declaring global shader variables.
VertexShader pVS = CompileShader( vs_5_0, VS() );
HullShader pHS = NULL;
DomainShader pDS = NULL;
GeometryShader pGS = ConstructGSWithSO( CompileShader( gs_5_0, VS() ), 
                                        "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                        "3:Texcoord.xyzw; 3:$SKIP.x;", 
                                        NULL, 
                                        NULL, 
                                        1 );
PixelShader pPS = NULL;
ComputeShader pCS = NULL;
This example illustrates declaring global state block variables.
BlendState myBS[2] < bool IsValid = true; >
{
  {
    BlendEnable[0] = false;
  },
  {
    BlendEnable[0] = true;
    SrcBlendAlpha[0] = Inv_Src_Alpha;
  }
};

RasterizerState myRS
{
      FillMode = Solid;
      CullMode = NONE;
      MultisampleEnable = true;
      DepthClipEnable = false;
};

DepthStencilState myDS
{
    DepthEnable = false;
    DepthWriteMask = Zero;
    DepthFunc = Less;
};
sampler mySS[2] : register(s3) 
{
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 3;
    },
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 4;
    }
};
  
  
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](d3d11-effect-format.md)
</dt> </dl>

 

 