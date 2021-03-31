---
title: Mensaje de MCM_SETCALENDARBORDER (commctrl. h)
description: Establece el tamaño del borde, en píxeles. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetCalendarBorder.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- MCM_SETCALENDARBORDER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490517"
---
# <a name="mcm_setcalendarborder-message"></a><span data-ttu-id="b15ba-105">Mensaje de MCM \_ SETCALENDARBORDER</span><span class="sxs-lookup"><span data-stu-id="b15ba-105">MCM\_SETCALENDARBORDER message</span></span>

<span data-ttu-id="b15ba-106">Establece el tamaño del borde, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b15ba-106">Sets the size of the border, in pixels.</span></span> <span data-ttu-id="b15ba-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) .</span><span class="sxs-lookup"><span data-stu-id="b15ba-107">You can send this message explicitly or by using the [**MonthCal\_SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b15ba-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b15ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b15ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b15ba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b15ba-110">Si es **true**, el tamaño del borde se establece en el número de píxeles que *lParam* especifica.</span><span class="sxs-lookup"><span data-stu-id="b15ba-110">If **TRUE**, then the border size is set to the number of pixels that *lParam* specifies.</span></span> <span data-ttu-id="b15ba-111">Si es **false**, el tamaño del borde se restablece en el valor predeterminado especificado por el tema, o bien, cero si no se usan los temas.</span><span class="sxs-lookup"><span data-stu-id="b15ba-111">If **FALSE**, then the border size is reset to the default value specified by the theme, or zero if themes are not being used.</span></span>

</dd> <dt>

<span data-ttu-id="b15ba-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b15ba-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b15ba-113">Número de píxeles del tamaño del borde.</span><span class="sxs-lookup"><span data-stu-id="b15ba-113">Number of pixels of the border size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b15ba-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b15ba-114">Return value</span></span>

<span data-ttu-id="b15ba-115">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b15ba-115">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b15ba-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b15ba-116">Requirements</span></span>



| <span data-ttu-id="b15ba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b15ba-117">Requirement</span></span> | <span data-ttu-id="b15ba-118">Value</span><span class="sxs-lookup"><span data-stu-id="b15ba-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b15ba-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b15ba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b15ba-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b15ba-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b15ba-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b15ba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b15ba-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b15ba-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b15ba-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b15ba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b15ba-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b15ba-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





