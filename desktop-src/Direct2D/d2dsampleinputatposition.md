---
title: Función D2DSampleInputAtPosition (D2d1effecthelpers. h)
description: Muestra la entrada N en una posición de escena absoluta, en lugar de una posición relativa de entrada. Solo está disponible para las entradas complejas.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- Función D2DSampleInputAtPosition Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681078"
---
# <a name="d2dsampleinputatposition-function"></a><span data-ttu-id="2c8c6-105">D2DSampleInputAtPosition función)</span><span class="sxs-lookup"><span data-stu-id="2c8c6-105">D2DSampleInputAtPosition function</span></span>

<span data-ttu-id="2c8c6-106">Muestra la entrada N en una posición de escena absoluta, en lugar de una posición relativa de entrada.</span><span class="sxs-lookup"><span data-stu-id="2c8c6-106">Samples input N at an absolute scene position, rather than an input-relative position.</span></span> <span data-ttu-id="2c8c6-107">Solo está disponible para las entradas complejas.</span><span class="sxs-lookup"><span data-stu-id="2c8c6-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8c6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c8c6-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="2c8c6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c8c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c8c6-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c8c6-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8c6-111">Número de entrada.</span><span class="sxs-lookup"><span data-stu-id="2c8c6-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="2c8c6-112">*UV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c8c6-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8c6-113">Posición UV.</span><span class="sxs-lookup"><span data-stu-id="2c8c6-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c8c6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c8c6-114">Return value</span></span>

<span data-ttu-id="2c8c6-115">La función devuelve una **FLOAT4**, en el formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="2c8c6-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c8c6-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c8c6-116">Remarks</span></span>

<span data-ttu-id="2c8c6-117">En el ejemplo siguiente se muestra la función utilizada en un ceñido circular.</span><span class="sxs-lookup"><span data-stu-id="2c8c6-117">The following example shows the function used in a circular wrap.</span></span>

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
}
```

## <a name="requirements"></a><span data-ttu-id="2c8c6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c8c6-118">Requirements</span></span>



| <span data-ttu-id="2c8c6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c8c6-119">Requirement</span></span> | <span data-ttu-id="2c8c6-120">Value</span><span class="sxs-lookup"><span data-stu-id="2c8c6-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8c6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c8c6-121">Header</span></span><br/> | <dl> <span data-ttu-id="2c8c6-122"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="2c8c6-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="2c8c6-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c8c6-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="2c8c6-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c8c6-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="2c8c6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c8c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8c6-126">Vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="2c8c6-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="2c8c6-127">Aplicaciones auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="2c8c6-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





