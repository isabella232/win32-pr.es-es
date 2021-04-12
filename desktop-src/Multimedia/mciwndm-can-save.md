---
title: Mensaje de MCIWNDM_CAN_SAVE (VFW. h)
description: El MCIWNDM \_ puede \_ guardar el mensaje determina si un dispositivo MCI puede guardar datos. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanSave.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- Mensaje de MCIWNDM_CAN_SAVE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11b60b8a5d93ac80befc8beeb6665399efe44f1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489574"
---
# <a name="mciwndm_can_save-message"></a><span data-ttu-id="c9d2e-105">MCIWNDM \_ puede \_ guardar el mensaje</span><span class="sxs-lookup"><span data-stu-id="c9d2e-105">MCIWNDM\_CAN\_SAVE message</span></span>

<span data-ttu-id="c9d2e-106">El **MCIWNDM \_ puede \_ Guardar** el mensaje determina si un dispositivo MCI puede guardar datos.</span><span class="sxs-lookup"><span data-stu-id="c9d2e-106">The **MCIWNDM\_CAN\_SAVE** message determines if an MCI device can save data.</span></span> <span data-ttu-id="c9d2e-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) .</span><span class="sxs-lookup"><span data-stu-id="c9d2e-107">You can send this message explicitly or by using the [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) macro.</span></span>


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="c9d2e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9d2e-108">Return Value</span></span>

<span data-ttu-id="c9d2e-109">Devuelve **true** si el dispositivo admite el guardado o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c9d2e-109">Returns **TRUE** if the device supports saving or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d2e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9d2e-110">Requirements</span></span>



| <span data-ttu-id="c9d2e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9d2e-111">Requirement</span></span> | <span data-ttu-id="c9d2e-112">Value</span><span class="sxs-lookup"><span data-stu-id="c9d2e-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c9d2e-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9d2e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c9d2e-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c9d2e-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c9d2e-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9d2e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c9d2e-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9d2e-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c9d2e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9d2e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9d2e-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9d2e-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d2e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9d2e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d2e-120">**MCIWndCanSave**</span><span class="sxs-lookup"><span data-stu-id="c9d2e-120">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





