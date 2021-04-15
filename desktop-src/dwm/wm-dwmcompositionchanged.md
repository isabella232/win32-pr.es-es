---
title: Mensaje de WM_DWMCOMPOSITIONCHANGED (Winuser. h)
description: Informa a todas las ventanas de nivel superior en las que se ha habilitado o deshabilitado la composición de Administrador de ventanas de escritorio (DWM).
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- WM_DWMCOMPOSITIONCHANGED Administrador de ventanas de escritorio de mensaje
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695944"
---
# <a name="wm_dwmcompositionchanged-message"></a><span data-ttu-id="ecc74-104">Mensaje de DWMCOMPOSITIONCHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="ecc74-104">WM\_DWMCOMPOSITIONCHANGED message</span></span>

<span data-ttu-id="ecc74-105">Informa a todas las ventanas de nivel superior en las que se ha habilitado o deshabilitado la composición de Administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="ecc74-105">Informs all top-level windows that Desktop Window Manager (DWM) composition has been enabled or disabled.</span></span>

> [!Note]  
> <span data-ttu-id="ecc74-106">A partir de Windows 8, la composición DWM siempre está habilitada, por lo que este mensaje no se envía independientemente de los cambios en el modo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ecc74-106">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="ecc74-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ecc74-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecc74-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecc74-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecc74-109">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ecc74-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ecc74-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecc74-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecc74-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ecc74-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecc74-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecc74-112">Return value</span></span>

<span data-ttu-id="ecc74-113">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="ecc74-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecc74-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecc74-114">Remarks</span></span>

<span data-ttu-id="ecc74-115">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ecc74-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="ecc74-116">La función [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) se puede utilizar para determinar el estado de composición actual.</span><span class="sxs-lookup"><span data-stu-id="ecc74-116">The [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) function can be used to determine the current composition state.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc74-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecc74-117">Requirements</span></span>



| <span data-ttu-id="ecc74-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecc74-118">Requirement</span></span> | <span data-ttu-id="ecc74-119">Value</span><span class="sxs-lookup"><span data-stu-id="ecc74-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc74-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecc74-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ecc74-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ecc74-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ecc74-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecc74-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ecc74-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecc74-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ecc74-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecc74-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecc74-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecc74-125"><dt>Winuser.h</dt></span></span> </dl> |



 

