---
description: Enviado por una aplicación de aprendizaje basado en PC (CBT) para separar los mensajes de entrada del usuario de otros mensajes enviados mediante el \_ procedimiento qu JOURNALPLAYBACK.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: Mensaje de WM_QUEUESYNC (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648387"
---
# <a name="wm_queuesync-message"></a><span data-ttu-id="d313d-103">Mensaje de QUEUESYNC de WM \_</span><span class="sxs-lookup"><span data-stu-id="d313d-103">WM\_QUEUESYNC message</span></span>

<span data-ttu-id="d313d-104">Enviado por una aplicación de aprendizaje basado en PC (CBT) para separar los mensajes de entrada del usuario de otros mensajes enviados mediante el procedimiento [**qu \_ JOURNALPLAYBACK**](about-hooks.md) .</span><span class="sxs-lookup"><span data-stu-id="d313d-104">Sent by a computer-based training (CBT) application to separate user-input messages from other messages sent through the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure.</span></span>


```C++
#define WM_QUEUESYNC                    0x0023
```



## <a name="parameters"></a><span data-ttu-id="d313d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d313d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d313d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d313d-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d313d-107">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d313d-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d313d-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d313d-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d313d-109">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d313d-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d313d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d313d-110">Return value</span></span>

<span data-ttu-id="d313d-111">Tipo: **void**</span><span class="sxs-lookup"><span data-stu-id="d313d-111">Type: **void**</span></span>

<span data-ttu-id="d313d-112">Una aplicación CBT debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="d313d-112">A CBT application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="d313d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d313d-113">Remarks</span></span>

<span data-ttu-id="d313d-114">Cada vez que una aplicación CBT usa el procedimiento [**qu \_ JOURNALPLAYBACK**](about-hooks.md) , el primero y el último mensaje son **WM \_ QUEUESYNC**.</span><span class="sxs-lookup"><span data-stu-id="d313d-114">Whenever a CBT application uses the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure, the first and last messages are **WM\_QUEUESYNC**.</span></span> <span data-ttu-id="d313d-115">Esto permite que la aplicación CBT intercepte y examine los mensajes iniciados por el usuario sin necesidad de hacerlo para los eventos que envía.</span><span class="sxs-lookup"><span data-stu-id="d313d-115">This allows the CBT application to intercept and examine user-initiated messages without doing so for events that it sends.</span></span>

<span data-ttu-id="d313d-116">Si una aplicación especifica un identificador de ventana **nulo** , el mensaje se envía a la cola de mensajes de la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="d313d-116">If an application specifies a **NULL** window handle, the message is posted to the message queue of the active window.</span></span>

## <a name="requirements"></a><span data-ttu-id="d313d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d313d-117">Requirements</span></span>



| <span data-ttu-id="d313d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d313d-118">Requirement</span></span> | <span data-ttu-id="d313d-119">Value</span><span class="sxs-lookup"><span data-stu-id="d313d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d313d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d313d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d313d-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d313d-121">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d313d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d313d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d313d-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d313d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d313d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d313d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d313d-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d313d-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d313d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d313d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d313d-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d313d-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="d313d-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d313d-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d313d-129">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="d313d-129">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="d313d-130">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d313d-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d313d-131">Enlaces</span><span class="sxs-lookup"><span data-stu-id="d313d-131">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
