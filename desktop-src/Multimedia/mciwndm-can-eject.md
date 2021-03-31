---
title: Mensaje de MCIWNDM_CAN_EJECT (VFW. h)
description: El \_ mensaje MCIWNDM puede \_ expulsar determina si un dispositivo MCI puede expulsar el contenido multimedia. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanEject.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- Mensaje de MCIWNDM_CAN_EJECT de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803914"
---
# <a name="mciwndm_can_eject-message"></a><span data-ttu-id="519a0-105">MCIWNDM \_ puede \_ expulsar el mensaje</span><span class="sxs-lookup"><span data-stu-id="519a0-105">MCIWNDM\_CAN\_EJECT message</span></span>

<span data-ttu-id="519a0-106">El mensaje **MCIWNDM \_ puede \_ expulsar** determina si un dispositivo MCI puede expulsar el contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="519a0-106">The **MCIWNDM\_CAN\_EJECT** message determines if an MCI device can eject its media.</span></span> <span data-ttu-id="519a0-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) .</span><span class="sxs-lookup"><span data-stu-id="519a0-107">You can send this message explicitly or by using the [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) macro.</span></span>


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="519a0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="519a0-108">Return Value</span></span>

<span data-ttu-id="519a0-109">Devuelve **true** si el dispositivo puede expulsar su medio o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="519a0-109">Returns **TRUE** if the device can eject its media or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="519a0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="519a0-110">Requirements</span></span>



| <span data-ttu-id="519a0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="519a0-111">Requirement</span></span> | <span data-ttu-id="519a0-112">Value</span><span class="sxs-lookup"><span data-stu-id="519a0-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="519a0-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="519a0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="519a0-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="519a0-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="519a0-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="519a0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="519a0-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="519a0-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="519a0-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="519a0-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="519a0-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="519a0-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="519a0-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="519a0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="519a0-120">**MCIWndCanEject**</span><span class="sxs-lookup"><span data-stu-id="519a0-120">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





