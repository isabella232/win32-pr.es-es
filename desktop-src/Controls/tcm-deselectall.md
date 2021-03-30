---
title: Mensaje de TCM_DESELECTALL (commctrl. h)
description: Restablece los elementos de un control de ficha, desactivando cualquier que se haya establecido en el \_ Estado TCIS BUTTONPRESSED. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ DeselectAll.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- TCM_DESELECTALL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150975"
---
# <a name="tcm_deselectall-message"></a><span data-ttu-id="c9569-105">\_Mensaje DESELECTALL de TCM</span><span class="sxs-lookup"><span data-stu-id="c9569-105">TCM\_DESELECTALL message</span></span>

<span data-ttu-id="c9569-106">Restablece los elementos de un control de ficha, desactivando cualquier que se haya establecido en el estado [**TCIS \_ BUTTONPRESSED**](tab-control-item-states.md) .</span><span class="sxs-lookup"><span data-stu-id="c9569-106">Resets items in a tab control, clearing any that were set to the [**TCIS\_BUTTONPRESSED**](tab-control-item-states.md) state.</span></span> <span data-ttu-id="c9569-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) .</span><span class="sxs-lookup"><span data-stu-id="c9569-107">You can send this message explicitly or by using the [**TabCtrl\_DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9569-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9569-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9569-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9569-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9569-110">Marca que especifica el ámbito de la anulación de la selección del elemento.</span><span class="sxs-lookup"><span data-stu-id="c9569-110">Flag that specifies the scope of the item deselection.</span></span> <span data-ttu-id="c9569-111">Si este parámetro se establece en **false**, se restablecerán todos los elementos de ficha.</span><span class="sxs-lookup"><span data-stu-id="c9569-111">If this parameter is set to **FALSE**, all tab items will be reset.</span></span> <span data-ttu-id="c9569-112">Si se establece en **true**, se restablecerán todos los elementos de ficha excepto el seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="c9569-112">If it is set to **TRUE**, then all tab items except for the one currently selected will be reset.</span></span>

</dd> <dt>

<span data-ttu-id="c9569-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9569-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c9569-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c9569-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9569-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9569-115">Return value</span></span>

<span data-ttu-id="c9569-116">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="c9569-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9569-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9569-117">Remarks</span></span>

<span data-ttu-id="c9569-118">Este mensaje solo es significativo si se ha establecido la marca de estilo [**\_ botones de TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c9569-118">This message is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9569-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9569-119">Requirements</span></span>



| <span data-ttu-id="c9569-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9569-120">Requirement</span></span> | <span data-ttu-id="c9569-121">Value</span><span class="sxs-lookup"><span data-stu-id="c9569-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9569-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9569-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c9569-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c9569-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9569-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9569-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c9569-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9569-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9569-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9569-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9569-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9569-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





