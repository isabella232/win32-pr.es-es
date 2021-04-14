---
title: Efecto resaltado y sombras
description: Ajusta las iluminaciones y las sombras de la imagen.
ms.assetid: ebbb7d99-9144-ffff-af73-d89e7d269924
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d595a5b82a2df0b0b0bab14c03e6a807511ed61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104555857"
---
# <a name="highlights-and-shadows-effect"></a><span data-ttu-id="31fef-103">Efecto resaltado y sombras</span><span class="sxs-lookup"><span data-stu-id="31fef-103">Highlights and shadows effect</span></span>

<span data-ttu-id="31fef-104">Ajusta las iluminaciones y las sombras de la imagen.</span><span class="sxs-lookup"><span data-stu-id="31fef-104">Adjusts the highlights and shadows of the image.</span></span>

<span data-ttu-id="31fef-105">El CLSID para este efecto es CLSID \_ D2D1HighlightsShadows.</span><span class="sxs-lookup"><span data-stu-id="31fef-105">The CLSID for this effect is CLSID\_D2D1HighlightsShadows.</span></span>

-   [<span data-ttu-id="31fef-106">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="31fef-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="31fef-107">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="31fef-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="31fef-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="31fef-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="31fef-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31fef-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="31fef-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31fef-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="31fef-111">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="31fef-111">Example image</span></span>

![ejemplo de resultado de efecto](images/highlights-and-shadows-effect.png)

## <a name="sample-code"></a><span data-ttu-id="31fef-113">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="31fef-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> highlightsAndShadowsEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HighlightsShadows, &highlightsAndShadowsEffect);
 
highlightsAndShadowsEffect->SetInput(0, bitmap);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS, 0.0f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS, 0.5f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY, 0.2f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA, D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA_LINEAR);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="31fef-114">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="31fef-114">Effect properties</span></span>

<span data-ttu-id="31fef-115">Las propiedades del efecto resaltados y sombras se definen mediante la enumeración [**\_ \_ prop de D2D1 HIGHLIGHTSANDSHADOWS**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) .</span><span class="sxs-lookup"><span data-stu-id="31fef-115">The properties for the highlights and shadows effect are defined by the [**D2D1\_HIGHLIGHTSANDSHADOWS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="31fef-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31fef-116">Requirements</span></span>

| <span data-ttu-id="31fef-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="31fef-117">Requirement</span></span> | <span data-ttu-id="31fef-118">Value</span><span class="sxs-lookup"><span data-stu-id="31fef-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="31fef-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31fef-119">Minimum supported client</span></span> | <span data-ttu-id="31fef-120">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="31fef-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="31fef-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31fef-121">Minimum supported server</span></span> | <span data-ttu-id="31fef-122">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="31fef-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="31fef-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31fef-123">Header</span></span>                   | <span data-ttu-id="31fef-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="31fef-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="31fef-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31fef-125">Library</span></span>                  | <span data-ttu-id="31fef-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="31fef-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="31fef-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31fef-127">Related topics</span></span>

* [<span data-ttu-id="31fef-128">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="31fef-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
