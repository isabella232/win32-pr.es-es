---
title: return (Instrucción)
description: Una instrucción return indica el final de una función.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- Instrucción return HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 525abf6d815d2073ee39a6bc6a5a81120cf652ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104983758"
---
# <a name="return-statement"></a>return (Instrucción)

Una instrucción return indica el final de una función.



|                   |
|-------------------|
| valor devuelto \[ \] ; |



 

La instrucción return más sencilla devuelve el control de la función al programa que realiza la llamada; no devuelve ningún valor.


```
void main()
{
    return ;
}
```



Sin embargo, una instrucción return puede devolver uno o más valores. Este ejemplo devuelve un valor literal:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



En este ejemplo se devuelve el resultado escalar de una expresión.


```
return  light.enabled = true ;
```



Este ejemplo devuelve un vector de cuatro componentes que se construye a partir de una variable local y un literal.


```
return  float4(color.rgb, 1) ;
```



Este ejemplo devuelve un vector de cuatro componentes que se construye a partir del resultado que se devuelve de una función intrínseca, junto con valores literales.


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



En este ejemplo se devuelve una estructura que contiene uno o más miembros.


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




