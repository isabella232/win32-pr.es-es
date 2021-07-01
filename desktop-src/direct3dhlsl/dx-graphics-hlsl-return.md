---
title: return (Instrucción)
description: Una instrucción return indica el final de una función.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- return (Instrucción HLSL)
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 876c69f3ecfcf1ee1c8391ccc503b2316056b37a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119590"
---
# <a name="return-statement"></a>return (Instrucción)

Una instrucción return indica el final de una función.

valor \[ devuelto \] ;



 

La instrucción return más sencilla devuelve el control de la función al programa que realiza la llamada; no devuelve ningún valor.


```
void main()
{
    return ;
}
```



Sin embargo, una instrucción return puede devolver uno o varios valores. Este ejemplo devuelve un valor literal:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



Este ejemplo devuelve el resultado escalar de una expresión.


```
return  light.enabled = true ;
```



Este ejemplo devuelve un vector de cuatro componentes que se construye a partir de una variable local y un literal.


```
return  float4(color.rgb, 1) ;
```



Este ejemplo devuelve un vector de cuatro componentes que se construye a partir del resultado que se devuelve a partir de una función intrínseca, junto con valores literales.


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



Este ejemplo devuelve una estructura que contiene uno o varios miembros.


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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones (HLSL de DirectX)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




