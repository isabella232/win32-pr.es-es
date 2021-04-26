---
title: Sintaxis de declaración de funciones
description: Las funciones HLSL se declaran con la sintaxis siguiente.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2781d173eb4a1c18a661495d9fb55a0cced81921
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998332"
---
# <a name="function-declaration-syntax"></a>Sintaxis de declaración de funciones

Las funciones HLSL se declaran con la sintaxis siguiente.



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| \[*StorageClass* \] \[clipplanes() \] \[ precise \] Return Value \_ *Name* ( \[ *ArgumentList* \] ) : \[ *Semantic* \] { \[ *StatementBlock* \] }; |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*
</dt> <dd>

Modificador que redefine una declaración de función. **inline** es actualmente el único valor modificador. El valor modificador debe estar **en línea** porque también es el valor predeterminado. Por lo tanto, una función está insertable independientemente de si se especifica en línea y todas las funciones de HLSL están insertadas. Una función insertda genera una copia del cuerpo de la función (al compilar) para cada llamada de función. Esto se hace para reducir la sobrecarga de llamar a la función.

</dd> <dt>

<span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*
</dt> <dd>

Lista opcional de planos de recorte, que es hasta 6 planos de recorte especificados por el usuario. Se trata de un mecanismo alternativo para [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) que funciona en el [nivel](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de característica 9 x \_ y superior.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nombre*
</dt> <dd>

Cadena ASCII que identifica de forma única el nombre de la función de sombreador.

</dd> <dt>

<span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*
</dt> <dd>

Lista de argumentos opcional, que es una lista separada por comas de [argumentos pasados](dx-graphics-hlsl-function-parameters.md) a una función.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semántica*
</dt> <dd>

Cadena opcional que identifica el uso previsto de los datos devueltos (vea [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Instrucciones [opcionales](dx-graphics-hlsl-statement-blocks.md) que son el cuerpo de la función. Una función definida sin un cuerpo se denomina prototipo de función; El cuerpo de una función de prototipo debe definirse en otro lugar antes de que se pueda llamar a la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El tipo de valor devuelto puede ser cualquiera de estos [tipos HLSL.](dx-graphics-hlsl-data-types.md)

## <a name="remarks"></a>Comentarios

La sintaxis de esta página describe casi todos los tipos de función HLSL, lo que incluye sombreadores de vértices, sombreadores de píxeles y funciones auxiliares. Aunque un sombreador de geometría también se implementa con una función, su sintaxis es un poco más complicada, por lo que hay una página independiente que define una declaración de función de sombreador de geometría (vea Objeto de sombreador de geometría [(HLSL de DirectX).](dx-graphics-hlsl-geometry-shader.md)

Una función se puede sobrecargar siempre y cuando se le de una combinación única de tipos de parámetro o orden de parámetros. HLSL también implementa una serie de funciones intrínsecas o [**integradas.**](dx-graphics-hlsl-intrinsic-functions.md)

Puede especificar planos de recorte específicos del usuario con el **atributo clipplanes.** Windows aplica estos planos de recorte a todas las primitivas dibujadas. El **atributo clipplanes** funciona como [SV \_ ClipDistance,](dx-graphics-hlsl-semantics.md) pero funciona en todas las características de [hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de nivel 9 x \_ y superiores. Para obtener más información, consulte [Planos de recorte de usuario en hardware de nivel de característica 9.](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)

## <a name="examples"></a>Ejemplos

Este ejemplo es de BasicHLSL10.fx del [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).


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



En este ejemplo de AdvancedParticles.fx del [ejemplo AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)se ilustra el uso de una semántica para el tipo de valor devuelto.


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

 

 
