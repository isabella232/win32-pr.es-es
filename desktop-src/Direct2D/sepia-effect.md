---
title: Efecto sepia
description: Convierte una imagen a tonos sepia.
ms.assetid: fe321be9-6ade-bd0c-1c66-cc8042e5a5e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6ead1d439e86cbd35be14d1f0ae32923de408d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996274"
---
# <a name="sepia-effect"></a><span data-ttu-id="71026-103">Efecto sepia</span><span class="sxs-lookup"><span data-stu-id="71026-103">Sepia effect</span></span>

<span data-ttu-id="71026-104">Convierte una imagen a tonos sepia.</span><span class="sxs-lookup"><span data-stu-id="71026-104">Converts an image to sepia tones.</span></span>

<span data-ttu-id="71026-105">El CLSID para este efecto es CLSID \_ D2D1Sepia.</span><span class="sxs-lookup"><span data-stu-id="71026-105">The CLSID for this effect is CLSID\_D2D1Sepia.</span></span>

-   [<span data-ttu-id="71026-106">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="71026-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="71026-107">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="71026-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="71026-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="71026-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="71026-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71026-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="71026-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71026-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="71026-111">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="71026-111">Example image</span></span>

![ejemplo de resultado de efecto](images/sepia-effect.png)

## <a name="sample-code"></a><span data-ttu-id="71026-113">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="71026-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sepiaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sepia, &sepiaEffect);
 
sepiaEffect->SetInput(0, bitmap);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_INTENSITY, 0.75f);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(sepiaEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="71026-114">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="71026-114">Effect properties</span></span>

<span data-ttu-id="71026-115">Las propiedades del efecto sepia se definen mediante la enumeración de [**D2D1 \_ sepia \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) .</span><span class="sxs-lookup"><span data-stu-id="71026-115">The properties for the sepia effect are defined by the [**D2D1\_SEPIA\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="71026-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71026-116">Requirements</span></span>



| <span data-ttu-id="71026-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="71026-117">Requirement</span></span> | <span data-ttu-id="71026-118">Value</span><span class="sxs-lookup"><span data-stu-id="71026-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="71026-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71026-119">Minimum supported client</span></span> | <span data-ttu-id="71026-120">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="71026-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="71026-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71026-121">Minimum supported server</span></span> | <span data-ttu-id="71026-122">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="71026-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="71026-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71026-123">Header</span></span>                   | <span data-ttu-id="71026-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="71026-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="71026-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71026-125">Library</span></span>                  | <span data-ttu-id="71026-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="71026-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="71026-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71026-127">Related topics</span></span>

* [<span data-ttu-id="71026-128">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="71026-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




