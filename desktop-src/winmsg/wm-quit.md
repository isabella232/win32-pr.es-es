---
description: Indica una solicitud para finalizar una aplicación y se genera cuando la aplicación llama a la función PostQuitMessage. Este mensaje hace que la función GetMessage devuelva cero.
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: Mensaje de WM_QUIT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e0d7413d65e9a0fb451fe63504f2ed5be02064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082679"
---
# <a name="wm_quit-message"></a><span data-ttu-id="0bd88-104">Mensaje de salida de WM \_</span><span class="sxs-lookup"><span data-stu-id="0bd88-104">WM\_QUIT message</span></span>

<span data-ttu-id="0bd88-105">Indica una solicitud para finalizar una aplicación y se genera cuando la aplicación llama a la función [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .</span><span class="sxs-lookup"><span data-stu-id="0bd88-105">Indicates a request to terminate an application, and is generated when the application calls the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span> <span data-ttu-id="0bd88-106">Este mensaje hace que la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) devuelva cero.</span><span class="sxs-lookup"><span data-stu-id="0bd88-106">This message causes the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function to return zero.</span></span>


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a><span data-ttu-id="0bd88-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bd88-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bd88-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0bd88-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bd88-109">Código de salida proporcionado en la función [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .</span><span class="sxs-lookup"><span data-stu-id="0bd88-109">The exit code given in the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="0bd88-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0bd88-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bd88-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0bd88-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bd88-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0bd88-112">Return value</span></span>

<span data-ttu-id="0bd88-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="0bd88-113">Type: **LRESULT**</span></span>

<span data-ttu-id="0bd88-114">Este mensaje no tiene un valor devuelto porque hace que el bucle de mensajes finalice antes de que el mensaje se envíe al procedimiento de ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0bd88-114">This message does not have a return value because it causes the message loop to terminate before the message is sent to the application's window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bd88-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bd88-115">Remarks</span></span>

<span data-ttu-id="0bd88-116">El mensaje de **\_ salida de WM** no está asociado a una ventana y, por tanto, nunca se recibirá a través del procedimiento de ventana de la ventana.</span><span class="sxs-lookup"><span data-stu-id="0bd88-116">The **WM\_QUIT** message is not associated with a window and therefore will never be received through a window's window procedure.</span></span> <span data-ttu-id="0bd88-117">Solo lo recuperan las funciones [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="0bd88-117">It is retrieved only by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions.</span></span>

<span data-ttu-id="0bd88-118">No publique el mensaje **de \_ salida de WM** con la función [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) ; use [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span><span class="sxs-lookup"><span data-stu-id="0bd88-118">Do not post the **WM\_QUIT** message using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function; use [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bd88-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bd88-119">Requirements</span></span>



| <span data-ttu-id="0bd88-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bd88-120">Requirement</span></span> | <span data-ttu-id="0bd88-121">Value</span><span class="sxs-lookup"><span data-stu-id="0bd88-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd88-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bd88-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0bd88-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0bd88-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0bd88-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bd88-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0bd88-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0bd88-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0bd88-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bd88-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bd88-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bd88-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bd88-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bd88-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="0bd88-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0bd88-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0bd88-130">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="0bd88-130">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="0bd88-131">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="0bd88-131">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="0bd88-132">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="0bd88-132">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

<span data-ttu-id="0bd88-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0bd88-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0bd88-134">Windows</span><span class="sxs-lookup"><span data-stu-id="0bd88-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
