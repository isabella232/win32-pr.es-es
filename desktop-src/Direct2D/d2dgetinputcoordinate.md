---
title: Función D2DGetInputCoordinate (D2d1effecthelpers. h)
description: Devuelve el valor de la TEXCOORDN de entrada. Solo está disponible para las entradas complejas.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- Función D2DGetInputCoordinate Direct2D
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5d9ee759de12bb8b017d582026dd5b5ca8c3fb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681018"
---
# <a name="d2dgetinputcoordinate-function"></a><span data-ttu-id="65687-105">D2DGetInputCoordinate función)</span><span class="sxs-lookup"><span data-stu-id="65687-105">D2DGetInputCoordinate function</span></span>

<span data-ttu-id="65687-106">Devuelve el valor de la TEXCOORDN de entrada.</span><span class="sxs-lookup"><span data-stu-id="65687-106">Returns the value of the input TEXCOORDN.</span></span> <span data-ttu-id="65687-107">Solo está disponible para las entradas complejas.</span><span class="sxs-lookup"><span data-stu-id="65687-107">Available only for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="65687-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65687-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="65687-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65687-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65687-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65687-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65687-111">Número de entrada.</span><span class="sxs-lookup"><span data-stu-id="65687-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65687-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65687-112">Return value</span></span>

<span data-ttu-id="65687-113">La función devuelve una **FLOAT4**, en el formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="65687-113">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="65687-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65687-114">Remarks</span></span>

<span data-ttu-id="65687-115">La coordenada devuelta por esta función está en el espacio textura.</span><span class="sxs-lookup"><span data-stu-id="65687-115">The coordinate returned by this function is in texel space.</span></span> <span data-ttu-id="65687-116">Un sombreador no debe tomar ninguna dependencia sobre cómo se calcula este valor.</span><span class="sxs-lookup"><span data-stu-id="65687-116">A shader shouldn't take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="65687-117">Solo debe usarlo para muestrear la entrada del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="65687-117">It should use it only to sample the pixel shader's input.</span></span> <span data-ttu-id="65687-118">Para obtener más información, vea [Agregar un sombreador de píxeles a una transformación personalizada](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span><span class="sxs-lookup"><span data-stu-id="65687-118">For more info, see [Adding a pixel shader to a custom transform](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span></span>

<span data-ttu-id="65687-119">En el ejemplo siguiente se muestra la función utilizada para un efecto de mapa de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="65687-119">The following example shows the function used for a displacement map effect.</span></span>

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
}  
```

## <a name="requirements"></a><span data-ttu-id="65687-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65687-120">Requirements</span></span>



| <span data-ttu-id="65687-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="65687-121">Requirement</span></span> | <span data-ttu-id="65687-122">Value</span><span class="sxs-lookup"><span data-stu-id="65687-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65687-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65687-123">Header</span></span><br/> | <dl> <span data-ttu-id="65687-124"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="65687-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="65687-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65687-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="65687-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65687-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="65687-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="65687-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65687-128">Vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="65687-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="65687-129">Aplicaciones auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="65687-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

