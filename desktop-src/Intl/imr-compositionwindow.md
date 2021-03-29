---
description: Notifica a una aplicación cuando un IME seleccionado necesita información sobre la ventana de composición. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con los parámetros establecidos como se muestra a continuación.
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: Código de notificación de IMR_COMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af0481ccebc59968fe85a489c856388a04dbece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652677"
---
# <a name="imr_compositionwindow-notification-code"></a><span data-ttu-id="ae578-104">Código de notificación de IMR \_ COMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="ae578-104">IMR\_COMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="ae578-105">Notifica a una aplicación cuando un IME seleccionado necesita información sobre la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="ae578-105">Notifies an application when a selected IME needs information about the composition window.</span></span> <span data-ttu-id="ae578-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con los parámetros establecidos como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="ae578-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="ae578-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae578-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae578-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae578-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="ae578-109">Establezca en IMR \_ COMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="ae578-109">Set to IMR\_COMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="ae578-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae578-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ae578-111">Puntero a un búfer que contiene una estructura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) .</span><span class="sxs-lookup"><span data-stu-id="ae578-111">Pointer to a buffer containing a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae578-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae578-112">Return Value</span></span>

<span data-ttu-id="ae578-113">Devuelve un valor distinto de cero si la aplicación rellena la estructura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) .</span><span class="sxs-lookup"><span data-stu-id="ae578-113">Returns a nonzero value if the application fills in the [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span> <span data-ttu-id="ae578-114">De lo contrario, el comando devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="ae578-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae578-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae578-115">Remarks</span></span>

<span data-ttu-id="ae578-116">El IME puede enviar este comando a una ventana que haya borrado la \_ marca SHOWUICOMPOSITIONWINDOW de ISC en el controlador de mensajes de [**\_ IME IME \_ SETCONTEXT**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="ae578-116">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae578-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae578-117">Requirements</span></span>



| <span data-ttu-id="ae578-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae578-118">Requirement</span></span> | <span data-ttu-id="ae578-119">Value</span><span class="sxs-lookup"><span data-stu-id="ae578-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae578-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae578-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae578-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ae578-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ae578-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae578-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae578-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ae578-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ae578-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae578-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae578-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae578-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae578-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae578-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae578-127">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="ae578-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="ae578-128">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="ae578-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="ae578-129">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="ae578-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="ae578-130">**\_solicitud de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ae578-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="ae578-131">**\_SETCONTEXT IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ae578-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 




