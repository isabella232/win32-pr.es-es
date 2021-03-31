---
title: Mensaje de WM_CAP_SINGLE_FRAME (VFW. h)
description: El mensaje de un \_ \_ solo fotograma Cap de WM \_ anexa un solo fotograma a un archivo de captura que se abrió con el \_ mensaje de apertura de trama único de Cap de WM \_ \_ \_ . Puede enviar este mensaje explícitamente o mediante la macro capCaptureSingleFrame.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- Mensaje de WM_CAP_SINGLE_FRAME de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151092"
---
# <a name="wm_cap_single_frame-message"></a><span data-ttu-id="9ef74-105">\_Mensaje de \_ marco único de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="9ef74-105">WM\_CAP\_SINGLE\_FRAME message</span></span>

<span data-ttu-id="9ef74-106">El mensaje de un **\_ \_ solo \_ fotograma Cap de WM** anexa un solo fotograma a un archivo de captura que se abrió con el mensaje de [**\_ \_ \_ \_ apertura de trama único de Cap de WM**](wm-cap-single-frame-open.md) .</span><span class="sxs-lookup"><span data-stu-id="9ef74-106">The **WM\_CAP\_SINGLE\_FRAME** message appends a single frame to a capture file that was opened using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="9ef74-107">Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) .</span><span class="sxs-lookup"><span data-stu-id="9ef74-107">You can send this message explicitly or by using the [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="9ef74-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ef74-108">Return Value</span></span>

<span data-ttu-id="9ef74-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9ef74-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef74-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ef74-110">Requirements</span></span>



| <span data-ttu-id="9ef74-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ef74-111">Requirement</span></span> | <span data-ttu-id="9ef74-112">Value</span><span class="sxs-lookup"><span data-stu-id="9ef74-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9ef74-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ef74-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef74-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9ef74-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9ef74-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ef74-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef74-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ef74-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9ef74-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ef74-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ef74-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ef74-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ef74-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ef74-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef74-120">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="9ef74-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9ef74-121">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="9ef74-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





