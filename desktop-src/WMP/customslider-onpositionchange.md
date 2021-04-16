---
title: CUSTOMSLIDER.onPositionChange
description: El controlador de eventos onPositionChange controla un evento que se produce cuando cambia la posición del control deslizante a medida que el usuario hace clic o arrastra. | CUSTOMSLIDER.onPositionChange
ms.assetid: d8fe99a2-69ff-4e75-8d7d-506bcb2f75bf
keywords:
- CUSTOMSLIDER. onPositionChange Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3d5547d66ca6dc1b770242301bd95ed010a8d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699731"
---
# <a name="customslideronpositionchange"></a><span data-ttu-id="4b1fb-105">CUSTOMSLIDER.onPositionChange</span><span class="sxs-lookup"><span data-stu-id="4b1fb-105">CUSTOMSLIDER.onPositionChange</span></span>

<span data-ttu-id="4b1fb-106">El controlador de eventos **onPositionChange** controla un evento que se produce cuando cambia la posición del control deslizante a medida que el usuario hace clic o arrastra.</span><span class="sxs-lookup"><span data-stu-id="4b1fb-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="4b1fb-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b1fb-107">Remarks</span></span>

<span data-ttu-id="4b1fb-108">Si cambia la posición del control deslizante personalizado como resultado del atributo de **valor** que se está modificando en el script, este evento no se desencadena.</span><span class="sxs-lookup"><span data-stu-id="4b1fb-108">If the position of the custom slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="4b1fb-109">Para dar cabida a esta posibilidad, implemente en su lugar el controlador de eventos **\_ onchange Value** .</span><span class="sxs-lookup"><span data-stu-id="4b1fb-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b1fb-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b1fb-110">Requirements</span></span>



| <span data-ttu-id="4b1fb-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b1fb-111">Requirement</span></span> | <span data-ttu-id="4b1fb-112">Value</span><span class="sxs-lookup"><span data-stu-id="4b1fb-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4b1fb-113">Versión</span><span class="sxs-lookup"><span data-stu-id="4b1fb-113">Version</span></span><br/> | <span data-ttu-id="4b1fb-114">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4b1fb-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b1fb-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b1fb-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b1fb-116">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="4b1fb-116">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





