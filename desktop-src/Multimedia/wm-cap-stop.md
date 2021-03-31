---
title: Mensaje de WM_CAP_STOP (VFW. h)
description: El mensaje de detención del Cap de WM \_ \_ detiene la operación de captura. Puede enviar este mensaje explícitamente o mediante la macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- Mensaje de WM_CAP_STOP de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803805"
---
# <a name="wm_cap_stop-message"></a><span data-ttu-id="5779d-105">Mensaje de detención de \_ Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="5779d-105">WM\_CAP\_STOP message</span></span>

<span data-ttu-id="5779d-106">El mensaje de **\_ \_ detención del Cap de WM** detiene la operación de captura.</span><span class="sxs-lookup"><span data-stu-id="5779d-106">The **WM\_CAP\_STOP** message stops the capture operation.</span></span> <span data-ttu-id="5779d-107">Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) .</span><span class="sxs-lookup"><span data-stu-id="5779d-107">You can send this message explicitly or by using the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro.</span></span>

<span data-ttu-id="5779d-108">En la captura de fotogramas del paso, los datos de la imagen que se recopilaron antes de que se enviara este mensaje se conservan en el archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="5779d-108">In step frame capture, the image data that was collected before this message was sent is retained in the capture file.</span></span> <span data-ttu-id="5779d-109">También se conserva una duración equivalente de los datos de audio en el archivo de captura si se ha habilitado la captura de audio.</span><span class="sxs-lookup"><span data-stu-id="5779d-109">An equivalent duration of audio data is also retained in the capture file if audio capture was enabled.</span></span>


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="5779d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5779d-110">Return Value</span></span>

<span data-ttu-id="5779d-111">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5779d-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5779d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5779d-112">Remarks</span></span>

<span data-ttu-id="5779d-113">La operación de captura debe proporcionar el uso de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="5779d-113">The capture operation must yield to use this message.</span></span> <span data-ttu-id="5779d-114">Use el mensaje de [**\_ \_ anulación de Cap de WM**](wm-cap-abort.md) para abandonar la operación de captura actual.</span><span class="sxs-lookup"><span data-stu-id="5779d-114">Use the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message to abandon the current capture operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="5779d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5779d-115">Requirements</span></span>



| <span data-ttu-id="5779d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5779d-116">Requirement</span></span> | <span data-ttu-id="5779d-117">Value</span><span class="sxs-lookup"><span data-stu-id="5779d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5779d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5779d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5779d-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5779d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5779d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5779d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5779d-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5779d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5779d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5779d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5779d-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5779d-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5779d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5779d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5779d-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="5779d-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="5779d-126">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="5779d-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





