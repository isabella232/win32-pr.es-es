---
title: Sintaxis de variable de efecto (Direct3D 11)
description: Una variable de efecto se declara con la sintaxis descrita en esta sección.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25057f3cd2535a0b48072616c3dd59393f90a24fe044c1cdad8acea677a541ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538398"
---
# <a name="effect-variable-syntax-direct3d-11"></a>Sintaxis de variable de efecto (Direct3D 11)

Una variable de efecto se declara con la sintaxis descrita en esta sección.

## <a name="syntax"></a>Sintaxis

Sintaxis básica:

*DataType* *VariableName* \[ *: Anotaciones SemanticName* = \]  <    >  \[ InitialValue \] ;

Consulte [Sintaxis de variables (HLSL de DirectX) para obtener](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) una sintaxis completa.



| Nombre         | Descripción                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Cualquier [tipo básico](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)de [bloque](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type)de estado, sombreador o vista de acceso sin ordenar.                            |
| VariableName | Cadena ASCII que identifica de forma única el nombre de la variable de efecto.                                                                                                                   |
| SemanticName | Cadena ASCII que denota información adicional sobre cómo se debe usar una variable. Una semántica es una cadena ASCII que puede ser un valor del sistema predefinido o una cadena de usuario personalizado. |
| anotaciones  | Uno o varios fragmentos de información proporcionada por el usuario (metadatos) que el sistema de efectos omite. Para obtener información sobre la [sintaxis, vea Annotation Syntax (Direct3D 11) (Sintaxis de anotación [Direct3D 11]).](d3d11-effect-annotation-syntax.md)     |
| InitialValue | Valor predeterminado de la variable.                                                                                                                                                          |



 

Una variable de efecto que se declara fuera de todas las funciones se considera global en el ámbito; Las variables declaradas dentro de una función son locales para esa función.

## <a name="example"></a>Ejemplo

En este ejemplo se muestran las variables numéricas de efecto global.


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



En este ejemplo se muestra cómo declarar una variable de textura global.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



El muestreo de una textura se realiza con un muestreador de textura. Para configurar un sampler en un efecto, vea el [tipo de sampler](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

En este ejemplo se muestra cómo declarar variables globales de vista de acceso no ordenado.


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

 

 