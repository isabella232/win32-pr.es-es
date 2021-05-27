---
title: D1111 usar capa cuando el clip es suficiente
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Se usa una capa con una máscara de opacidad NULL, una opacidad de 1,0 y una máscara geométrica rectangular alineada en el eje. Push/Pop Clip API debe lograr los mismos resultados con un mayor rendimiento.
keywords:
- D1111 Usar capa cuando clip es suficiente con Direct2D
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8463cc3940b69e326f13df6be9602dd6073fec0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549910"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a><span data-ttu-id="abd74-105">D1111: Usar la capa cuando el clip es suficiente</span><span class="sxs-lookup"><span data-stu-id="abd74-105">D1111: Using Layer When Clip Is Sufficient</span></span>

<span data-ttu-id="abd74-106">PERF: se usa una capa con una máscara de opacidad **NULL,** una opacidad de 1,0 y una máscara geométrica rectangular alineada en el eje.</span><span class="sxs-lookup"><span data-stu-id="abd74-106">PERF - A layer is being used with a **NULL** opacity mask, 1.0 opacity, and an axis aligned rectangular geometric mask.</span></span> <span data-ttu-id="abd74-107">Push/Pop Clip API debe lograr los mismos resultados con un mayor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="abd74-107">The Push/Pop Clip API should achieve the same results with higher performance.</span></span>

## <a name="placeholders"></a><span data-ttu-id="abd74-108">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="abd74-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="abd74-109"><span id="interface"></span><span id="INTERFACE"></span>*Interfaz*</span><span class="sxs-lookup"><span data-stu-id="abd74-109"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="abd74-110">Dirección de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="abd74-110">The address of the interface.</span></span>

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| <span data-ttu-id="abd74-111">Nivel de error</span><span class="sxs-lookup"><span data-stu-id="abd74-111">Error Level</span></span> | <span data-ttu-id="abd74-112">Information</span><span class="sxs-lookup"><span data-stu-id="abd74-112">Information</span></span> |



 

## <a name="examples"></a><span data-ttu-id="abd74-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="abd74-113">Examples</span></span>

<span data-ttu-id="abd74-114">En el código siguiente se usan [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) cuando la capa contiene solo un primitivo (un rectángulo) y los campos de la estructura LAYER PARAMETERS de [**D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) se establecen en valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="abd74-114">The following code uses the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) when the layer contains only one primitive (a rectangle) and the fields of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to defaults.</span></span> <span data-ttu-id="abd74-115">Para obtener los valores predeterminados de la estructura **D2D1 \_ LAYER \_ PARAMETERS,** vea [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span><span class="sxs-lookup"><span data-stu-id="abd74-115">For the default values of the **D2D1\_LAYER\_PARAMETERS** structure, see [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span></span>


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



<span data-ttu-id="abd74-116">En este ejemplo se genera el siguiente mensaje de depuración:</span><span class="sxs-lookup"><span data-stu-id="abd74-116">This example produces the following debug message:</span></span>

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a><span data-ttu-id="abd74-117">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="abd74-117">Possible Causes</span></span>

<span data-ttu-id="abd74-118">Se usó una capa cuando los [**métodos PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) y [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) hubieran bastado.</span><span class="sxs-lookup"><span data-stu-id="abd74-118">A layer was used when the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) methods would have sufficed.</span></span>

 

 