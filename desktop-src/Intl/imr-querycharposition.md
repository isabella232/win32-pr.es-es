---
description: Notifica a una aplicación cuando el IME seleccionado necesita información sobre las coordenadas de un carácter en la cadena de composición. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: Código de notificación de IMR_QUERYCHARPOSITION (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947eec9b3dd1f678d9266bb795214cf392629193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687455"
---
# <a name="imr_querycharposition-notification-code"></a><span data-ttu-id="b1da6-104">Código de notificación de IMR \_ QUERYCHARPOSITION</span><span class="sxs-lookup"><span data-stu-id="b1da6-104">IMR\_QUERYCHARPOSITION notification code</span></span>

<span data-ttu-id="b1da6-105">Notifica a una aplicación cuando el IME seleccionado necesita información sobre las coordenadas de un carácter en la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="b1da6-105">Notifies an application when the selected IME needs information about the coordinates of a character in the composition string.</span></span> <span data-ttu-id="b1da6-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="b1da6-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a><span data-ttu-id="b1da6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1da6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1da6-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1da6-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="b1da6-109">Establezca en IMR \_ QUERYCHARPOSITION.</span><span class="sxs-lookup"><span data-stu-id="b1da6-109">Set to IMR\_QUERYCHARPOSITION.</span></span>

</dd> <dt>

<span data-ttu-id="b1da6-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1da6-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b1da6-111">Puntero a una estructura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) que contiene la posición del carácter en la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="b1da6-111">Pointer to an [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure that contains the position of the character in the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1da6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1da6-112">Return Value</span></span>

<span data-ttu-id="b1da6-113">Devuelve un valor distinto de cero si la aplicación rellena la estructura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) .</span><span class="sxs-lookup"><span data-stu-id="b1da6-113">Returns a nonzero value if the application fills the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="b1da6-114">De lo contrario, el comando devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="b1da6-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1da6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1da6-115">Remarks</span></span>

<span data-ttu-id="b1da6-116">Una aplicación que dibuja la propia cadena de composición, en lugar de depender del IME, es responsable de rellenar todos los miembros de la estructura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) .</span><span class="sxs-lookup"><span data-stu-id="b1da6-116">An application that draws the composition string itself, instead of relying on the IME, is responsible for filling in all the members of the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="b1da6-117">De lo contrario, la aplicación debe pasar el comando a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) si tiene su propia ventana de interfaz de usuario de IME.</span><span class="sxs-lookup"><span data-stu-id="b1da6-117">Otherwise, the application should pass the command to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) if it has its own IME user interface window.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1da6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1da6-118">Requirements</span></span>



| <span data-ttu-id="b1da6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1da6-119">Requirement</span></span> | <span data-ttu-id="b1da6-120">Value</span><span class="sxs-lookup"><span data-stu-id="b1da6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1da6-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1da6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b1da6-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b1da6-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b1da6-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1da6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b1da6-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b1da6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b1da6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1da6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1da6-126"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1da6-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1da6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1da6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1da6-128">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="b1da6-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b1da6-129">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="b1da6-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="b1da6-130">**IMECHARPOSITION**</span><span class="sxs-lookup"><span data-stu-id="b1da6-130">**IMECHARPOSITION**</span></span>](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[<span data-ttu-id="b1da6-131">**ImmIsUIMessage**</span><span class="sxs-lookup"><span data-stu-id="b1da6-131">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[<span data-ttu-id="b1da6-132">**\_solicitud de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="b1da6-132">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 
