---
title: Mensaje de WM_CAP_DRIVER_DISCONNECT (VFW. h)
description: El \_ \_ \_ mensaje de desconexión del controlador Cap de WM desconecta un controlador de captura de una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capDriverDisconnect.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- Mensaje de WM_CAP_DRIVER_DISCONNECT de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acad628cc61bbb50c56f68fda91ac87be4feb728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996266"
---
# <a name="wm_cap_driver_disconnect-message"></a><span data-ttu-id="49724-105">\_Mensaje de \_ desconexión del controlador Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="49724-105">WM\_CAP\_DRIVER\_DISCONNECT message</span></span>

<span data-ttu-id="49724-106">El mensaje de **\_ \_ \_ desconexión del controlador Cap de WM** desconecta un controlador de captura de una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="49724-106">The **WM\_CAP\_DRIVER\_DISCONNECT** message disconnects a capture driver from a capture window.</span></span> <span data-ttu-id="49724-107">Puede enviar este mensaje explícitamente o mediante la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) .</span><span class="sxs-lookup"><span data-stu-id="49724-107">You can send this message explicitly or by using the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="49724-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49724-108">Return Value</span></span>

<span data-ttu-id="49724-109">Devuelve **true** si es correcto o **false** si la ventana de captura no está conectada a un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="49724-109">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="49724-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49724-110">Requirements</span></span>



| <span data-ttu-id="49724-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="49724-111">Requirement</span></span> | <span data-ttu-id="49724-112">Value</span><span class="sxs-lookup"><span data-stu-id="49724-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="49724-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49724-113">Minimum supported client</span></span><br/> | <span data-ttu-id="49724-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="49724-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="49724-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49724-115">Minimum supported server</span></span><br/> | <span data-ttu-id="49724-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="49724-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="49724-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49724-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="49724-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="49724-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49724-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="49724-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49724-120">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="49724-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="49724-121">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="49724-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





