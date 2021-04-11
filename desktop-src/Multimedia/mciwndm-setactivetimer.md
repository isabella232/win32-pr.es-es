---
title: Mensaje de MCIWNDM_SETACTIVETIMER (VFW. h)
description: El \_ mensaje MCIWNDM SETACTIVETIMER establece el período de actualización que usa MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de la posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana de MCIWnd está activa. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetActiveTimer.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- Mensaje de MCIWNDM_SETACTIVETIMER de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150630"
---
# <a name="mciwndm_setactivetimer-message"></a><span data-ttu-id="26f5a-105">MCIWNDM \_ SETACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="26f5a-105">MCIWNDM\_SETACTIVETIMER message</span></span>

<span data-ttu-id="26f5a-106">El mensaje **MCIWNDM \_ SETACTIVETIMER** establece el período de actualización que usa MCIWnd para actualizar la barra de control en la ventana MCIWnd, actualizar la información de la posición que se muestra en la barra de título de la ventana y enviar mensajes de notificación a la ventana primaria cuando la ventana de MCIWnd está activa.</span><span class="sxs-lookup"><span data-stu-id="26f5a-106">The **MCIWNDM\_SETACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is active.</span></span> <span data-ttu-id="26f5a-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="26f5a-107">You can send this message explicitly or by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span>


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="26f5a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26f5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f5a-109"><span id="active"></span><span id="ACTIVE"></span>*Active*</span><span class="sxs-lookup"><span data-stu-id="26f5a-109"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="26f5a-110">Período de actualización, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="26f5a-110">Update period, in milliseconds.</span></span> <span data-ttu-id="26f5a-111">El valor predeterminado es 500 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="26f5a-111">The default is 500 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f5a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26f5a-112">Return Value</span></span>

<span data-ttu-id="26f5a-113">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="26f5a-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f5a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26f5a-114">Requirements</span></span>



| <span data-ttu-id="26f5a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f5a-115">Requirement</span></span> | <span data-ttu-id="26f5a-116">Value</span><span class="sxs-lookup"><span data-stu-id="26f5a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="26f5a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26f5a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="26f5a-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="26f5a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="26f5a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26f5a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="26f5a-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="26f5a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="26f5a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26f5a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="26f5a-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="26f5a-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f5a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="26f5a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f5a-124">**MCIWndSetActiveTimer**</span><span class="sxs-lookup"><span data-stu-id="26f5a-124">**MCIWndSetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





