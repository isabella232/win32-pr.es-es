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
# <a name="return-statement"></a><span data-ttu-id="fbb88-104">return (Instrucción)</span><span class="sxs-lookup"><span data-stu-id="fbb88-104">return Statement</span></span>

<span data-ttu-id="fbb88-105">Una instrucción return indica el final de una función.</span><span class="sxs-lookup"><span data-stu-id="fbb88-105">A return statement signals the end of a function.</span></span>

<span data-ttu-id="fbb88-106">valor \[ devuelto \] ;</span><span class="sxs-lookup"><span data-stu-id="fbb88-106">return \[value\];</span></span>



 

<span data-ttu-id="fbb88-107">La instrucción return más sencilla devuelve el control de la función al programa que realiza la llamada; no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fbb88-107">The simplest return statement returns control from the function to the calling program; it returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="fbb88-108">Sin embargo, una instrucción return puede devolver uno o varios valores.</span><span class="sxs-lookup"><span data-stu-id="fbb88-108">However, a return statement can return one or more values.</span></span> <span data-ttu-id="fbb88-109">Este ejemplo devuelve un valor literal:</span><span class="sxs-lookup"><span data-stu-id="fbb88-109">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="fbb88-110">Este ejemplo devuelve el resultado escalar de una expresión.</span><span class="sxs-lookup"><span data-stu-id="fbb88-110">This example returns the scalar result of an expression.</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="fbb88-111">Este ejemplo devuelve un vector de cuatro componentes que se construye a partir de una variable local y un literal.</span><span class="sxs-lookup"><span data-stu-id="fbb88-111">This example returns a four-component vector that is constructed from a local variable and a literal.</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="fbb88-112">Este ejemplo devuelve un vector de cuatro componentes que se construye a partir del resultado que se devuelve a partir de una función intrínseca, junto con valores literales.</span><span class="sxs-lookup"><span data-stu-id="fbb88-112">This example returns a four-component vector that is constructed from the result that is returned from an intrinsic function, together with literal values.</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="fbb88-113">Este ejemplo devuelve una estructura que contiene uno o varios miembros.</span><span class="sxs-lookup"><span data-stu-id="fbb88-113">This example returns a structure that contains one or more members.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="fbb88-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fbb88-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb88-115">Funciones (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="fbb88-115">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




