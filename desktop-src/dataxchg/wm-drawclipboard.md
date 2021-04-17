---
title: Mensaje de WM_DRAWCLIPBOARD (Winuser. h)
description: Se envía a la primera ventana de la cadena del visor del portapapeles cuando cambia el contenido del portapapeles. Esto permite que una ventana del visor del portapapeles muestre el nuevo contenido del portapapeles. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- Intercambio de datos de mensajes de WM_DRAWCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665993"
---
# <a name="wm_drawclipboard-message"></a><span data-ttu-id="91714-106">Mensaje de DRAWCLIPBOARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="91714-106">WM\_DRAWCLIPBOARD message</span></span>

<span data-ttu-id="91714-107">Se envía a la primera ventana de la cadena del visor del portapapeles cuando cambia el contenido del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="91714-107">Sent to the first window in the clipboard viewer chain when the content of the clipboard changes.</span></span> <span data-ttu-id="91714-108">Esto permite que una ventana del visor del portapapeles muestre el nuevo contenido del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="91714-108">This enables a clipboard viewer window to display the new content of the clipboard.</span></span>

<span data-ttu-id="91714-109">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="91714-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a><span data-ttu-id="91714-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91714-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91714-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91714-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91714-112">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="91714-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="91714-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91714-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91714-114">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="91714-114">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91714-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91714-115">Remarks</span></span>

<span data-ttu-id="91714-116">Solo las ventanas del visor del portapapeles reciben este mensaje.</span><span class="sxs-lookup"><span data-stu-id="91714-116">Only clipboard viewer windows receive this message.</span></span> <span data-ttu-id="91714-117">Se trata de ventanas que se han agregado a la cadena del visor del portapapeles mediante la función [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="91714-117">These are windows that have been added to the clipboard viewer chain by using the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="91714-118">Cada ventana que recibe el mensaje de **\_ DRAWCLIPBOARD de WM** debe llamar a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para pasar el mensaje a la siguiente ventana de la cadena del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="91714-118">Each window that receives the **WM\_DRAWCLIPBOARD** message must call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message on to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="91714-119">[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)devuelve el identificador de la siguiente ventana de la cadena y puede cambiar en respuesta a un mensaje de [**\_ CHANGECBCHAIN de WM**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="91714-119">The handle to the next window in the chain is returned by [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer), and may change in response to a [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="91714-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91714-120">Requirements</span></span>



| <span data-ttu-id="91714-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="91714-121">Requirement</span></span> | <span data-ttu-id="91714-122">Value</span><span class="sxs-lookup"><span data-stu-id="91714-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91714-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91714-123">Minimum supported client</span></span><br/> | <span data-ttu-id="91714-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="91714-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="91714-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91714-125">Minimum supported server</span></span><br/> | <span data-ttu-id="91714-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="91714-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="91714-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91714-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="91714-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91714-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91714-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="91714-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="91714-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="91714-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="91714-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="91714-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="91714-132">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="91714-132">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="91714-133">**CHANGECBCHAIN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="91714-133">**WM\_CHANGECBCHAIN**</span></span>](wm-changecbchain.md)
</dt> <dt>

<span data-ttu-id="91714-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="91714-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="91714-135">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="91714-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

