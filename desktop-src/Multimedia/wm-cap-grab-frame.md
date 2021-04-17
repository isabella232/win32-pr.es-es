---
title: Mensaje de WM_CAP_GRAB_FRAME (VFW. h)
description: El \_ mensaje del \_ \_ marco de captación de Cap de WM recupera y muestra un único fotograma del controlador de captura. Después de la captura, la superposición y la vista previa están deshabilitadas. Puede enviar este mensaje explícitamente o mediante la macro capGrabFrame.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- Mensaje de WM_CAP_GRAB_FRAME de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd91ce767ad86ddac002bb216420b604883d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491146"
---
# <a name="wm_cap_grab_frame-message"></a><span data-ttu-id="31799-106">\_Mensaje de \_ marco de captura de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="31799-106">WM\_CAP\_GRAB\_FRAME message</span></span>

<span data-ttu-id="31799-107">El mensaje del **\_ \_ \_ marco de captación de Cap de WM** recupera y muestra un único fotograma del controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="31799-107">The **WM\_CAP\_GRAB\_FRAME** message retrieves and displays a single frame from the capture driver.</span></span> <span data-ttu-id="31799-108">Después de la captura, la superposición y la vista previa están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="31799-108">After capture, overlay and preview are disabled.</span></span> <span data-ttu-id="31799-109">Puede enviar este mensaje explícitamente o mediante la macro [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) .</span><span class="sxs-lookup"><span data-stu-id="31799-109">You can send this message explicitly or by using the [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
```



## <a name="return-value"></a><span data-ttu-id="31799-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31799-110">Return Value</span></span>

<span data-ttu-id="31799-111">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="31799-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="31799-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31799-112">Remarks</span></span>

<span data-ttu-id="31799-113">Para obtener información sobre la instalación de funciones de devolución de llamada, consulte los mensajes de [**\_ error de devolución de \_ \_ llamada \_ set Cap de WM**](wm-cap-set-callback-error.md) y del marco de [**\_ \_ devolución de \_ llamada \_ de WM**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="31799-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="31799-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31799-114">Requirements</span></span>



| <span data-ttu-id="31799-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="31799-115">Requirement</span></span> | <span data-ttu-id="31799-116">Value</span><span class="sxs-lookup"><span data-stu-id="31799-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="31799-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31799-117">Minimum supported client</span></span><br/> | <span data-ttu-id="31799-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="31799-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="31799-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31799-119">Minimum supported server</span></span><br/> | <span data-ttu-id="31799-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="31799-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="31799-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31799-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="31799-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="31799-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31799-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="31799-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31799-124">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="31799-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="31799-125">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="31799-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





