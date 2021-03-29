---
title: D1111 usando la capa cuando el clip sea suficiente
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Una capa se usa con una máscara de opacidad nula, una opacidad de 1,0 y una máscara geométrica rectangular alineada de eje. La API de recorte de inserciones/pop debe lograr los mismos resultados con un rendimiento mayor.
keywords:
- D1111 usar la capa cuando el clip sea Direct2D suficiente
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: a30bbfd7b8ca448928249018a28bc4d6a8a2f57f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793702"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a><span data-ttu-id="14ecb-105">D1111: uso de la capa cuando el clip es suficiente</span><span class="sxs-lookup"><span data-stu-id="14ecb-105">D1111: Using Layer When Clip Is Sufficient</span></span>

<span data-ttu-id="14ecb-106">PERF: una capa se usa con una máscara de opacidad **nula** , una opacidad de 1,0 y una máscara geométrica rectangular alineada de eje.</span><span class="sxs-lookup"><span data-stu-id="14ecb-106">PERF - A layer is being used with a **NULL** opacity mask, 1.0 opacity, and an axis aligned rectangular geometric mask.</span></span> <span data-ttu-id="14ecb-107">La API de recorte de inserciones/pop debe lograr los mismos resultados con un rendimiento mayor.</span><span class="sxs-lookup"><span data-stu-id="14ecb-107">The Push/Pop Clip API should achieve the same results with higher performance.</span></span>

## <a name="placeholders"></a><span data-ttu-id="14ecb-108">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="14ecb-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="14ecb-109"><span id="interface"></span><span id="INTERFACE"></span>*interfaz*</span><span class="sxs-lookup"><span data-stu-id="14ecb-109"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="14ecb-110">Dirección de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="14ecb-110">The address of the interface.</span></span>

</dd> </dl> 

|             |             |
|-------------|-------------|
| <span data-ttu-id="14ecb-111">Nivel de error</span><span class="sxs-lookup"><span data-stu-id="14ecb-111">Error Level</span></span> | <span data-ttu-id="14ecb-112">Información</span><span class="sxs-lookup"><span data-stu-id="14ecb-112">Information</span></span> |



 

## <a name="examples"></a><span data-ttu-id="14ecb-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="14ecb-113">Examples</span></span>

<span data-ttu-id="14ecb-114">El código siguiente usa [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) cuando la capa contiene solo un primitivo (un rectángulo) y los campos de la estructura [**de \_ \_ parámetros de capa D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) se establecen en valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="14ecb-114">The following code uses the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) when the layer contains only one primitive (a rectangle) and the fields of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to defaults.</span></span> <span data-ttu-id="14ecb-115">Para obtener los valores predeterminados de la estructura de **\_ \_ parámetros de capa D2D1** , vea [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span><span class="sxs-lookup"><span data-stu-id="14ecb-115">For the default values of the **D2D1\_LAYER\_PARAMETERS** structure, see [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span></span>


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



<span data-ttu-id="14ecb-116">Este ejemplo genera el siguiente mensaje de depuración:</span><span class="sxs-lookup"><span data-stu-id="14ecb-116">This example produces the following debug message:</span></span>

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a><span data-ttu-id="14ecb-117">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="14ecb-117">Possible Causes</span></span>

<span data-ttu-id="14ecb-118">Se usó una capa cuando los métodos [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) y [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) hubieran sido suficientes.</span><span class="sxs-lookup"><span data-stu-id="14ecb-118">A layer was used when the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) methods would have sufficed.</span></span>

 

 