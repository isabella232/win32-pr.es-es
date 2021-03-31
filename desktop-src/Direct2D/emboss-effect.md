---
title: Efecto de relieve
description: Crea una versión de escala de grises de la imagen que aparece como si se hubiera estampado en papel.
ms.assetid: 74f63875-35cd-f335-62cd-410a953e53ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dde087eb7f85fcd68615c39730bf6208024fc43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802300"
---
# <a name="emboss-effect"></a><span data-ttu-id="e1405-103">Efecto de relieve</span><span class="sxs-lookup"><span data-stu-id="e1405-103">Emboss effect</span></span>

<span data-ttu-id="e1405-104">Crea una versión de escala de grises de la imagen que aparece como si se hubiera estampado en papel.</span><span class="sxs-lookup"><span data-stu-id="e1405-104">Creates a grayscale version of the image that appears as though it has been stamped into paper.</span></span>

<span data-ttu-id="e1405-105">El CLSID para este efecto es CLSID \_ D2D1Emboss.</span><span class="sxs-lookup"><span data-stu-id="e1405-105">The CLSID for this effect is CLSID\_D2D1Emboss.</span></span>

-   [<span data-ttu-id="e1405-106">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1405-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="e1405-107">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1405-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="e1405-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="e1405-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e1405-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1405-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e1405-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1405-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="e1405-111">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1405-111">Example image</span></span>

![ejemplo de resultado de efecto](images/emboss-effect.png)

## <a name="sample-code"></a><span data-ttu-id="e1405-113">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1405-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> embossEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Emboss, &embossEffect);
 
embossEffect->SetInput(0, bitmap);
embossEffect->SetValue(D2D1_EMBOSS_PROP_HEIGHT, 1.0f);
embossEffect->SetValue(D2D1_EMBOSS_PROP_DIRECTION, 0.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(embossEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="e1405-114">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="e1405-114">Effect properties</span></span>

<span data-ttu-id="e1405-115">Las propiedades del efecto de relieve se definen mediante la enumeración de [**D2D1 \_ relieve \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) .</span><span class="sxs-lookup"><span data-stu-id="e1405-115">The properties for the emboss effect are defined by the [**D2D1\_EMBOSS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1405-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1405-116">Requirements</span></span>



| <span data-ttu-id="e1405-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1405-117">Requirement</span></span> | <span data-ttu-id="e1405-118">Value</span><span class="sxs-lookup"><span data-stu-id="e1405-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="e1405-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1405-119">Minimum supported client</span></span> | <span data-ttu-id="e1405-120">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="e1405-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e1405-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1405-121">Minimum supported server</span></span> | <span data-ttu-id="e1405-122">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="e1405-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e1405-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1405-123">Header</span></span>                   | <span data-ttu-id="e1405-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="e1405-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="e1405-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1405-125">Library</span></span>                  | <span data-ttu-id="e1405-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e1405-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="e1405-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1405-127">Related topics</span></span>

* [<span data-ttu-id="e1405-128">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="e1405-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
