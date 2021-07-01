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
ms.openlocfilehash: 847194c08b865542cff1deb20c8518a7e4b62ab9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119050"
---
# <a name="function-declaration-syntax"></a><span data-ttu-id="fac94-103">Sintaxis de declaración de funciones</span><span class="sxs-lookup"><span data-stu-id="fac94-103">Function Declaration Syntax</span></span>

<span data-ttu-id="fac94-104">Las funciones HLSL se declaran con la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="fac94-104">HLSL functions are declared with the following syntax.</span></span>

<span data-ttu-id="fac94-105">\[*StorageClass* \] \[clipplanes() \] \[ precise \] Return Value \_ *Name* ( \[ *ArgumentList* \] ) : \[ *Semantic* \] { \[ *StatementBlock* \] };</span><span class="sxs-lookup"><span data-stu-id="fac94-105">\[*StorageClass*\] \[clipplanes()\] \[precise\] Return\_Value *Name* ( \[*ArgumentList*\] ) \[: *Semantic*\] {   \[*StatementBlock*\] };</span></span>



 

## <a name="parameters"></a><span data-ttu-id="fac94-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fac94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac94-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span><span class="sxs-lookup"><span data-stu-id="fac94-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span></span>
</dt> <dd>

<span data-ttu-id="fac94-108">Modificador que redefine una declaración de función.</span><span class="sxs-lookup"><span data-stu-id="fac94-108">Modifier that redefines a function declaration.</span></span> <span data-ttu-id="fac94-109">**inline** es actualmente el único valor modificador.</span><span class="sxs-lookup"><span data-stu-id="fac94-109">**inline** is currently the only modifier value.</span></span> <span data-ttu-id="fac94-110">El valor modificador debe **estar en línea** porque también es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fac94-110">The modifier value must be **inline** because it is also the default value.</span></span> <span data-ttu-id="fac94-111">Por lo tanto, una función está insertable independientemente de si se especifica en línea **y** todas las funciones de HLSL están insertadas.</span><span class="sxs-lookup"><span data-stu-id="fac94-111">Therefore, a function is inline regardless of whether you specify **inline**, and all functions in HLSL are inline.</span></span> <span data-ttu-id="fac94-112">Una función insertda genera una copia del cuerpo de la función (al compilar) para cada llamada de función.</span><span class="sxs-lookup"><span data-stu-id="fac94-112">An inline function generates a copy of the function body (when compiling) for each function call.</span></span> <span data-ttu-id="fac94-113">Esto se hace para reducir la sobrecarga de llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="fac94-113">This is done to decrease the overhead of calling the function.</span></span>

</dd> <dt>

<span data-ttu-id="fac94-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span><span class="sxs-lookup"><span data-stu-id="fac94-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span></span>
</dt> <dd>

<span data-ttu-id="fac94-115">Lista opcional de planos de recorte, que es hasta 6 planos de clips especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="fac94-115">Optional list of clip planes, which is up to 6 user-specified clip planes.</span></span> <span data-ttu-id="fac94-116">Se trata de un mecanismo alternativo para [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) que funciona [en](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) el nivel de característica 9 x y \_ superior.</span><span class="sxs-lookup"><span data-stu-id="fac94-116">This is an alternate mechanism for [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) that works on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

</dd> <dt>

<span data-ttu-id="fac94-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nombre*</span><span class="sxs-lookup"><span data-stu-id="fac94-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="fac94-118">Cadena ASCII que identifica de forma única el nombre de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fac94-118">An ASCII string that uniquely identifies the name of the shader function.</span></span>

</dd> <dt>

<span data-ttu-id="fac94-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span><span class="sxs-lookup"><span data-stu-id="fac94-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span></span>
</dt> <dd>

<span data-ttu-id="fac94-120">Lista de argumentos opcional, que es una lista separada por comas de [argumentos pasados](dx-graphics-hlsl-function-parameters.md) a una función.</span><span class="sxs-lookup"><span data-stu-id="fac94-120">Optional argument list, which is a comma-separated list of [arguments](dx-graphics-hlsl-function-parameters.md) passed into a function.</span></span>

</dd> <dt>

<span data-ttu-id="fac94-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semántica*</span><span class="sxs-lookup"><span data-stu-id="fac94-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="fac94-122">Cadena opcional que identifica el uso previsto de los datos devueltos (vea [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span><span class="sxs-lookup"><span data-stu-id="fac94-122">Optional string that identifies the intended usage of the return data (see [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span></span>

</dd> <dt>

<span data-ttu-id="fac94-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="fac94-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="fac94-124">Instrucciones [opcionales](dx-graphics-hlsl-statement-blocks.md) que son el cuerpo de la función.</span><span class="sxs-lookup"><span data-stu-id="fac94-124">Optional [statements](dx-graphics-hlsl-statement-blocks.md) that make up the body of the function.</span></span> <span data-ttu-id="fac94-125">Una función definida sin un cuerpo se denomina prototipo de función; El cuerpo de una función de prototipo debe definirse en otro lugar antes de que se pueda llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="fac94-125">A function defined without a body is called a function prototype; the body of a prototype function must be defined elsewhere before the function can be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac94-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fac94-126">Return Value</span></span>

<span data-ttu-id="fac94-127">El tipo de valor devuelto puede ser cualquiera de estos [tipos HLSL.](dx-graphics-hlsl-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="fac94-127">The return type can be any one of these [HLSL types](dx-graphics-hlsl-data-types.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fac94-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fac94-128">Remarks</span></span>

<span data-ttu-id="fac94-129">La sintaxis de esta página describe casi todos los tipos de función HLSL, lo que incluye sombreadores de vértices, sombreadores de píxeles y funciones auxiliares.</span><span class="sxs-lookup"><span data-stu-id="fac94-129">The syntax on this page describes almost every type of HLSL function, this includes vertex shaders, pixel shaders, and helper functions.</span></span> <span data-ttu-id="fac94-130">Aunque un sombreador de geometría también se implementa con una función, su sintaxis es un poco más complicada, por lo que hay una página independiente que define una declaración de función de sombreador de geometría (vea Objeto de sombreador de geometría [(HLSL de DirectX).](dx-graphics-hlsl-geometry-shader.md)</span><span class="sxs-lookup"><span data-stu-id="fac94-130">While a geometry shader is also implemented with a function, its syntax is a little more complicated, so there is a separate page that defines a geometry shader function declaration (see [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span></span>

<span data-ttu-id="fac94-131">Una función se puede sobrecargar siempre y cuando se le de una combinación única de tipos de parámetro o orden de parámetros.</span><span class="sxs-lookup"><span data-stu-id="fac94-131">A function can be overloaded as long as it is given a unique combination of parameter types and/or parameter order.</span></span> <span data-ttu-id="fac94-132">HLSL también implementa una serie de funciones intrínsecas o [**integradas.**](dx-graphics-hlsl-intrinsic-functions.md)</span><span class="sxs-lookup"><span data-stu-id="fac94-132">HLSL also implements a number of built in, or [**intrinsic functions**](dx-graphics-hlsl-intrinsic-functions.md).</span></span>

<span data-ttu-id="fac94-133">Puede especificar planos de recorte específicos del usuario con el **atributo clipplanes.**</span><span class="sxs-lookup"><span data-stu-id="fac94-133">You can specify user-specific clip planes with the **clipplanes** attribute.</span></span> <span data-ttu-id="fac94-134">Windows aplica estos planos de recorte a todas las primitivas dibujadas.</span><span class="sxs-lookup"><span data-stu-id="fac94-134">Windows applies these clip planes to all of the primitives drawn.</span></span> <span data-ttu-id="fac94-135">El **atributo clipplanes** funciona como [SV \_ ClipDistance,](dx-graphics-hlsl-semantics.md) pero funciona en todas las características [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) hardware de nivel 9 x \_ y superior.</span><span class="sxs-lookup"><span data-stu-id="fac94-135">The **clipplanes** attribute works like [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) but works on all hardware [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="fac94-136">Para obtener más información, consulte [Planos de recorte de usuario en hardware de nivel de característica 9.](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)</span><span class="sxs-lookup"><span data-stu-id="fac94-136">For more info, see [User clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span></span>

## <a name="examples"></a><span data-ttu-id="fac94-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fac94-137">Examples</span></span>

<span data-ttu-id="fac94-138">Este ejemplo es de BasicHLSL10.fx del [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="fac94-138">This example is from BasicHLSL10.fx from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


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



<span data-ttu-id="fac94-139">En este ejemplo de AdvancedParticles.fx del [ejemplo AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)se ilustra el uso de una semántica para el tipo de valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="fac94-139">This example from AdvancedParticles.fx from the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), illustrates using a semantic for the return type.</span></span>


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a><span data-ttu-id="fac94-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fac94-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fac94-141">Funciones (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="fac94-141">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
