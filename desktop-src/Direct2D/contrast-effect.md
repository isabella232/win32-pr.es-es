---
title: Efecto de contraste
description: Aumenta o disminuye el contraste de una imagen.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079480"
---
# <a name="contrast-effect"></a><span data-ttu-id="acae7-103">Efecto de contraste</span><span class="sxs-lookup"><span data-stu-id="acae7-103">Contrast effect</span></span>

<span data-ttu-id="acae7-104">Aumenta o disminuye el contraste de una imagen.</span><span class="sxs-lookup"><span data-stu-id="acae7-104">Increases or decreases the contrast of an image.</span></span>

<span data-ttu-id="acae7-105">El CLSID para este efecto es CLSID \_ D2D1Contrast.</span><span class="sxs-lookup"><span data-stu-id="acae7-105">The CLSID for this effect is CLSID\_D2D1Contrast.</span></span>

<span data-ttu-id="acae7-106">La función Contrast modifica cada valor del canal de color mediante dos polinómicas cuadráticas a trozos que se cumplen con la continuidad de la pendiente en el punto (0,5, 0,5).</span><span class="sxs-lookup"><span data-stu-id="acae7-106">The contrast function modifies each color channel value using two, piecewise quadratic polynomials that meet with slope continuity at the point (0.5, 0.5).</span></span>

![a trozos polinómicos cuadráticas que se cumplen con la continuidad de la pendiente en el punto (0,5, 0,5)](images/contrast-effect-slope.png)

-   [<span data-ttu-id="acae7-108">Imágenes de ejemplo</span><span class="sxs-lookup"><span data-stu-id="acae7-108">Example Images</span></span>](#example-images)
-   [<span data-ttu-id="acae7-109">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="acae7-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="acae7-110">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="acae7-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="acae7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acae7-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="acae7-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acae7-112">Related topics</span></span>](#related-topics)

## <a name="example-images"></a><span data-ttu-id="acae7-113">Imágenes de ejemplo</span><span class="sxs-lookup"><span data-stu-id="acae7-113">Example images</span></span>

<span data-ttu-id="acae7-114">En este ejemplo se muestra el resultado del efecto con el contraste máximo aplicado (Contrast = 1,0).</span><span class="sxs-lookup"><span data-stu-id="acae7-114">This example shows the output of the effect with maximum contrast applied (Contrast = 1.0).</span></span>

<span data-ttu-id="acae7-115">Antes</span><span class="sxs-lookup"><span data-stu-id="acae7-115">Before</span></span>

![imagen antes de aplicar el efecto](images/contrast-effect-before.png)

<span data-ttu-id="acae7-117">Después</span><span class="sxs-lookup"><span data-stu-id="acae7-117">After</span></span>

![se aplica la imagen después del efecto](images/contrast-effect-after.png)

## <a name="sample-code"></a><span data-ttu-id="acae7-119">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="acae7-119">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="acae7-120">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="acae7-120">Effect properties</span></span>

<span data-ttu-id="acae7-121">Las propiedades del efecto de contraste se definen mediante la enumeración de la propiedad [**\_ \_ contraste D2D1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) .</span><span class="sxs-lookup"><span data-stu-id="acae7-121">The properties for the contrast effect are defined by the [**D2D1\_CONTRAST\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="acae7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acae7-122">Requirements</span></span>

| <span data-ttu-id="acae7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="acae7-123">Requirement</span></span> | <span data-ttu-id="acae7-124">Value</span><span class="sxs-lookup"><span data-stu-id="acae7-124">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="acae7-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acae7-125">Minimum supported client</span></span> | <span data-ttu-id="acae7-126">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="acae7-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="acae7-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acae7-127">Minimum supported server</span></span> | <span data-ttu-id="acae7-128">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="acae7-128">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="acae7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="acae7-129">Header</span></span>                   | <span data-ttu-id="acae7-130">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="acae7-130">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="acae7-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="acae7-131">Library</span></span>                  | <span data-ttu-id="acae7-132">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="acae7-132">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="acae7-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acae7-133">Related topics</span></span>

* [<span data-ttu-id="acae7-134">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="acae7-134">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
