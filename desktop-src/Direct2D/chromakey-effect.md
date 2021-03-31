---
title: Efecto de clave de croma
description: Convierte un color dado más o menos una tolerancia en alfa. Por ejemplo, croma-key puede quitar el fondo de una imagen para un efecto de superposición de pantalla verde.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a13d5558d103d6f937ed6638d0debbeddaf71dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905162"
---
# <a name="chroma-key-effect"></a><span data-ttu-id="4c3f8-104">Efecto de clave de croma</span><span class="sxs-lookup"><span data-stu-id="4c3f8-104">Chroma-key effect</span></span>

<span data-ttu-id="4c3f8-105">Convierte un color dado más o menos una tolerancia en alfa.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-105">Converts a given color plus or minus a tolerance to alpha.</span></span> <span data-ttu-id="4c3f8-106">Por ejemplo, croma-key puede quitar el fondo de una imagen para un efecto de superposición de pantalla verde.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-106">For example, chroma-key can remove the background of an image for a green-screen overlay effect.</span></span>

<span data-ttu-id="4c3f8-107">El CLSID para este efecto es CLSID \_ D2D1ChromaKey.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-107">The CLSID for this effect is CLSID\_D2D1ChromaKey.</span></span>

-   [<span data-ttu-id="4c3f8-108">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c3f8-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="4c3f8-109">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c3f8-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="4c3f8-110">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="4c3f8-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="4c3f8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c3f8-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4c3f8-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c3f8-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="4c3f8-113">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c3f8-113">Example image</span></span>

![ejemplo de resultado de efecto](images/chromakey-effect.png)

> [!Note]  
> <span data-ttu-id="4c3f8-115">En este ejemplo, la salida del efecto de clave de croma es la segunda imagen con el fondo transparente de tablero de ajedrez.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-115">In this example, the output of the chroma-key effect is the second image with the checkerboard transparent background.</span></span> <span data-ttu-id="4c3f8-116">La tercera imagen lo combina con una imagen de fondo para la superposición de la pantalla verde final.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-116">The third image combines this with a background image for the final green-screen overlay.</span></span>

## <a name="sample-code"></a><span data-ttu-id="4c3f8-117">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c3f8-117">Sample code</span></span>

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="4c3f8-118">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="4c3f8-118">Effect properties</span></span>

<span data-ttu-id="4c3f8-119">Las propiedades del efecto de clave de croma se definen mediante la enumeración [**\_ \_ prop de D2D1 Chromakey**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) .</span><span class="sxs-lookup"><span data-stu-id="4c3f8-119">The properties for the chroma-key effect are defined by the [**D2D1\_CHROMAKEY\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c3f8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c3f8-120">Requirements</span></span>

| <span data-ttu-id="4c3f8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c3f8-121">Requirement</span></span> | <span data-ttu-id="4c3f8-122">Value</span><span class="sxs-lookup"><span data-stu-id="4c3f8-122">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="4c3f8-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c3f8-123">Minimum supported client</span></span> | <span data-ttu-id="4c3f8-124">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="4c3f8-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4c3f8-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c3f8-125">Minimum supported server</span></span> | <span data-ttu-id="4c3f8-126">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="4c3f8-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4c3f8-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c3f8-127">Header</span></span>                   | <span data-ttu-id="4c3f8-128">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="4c3f8-128">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="4c3f8-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c3f8-129">Library</span></span>                  | <span data-ttu-id="4c3f8-130">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="4c3f8-130">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="4c3f8-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c3f8-131">Related topics</span></span>

* [<span data-ttu-id="4c3f8-132">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="4c3f8-132">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
