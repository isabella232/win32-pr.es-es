---
title: Mensaje de MCIWNDM_SETINACTIVETIMER (VFW. h)
description: El \_ mensaje MCIWNDM SETINACTIVETIMER establece el período de actualización que usa MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de la posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana de MCIWnd está inactiva. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetInactiveTimer.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- Mensaje de MCIWNDM_SETINACTIVETIMER de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534636"
---
# <a name="mciwndm_setinactivetimer-message"></a><span data-ttu-id="c938a-105">MCIWNDM \_ SETINACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="c938a-105">MCIWNDM\_SETINACTIVETIMER message</span></span>

<span data-ttu-id="c938a-106">El mensaje **MCIWNDM \_ SETINACTIVETIMER** establece el período de actualización que usa MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de la posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana de MCIWnd está inactiva.</span><span class="sxs-lookup"><span data-stu-id="c938a-106">The **MCIWNDM\_SETINACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive.</span></span> <span data-ttu-id="c938a-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="c938a-107">You can send this message explicitly or by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span>


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="c938a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c938a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c938a-109"><span id="inactive"></span><span id="INACTIVE"></span>*inactiva*</span><span class="sxs-lookup"><span data-stu-id="c938a-109"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="c938a-110">Período de actualización, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="c938a-110">Update period, in milliseconds.</span></span> <span data-ttu-id="c938a-111">El valor predeterminado es 2000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="c938a-111">The default is 2000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c938a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c938a-112">Return Value</span></span>

<span data-ttu-id="c938a-113">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c938a-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c938a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c938a-114">Requirements</span></span>



| <span data-ttu-id="c938a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c938a-115">Requirement</span></span> | <span data-ttu-id="c938a-116">Value</span><span class="sxs-lookup"><span data-stu-id="c938a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c938a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c938a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c938a-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c938a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c938a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c938a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c938a-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c938a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c938a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c938a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c938a-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c938a-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c938a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c938a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c938a-124">**MCIWndSetInactiveTimer**</span><span class="sxs-lookup"><span data-stu-id="c938a-124">**MCIWndSetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





