---
title: Mensaje de WM_CAP_GRAB_FRAME_NOSTOP (VFW. h)
description: El \_ mensaje de \_ \_ \_ punto de interrupción del casquillo de WM rellena el búfer de fotogramas con un solo fotograma sin comprimir del dispositivo de captura y lo muestra.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- Mensaje de WM_CAP_GRAB_FRAME_NOSTOP de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5073cf5eae44f564d24cd1ebb67193d8738fd77b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905490"
---
# <a name="wm_cap_grab_frame_nostop-message"></a><span data-ttu-id="3e986-104">\_Mensaje de \_ marco de captación de Cap de \_ WM \_</span><span class="sxs-lookup"><span data-stu-id="3e986-104">WM\_CAP\_GRAB\_FRAME\_NOSTOP message</span></span>

<span data-ttu-id="3e986-105">El mensaje de **\_ punto de \_ \_ \_ interrupción del casquillo de WM** rellena el búfer de fotogramas con un solo fotograma sin comprimir del dispositivo de captura y lo muestra.</span><span class="sxs-lookup"><span data-stu-id="3e986-105">The **WM\_CAP\_GRAB\_FRAME\_NOSTOP** message fills the frame buffer with a single uncompressed frame from the capture device and displays it.</span></span> <span data-ttu-id="3e986-106">A diferencia de lo que sucede con el mensaje del [**\_ \_ \_ marco de captación de Cap de WM**](wm-cap-grab-frame.md) , este mensaje no modifica el estado de superposición o vista previa.</span><span class="sxs-lookup"><span data-stu-id="3e986-106">Unlike with the [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message, the state of overlay or preview is not altered by this message.</span></span> <span data-ttu-id="3e986-107">Puede enviar este mensaje explícitamente o mediante la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) .</span><span class="sxs-lookup"><span data-stu-id="3e986-107">You can send this message explicitly or by using the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="3e986-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e986-108">Return Value</span></span>

<span data-ttu-id="3e986-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3e986-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e986-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e986-110">Remarks</span></span>

<span data-ttu-id="3e986-111">Para obtener información sobre la instalación de funciones de devolución de llamada, consulte los mensajes de [**\_ error de devolución de \_ \_ llamada \_ set Cap de WM**](wm-cap-set-callback-error.md) y del marco de [**\_ \_ devolución de \_ llamada \_ de WM**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="3e986-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e986-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e986-112">Requirements</span></span>



| <span data-ttu-id="3e986-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e986-113">Requirement</span></span> | <span data-ttu-id="3e986-114">Value</span><span class="sxs-lookup"><span data-stu-id="3e986-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3e986-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e986-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3e986-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3e986-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3e986-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e986-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3e986-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e986-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3e986-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e986-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e986-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e986-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e986-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e986-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e986-122">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3e986-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3e986-123">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3e986-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





