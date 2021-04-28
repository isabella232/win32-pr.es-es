---
title: Temperatura y efecto de tono
description: Temperatura y efecto de tono
ms.assetid: 8df72105-26ea-2dea-a4de-ef06902b7e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c3628e1fdcb1c72a84a9e08736e4215d55514
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096643"
---
# <a name="temperature-and-tint-effect"></a><span data-ttu-id="f866c-103">Temperatura y efecto de tono</span><span class="sxs-lookup"><span data-stu-id="f866c-103">Temperature and tint effect</span></span>

<span data-ttu-id="f866c-104">El CLSID para este efecto es CLSID \_ D2D1TemperatureTint.</span><span class="sxs-lookup"><span data-stu-id="f866c-104">The CLSID for this effect is CLSID\_D2D1TemperatureTint.</span></span>

## <a name="sample-code"></a><span data-ttu-id="f866c-105">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f866c-105">Sample code</span></span>

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

## <a name="effect-properties"></a><span data-ttu-id="f866c-106">Propiedades de efecto</span><span class="sxs-lookup"><span data-stu-id="f866c-106">Effect properties</span></span>

<span data-ttu-id="f866c-107">Las propiedades de la temperatura y el efecto de tono se definen mediante la [**enumeración \_ TEMPERATUREANDTINT \_ PROP de D2D1.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop)</span><span class="sxs-lookup"><span data-stu-id="f866c-107">The properties for the temperature and tint effect are defined by the [**D2D1\_TEMPERATUREANDTINT\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="f866c-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f866c-108">Requirements</span></span>



| <span data-ttu-id="f866c-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="f866c-109">Requirement</span></span> | <span data-ttu-id="f866c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f866c-110">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="f866c-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f866c-111">Minimum supported client</span></span> | <span data-ttu-id="f866c-112">Windows 10 aplicaciones \[ de escritorio aplicaciones \| de la Tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="f866c-112">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f866c-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f866c-113">Minimum supported server</span></span> | <span data-ttu-id="f866c-114">Windows 10 aplicaciones \[ de escritorio aplicaciones \| de la Tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="f866c-114">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f866c-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f866c-115">Header</span></span>                   | <span data-ttu-id="f866c-116">d2d1effects \_ 2.h</span><span class="sxs-lookup"><span data-stu-id="f866c-116">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="f866c-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f866c-117">Library</span></span>                  | <span data-ttu-id="f866c-118">d2d1.lib, dxguid.lib</span><span class="sxs-lookup"><span data-stu-id="f866c-118">d2d1.lib, dxguid.lib</span></span>                              |



 

## <a name="related-topics"></a><span data-ttu-id="f866c-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f866c-119">Related topics</span></span>

* [<span data-ttu-id="f866c-120">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="f866c-120">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
