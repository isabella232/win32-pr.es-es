---
title: Mensaje de PGM_FORWARDMOUSE (commctrl. h)
description: Habilita o deshabilita el reenvío del mouse para el control de paginación. Cuando está habilitado el reenvío del mouse, el control de paginación reenvía \_ los mensajes de WM MOUSEMOVE a la ventana contenida. Puede enviar este mensaje explícitamente o utilizar la macro ForwardMouse de buscapersonas \_ .
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- PGM_FORWARDMOUSE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658261"
---
# <a name="pgm_forwardmouse-message"></a><span data-ttu-id="da1b5-106">\_Mensaje FORWARDMOUSE PGM</span><span class="sxs-lookup"><span data-stu-id="da1b5-106">PGM\_FORWARDMOUSE message</span></span>

<span data-ttu-id="da1b5-107">Habilita o deshabilita el reenvío del mouse para el control de paginación.</span><span class="sxs-lookup"><span data-stu-id="da1b5-107">Enables or disables mouse forwarding for the pager control.</span></span> <span data-ttu-id="da1b5-108">Cuando está habilitado el reenvío del mouse, el control de paginación reenvía los mensajes de [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) a la ventana contenida.</span><span class="sxs-lookup"><span data-stu-id="da1b5-108">When mouse forwarding is enabled, the pager control forwards [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to the contained window.</span></span> <span data-ttu-id="da1b5-109">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ ForwardMouse de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) .</span><span class="sxs-lookup"><span data-stu-id="da1b5-109">You can send this message explicitly or use the [**Pager\_ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="da1b5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da1b5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da1b5-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da1b5-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da1b5-112">Valor **booleano** que determina si está habilitado o deshabilitado el reenvío del mouse.</span><span class="sxs-lookup"><span data-stu-id="da1b5-112">**BOOL** value that determines if mouse forwarding is enabled or disabled.</span></span> <span data-ttu-id="da1b5-113">Si este valor es distinto de cero, se habilita el reenvío del mouse.</span><span class="sxs-lookup"><span data-stu-id="da1b5-113">If this value is nonzero, mouse forwarding is enabled.</span></span> <span data-ttu-id="da1b5-114">Si este valor es cero, el reenvío del mouse está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="da1b5-114">If this value is zero, mouse forwarding is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="da1b5-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da1b5-115">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="da1b5-116">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="da1b5-116">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da1b5-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da1b5-117">Return value</span></span>

<span data-ttu-id="da1b5-118">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="da1b5-118">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="da1b5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da1b5-119">Requirements</span></span>



| <span data-ttu-id="da1b5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="da1b5-120">Requirement</span></span> | <span data-ttu-id="da1b5-121">Value</span><span class="sxs-lookup"><span data-stu-id="da1b5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da1b5-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da1b5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="da1b5-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="da1b5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da1b5-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da1b5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="da1b5-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="da1b5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da1b5-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da1b5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="da1b5-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="da1b5-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

