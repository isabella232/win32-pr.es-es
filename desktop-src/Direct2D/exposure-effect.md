---
title: Efecto de exposición
description: Aumentar o disminuir la exposición de la imagen.
ms.assetid: d384f539-5c19-53c7-e52b-bf833e221449
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6f5bda52fecc0b5e3896515b04a6560f17da49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996777"
---
# <a name="exposure-effect"></a><span data-ttu-id="5dbeb-103">Efecto de exposición</span><span class="sxs-lookup"><span data-stu-id="5dbeb-103">Exposure effect</span></span>

<span data-ttu-id="5dbeb-104">Aumentar o disminuir la exposición de la imagen.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-104">Increase or decreases the exposure of the image.</span></span>

<span data-ttu-id="5dbeb-105">El CLSID para este efecto es CLSID \_ D2D1Exposure.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-105">The CLSID for this effect is CLSID\_D2D1Exposure.</span></span>

-   [<span data-ttu-id="5dbeb-106">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="5dbeb-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="5dbeb-107">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="5dbeb-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="5dbeb-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="5dbeb-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="5dbeb-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dbeb-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5dbeb-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5dbeb-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="5dbeb-111">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="5dbeb-111">Example image</span></span>

![ejemplo de resultado de efecto](images/exposure-effect.png)

## <a name="sample-code"></a><span data-ttu-id="5dbeb-113">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="5dbeb-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> exposureEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Exposure, &exposureEffect);
 
exposureEffect->SetInput(0, bitmap);
exposureEffect->SetValue(D2D1_EXPOSURE_PROP_EXPOSURE_VALUE, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(exposureEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="5dbeb-114">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="5dbeb-114">Effect properties</span></span>

<span data-ttu-id="5dbeb-115">Las propiedades del efecto exposición se definen mediante la enumeración de [**\_ \_ exposición D2D1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) .</span><span class="sxs-lookup"><span data-stu-id="5dbeb-115">The properties for the exposure effect are defined by the [**D2D1\_EXPOSURE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dbeb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dbeb-116">Requirements</span></span>



| <span data-ttu-id="5dbeb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dbeb-117">Requirement</span></span> | <span data-ttu-id="5dbeb-118">Value</span><span class="sxs-lookup"><span data-stu-id="5dbeb-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="5dbeb-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dbeb-119">Minimum supported client</span></span> | <span data-ttu-id="5dbeb-120">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5dbeb-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dbeb-121">Minimum supported server</span></span> | <span data-ttu-id="5dbeb-122">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5dbeb-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5dbeb-123">Header</span></span>                   | <span data-ttu-id="5dbeb-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="5dbeb-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="5dbeb-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5dbeb-125">Library</span></span>                  | <span data-ttu-id="5dbeb-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="5dbeb-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="5dbeb-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5dbeb-127">Related topics</span></span>

* [<span data-ttu-id="5dbeb-128">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="5dbeb-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




