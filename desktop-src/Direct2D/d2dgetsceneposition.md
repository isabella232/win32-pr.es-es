---
title: Función D2DGetScenePosition (D2d1effecthelpers. h)
description: Devuelve el valor de la posición de la escena de entrada \_ . Solo está disponible cuando \_ D2D \_ requiere \_ que la posición de la escena se declare en el archivo de código fuente.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- Función D2DGetScenePosition Direct2D
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661211"
---
# <a name="d2dgetsceneposition-function"></a><span data-ttu-id="3f799-105">D2DGetScenePosition función)</span><span class="sxs-lookup"><span data-stu-id="3f799-105">D2DGetScenePosition function</span></span>

<span data-ttu-id="3f799-106">Devuelve el valor de la posición de la escena de entrada \_ .</span><span class="sxs-lookup"><span data-stu-id="3f799-106">Returns the value of the input SCENE\_POSITION.</span></span> <span data-ttu-id="3f799-107">Solo está disponible cuando \_ D2D \_ requiere \_ que la posición de la escena se declare en el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="3f799-107">Only available when D2D\_REQUIRES\_SCENE\_POSITION is declared in the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f799-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f799-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a><span data-ttu-id="3f799-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f799-109">Parameters</span></span>

<span data-ttu-id="3f799-110">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3f799-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f799-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f799-111">Return value</span></span>

<span data-ttu-id="3f799-112">La función devuelve una **FLOAT4** en el formato posición de la escena \_ .</span><span class="sxs-lookup"><span data-stu-id="3f799-112">The function returns a **float4** in the format SCENE\_POSITION.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f799-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f799-113">Remarks</span></span>

<span data-ttu-id="3f799-114">En el ejemplo siguiente se muestra el uso de la función para generar un patrón de resolución.</span><span class="sxs-lookup"><span data-stu-id="3f799-114">The following example shows the use of the function in generating a dissolve pattern.</span></span>

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
}  
```

## <a name="requirements"></a><span data-ttu-id="3f799-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f799-115">Requirements</span></span>



| <span data-ttu-id="3f799-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f799-116">Requirement</span></span> | <span data-ttu-id="3f799-117">Value</span><span class="sxs-lookup"><span data-stu-id="3f799-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f799-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f799-118">Header</span></span><br/> | <dl> <span data-ttu-id="3f799-119"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="3f799-119"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="3f799-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f799-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="3f799-121"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f799-121"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="3f799-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f799-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f799-123">Vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="3f799-123">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="3f799-124">Aplicaciones auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="3f799-124">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





