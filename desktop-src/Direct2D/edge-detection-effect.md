---
title: Efecto de detección perimetral
description: Filtra el contenido de una imagen, manteniendo las líneas en los bordes de las secciones de contraste de la imagen.
ms.assetid: d22868cf-95fe-690e-66ac-268d7e116aee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47239bede77dc5d32582c6e83c8101e5c9bbf2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079773"
---
# <a name="edge-detection-effect"></a><span data-ttu-id="97176-103">Efecto de detección perimetral</span><span class="sxs-lookup"><span data-stu-id="97176-103">Edge-detection effect</span></span>

<span data-ttu-id="97176-104">Filtra el contenido de una imagen, manteniendo las líneas en los bordes de las secciones de contraste de la imagen.</span><span class="sxs-lookup"><span data-stu-id="97176-104">Filters out the content of an image, leaving lines at the edges of contrasting sections of the image.</span></span>

<span data-ttu-id="97176-105">El CLSID para este efecto es CLSID \_ D2D1EdgeDetection.</span><span class="sxs-lookup"><span data-stu-id="97176-105">The CLSID for this effect is CLSID\_D2D1EdgeDetection.</span></span>

-   [<span data-ttu-id="97176-106">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="97176-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="97176-107">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="97176-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="97176-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="97176-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="97176-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97176-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="97176-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97176-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="97176-111">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="97176-111">Example image</span></span>

![ejemplo de resultado de efecto](images/edge-detection-effect.png)

## <a name="sample-code"></a><span data-ttu-id="97176-113">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="97176-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> edgeDetectionEffect;
m_d2dContext->CreateEffect(CLSID_D2D1EdgeDetection, &edgeDetectionEffect);
 
edgeDetectionEffect->SetInput(0, bitmap);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_STRENGTH, 0.5f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, 0.0f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_MODE_SOBEL);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, false);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(edgeDetectionEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="97176-114">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="97176-114">Effect properties</span></span>

<span data-ttu-id="97176-115">Las propiedades del efecto de detección perimetral se definen mediante la enumeración [**\_ \_ prop de D2D1 EDGEDETECTION**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) .</span><span class="sxs-lookup"><span data-stu-id="97176-115">The properties for the edge detection effect are defined by the [**D2D1\_EDGEDETECTION\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="97176-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97176-116">Requirements</span></span>



| <span data-ttu-id="97176-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="97176-117">Requirement</span></span> | <span data-ttu-id="97176-118">Value</span><span class="sxs-lookup"><span data-stu-id="97176-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="97176-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97176-119">Minimum supported client</span></span> | <span data-ttu-id="97176-120">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="97176-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="97176-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97176-121">Minimum supported server</span></span> | <span data-ttu-id="97176-122">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="97176-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="97176-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97176-123">Header</span></span>                   | <span data-ttu-id="97176-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="97176-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="97176-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97176-125">Library</span></span>                  | <span data-ttu-id="97176-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="97176-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="97176-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97176-127">Related topics</span></span>

* [<span data-ttu-id="97176-128">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="97176-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
