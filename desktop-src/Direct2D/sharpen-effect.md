---
title: Nitidez del efecto
description: Enfoca la imagen.
ms.assetid: 1eb12d1e-83c1-ba13-33be-df2078f3ccb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54203cfeb786204500c905e2ff4cfc83bf9719e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802035"
---
# <a name="sharpen-effect"></a><span data-ttu-id="81baf-103">Nitidez del efecto</span><span class="sxs-lookup"><span data-stu-id="81baf-103">Sharpen effect</span></span>

<span data-ttu-id="81baf-104">Enfoca la imagen.</span><span class="sxs-lookup"><span data-stu-id="81baf-104">Sharpens the image.</span></span>

<span data-ttu-id="81baf-105">El CLSID para este efecto es CLSID \_ D2D1Sharpen.</span><span class="sxs-lookup"><span data-stu-id="81baf-105">The CLSID for this effect is CLSID\_D2D1Sharpen.</span></span>

-   [<span data-ttu-id="81baf-106">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="81baf-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="81baf-107">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="81baf-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="81baf-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="81baf-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="81baf-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81baf-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="81baf-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81baf-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="81baf-111">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="81baf-111">Example image</span></span>

![ejemplo de resultado de efecto](images/sharpen-effect.png)

## <a name="sample-code"></a><span data-ttu-id="81baf-113">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="81baf-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sharpenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sharpen, &sharpenEffect);
 
sharpenEffect->SetInput(0, bitmap);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_SHARPNESS, 1.0f);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_THRESHOLD, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="81baf-114">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="81baf-114">Effect properties</span></span>

<span data-ttu-id="81baf-115">Las propiedades del efecto de enfoque se definen mediante la enumeración [**D2D1 \_ Sharp \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) .</span><span class="sxs-lookup"><span data-stu-id="81baf-115">The properties for the sharpen effect are defined by the [**D2D1\_SHARPEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="81baf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81baf-116">Requirements</span></span>



| <span data-ttu-id="81baf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81baf-117">Requirement</span></span> | <span data-ttu-id="81baf-118">Value</span><span class="sxs-lookup"><span data-stu-id="81baf-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="81baf-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81baf-119">Minimum supported client</span></span> | <span data-ttu-id="81baf-120">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="81baf-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="81baf-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81baf-121">Minimum supported server</span></span> | <span data-ttu-id="81baf-122">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="81baf-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="81baf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81baf-123">Header</span></span>                   | <span data-ttu-id="81baf-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="81baf-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="81baf-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81baf-125">Library</span></span>                  | <span data-ttu-id="81baf-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="81baf-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="81baf-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81baf-127">Related topics</span></span>

* [<span data-ttu-id="81baf-128">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="81baf-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)



