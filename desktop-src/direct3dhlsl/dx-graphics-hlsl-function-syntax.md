---
title: Sintaxis de declaración de funciones
description: Las funciones de HLSL se declaran con la sintaxis siguiente.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7358a59dba0096f5c8ffe58072a974ebff9a1050
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421259"
---
# <a name="function-declaration-syntax"></a>Sintaxis de declaración de funciones

Las funciones de HLSL se declaran con la sintaxis siguiente.



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| \[*StorageClass* \] \[clipplanes () \] \[ \]nombre de valor devuelto preciso \_  ( \[ *ArgumentList* \] ) \[ : *semántico* \] { \[ *StatementBlock* \] }; |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*
</dt> <dd>

Modificador que redefine una declaración de función. **en** la actualidad, es el único valor modificador. El valor del modificador debe estar **insertado** porque también es el valor predeterminado. Por lo tanto, una función está alineada, independientemente de si se especifica **insertado** y todas las funciones de HLSL están alineadas. Una función insertada genera una copia del cuerpo de la función (al compilar) para cada llamada de función. Esto se hace para reducir la sobrecarga de llamar a la función.

</dd> <dt>

<span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*
</dt> <dd>

Lista opcional de planos de recortes, que es hasta 6 planos de clip especificados por el usuario. Se trata de un mecanismo alternativo [para \_ ClipDistance de SV](dx-graphics-hlsl-semantics.md) que funciona en el [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x y superior.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*
</dt> <dd>

Cadena ASCII que identifica de forma única el nombre de la función de sombreador.

</dd> <dt>

<span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*
</dt> <dd>

Lista de argumentos opcional, que es una lista separada por comas de [argumentos](dx-graphics-hlsl-function-parameters.md) pasados a una función.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semántica*
</dt> <dd>

Cadena opcional que identifica el uso previsto de los datos devueltos (vea [semántica (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

[Instrucciones](dx-graphics-hlsl-statement-blocks.md) opcionales que componen el cuerpo de la función. Una función definida sin cuerpo se denomina prototipo de función. el cuerpo de una función de prototipo debe definirse en otro lugar antes de que se pueda llamar a la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El tipo de valor devuelto puede ser cualquiera de estos [tipos HLSL](dx-graphics-hlsl-data-types.md).

## <a name="remarks"></a>Observaciones

La sintaxis de esta página describe casi todos los tipos de funciones HLSL; esto incluye sombreadores de vértices, sombreadores de píxeles y funciones auxiliares. Aunque un sombreador de geometría también se implementa con una función, su sintaxis es un poco más complicada, por lo que hay una página independiente que define una declaración de función de sombreador de geometría (vea [objeto de sombreador de geometría (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).

Una función se puede sobrecargar siempre que se le proporcione una combinación única de tipos de parámetros y/o el orden de los parámetros. HLSL también implementa varias funciones integradas o [**intrínsecas**](dx-graphics-hlsl-intrinsic-functions.md).

Puede especificar planos de clips específicos del usuario con el atributo **clipplanes** . Windows aplica estos planos de recorte a todas las primitivas dibujadas. El atributo **clipplanes** funciona como la [VP \_ ClipDistance](dx-graphics-hlsl-semantics.md) , pero funciona en todo el nivel de [características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de hardware 9 \_ x y versiones posteriores. Para obtener más información, consulte [planos de clips de usuario en hardware de nivel de característica 9](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="examples"></a>Ejemplos

Este ejemplo es de BasicHLSL10. FX del [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



En este ejemplo de AdvancedParticles. FX del [ejemplo AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), se ilustra el uso de una semántica para el tipo de valor devuelto.


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 