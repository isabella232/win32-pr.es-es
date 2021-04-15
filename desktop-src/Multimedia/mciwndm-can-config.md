---
title: Mensaje de MCIWNDM_CAN_CONFIG (VFW. h)
description: El \_ mensaje MCIWNDM puede \_ configurar determina si un dispositivo MCI puede mostrar un cuadro de diálogo de configuración. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanConfig.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- Mensaje de MCIWNDM_CAN_CONFIG de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493030"
---
# <a name="mciwndm_can_config-message"></a><span data-ttu-id="03bbd-105">MCIWNDM \_ puede \_ configurar el mensaje</span><span class="sxs-lookup"><span data-stu-id="03bbd-105">MCIWNDM\_CAN\_CONFIG message</span></span>

<span data-ttu-id="03bbd-106">El mensaje **MCIWNDM \_ puede \_ configurar** determina si un dispositivo MCI puede mostrar un cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="03bbd-106">The **MCIWNDM\_CAN\_CONFIG** message determines if an MCI device can display a configuration dialog box.</span></span> <span data-ttu-id="03bbd-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) .</span><span class="sxs-lookup"><span data-stu-id="03bbd-107">You can send this message explicitly or by using the [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) macro.</span></span>


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="03bbd-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03bbd-108">Return Value</span></span>

<span data-ttu-id="03bbd-109">Devuelve **true** si el dispositivo admite la configuración o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="03bbd-109">Returns **TRUE** if the device supports configuration or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="03bbd-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03bbd-110">Requirements</span></span>



| <span data-ttu-id="03bbd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="03bbd-111">Requirement</span></span> | <span data-ttu-id="03bbd-112">Value</span><span class="sxs-lookup"><span data-stu-id="03bbd-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="03bbd-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03bbd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="03bbd-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="03bbd-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="03bbd-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03bbd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="03bbd-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03bbd-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="03bbd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03bbd-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="03bbd-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="03bbd-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03bbd-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="03bbd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03bbd-120">**MCIWndCanConfig**</span><span class="sxs-lookup"><span data-stu-id="03bbd-120">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





