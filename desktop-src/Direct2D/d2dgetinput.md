---
title: Función D2DGetInput (D2d1effecthelpers. h)
description: Devuelve el color de entrada N en la coordenada de entrada. Solo está disponible para entradas simples.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- Función D2DGetInput Direct2D
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661104"
---
# <a name="d2dgetinput-function"></a><span data-ttu-id="8d242-105">D2DGetInput función)</span><span class="sxs-lookup"><span data-stu-id="8d242-105">D2DGetInput function</span></span>

<span data-ttu-id="8d242-106">Devuelve el color de entrada N en la coordenada de entrada.</span><span class="sxs-lookup"><span data-stu-id="8d242-106">Returns the color of input N at the input coordinate.</span></span> <span data-ttu-id="8d242-107">Solo está disponible para entradas simples.</span><span class="sxs-lookup"><span data-stu-id="8d242-107">Only available for simple inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d242-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d242-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInput(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="8d242-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d242-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d242-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d242-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d242-111">Número de entrada.</span><span class="sxs-lookup"><span data-stu-id="8d242-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d242-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d242-112">Return value</span></span>

<span data-ttu-id="8d242-113">La función devuelve una **FLOAT4**, que contiene el color RGBA en el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="8d242-113">The function returns a **float4**, containing the RGBA color in the format INPUTN.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d242-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d242-114">Remarks</span></span>

<span data-ttu-id="8d242-115">En el ejemplo siguiente se muestra la función que se utiliza como parte de un efecto compuesto aritmético.</span><span class="sxs-lookup"><span data-stu-id="8d242-115">The following example shows the function being used as part of an arithmetic composite effect.</span></span>

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

<span data-ttu-id="8d242-116">Además, consulte la entrada de comentarios [de \_ D2D \_ PS](d2d-ps-entry.md) para ver otro ejemplo del uso de esta función.</span><span class="sxs-lookup"><span data-stu-id="8d242-116">Also, refer to the remarks for [D2D\_PS\_ENTRY](d2d-ps-entry.md) for another example of the use of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d242-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d242-117">Requirements</span></span>



| <span data-ttu-id="8d242-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d242-118">Requirement</span></span> | <span data-ttu-id="8d242-119">Value</span><span class="sxs-lookup"><span data-stu-id="8d242-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d242-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d242-120">Header</span></span><br/> | <dl> <span data-ttu-id="8d242-121"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="8d242-121"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="8d242-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d242-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="8d242-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d242-123"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="8d242-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d242-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d242-125">Vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="8d242-125">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="8d242-126">Aplicaciones auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="8d242-126">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





