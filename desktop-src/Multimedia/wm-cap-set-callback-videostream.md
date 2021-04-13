---
title: Mensaje de WM_CAP_SET_CALLBACK_VIDEOSTREAM (VFW. h)
description: El \_ \_ \_ \_ mensaje de Videostream de devolución de llamada de devoluciones de Cap de WM establece una función de devolución de llamada en la aplicación.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_VIDEOSTREAM de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421945"
---
# <a name="wm_cap_set_callback_videostream-message"></a><span data-ttu-id="4d271-104">\_Mensaje de \_ \_ Videostream de devolución de llamada de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="4d271-104">WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM message</span></span>

<span data-ttu-id="4d271-105">El mensaje de **\_ \_ \_ \_ Videostream de devolución de llamada de devoluciones de Cap de WM** establece una función de devolución de llamada en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d271-105">The **WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="4d271-106">AVICap llama a este procedimiento durante la captura de streaming cuando se rellena un búfer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4d271-106">AVICap calls this procedure during streaming capture when a video buffer is filled.</span></span> <span data-ttu-id="4d271-107">Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) .</span><span class="sxs-lookup"><span data-stu-id="4d271-107">You can send this message explicitly or by using the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="4d271-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d271-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d271-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="4d271-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="4d271-110">Puntero a la función de devolución de llamada de flujo de vídeo, de tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="4d271-110">Pointer to the video-stream callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="4d271-111">Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada de flujo de vídeo instalada previamente.</span><span class="sxs-lookup"><span data-stu-id="4d271-111">Specify **NULL** for this parameter to disable a previously installed video-stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d271-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d271-112">Return Value</span></span>

<span data-ttu-id="4d271-113">Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.</span><span class="sxs-lookup"><span data-stu-id="4d271-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d271-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d271-114">Remarks</span></span>

<span data-ttu-id="4d271-115">La ventana captura llama a la función de devolución de llamada antes de escribir el fotograma capturado en el disco.</span><span class="sxs-lookup"><span data-stu-id="4d271-115">The capture window calls the callback function before writing the captured frame to disk.</span></span> <span data-ttu-id="4d271-116">Esto permite que las aplicaciones modifiquen el marco si se desea.</span><span class="sxs-lookup"><span data-stu-id="4d271-116">This allows applications to modify the frame if desired.</span></span>

<span data-ttu-id="4d271-117">Si se usa una función de devolución de llamada de secuencia de vídeo para la captura de streaming, el procedimiento debe instalarse antes de iniciar la sesión de captura y debe permanecer habilitado mientras dure la sesión.</span><span class="sxs-lookup"><span data-stu-id="4d271-117">If a video stream callback function is used for streaming capture, the procedure must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="4d271-118">Se puede deshabilitar después de que finalice la captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="4d271-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d271-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d271-119">Requirements</span></span>



| <span data-ttu-id="4d271-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d271-120">Requirement</span></span> | <span data-ttu-id="4d271-121">Value</span><span class="sxs-lookup"><span data-stu-id="4d271-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4d271-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d271-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4d271-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4d271-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4d271-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d271-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4d271-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4d271-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4d271-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d271-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d271-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d271-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d271-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d271-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d271-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="4d271-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4d271-130">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="4d271-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





