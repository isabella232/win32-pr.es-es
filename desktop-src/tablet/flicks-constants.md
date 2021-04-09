---
description: A continuación se muestran las constantes de gestos.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Constantes de gestos (Tabflicks. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154455"
---
# <a name="flicks-constants"></a><span data-ttu-id="b0726-103">Gestos constantes</span><span class="sxs-lookup"><span data-stu-id="b0726-103">Flicks Constants</span></span>

<span data-ttu-id="b0726-104">A continuación se muestran las constantes de gestos.</span><span class="sxs-lookup"><span data-stu-id="b0726-104">The following are the Flicks constants.</span></span>



| <span data-ttu-id="b0726-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="b0726-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="b0726-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0726-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <span data-ttu-id="b0726-107"><dt>**Gesto \_ de \_ \_ Máscara administrada de WM**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="b0726-107"><dt>**FLICK\_WM\_HANDLED\_MASK**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="b0726-108">Valor que se va a devolver después de controlar el mensaje de [**\_ mensaje de \_ gesto de Tablet PC de WM**](wm-tablet-flick-message.md) .</span><span class="sxs-lookup"><span data-stu-id="b0726-108">The value to return after handling the [**WM\_TABLET\_FLICK Message**](wm-tablet-flick-message.md) message.</span></span> <span data-ttu-id="b0726-109">Si se devuelve la **\_ \_ \_ máscara** superpuesto de WM, no se realiza ninguna otra acción.</span><span class="sxs-lookup"><span data-stu-id="b0726-109">If **FLICK\_WM\_HANDLED\_MASK** is returned, no further action occurs.</span></span> <span data-ttu-id="b0726-110">De lo contrario, Windows envía notificaciones de seguimiento, como [**WM \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)o [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown), dependiendo de la acción que esté asociada con el gesto de lápiz.</span><span class="sxs-lookup"><span data-stu-id="b0726-110">Otherwise, Windows sends follow-up notifications, such as [**WM\_APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll), or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown), depending on which action is associated with the pen flick.</span></span> <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <span data-ttu-id="b0726-111"><dt>**Número \_ de \_Direcciones de gesto**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b0726-111"><dt>**NUM\_FLICK\_DIRECTIONS**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="b0726-112">El número de direcciones definidas en la enumeración [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) .</span><span class="sxs-lookup"><span data-stu-id="b0726-112">The number of directions defined in the [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) enumeration.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="b0726-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0726-113">Requirements</span></span>



| <span data-ttu-id="b0726-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0726-114">Requirement</span></span> | <span data-ttu-id="b0726-115">Value</span><span class="sxs-lookup"><span data-stu-id="b0726-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0726-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0726-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b0726-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b0726-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b0726-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0726-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b0726-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0726-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b0726-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0726-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0726-121"><dt>Tabflicks. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0726-121"><dt>Tabflicks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0726-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0726-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0726-123">**Enumeración FLICKDIRECTION**</span><span class="sxs-lookup"><span data-stu-id="b0726-123">**FLICKDIRECTION Enumeration**</span></span>](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[<span data-ttu-id="b0726-124">**\_Mensaje de gesto de Tablet PC de WM \_**</span><span class="sxs-lookup"><span data-stu-id="b0726-124">**WM\_TABLET\_FLICK Message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="b0726-125">Gestos de gestos</span><span class="sxs-lookup"><span data-stu-id="b0726-125">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="b0726-126">[Responder a gestos de lápiz](/previous-versions//dd356077(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b0726-126">[Responding to Pen Flicks](/previous-versions//dd356077(v=vs.85))</span></span>
</dt> </dl>

 

