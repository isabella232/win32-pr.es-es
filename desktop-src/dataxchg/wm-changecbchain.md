---
title: Mensaje de WM_CHANGECBCHAIN (Winuser. h)
description: Se envía a la primera ventana de la cadena del visor del portapapeles cuando se quita una ventana de la cadena. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- Intercambio de datos de mensajes de WM_CHANGECBCHAIN
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150422"
---
# <a name="wm_changecbchain-message"></a><span data-ttu-id="83fbe-105">Mensaje de CHANGECBCHAIN de WM \_</span><span class="sxs-lookup"><span data-stu-id="83fbe-105">WM\_CHANGECBCHAIN message</span></span>

<span data-ttu-id="83fbe-106">Se envía a la primera ventana de la cadena del visor del portapapeles cuando se quita una ventana de la cadena.</span><span class="sxs-lookup"><span data-stu-id="83fbe-106">Sent to the first window in the clipboard viewer chain when a window is being removed from the chain.</span></span>

<span data-ttu-id="83fbe-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="83fbe-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a><span data-ttu-id="83fbe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83fbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83fbe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83fbe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83fbe-110">Identificador de la ventana que se va a quitar de la cadena del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="83fbe-110">A handle to the window being removed from the clipboard viewer chain.</span></span>

</dd> <dt>

<span data-ttu-id="83fbe-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83fbe-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83fbe-112">Identificador de la siguiente ventana de la cadena que sigue a la ventana que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="83fbe-112">A handle to the next window in the chain following the window being removed.</span></span> <span data-ttu-id="83fbe-113">Este parámetro es **null** si la ventana que se va a quitar es la última ventana de la cadena.</span><span class="sxs-lookup"><span data-stu-id="83fbe-113">This parameter is **NULL** if the window being removed is the last window in the chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83fbe-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83fbe-114">Return value</span></span>

<span data-ttu-id="83fbe-115">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="83fbe-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="83fbe-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83fbe-116">Remarks</span></span>

<span data-ttu-id="83fbe-117">Cada ventana del visor del portapapeles guarda el identificador en la siguiente ventana de la cadena del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="83fbe-117">Each clipboard viewer window saves the handle to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="83fbe-118">Inicialmente, este identificador es el valor devuelto de la función [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="83fbe-118">Initially, this handle is the return value of the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="83fbe-119">Cuando una ventana del visor del portapapeles recibe el mensaje de **\_ CHANGECBCHAIN de WM** , debe llamar a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para pasar el mensaje a la siguiente ventana de la cadena, a menos que la ventana siguiente sea la ventana que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="83fbe-119">When a clipboard viewer window receives the **WM\_CHANGECBCHAIN** message, it should call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message to the next window in the chain, unless the next window is the window being removed.</span></span> <span data-ttu-id="83fbe-120">En este caso, el visor del portapapeles debe guardar el identificador especificado por el parámetro *lParam* como la siguiente ventana de la cadena.</span><span class="sxs-lookup"><span data-stu-id="83fbe-120">In this case, the clipboard viewer should save the handle specified by the *lParam* parameter as the next window in the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="83fbe-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83fbe-121">Requirements</span></span>



| <span data-ttu-id="83fbe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="83fbe-122">Requirement</span></span> | <span data-ttu-id="83fbe-123">Value</span><span class="sxs-lookup"><span data-stu-id="83fbe-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83fbe-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83fbe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="83fbe-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="83fbe-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="83fbe-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83fbe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="83fbe-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="83fbe-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="83fbe-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83fbe-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="83fbe-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83fbe-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83fbe-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="83fbe-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="83fbe-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="83fbe-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="83fbe-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="83fbe-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="83fbe-133">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="83fbe-133">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

<span data-ttu-id="83fbe-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="83fbe-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="83fbe-135">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="83fbe-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

