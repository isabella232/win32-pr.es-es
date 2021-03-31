---
title: Mensaje de WM_CAP_SINGLE_FRAME_CLOSE (VFW. h)
description: El \_ mensaje de cierre de trama único de Cap de WM \_ \_ \_ cierra el archivo de captura abierto por el \_ mensaje de apertura de trama único de Cap de WM \_ \_ \_ . Puede enviar este mensaje explícitamente o mediante la macro capCaptureSingleFrameClose.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- Mensaje de WM_CAP_SINGLE_FRAME_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35523476dde1c74c4a20447d7c46d5eafc5e529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803811"
---
# <a name="wm_cap_single_frame_close-message"></a><span data-ttu-id="13263-105">\_Mensaje de \_ \_ cierre de fotograma único de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="13263-105">WM\_CAP\_SINGLE\_FRAME\_CLOSE message</span></span>

<span data-ttu-id="13263-106">El mensaje de **\_ \_ \_ \_ cierre de trama único de Cap de WM** cierra el archivo de captura abierto por el mensaje de [**\_ \_ \_ \_ apertura de trama único de Cap de WM**](wm-cap-single-frame-open.md) .</span><span class="sxs-lookup"><span data-stu-id="13263-106">The **WM\_CAP\_SINGLE\_FRAME\_CLOSE** message closes the capture file opened by the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="13263-107">Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) .</span><span class="sxs-lookup"><span data-stu-id="13263-107">You can send this message explicitly or by using the [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="13263-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13263-108">Return Value</span></span>

<span data-ttu-id="13263-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="13263-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="13263-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13263-110">Remarks</span></span>

<span data-ttu-id="13263-111">Para obtener información sobre la instalación de funciones de devolución de llamada, consulte los mensajes de [**\_ error de devolución de \_ \_ llamada \_ set Cap de WM**](wm-cap-set-callback-error.md) y del marco de [**\_ \_ devolución de \_ llamada \_ de WM**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="13263-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="13263-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13263-112">Requirements</span></span>



| <span data-ttu-id="13263-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="13263-113">Requirement</span></span> | <span data-ttu-id="13263-114">Value</span><span class="sxs-lookup"><span data-stu-id="13263-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="13263-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13263-115">Minimum supported client</span></span><br/> | <span data-ttu-id="13263-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="13263-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="13263-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13263-117">Minimum supported server</span></span><br/> | <span data-ttu-id="13263-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13263-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="13263-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13263-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="13263-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="13263-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13263-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="13263-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13263-122">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="13263-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="13263-123">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="13263-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





