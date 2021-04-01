---
title: Efecto de matiz a RGB
description: Convierte una imagen HSL (matiz, saturación, luminosidad) o HSV (matiz, saturación, valor) en el espacio de colores RGB.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996322"
---
# <a name="hue-to-rgb-effect"></a><span data-ttu-id="2cc13-103">Efecto de matiz a RGB</span><span class="sxs-lookup"><span data-stu-id="2cc13-103">Hue-to-RGB effect</span></span>

<span data-ttu-id="2cc13-104">Convierte una imagen HSL (matiz, saturación, luminosidad) o HSV (matiz, saturación, valor) en el espacio de colores RGB.</span><span class="sxs-lookup"><span data-stu-id="2cc13-104">Converts an HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) image to the RGB color space.</span></span>

<span data-ttu-id="2cc13-105">HSL y HSV son dos modelos diferentes para representar un color RGB en un espacio de colores cilíndrico.</span><span class="sxs-lookup"><span data-stu-id="2cc13-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="2cc13-106">Son útiles porque le permiten motivar un color mediante conceptos más intuitivos como el matiz y la intensidad, frente a la combinación de valores rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="2cc13-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="2cc13-107">Este efecto pasa por cualquier valor alfa de entrada.</span><span class="sxs-lookup"><span data-stu-id="2cc13-107">This effect passes through any input alpha values.</span></span>

<span data-ttu-id="2cc13-108">El CLSID para este efecto es CLSID \_ D2D1HueToRgb.</span><span class="sxs-lookup"><span data-stu-id="2cc13-108">The CLSID for this effect is CLSID\_D2D1HueToRgb.</span></span>

<span data-ttu-id="2cc13-109">Para invertir el comportamiento de este efecto, utilice el [efecto de RGB a matiz](rgb-to-hue-effect.md).</span><span class="sxs-lookup"><span data-stu-id="2cc13-109">To reverse the behavior of this effect, use the [RGB to Hue effect](rgb-to-hue-effect.md).</span></span>

-   [<span data-ttu-id="2cc13-110">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cc13-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="2cc13-111">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="2cc13-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="2cc13-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cc13-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2cc13-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cc13-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="2cc13-114">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cc13-114">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="2cc13-115">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="2cc13-115">Effect properties</span></span>

<span data-ttu-id="2cc13-116">Las propiedades del efecto de contraste se definen mediante la enumeración [**\_ \_ prop de D2D1 HUETORGB**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) .</span><span class="sxs-lookup"><span data-stu-id="2cc13-116">The properties for the contrast effect are defined by the [**D2D1\_HUETORGB\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc13-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cc13-117">Requirements</span></span>



| <span data-ttu-id="2cc13-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cc13-118">Requirement</span></span> | <span data-ttu-id="2cc13-119">Value</span><span class="sxs-lookup"><span data-stu-id="2cc13-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="2cc13-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cc13-120">Minimum supported client</span></span> | <span data-ttu-id="2cc13-121">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="2cc13-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2cc13-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cc13-122">Minimum supported server</span></span> | <span data-ttu-id="2cc13-123">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="2cc13-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2cc13-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cc13-124">Header</span></span>                   | <span data-ttu-id="2cc13-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="2cc13-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="2cc13-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2cc13-126">Library</span></span>                  | <span data-ttu-id="2cc13-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="2cc13-127">d2d1.lib, dxguid.lib</span></span>                              |



## <a name="related-topics"></a><span data-ttu-id="2cc13-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cc13-128">Related topics</span></span>

* [<span data-ttu-id="2cc13-129">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="2cc13-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
