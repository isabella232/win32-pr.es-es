---
title: D2D_PS_ENTRY función (D2d1effecthelpers. h)
description: Macro que define un punto de entrada del sombreador de píxeles con el nombre de función especificado.
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- D2D_PS_ENTRY función Direct2D
topic_type:
- apiref
api_name:
- D2D_PS_ENTRY
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7525416eed7700709d02d2ec17823cd57a8c12ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670376"
---
# <a name="d2d_ps_entry-function"></a><span data-ttu-id="804d7-104">D2D \_ \_ función de entrada PS</span><span class="sxs-lookup"><span data-stu-id="804d7-104">D2D\_PS\_ENTRY function</span></span>

<span data-ttu-id="804d7-105">Macro que define un punto de entrada del sombreador de píxeles con el nombre de función especificado.</span><span class="sxs-lookup"><span data-stu-id="804d7-105">A macro that defines a pixel shader entry point with the given function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="804d7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="804d7-106">Syntax</span></span>

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a><span data-ttu-id="804d7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="804d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="804d7-108">*Nombreentrada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="804d7-108">*Entryname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="804d7-109">Nombre del punto de entrada del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="804d7-109">The pixel shader entry point name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="804d7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="804d7-110">Return value</span></span>

<span data-ttu-id="804d7-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="804d7-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="804d7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="804d7-112">Remarks</span></span>

<span data-ttu-id="804d7-113">Use esta macro en lugar de especificar la firma de entrada de punto de entrada de la manera normal: todos los parámetros son implícitos y se agregan mediante Direct2D durante la compilación según el tipo de destino de compilación (sombreador completo o función de exportación).</span><span class="sxs-lookup"><span data-stu-id="804d7-113">Use this macro instead of specifying the entry point s input signature in the normal manner: all parameters are implicit and added by Direct2D during compilation depending on the compilation target type (full shader or export function).</span></span>

``` syntax
#define D2D_INPUT_COUNT 1 
#define D2D_INPUT0_SIMPLE 
#include  d2d1effectauthor.hlsli  

D2D_PS_ENTRY(LinkingCompatiblePixelShader) 
{ 
    float4 input = D2DGetInput(0);  

    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="804d7-114">En este breve ejemplo, observe que no se declara ningún parámetro de función, que el número de entradas y el tipo de cada entrada se declara antes que la función de entrada, la entrada se recupera llamando a [D2DGetInput](d2dgetinput.md)y que se deben definir las directivas de preprocesador antes de que se incluya el archivo auxiliar.</span><span class="sxs-lookup"><span data-stu-id="804d7-114">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="804d7-115">Un sombreador compatible con vinculación debe proporcionar un sombreador de píxeles de paso único normal y una función de sombreador de exportación.</span><span class="sxs-lookup"><span data-stu-id="804d7-115">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="804d7-116">La \_ macro D2D PS \_ entry permite que cada una de ellas se genere a partir del mismo código, cuando se usa junto con el script de compilación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="804d7-116">The D2D\_PS\_ENTRY macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="804d7-117">Al compilar un sombreador completo, las macros se expanden en el código siguiente, que tiene una firma de entrada compatible con efectos de D2D.</span><span class="sxs-lookup"><span data-stu-id="804d7-117">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

``` syntax
Texture2D<float4> InputTexture0; 
SamplerState InputSampler0; 

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,   
    float4 posScene : SCENE_POSITION,    
    float4 uv0  : TEXCOORD0 
    ) : SV_Target 
{ 
    float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);  

    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="804d7-118">Al compilar una versión de función de exportación del mismo código, se genera el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="804d7-118">When compiling an export function version of the same code, the following code is generated:</span></span>

``` syntax
// Shader function version 
export float4 LinkingCompatiblePixelShader_Function( 
    float4 input0 : INPUT0 
    ) 
{ 
    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="804d7-119">Tenga en cuenta que la entrada de textura, que normalmente se recupera mediante el muestreo de un Texture2D, se ha reemplazado por una entrada de función input0.</span><span class="sxs-lookup"><span data-stu-id="804d7-119">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input input0.</span></span>

## <a name="requirements"></a><span data-ttu-id="804d7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="804d7-120">Requirements</span></span>



| <span data-ttu-id="804d7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="804d7-121">Requirement</span></span> | <span data-ttu-id="804d7-122">Value</span><span class="sxs-lookup"><span data-stu-id="804d7-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="804d7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="804d7-123">Header</span></span><br/> | <dl> <span data-ttu-id="804d7-124"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="804d7-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="804d7-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="804d7-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="804d7-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="804d7-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="804d7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="804d7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804d7-128">Vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="804d7-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="804d7-129">Aplicaciones auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="804d7-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





