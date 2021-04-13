---
title: Mensaje de WM_DWMWINDOWMAXIMIZEDCHANGE (Winuser. h)
description: Se envía cuando se maximiza una ventana compuesta de Administrador de ventanas de escritorio (DWM).
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- WM_DWMWINDOWMAXIMIZEDCHANGE Administrador de ventanas de escritorio de mensaje
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422350"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a><span data-ttu-id="ce6c6-104">Mensaje de DWMWINDOWMAXIMIZEDCHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="ce6c6-104">WM\_DWMWINDOWMAXIMIZEDCHANGE message</span></span>

<span data-ttu-id="ce6c6-105">Se envía cuando se maximiza una ventana compuesta de Administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="ce6c6-105">Sent when a Desktop Window Manager (DWM) composed window is maximized.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce6c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce6c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce6c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce6c6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce6c6-108">Establézcalo en true para especificar que la ventana se ha maximizado.</span><span class="sxs-lookup"><span data-stu-id="ce6c6-108">Set to true to specify that the window has been maximized.</span></span>

</dd> <dt>

<span data-ttu-id="ce6c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce6c6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce6c6-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ce6c6-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce6c6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce6c6-111">Return value</span></span>

<span data-ttu-id="ce6c6-112">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="ce6c6-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce6c6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce6c6-113">Remarks</span></span>

<span data-ttu-id="ce6c6-114">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ce6c6-114">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6c6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce6c6-115">Requirements</span></span>



| <span data-ttu-id="ce6c6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce6c6-116">Requirement</span></span> | <span data-ttu-id="ce6c6-117">Value</span><span class="sxs-lookup"><span data-stu-id="ce6c6-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6c6-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce6c6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6c6-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ce6c6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ce6c6-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce6c6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6c6-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce6c6-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ce6c6-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce6c6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce6c6-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce6c6-123"><dt>Winuser.h</dt></span></span> </dl> |



 

