---
title: SLIDEr. onPositionChange
description: El controlador de eventos onPositionChange controla un evento que se produce cuando cambia la posición del control deslizante a medida que el usuario hace clic o arrastra. | SLIDEr. onPositionChange
ms.assetid: c18e9a49-9576-42ae-9f30-249c44d40f41
keywords:
- CONTROL SLIDEr. onPositionChange Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68faa9e7addd85b9b5f02b8a6c445e7ddf54e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699971"
---
# <a name="slideronpositionchange"></a><span data-ttu-id="ddb6f-105">SLIDEr. onPositionChange</span><span class="sxs-lookup"><span data-stu-id="ddb6f-105">SLIDER.onPositionChange</span></span>

<span data-ttu-id="ddb6f-106">El controlador de eventos **onPositionChange** controla un evento que se produce cuando cambia la posición del control deslizante a medida que el usuario hace clic o arrastra.</span><span class="sxs-lookup"><span data-stu-id="ddb6f-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="ddb6f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddb6f-107">Remarks</span></span>

<span data-ttu-id="ddb6f-108">Si cambia la posición del control deslizante como resultado del atributo de **valor** que se está modificando en el script, este evento no se desencadena.</span><span class="sxs-lookup"><span data-stu-id="ddb6f-108">If the position of the slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="ddb6f-109">Para dar cabida a esta posibilidad, implemente en su lugar el controlador de eventos **\_ onchange Value** .</span><span class="sxs-lookup"><span data-stu-id="ddb6f-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb6f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddb6f-110">Requirements</span></span>



| <span data-ttu-id="ddb6f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddb6f-111">Requirement</span></span> | <span data-ttu-id="ddb6f-112">Value</span><span class="sxs-lookup"><span data-stu-id="ddb6f-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ddb6f-113">Versión</span><span class="sxs-lookup"><span data-stu-id="ddb6f-113">Version</span></span><br/> | <span data-ttu-id="ddb6f-114">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ddb6f-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ddb6f-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddb6f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb6f-116">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="ddb6f-116">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





