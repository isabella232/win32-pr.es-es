---
title: SV_InnerCoverage
description: Entrada SVCoverage representa información de rasterización conservadora subestimada (es decir, si se garantiza que un píxel esté totalmente \_ cubierto).
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
ms.openlocfilehash: e1ac278f0524446b5171ef278e169fbe7c3a082f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996972"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="a28d5-104">SV \_ InnerCoverage</span><span class="sxs-lookup"><span data-stu-id="a28d5-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="a28d5-105">Entrada SVCoverage representa información de rasterización conservadora subestimada (es decir, si se garantiza que un píxel esté totalmente \_ cubierto).</span><span class="sxs-lookup"><span data-stu-id="a28d5-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="a28d5-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a28d5-106">Type</span></span>



|      |
|------|
| <span data-ttu-id="a28d5-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a28d5-107">Type</span></span> |
| <span data-ttu-id="a28d5-108">uint</span><span class="sxs-lookup"><span data-stu-id="a28d5-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a28d5-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a28d5-109">Remarks</span></span>

<span data-ttu-id="a28d5-110">Este valor generado por el sistema es necesario para la compatibilidad con el nivel 3 y solo está disponible en ese nivel.</span><span class="sxs-lookup"><span data-stu-id="a28d5-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="a28d5-111">Esta entrada es mutuamente excluyente con la cobertura \_ SV; no se pueden usar ambos.</span><span class="sxs-lookup"><span data-stu-id="a28d5-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="a28d5-112">Para acceder a SV InnerCoverage, debe declararse como un único componente de uno de los registros de entrada del \_ sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="a28d5-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="a28d5-113">El modo de interpolación de la declaración debe ser constante (no se aplica la interpolación).</span><span class="sxs-lookup"><span data-stu-id="a28d5-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="a28d5-114">La rasterización conservadora está disponible en D3D11.3 y D3D12.</span><span class="sxs-lookup"><span data-stu-id="a28d5-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="a28d5-115">Consulte</span><span class="sxs-lookup"><span data-stu-id="a28d5-115">Refer to:</span></span>

-   [<span data-ttu-id="a28d5-116">Rasterización conservadora de D3D11.3</span><span class="sxs-lookup"><span data-stu-id="a28d5-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="a28d5-117">Rasterización conservadora de D3D12</span><span class="sxs-lookup"><span data-stu-id="a28d5-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="a28d5-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a28d5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a28d5-119">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="a28d5-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="a28d5-120">Modelos de sombreador 5.1 Valores del sistema</span><span class="sxs-lookup"><span data-stu-id="a28d5-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
