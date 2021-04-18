---
title: Efecto de RGB a matiz
description: Convierte una imagen RGB en los espacios de colores HSL (Hue, saturación, luminosidad) o HSV (matiz, saturación, valor).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422229"
---
# <a name="rgb-to-hue-effect"></a><span data-ttu-id="24ffc-103">Efecto de RGB a matiz</span><span class="sxs-lookup"><span data-stu-id="24ffc-103">RGB-to-hue effect</span></span>

<span data-ttu-id="24ffc-104">Convierte una imagen RGB en los espacios de colores HSL (Hue, saturación, luminosidad) o HSV (matiz, saturación, valor).</span><span class="sxs-lookup"><span data-stu-id="24ffc-104">Converts an RGB image to either the HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) color spaces.</span></span>

<span data-ttu-id="24ffc-105">HSL y HSV son dos modelos diferentes para representar un color RGB en un espacio de colores cilíndrico.</span><span class="sxs-lookup"><span data-stu-id="24ffc-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="24ffc-106">Son útiles porque le permiten motivar un color mediante conceptos más intuitivos como el matiz y la intensidad, frente a la combinación de valores rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="24ffc-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="24ffc-107">Este efecto normaliza los datos de salida (matiz, valor de saturación para HSV o Hue, saturación, luminosidad para HSL) al intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="24ffc-107">This effect normalizes the output data (hue, saturation value for HSV or hue, saturation, lightness for HSL) to the range \[0, 1\].</span></span>

<span data-ttu-id="24ffc-108">El CLSID para este efecto es CLSID \_ D2D1RgbToHue.</span><span class="sxs-lookup"><span data-stu-id="24ffc-108">The CLSID for this effect is CLSID\_D2D1RgbToHue.</span></span>

<span data-ttu-id="24ffc-109">Para invertir el comportamiento de este efecto, use el [efecto matiz a RGB](hue-to-rgb-effect.md).</span><span class="sxs-lookup"><span data-stu-id="24ffc-109">To reverse the behavior of this effect, use the [Hue to RGB effect](hue-to-rgb-effect.md).</span></span>

-   [<span data-ttu-id="24ffc-110">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="24ffc-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="24ffc-111">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="24ffc-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="24ffc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24ffc-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="24ffc-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24ffc-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="24ffc-114">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="24ffc-114">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a><span data-ttu-id="24ffc-115">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="24ffc-115">Effect properties</span></span>

<span data-ttu-id="24ffc-116">Las propiedades del efecto de contraste se definen mediante la enumeración [**\_ \_ prop de D2D1 RGBTOHUE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) .</span><span class="sxs-lookup"><span data-stu-id="24ffc-116">The properties for the contrast effect are defined by the [**D2D1\_RGBTOHUE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="24ffc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24ffc-117">Requirements</span></span>



| <span data-ttu-id="24ffc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24ffc-118">Requirement</span></span> | <span data-ttu-id="24ffc-119">Value</span><span class="sxs-lookup"><span data-stu-id="24ffc-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="24ffc-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24ffc-120">Minimum supported client</span></span> | <span data-ttu-id="24ffc-121">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="24ffc-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="24ffc-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24ffc-122">Minimum supported server</span></span> | <span data-ttu-id="24ffc-123">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="24ffc-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="24ffc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24ffc-124">Header</span></span>                   | <span data-ttu-id="24ffc-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="24ffc-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="24ffc-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24ffc-126">Library</span></span>                  | <span data-ttu-id="24ffc-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="24ffc-127">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="24ffc-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24ffc-128">Related topics</span></span>

* [<span data-ttu-id="24ffc-129">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="24ffc-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
