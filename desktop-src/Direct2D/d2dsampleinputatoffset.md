---
title: Función D2DSampleInputAtOffset (D2d1effecthelpers. h)
description: Los ejemplos de entrada N tienen un desplazamiento de desplazamiento desde la coordenada de entrada. Solo está disponible para las entradas complejas.
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- Función D2DSampleInputAtOffset Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7718f8f48ddfd316d1312dbdff3a5da1f45dfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661251"
---
# <a name="d2dsampleinputatoffset-function"></a><span data-ttu-id="b0bef-105">D2DSampleInputAtOffset función)</span><span class="sxs-lookup"><span data-stu-id="b0bef-105">D2DSampleInputAtOffset function</span></span>

<span data-ttu-id="b0bef-106">Los ejemplos de entrada N tienen un desplazamiento de desplazamiento desde la coordenada de entrada.</span><span class="sxs-lookup"><span data-stu-id="b0bef-106">Samples input N at an offset of offset from the input coordinate.</span></span> <span data-ttu-id="b0bef-107">Solo está disponible para las entradas complejas.</span><span class="sxs-lookup"><span data-stu-id="b0bef-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0bef-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0bef-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="b0bef-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0bef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0bef-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0bef-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0bef-111">Número de entrada.</span><span class="sxs-lookup"><span data-stu-id="b0bef-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="b0bef-112">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0bef-112">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0bef-113">Desplazamiento de UV.</span><span class="sxs-lookup"><span data-stu-id="b0bef-113">The uv offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0bef-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0bef-114">Return value</span></span>

<span data-ttu-id="b0bef-115">La función devuelve una **FLOAT4**, en el formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="b0bef-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0bef-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0bef-116">Remarks</span></span>

<span data-ttu-id="b0bef-117">En el ejemplo siguiente se muestra la función que se usa como parte de una máscara de degradado de resaltado y sombras.</span><span class="sxs-lookup"><span data-stu-id="b0bef-117">The following example shows the function being used as part of a highlighting and shadows gradient mask.</span></span>

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
}  
```

## <a name="requirements"></a><span data-ttu-id="b0bef-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0bef-118">Requirements</span></span>



| <span data-ttu-id="b0bef-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0bef-119">Requirement</span></span> | <span data-ttu-id="b0bef-120">Value</span><span class="sxs-lookup"><span data-stu-id="b0bef-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0bef-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0bef-121">Header</span></span><br/> | <dl> <span data-ttu-id="b0bef-122"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="b0bef-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="b0bef-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0bef-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="b0bef-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0bef-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="b0bef-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0bef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0bef-126">Vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="b0bef-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="b0bef-127">Aplicaciones auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="b0bef-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





