---
title: Mensaje de WM_DWMNCRENDERINGCHANGED (Winuser. h)
description: Se envía cuando cambia la Directiva de representación del área que no es de cliente.
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- WM_DWMNCRENDERINGCHANGED Administrador de ventanas de escritorio de mensaje
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac32704ea240ccfc4d4de913b940e098ff8f4de4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996474"
---
# <a name="wm_dwmncrenderingchanged-message"></a><span data-ttu-id="36fec-104">Mensaje de DWMNCRENDERINGCHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="36fec-104">WM\_DWMNCRENDERINGCHANGED message</span></span>

<span data-ttu-id="36fec-105">Se envía cuando cambia la Directiva de representación del área que no es de cliente.</span><span class="sxs-lookup"><span data-stu-id="36fec-105">Sent when the non-client area rendering policy has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="36fec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36fec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36fec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36fec-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36fec-108">Especifica si la representación de DWM está habilitada para el área no cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="36fec-108">Specifies whether DWM rendering is enabled for the non-client area of the window.</span></span> <span data-ttu-id="36fec-109">**True** si está habilitado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="36fec-109">**TRUE** if enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="36fec-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36fec-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36fec-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="36fec-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36fec-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36fec-112">Return value</span></span>

<span data-ttu-id="36fec-113">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="36fec-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="36fec-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36fec-114">Remarks</span></span>

<span data-ttu-id="36fec-115">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="36fec-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="36fec-116">Las funciones [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) y [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) se usan para obtener o establecer la Directiva de representación que no es de cliente.</span><span class="sxs-lookup"><span data-stu-id="36fec-116">The [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions are used to get or set the non-client rendering policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="36fec-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36fec-117">Requirements</span></span>



| <span data-ttu-id="36fec-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="36fec-118">Requirement</span></span> | <span data-ttu-id="36fec-119">Value</span><span class="sxs-lookup"><span data-stu-id="36fec-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="36fec-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36fec-120">Minimum supported client</span></span><br/> | <span data-ttu-id="36fec-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="36fec-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="36fec-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36fec-122">Minimum supported server</span></span><br/> | <span data-ttu-id="36fec-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="36fec-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="36fec-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36fec-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="36fec-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="36fec-125"><dt>Winuser.h</dt></span></span> </dl> |



 

