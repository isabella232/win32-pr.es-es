---
title: Mensaje de MCIWNDM_CAN_WINDOW (VFW. h)
description: El mensaje de ventana de MCIWNDM \_ puede \_ determinar si un dispositivo MCI admite comandos MCI orientados a ventanas. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanWindow.
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- Mensaje de MCIWNDM_CAN_WINDOW de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d638b61093483b6e834b57af1d5c892d77d0f1d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996270"
---
# <a name="mciwndm_can_window-message"></a><span data-ttu-id="633fe-105">MCIWNDM \_ puede \_ ventana Message</span><span class="sxs-lookup"><span data-stu-id="633fe-105">MCIWNDM\_CAN\_WINDOW message</span></span>

<span data-ttu-id="633fe-106">El mensaje de **\_ \_ ventana de MCIWNDM puede** determinar si un dispositivo MCI admite comandos MCI orientados a ventanas.</span><span class="sxs-lookup"><span data-stu-id="633fe-106">The **MCIWNDM\_CAN\_WINDOW** message determines if an MCI device supports window-oriented MCI commands.</span></span> <span data-ttu-id="633fe-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) .</span><span class="sxs-lookup"><span data-stu-id="633fe-107">You can send this message explicitly or by using the [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) macro.</span></span>


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="633fe-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="633fe-108">Return Value</span></span>

<span data-ttu-id="633fe-109">Devuelve **true** si el dispositivo admite comandos MCI orientados a ventanas o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="633fe-109">Returns **TRUE** if the device supports window-oriented MCI commands or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="633fe-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="633fe-110">Requirements</span></span>



| <span data-ttu-id="633fe-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="633fe-111">Requirement</span></span> | <span data-ttu-id="633fe-112">Value</span><span class="sxs-lookup"><span data-stu-id="633fe-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="633fe-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="633fe-113">Minimum supported client</span></span><br/> | <span data-ttu-id="633fe-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="633fe-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="633fe-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="633fe-115">Minimum supported server</span></span><br/> | <span data-ttu-id="633fe-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="633fe-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="633fe-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="633fe-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="633fe-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="633fe-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="633fe-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="633fe-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633fe-120">**MCIWndCanWindow**</span><span class="sxs-lookup"><span data-stu-id="633fe-120">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





