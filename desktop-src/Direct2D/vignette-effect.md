---
title: Efecto de viñetas
description: Difumina la imagen de entrada en los bordes hasta un color establecido por el usuario.
ms.assetid: 34da221f-44a2-1d01-d88d-d7846b9770b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fe9302a86a49b060aa05ecb856ce43122d946d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150704"
---
# <a name="vignette-effect"></a><span data-ttu-id="36975-103">Efecto de viñetas</span><span class="sxs-lookup"><span data-stu-id="36975-103">Vignette effect</span></span>

<span data-ttu-id="36975-104">Difumina la imagen de entrada en los bordes hasta un color establecido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="36975-104">Fades the input image at the edges to a user-set color.</span></span>

<span data-ttu-id="36975-105">El CLSID para este efecto es CLSID \_ D2D1Vignette.</span><span class="sxs-lookup"><span data-stu-id="36975-105">The CLSID for this effect is CLSID\_D2D1Vignette.</span></span>

-   [<span data-ttu-id="36975-106">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="36975-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="36975-107">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="36975-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="36975-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="36975-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="36975-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36975-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="36975-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36975-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="36975-111">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="36975-111">Example image</span></span>

![ejemplo de resultado de efecto](images/vignette-effect.png)

## <a name="sample-code"></a><span data-ttu-id="36975-113">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="36975-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> vignetteEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Vignette, &vignetteEffect);
 
vignetteEffect->SetInput(0, bitmap);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_COLOR, );
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_TRANSITION_SIZE, 0.1f);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_STRENGTH, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(vignetteEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="36975-114">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="36975-114">Effect properties</span></span>

<span data-ttu-id="36975-115">Las propiedades para el efecto de viñetas se definen mediante la enumeración de propiedades [**D2D1 \_ Vignette \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) .</span><span class="sxs-lookup"><span data-stu-id="36975-115">The properties for the vignette effect are defined by the [**D2D1\_VIGNETTE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="36975-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36975-116">Requirements</span></span>

| <span data-ttu-id="36975-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="36975-117">Requirement</span></span> | <span data-ttu-id="36975-118">Value</span><span class="sxs-lookup"><span data-stu-id="36975-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="36975-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36975-119">Minimum supported client</span></span> | <span data-ttu-id="36975-120">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="36975-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="36975-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36975-121">Minimum supported server</span></span> | <span data-ttu-id="36975-122">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="36975-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="36975-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36975-123">Header</span></span>                   | <span data-ttu-id="36975-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="36975-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="36975-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36975-125">Library</span></span>                  | <span data-ttu-id="36975-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="36975-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="36975-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36975-127">Related topics</span></span>

* [<span data-ttu-id="36975-128">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="36975-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
