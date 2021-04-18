---
title: Mensaje de BCM_SETSPLITINFO (commctrl. h)
description: Establece la información de un control de botón de expansión. Envíe este mensaje explícitamente o mediante la \_ macro Button SetSplitInfo.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- BCM_SETSPLITINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658213"
---
# <a name="bcm_setsplitinfo-message"></a><span data-ttu-id="8c95d-105">\_Mensaje SETSPLITINFO de BCM</span><span class="sxs-lookup"><span data-stu-id="8c95d-105">BCM\_SETSPLITINFO message</span></span>

<span data-ttu-id="8c95d-106">Establece la información de un control de botón de expansión.</span><span class="sxs-lookup"><span data-stu-id="8c95d-106">Sets information for a split button control.</span></span> <span data-ttu-id="8c95d-107">Envíe este mensaje explícitamente o mediante la macro [**Button \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) .</span><span class="sxs-lookup"><span data-stu-id="8c95d-107">Send this message explicitly or by using the [**Button\_SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c95d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c95d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c95d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c95d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c95d-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8c95d-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8c95d-111">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c95d-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c95d-112">Puntero a una estructura [**\_ SPLITINFO de botón**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) que contiene información sobre el botón de expansión.</span><span class="sxs-lookup"><span data-stu-id="8c95d-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure containing information about the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c95d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c95d-113">Return value</span></span>

<span data-ttu-id="8c95d-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8c95d-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c95d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c95d-115">Remarks</span></span>

<span data-ttu-id="8c95d-116">Use este mensaje solo con los estilos de botón [**BS \_ SPLITBUTTON**](button-styles.md) y [**BS \_ DEFSPLITBUTTON**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8c95d-116">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c95d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c95d-117">Requirements</span></span>



| <span data-ttu-id="8c95d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c95d-118">Requirement</span></span> | <span data-ttu-id="8c95d-119">Value</span><span class="sxs-lookup"><span data-stu-id="8c95d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c95d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c95d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c95d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8c95d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c95d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c95d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c95d-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c95d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c95d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c95d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c95d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c95d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c95d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c95d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c95d-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8c95d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8c95d-128">Estilos de botón</span><span class="sxs-lookup"><span data-stu-id="8c95d-128">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="8c95d-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="8c95d-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8c95d-130">Tipos de botón</span><span class="sxs-lookup"><span data-stu-id="8c95d-130">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





