---
description: Notfies una aplicación cuando un IME seleccionado necesita información sobre la ventana candidata. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: Código de notificación de IMR_CANDIDATEWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667157"
---
# <a name="imr_candidatewindow-notification-code"></a><span data-ttu-id="ccc59-104">Código de notificación de IMR \_ CANDIDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="ccc59-104">IMR\_CANDIDATEWINDOW notification code</span></span>

<span data-ttu-id="ccc59-105">Notfies una aplicación cuando un IME seleccionado necesita información sobre la ventana candidata.</span><span class="sxs-lookup"><span data-stu-id="ccc59-105">Notfies an application when a selected IME needs information about the candidate window.</span></span> <span data-ttu-id="ccc59-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="ccc59-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a><span data-ttu-id="ccc59-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ccc59-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc59-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccc59-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="ccc59-109">Establezca en IMR \_ CANDIDATEWINDOW.</span><span class="sxs-lookup"><span data-stu-id="ccc59-109">Set to IMR\_CANDIDATEWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="ccc59-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccc59-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ccc59-111">Puntero a un búfer que contiene una estructura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) .</span><span class="sxs-lookup"><span data-stu-id="ccc59-111">Pointer to a buffer containing a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="ccc59-112">Su miembro **dwIndex** contiene el índice de la ventana candidata a la que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="ccc59-112">Its **dwIndex** member contains the index to the candidate window referenced.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccc59-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccc59-113">Return Value</span></span>

<span data-ttu-id="ccc59-114">Devuelve un valor distinto de cero si la aplicación rellena la estructura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) .</span><span class="sxs-lookup"><span data-stu-id="ccc59-114">Returns a nonzero value if the application fills in the [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="ccc59-115">De lo contrario, el comando devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="ccc59-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccc59-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ccc59-116">Remarks</span></span>

<span data-ttu-id="ccc59-117">El IME puede enviar este comando a una ventana que haya borrado la \_ marca SHOWUICANDIDATEWINDOW de ISC en el controlador de mensajes de [**\_ IME IME \_ SETCONTEXT**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="ccc59-117">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICANDIDATEWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc59-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccc59-118">Requirements</span></span>



| <span data-ttu-id="ccc59-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccc59-119">Requirement</span></span> | <span data-ttu-id="ccc59-120">Value</span><span class="sxs-lookup"><span data-stu-id="ccc59-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc59-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccc59-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc59-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ccc59-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ccc59-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccc59-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc59-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ccc59-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ccc59-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ccc59-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc59-126"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccc59-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccc59-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccc59-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc59-128">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="ccc59-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="ccc59-129">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="ccc59-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="ccc59-130">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="ccc59-130">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="ccc59-131">**\_solicitud de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ccc59-131">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="ccc59-132">**\_SETCONTEXT IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ccc59-132">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 




