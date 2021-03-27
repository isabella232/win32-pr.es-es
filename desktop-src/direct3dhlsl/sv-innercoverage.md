---
title: SV_InnerCoverage
description: SV \_ InputCoverage representa la información de rasterización conservadora desestimada (es decir, si se garantiza que un píxel está totalmente incluido).
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f1393a6a11a95c8c08746f57083fe193791a60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997141"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="a5780-104">VP \_ InnerCoverage</span><span class="sxs-lookup"><span data-stu-id="a5780-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="a5780-105">SV \_ InputCoverage representa la información de rasterización conservadora desestimada (es decir, si se garantiza que un píxel está totalmente incluido).</span><span class="sxs-lookup"><span data-stu-id="a5780-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="a5780-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5780-106">Type</span></span>



|      |
|------|
| <span data-ttu-id="a5780-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5780-107">Type</span></span> |
| <span data-ttu-id="a5780-108">uint</span><span class="sxs-lookup"><span data-stu-id="a5780-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a5780-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5780-109">Remarks</span></span>

<span data-ttu-id="a5780-110">Este valor generado por el sistema es necesario para la compatibilidad de nivel 3 y solo está disponible en ese nivel.</span><span class="sxs-lookup"><span data-stu-id="a5780-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="a5780-111">Esta entrada es mutuamente excluyente con la \_ cobertura de SV; no se pueden usar las dos.</span><span class="sxs-lookup"><span data-stu-id="a5780-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="a5780-112">Para tener acceso a \_ la InnerCoverage de SV, debe declararse como un componente único de uno de los registros de entrada del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="a5780-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="a5780-113">El modo de interpolación en la declaración debe ser constante (no se aplica la interpolación).</span><span class="sxs-lookup"><span data-stu-id="a5780-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="a5780-114">La rasterización conservadora está disponible tanto en D3D 11.3 como en D3D12.</span><span class="sxs-lookup"><span data-stu-id="a5780-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="a5780-115">Consulte</span><span class="sxs-lookup"><span data-stu-id="a5780-115">Refer to:</span></span>

-   [<span data-ttu-id="a5780-116">Rasterización conservadora de D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="a5780-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="a5780-117">Rasterización conservadora D3D12</span><span class="sxs-lookup"><span data-stu-id="a5780-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="a5780-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5780-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5780-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a5780-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="a5780-120">Modelo de sombreador 5,1 valores del sistema</span><span class="sxs-lookup"><span data-stu-id="a5780-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 