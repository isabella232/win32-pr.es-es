---
title: Mensaje de TTM_TRACKPOSITION (commctrl. h)
description: Establece la posición de una información sobre herramientas de seguimiento.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- TTM_TRACKPOSITION controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079523"
---
# <a name="ttm_trackposition-message"></a><span data-ttu-id="0f6ba-104">TTM \_ TRACKPOSITION</span><span class="sxs-lookup"><span data-stu-id="0f6ba-104">TTM\_TRACKPOSITION message</span></span>

<span data-ttu-id="0f6ba-105">Establece la posición de una información sobre herramientas de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-105">Sets the position of a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f6ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f6ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f6ba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f6ba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f6ba-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f6ba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f6ba-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la coordenada x del punto en el que se mostrará la información sobre herramientas de seguimiento, en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span> <span data-ttu-id="0f6ba-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la coordenada y del punto en el que se mostrará la información sobre herramientas de seguimiento, en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f6ba-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f6ba-112">Return value</span></span>

<span data-ttu-id="0f6ba-113">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f6ba-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f6ba-114">Remarks</span></span>

<span data-ttu-id="0f6ba-115">El control ToolTip elige dónde Mostrar la ventana de información sobre herramientas en función de las coordenadas proporcionadas con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-115">The tooltip control chooses where to display the tooltip window based on the coordinates you provide with this message.</span></span> <span data-ttu-id="0f6ba-116">Esto hace que la ventana de información sobre herramientas aparezca junto a la herramienta a la que corresponde.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-116">This causes the tooltip window to appear beside the tool to which it corresponds.</span></span> <span data-ttu-id="0f6ba-117">Para que las ventanas de información sobre herramientas se muestren en coordenadas específicas, incluya la \_ marca absoluta ttf en el miembro **uFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) al agregar la herramienta.</span><span class="sxs-lookup"><span data-stu-id="0f6ba-117">To have tooltip windows displayed at specific coordinates, include the TTF\_ABSOLUTE flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when adding the tool.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f6ba-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f6ba-118">Requirements</span></span>



| <span data-ttu-id="0f6ba-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f6ba-119">Requirement</span></span> | <span data-ttu-id="0f6ba-120">Value</span><span class="sxs-lookup"><span data-stu-id="0f6ba-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6ba-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f6ba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f6ba-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0f6ba-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f6ba-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f6ba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f6ba-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f6ba-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f6ba-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f6ba-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f6ba-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f6ba-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f6ba-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f6ba-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f6ba-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0f6ba-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0f6ba-129">**TTM \_ TRACKACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="0f6ba-129">**TTM\_TRACKACTIVATE**</span></span>](ttm-trackactivate.md)
</dt> <dt>

<span data-ttu-id="0f6ba-130">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0f6ba-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0f6ba-131">Usar controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="0f6ba-131">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

