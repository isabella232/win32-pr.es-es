---
title: Mensaje de WM_KILLFOCUS (Winuser. h)
description: Se envía a una ventana inmediatamente antes de que pierda el foco de teclado.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- Entrada de mouse y teclado de mensaje de WM_KILLFOCUS
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e3bba54f2cdb500ba2ba691ffd30419d5beff1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079235"
---
# <a name="wm_killfocus-message"></a><span data-ttu-id="71cda-104">Mensaje de KILLFOCUS de WM \_</span><span class="sxs-lookup"><span data-stu-id="71cda-104">WM\_KILLFOCUS message</span></span>

<span data-ttu-id="71cda-105">Se envía a una ventana inmediatamente antes de que pierda el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="71cda-105">Sent to a window immediately before it loses the keyboard focus.</span></span>


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a><span data-ttu-id="71cda-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71cda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71cda-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71cda-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71cda-108">Identificador de la ventana que recibe el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="71cda-108">A handle to the window that receives the keyboard focus.</span></span> <span data-ttu-id="71cda-109">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="71cda-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="71cda-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71cda-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71cda-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="71cda-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71cda-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71cda-112">Return value</span></span>

<span data-ttu-id="71cda-113">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="71cda-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="71cda-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71cda-114">Remarks</span></span>

<span data-ttu-id="71cda-115">Si una aplicación muestra un símbolo de intercalación, el símbolo de intercalación debería destruirse en este momento.</span><span class="sxs-lookup"><span data-stu-id="71cda-115">If an application is displaying a caret, the caret should be destroyed at this point.</span></span>

<span data-ttu-id="71cda-116">Al procesar este mensaje, no realice ninguna llamada de función que muestre o Active una ventana.</span><span class="sxs-lookup"><span data-stu-id="71cda-116">While processing this message, do not make any function calls that display or activate a window.</span></span> <span data-ttu-id="71cda-117">Esto hace que el subproceso produzca el control y puede hacer que la aplicación deje de responder a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="71cda-117">This causes the thread to yield control and can cause the application to stop responding to messages.</span></span> <span data-ttu-id="71cda-118">Para obtener más información, vea [interbloqueos de mensajes](/windows/desktop/winmsg/about-messages-and-message-queues).</span><span class="sxs-lookup"><span data-stu-id="71cda-118">For more information, see [Message Deadlocks](/windows/desktop/winmsg/about-messages-and-message-queues).</span></span>

## <a name="requirements"></a><span data-ttu-id="71cda-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71cda-119">Requirements</span></span>



| <span data-ttu-id="71cda-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="71cda-120">Requirement</span></span> | <span data-ttu-id="71cda-121">Value</span><span class="sxs-lookup"><span data-stu-id="71cda-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71cda-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71cda-122">Minimum supported client</span></span><br/> | <span data-ttu-id="71cda-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="71cda-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="71cda-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71cda-124">Minimum supported server</span></span><br/> | <span data-ttu-id="71cda-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71cda-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71cda-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71cda-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="71cda-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71cda-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71cda-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="71cda-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="71cda-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="71cda-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="71cda-130">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="71cda-130">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="71cda-131">**SETFOCUS de WM \_**</span><span class="sxs-lookup"><span data-stu-id="71cda-131">**WM\_SETFOCUS**</span></span>](wm-setfocus.md)
</dt> <dt>

<span data-ttu-id="71cda-132">**Vista**</span><span class="sxs-lookup"><span data-stu-id="71cda-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="71cda-133">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="71cda-133">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

