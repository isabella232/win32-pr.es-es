---
description: Notifica a una aplicación cuando un IME seleccionado necesita información sobre la fuente utilizada por la ventana de composición. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con parámetros, como se muestra a continuación.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: Código de notificación de IMR_COMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687457"
---
# <a name="imr_compositionfont-notification-code"></a><span data-ttu-id="1dac2-104">Código de notificación de IMR \_ COMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="1dac2-104">IMR\_COMPOSITIONFONT notification code</span></span>

<span data-ttu-id="1dac2-105">Notifica a una aplicación cuando un IME seleccionado necesita información sobre la fuente utilizada por la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="1dac2-105">Notifies an application when a selected IME needs information about the font used by the composition window.</span></span> <span data-ttu-id="1dac2-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="1dac2-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="1dac2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1dac2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dac2-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="1dac2-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="1dac2-109">Establezca en IMR \_ COMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="1dac2-109">Set to IMR\_COMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="1dac2-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="1dac2-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="1dac2-111">Puntero a un búfer que contiene una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="1dac2-111">Pointer to a buffer containing a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="1dac2-112">La aplicación rellena los valores de la ventana de composición actual.</span><span class="sxs-lookup"><span data-stu-id="1dac2-112">The application fills in the values for the current composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dac2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dac2-113">Return Value</span></span>

<span data-ttu-id="1dac2-114">Devuelve un valor distinto de cero si la aplicación rellena la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="1dac2-114">Returns a nonzero value if the application fills in the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="1dac2-115">De lo contrario, el comando devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="1dac2-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dac2-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1dac2-116">Remarks</span></span>

<span data-ttu-id="1dac2-117">El IME puede enviar este comando a una ventana que borró la \_ marca SHOWUICOMPOSITIONWINDOW de ISC en el controlador de mensajes de [**\_ IME \_ de WM**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="1dac2-117">This command can be sent by the IME to a window that cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dac2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dac2-118">Requirements</span></span>



| <span data-ttu-id="1dac2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dac2-119">Requirement</span></span> | <span data-ttu-id="1dac2-120">Value</span><span class="sxs-lookup"><span data-stu-id="1dac2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dac2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dac2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1dac2-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1dac2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1dac2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dac2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1dac2-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1dac2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1dac2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dac2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dac2-126"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1dac2-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dac2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1dac2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dac2-128">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="1dac2-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="1dac2-129">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="1dac2-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="1dac2-130">**\_solicitud de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1dac2-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="1dac2-131">**\_SETCONTEXT IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1dac2-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 
