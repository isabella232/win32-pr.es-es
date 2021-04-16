---
title: BUTTONELEMENT. Down
description: El atributo Down especifica o recupera un valor que indica si el elemento de botón está en la posición arriba o abajo.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONELEMENT. Down Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699790"
---
# <a name="buttonelementdown"></a><span data-ttu-id="7c5c6-104">BUTTONELEMENT. Down</span><span class="sxs-lookup"><span data-stu-id="7c5c6-104">BUTTONELEMENT.down</span></span>

<span data-ttu-id="7c5c6-105">El atributo **Down** especifica o recupera un valor que indica si el elemento de botón está en la posición arriba o abajo.</span><span class="sxs-lookup"><span data-stu-id="7c5c6-105">The **down** attribute specifies or retrieves a value indicating whether the button element is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="7c5c6-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="7c5c6-106">Possible Values</span></span>

<span data-ttu-id="7c5c6-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="7c5c6-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="7c5c6-108">Value</span><span class="sxs-lookup"><span data-stu-id="7c5c6-108">Value</span></span> | <span data-ttu-id="7c5c6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c5c6-109">Description</span></span>                                                     |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="7c5c6-110">true</span><span class="sxs-lookup"><span data-stu-id="7c5c6-110">true</span></span>  | <span data-ttu-id="7c5c6-111">Indica que **BUTTONELEMENT** está en la posición hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="7c5c6-111">Indicates the **BUTTONELEMENT** is in the down position.</span></span>        |
| <span data-ttu-id="7c5c6-112">false</span><span class="sxs-lookup"><span data-stu-id="7c5c6-112">false</span></span> | <span data-ttu-id="7c5c6-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7c5c6-113">Default.</span></span> <span data-ttu-id="7c5c6-114">Indica que **BUTTONELEMENT** está en la posición de arriba.</span><span class="sxs-lookup"><span data-stu-id="7c5c6-114">Indicates the **BUTTONELEMENT** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7c5c6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c5c6-115">Remarks</span></span>

<span data-ttu-id="7c5c6-116">Para que un elemento de botón permanezca en la posición hacia abajo, la configuración **rápida** debe estar establecida en true.</span><span class="sxs-lookup"><span data-stu-id="7c5c6-116">For a button element to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="7c5c6-117">De forma predeterminada, la **permanencia** es falsa y se omitirá cualquier intento **de establecer en** true.</span><span class="sxs-lookup"><span data-stu-id="7c5c6-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="7c5c6-118">Si se especifica un valor no válido, se mantiene el estado anterior.</span><span class="sxs-lookup"><span data-stu-id="7c5c6-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c5c6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c5c6-119">Requirements</span></span>



| <span data-ttu-id="7c5c6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c5c6-120">Requirement</span></span> | <span data-ttu-id="7c5c6-121">Value</span><span class="sxs-lookup"><span data-stu-id="7c5c6-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7c5c6-122">Versión</span><span class="sxs-lookup"><span data-stu-id="7c5c6-122">Version</span></span><br/> | <span data-ttu-id="7c5c6-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7c5c6-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c5c6-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c5c6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c5c6-125">**BUTTONELEMENT (elemento)**</span><span class="sxs-lookup"><span data-stu-id="7c5c6-125">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="7c5c6-126">**BUTTONELEMENT. downToolTip**</span><span class="sxs-lookup"><span data-stu-id="7c5c6-126">**BUTTONELEMENT.downToolTip**</span></span>](buttonelement-downtooltip.md)
</dt> </dl>

 

 





