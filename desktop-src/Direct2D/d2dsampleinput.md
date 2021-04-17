---
title: Función D2DSampleInput (D2d1effecthelpers. h)
description: Los ejemplos de entrada N en la posición UV. Solo está disponible para las entradas complejas.
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- Función D2DSampleInput Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5929e9c113e5fa9a7c8a72003357b280a810e49e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681079"
---
# <a name="d2dsampleinput-function"></a><span data-ttu-id="28a34-105">D2DSampleInput función)</span><span class="sxs-lookup"><span data-stu-id="28a34-105">D2DSampleInput function</span></span>

<span data-ttu-id="28a34-106">Los ejemplos de entrada N en la posición UV.</span><span class="sxs-lookup"><span data-stu-id="28a34-106">Samples input N at position uv.</span></span> <span data-ttu-id="28a34-107">Solo está disponible para las entradas complejas.</span><span class="sxs-lookup"><span data-stu-id="28a34-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="28a34-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28a34-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="28a34-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28a34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28a34-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28a34-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28a34-111">Número de entrada.</span><span class="sxs-lookup"><span data-stu-id="28a34-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="28a34-112">*UV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28a34-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28a34-113">Posición UV.</span><span class="sxs-lookup"><span data-stu-id="28a34-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28a34-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28a34-114">Return value</span></span>

<span data-ttu-id="28a34-115">La función devuelve una **FLOAT4**, en el formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="28a34-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="28a34-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28a34-116">Remarks</span></span>

<span data-ttu-id="28a34-117">En el ejemplo siguiente se muestra la función que se utiliza para calcular las normales de superficie.</span><span class="sxs-lookup"><span data-stu-id="28a34-117">The following example shows the function being used to calculate surface normals.</span></span>

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
}  
```

## <a name="requirements"></a><span data-ttu-id="28a34-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28a34-118">Requirements</span></span>



| <span data-ttu-id="28a34-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="28a34-119">Requirement</span></span> | <span data-ttu-id="28a34-120">Value</span><span class="sxs-lookup"><span data-stu-id="28a34-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28a34-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28a34-121">Header</span></span><br/> | <dl> <span data-ttu-id="28a34-122"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="28a34-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="28a34-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28a34-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="28a34-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28a34-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="28a34-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="28a34-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a34-126">Vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="28a34-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="28a34-127">Aplicaciones auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="28a34-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





