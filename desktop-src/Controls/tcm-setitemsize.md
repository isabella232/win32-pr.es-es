---
title: Mensaje de TCM_SETITEMSIZE (commctrl. h)
description: Establece el ancho y el alto de las pestañas en un control de ficha de ancho fijo o dibujado por el propietario. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetItemSize.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- TCM_SETITEMSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904982"
---
# <a name="tcm_setitemsize-message"></a><span data-ttu-id="b3cbd-105">\_Mensaje SETITEMSIZE de TCM</span><span class="sxs-lookup"><span data-stu-id="b3cbd-105">TCM\_SETITEMSIZE message</span></span>

<span data-ttu-id="b3cbd-106">Establece el ancho y el alto de las pestañas en un control de ficha de ancho fijo o dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="b3cbd-106">Sets the width and height of tabs in a fixed-width or owner-drawn tab control.</span></span> <span data-ttu-id="b3cbd-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) .</span><span class="sxs-lookup"><span data-stu-id="b3cbd-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3cbd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3cbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3cbd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3cbd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b3cbd-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b3cbd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b3cbd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3cbd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3cbd-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor **int** que especifica el nuevo ancho, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b3cbd-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the new width, in pixels.</span></span> <span data-ttu-id="b3cbd-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es un valor **int** que especifica el nuevo alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b3cbd-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the new height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3cbd-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3cbd-114">Return value</span></span>

<span data-ttu-id="b3cbd-115">Devuelve el ancho y el alto antiguos.</span><span class="sxs-lookup"><span data-stu-id="b3cbd-115">Returns the old width and height.</span></span> <span data-ttu-id="b3cbd-116">El ancho está en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del valor devuelto y el alto está en [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b3cbd-116">The width is in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the height is in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3cbd-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3cbd-117">Remarks</span></span>

<span data-ttu-id="b3cbd-118">Si el ancho se establece en un valor menor que el ancho de imagen establecido por [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), el ancho de la pestaña se establece en el valor más bajo que sea mayor que el ancho de la imagen.</span><span class="sxs-lookup"><span data-stu-id="b3cbd-118">If the width is set to a value less than the image width set by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), the width of the tab is set to the lowest value that is greater than the image width.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3cbd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3cbd-119">Requirements</span></span>



| <span data-ttu-id="b3cbd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3cbd-120">Requirement</span></span> | <span data-ttu-id="b3cbd-121">Value</span><span class="sxs-lookup"><span data-stu-id="b3cbd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3cbd-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3cbd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b3cbd-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b3cbd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3cbd-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3cbd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b3cbd-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3cbd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3cbd-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3cbd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3cbd-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3cbd-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

