---
title: Efecto de temperatura y matiz
description: .
ms.assetid: 8df72105-26ea-2dea-a4de-ef06902b7e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8a483b926b26c115002b2bb352d8e3120e7479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905252"
---
# <a name="temperature-and-tint-effect"></a><span data-ttu-id="f4090-103">Efecto de temperatura y matiz</span><span class="sxs-lookup"><span data-stu-id="f4090-103">Temperature and tint effect</span></span>

<span data-ttu-id="f4090-104">El CLSID para este efecto es CLSID \_ D2D1TemperatureTint.</span><span class="sxs-lookup"><span data-stu-id="f4090-104">The CLSID for this effect is CLSID\_D2D1TemperatureTint.</span></span>

## <a name="sample-code"></a><span data-ttu-id="f4090-105">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4090-105">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> temperatureTintEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TemperatureTint, &temperatureTintEffect);
 
temperatureTintEffect->SetInput(0, bitmap);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, 0.5f);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TINT, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(temperatureTintEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="f4090-106">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="f4090-106">Effect properties</span></span>

<span data-ttu-id="f4090-107">Las propiedades del efecto temperatura y matiz se definen mediante la enumeración [**\_ \_ prop de D2D1 TEMPERATUREANDTINT**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) .</span><span class="sxs-lookup"><span data-stu-id="f4090-107">The properties for the temperature and tint effect are defined by the [**D2D1\_TEMPERATUREANDTINT\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4090-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4090-108">Requirements</span></span>



| <span data-ttu-id="f4090-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4090-109">Requirement</span></span> | <span data-ttu-id="f4090-110">Value</span><span class="sxs-lookup"><span data-stu-id="f4090-110">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="f4090-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4090-111">Minimum supported client</span></span> | <span data-ttu-id="f4090-112">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="f4090-112">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f4090-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4090-113">Minimum supported server</span></span> | <span data-ttu-id="f4090-114">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="f4090-114">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f4090-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4090-115">Header</span></span>                   | <span data-ttu-id="f4090-116">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="f4090-116">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="f4090-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4090-117">Library</span></span>                  | <span data-ttu-id="f4090-118">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="f4090-118">d2d1.lib, dxguid.lib</span></span>                              |



 

## <a name="related-topics"></a><span data-ttu-id="f4090-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4090-119">Related topics</span></span>

* [<span data-ttu-id="f4090-120">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="f4090-120">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
