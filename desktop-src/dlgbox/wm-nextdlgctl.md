---
title: Mensaje de WM_NEXTDLGCTL (Winuser. h)
description: Se envía a un procedimiento de cuadro de diálogo para establecer el foco de teclado en un control diferente en el cuadro de diálogo.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- WM_NEXTDLGCTL cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534731"
---
# <a name="wm_nextdlgctl-message"></a><span data-ttu-id="0f0ac-104">Mensaje de NEXTDLGCTL de WM \_</span><span class="sxs-lookup"><span data-stu-id="0f0ac-104">WM\_NEXTDLGCTL message</span></span>

<span data-ttu-id="0f0ac-105">Se envía a un procedimiento de cuadro de diálogo para establecer el foco de teclado en un control diferente en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0f0ac-105">Sent to a dialog box procedure to set the keyboard focus to a different control in the dialog box.</span></span>


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a><span data-ttu-id="0f0ac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f0ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f0ac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f0ac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f0ac-108">Si *lParam* es **true**, este parámetro identifica el control que recibe el foco.</span><span class="sxs-lookup"><span data-stu-id="0f0ac-108">If *lParam* is **TRUE**, this parameter identifies the control that receives the focus.</span></span> <span data-ttu-id="0f0ac-109">Si *lParam* es **false**, este parámetro indica si el control siguiente o anterior con el estilo **WS \_ TABSTOP** recibe el foco.</span><span class="sxs-lookup"><span data-stu-id="0f0ac-109">If *lParam* is **FALSE**, this parameter indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span> <span data-ttu-id="0f0ac-110">Si *wParam* es cero, el control siguiente recibe el foco; de lo contrario, el control anterior con el estilo **WS \_ TABSTOP** recibe el foco.</span><span class="sxs-lookup"><span data-stu-id="0f0ac-110">If *wParam* is zero, the next control receives the focus; otherwise, the previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> <dt>

<span data-ttu-id="0f0ac-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f0ac-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f0ac-112">La palabra de orden inferior indica el modo en que el sistema utiliza *wParam*.</span><span class="sxs-lookup"><span data-stu-id="0f0ac-112">The low-order word indicates how the system uses *wParam*.</span></span> <span data-ttu-id="0f0ac-113">Si la palabra de orden inferior es **true**, *wParam* es un identificador asociado al control que recibe el foco. de lo contrario, *wParam* es una marca que indica si el control siguiente o anterior con el estilo **WS \_ TABSTOP** recibe el foco.</span><span class="sxs-lookup"><span data-stu-id="0f0ac-113">If the low-order word is **TRUE**, *wParam* is a handle associated with the control that receives the focus; otherwise, *wParam* is a flag that indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f0ac-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f0ac-114">Return value</span></span>

<span data-ttu-id="0f0ac-115">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="0f0ac-115">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f0ac-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f0ac-116">Remarks</span></span>

<span data-ttu-id="0f0ac-117">Este mensaje realiza operaciones adicionales de administración de cuadros de diálogo más allá de las realizadas por la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) **\_ NEXTDLGCTL** actualiza el borde de pulsador predeterminado, establece el identificador de control predeterminado y selecciona automáticamente el texto de un control de edición (si la ventana de destino es un control de edición).</span><span class="sxs-lookup"><span data-stu-id="0f0ac-117">This message performs additional dialog box management operations beyond those performed by the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function **WM\_NEXTDLGCTL** updates the default pushbutton border, sets the default control identifier, and automatically selects the text of an edit control (if the target window is an edit control).</span></span>

<span data-ttu-id="0f0ac-118">No use la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para enviar un mensaje **de \_ NEXTDLGCTL de WM** si la aplicación va a procesar simultáneamente otros mensajes que establecieron el foco.</span><span class="sxs-lookup"><span data-stu-id="0f0ac-118">Do not use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to send a **WM\_NEXTDLGCTL** message if your application will concurrently process other messages that set the focus.</span></span> <span data-ttu-id="0f0ac-119">En su lugar, use la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .</span><span class="sxs-lookup"><span data-stu-id="0f0ac-119">Use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f0ac-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f0ac-120">Requirements</span></span>



| <span data-ttu-id="0f0ac-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f0ac-121">Requirement</span></span> | <span data-ttu-id="0f0ac-122">Value</span><span class="sxs-lookup"><span data-stu-id="0f0ac-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f0ac-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f0ac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0f0ac-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0f0ac-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0f0ac-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f0ac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0f0ac-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0f0ac-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0f0ac-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f0ac-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f0ac-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f0ac-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f0ac-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f0ac-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f0ac-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0f0ac-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0f0ac-131">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="0f0ac-131">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="0f0ac-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="0f0ac-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="0f0ac-133">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="0f0ac-133">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="0f0ac-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0f0ac-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0f0ac-135">Cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="0f0ac-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

