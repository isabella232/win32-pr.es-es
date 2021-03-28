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
# <a name="return-statement"></a><span data-ttu-id="1e0b6-104">return (Instrucción)</span><span class="sxs-lookup"><span data-stu-id="1e0b6-104">return Statement</span></span>

<span data-ttu-id="1e0b6-105">Una instrucción return indica el final de una función.</span><span class="sxs-lookup"><span data-stu-id="1e0b6-105">A return statement signals the end of a function.</span></span>



|                   |
|-------------------|
| <span data-ttu-id="1e0b6-106">valor devuelto \[ \] ;</span><span class="sxs-lookup"><span data-stu-id="1e0b6-106">return \[value\];</span></span> |



 

<span data-ttu-id="1e0b6-107">La instrucción return más sencilla devuelve el control de la función al programa que realiza la llamada; no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1e0b6-107">The simplest return statement returns control from the function to the calling program; it returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="1e0b6-108">Sin embargo, una instrucción return puede devolver uno o más valores.</span><span class="sxs-lookup"><span data-stu-id="1e0b6-108">However, a return statement can return one or more values.</span></span> <span data-ttu-id="1e0b6-109">Este ejemplo devuelve un valor literal:</span><span class="sxs-lookup"><span data-stu-id="1e0b6-109">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="1e0b6-110">En este ejemplo se devuelve el resultado escalar de una expresión.</span><span class="sxs-lookup"><span data-stu-id="1e0b6-110">This example returns the scalar result of an expression.</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="1e0b6-111">Este ejemplo devuelve un vector de cuatro componentes que se construye a partir de una variable local y un literal.</span><span class="sxs-lookup"><span data-stu-id="1e0b6-111">This example returns a four-component vector that is constructed from a local variable and a literal.</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="1e0b6-112">Este ejemplo devuelve un vector de cuatro componentes que se construye a partir del resultado que se devuelve de una función intrínseca, junto con valores literales.</span><span class="sxs-lookup"><span data-stu-id="1e0b6-112">This example returns a four-component vector that is constructed from the result that is returned from an intrinsic function, together with literal values.</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="1e0b6-113">En este ejemplo se devuelve una estructura que contiene uno o más miembros.</span><span class="sxs-lookup"><span data-stu-id="1e0b6-113">This example returns a structure that contains one or more members.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="1e0b6-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e0b6-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0b6-115">Funciones (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e0b6-115">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




