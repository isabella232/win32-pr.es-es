---
title: Mensaje de MCIWNDM_SETOWNER (VFW. h)
description: El \_ mensaje MCIWNDM SETOWNER establece la ventana para recibir los mensajes de notificación asociados a la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetOwner.
ms.assetid: c2d0f9d5-bf60-4036-a613-65ba1ed83110
keywords:
- Mensaje de MCIWNDM_SETOWNER de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETOWNER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3989632e83a65cda5e805bd91da3f502ca387d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150632"
---
# <a name="mciwndm_setowner-message"></a><span data-ttu-id="9ba90-105">MCIWNDM \_ SETOWNER</span><span class="sxs-lookup"><span data-stu-id="9ba90-105">MCIWNDM\_SETOWNER message</span></span>

<span data-ttu-id="9ba90-106">El mensaje **MCIWNDM \_ SETOWNER** establece la ventana para recibir los mensajes de notificación asociados a la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="9ba90-106">The **MCIWNDM\_SETOWNER** message sets the window to receive notification messages associated with the MCIWnd window.</span></span> <span data-ttu-id="9ba90-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .</span><span class="sxs-lookup"><span data-stu-id="9ba90-107">You can send this message explicitly or by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>


```C++
MCIWNDM_SETOWNER 
wParam = (WPARAM) hwndP; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="9ba90-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ba90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ba90-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span><span class="sxs-lookup"><span data-stu-id="9ba90-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span></span>
</dt> <dd>

<span data-ttu-id="9ba90-110">Identificador de la ventana para recibir los mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="9ba90-110">Handle to the window to receive the notification messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ba90-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ba90-111">Return Value</span></span>

<span data-ttu-id="9ba90-112">Devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="9ba90-112">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba90-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ba90-113">Requirements</span></span>



| <span data-ttu-id="9ba90-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ba90-114">Requirement</span></span> | <span data-ttu-id="9ba90-115">Value</span><span class="sxs-lookup"><span data-stu-id="9ba90-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9ba90-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ba90-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba90-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9ba90-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9ba90-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ba90-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba90-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ba90-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9ba90-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ba90-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ba90-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ba90-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba90-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ba90-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba90-123">**MCIWndSetOwner**</span><span class="sxs-lookup"><span data-stu-id="9ba90-123">**MCIWndSetOwner**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)
</dt> </dl>

 

 





