---
title: Mensaje de WM_CAP_SEQUENCE_NOFILE (VFW. h)
description: El \_ mensaje nofile de la secuencia de Cap de WM inicia la captura de vídeo de \_ \_ streaming sin escribir datos en un archivo. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSequenceNoFile.
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- Mensaje de WM_CAP_SEQUENCE_NOFILE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE_NOFILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a08f470989b8000e9757c1cb81924b875b5303
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149967"
---
# <a name="wm_cap_sequence_nofile-message"></a><span data-ttu-id="6b174-105">\_ \_ Mensaje nofile de secuencia de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="6b174-105">WM\_CAP\_SEQUENCE\_NOFILE message</span></span>

<span data-ttu-id="6b174-106">El **mensaje \_ \_ \_ nofile** de la secuencia de Cap de WM inicia la captura de vídeo de streaming sin escribir datos en un archivo.</span><span class="sxs-lookup"><span data-stu-id="6b174-106">The **WM\_CAP\_SEQUENCE\_NOFILE** message initiates streaming video capture without writing data to a file.</span></span> <span data-ttu-id="6b174-107">Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) .</span><span class="sxs-lookup"><span data-stu-id="6b174-107">You can send this message explicitly or by using the [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) macro.</span></span>


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="6b174-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b174-108">Return Value</span></span>

<span data-ttu-id="6b174-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6b174-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b174-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b174-110">Remarks</span></span>

<span data-ttu-id="6b174-111">Este mensaje es útil junto con las funciones de devolución de llamada de secuencia de audio o de flujo de vídeo que permiten que la aplicación use los datos de vídeo y audio directamente.</span><span class="sxs-lookup"><span data-stu-id="6b174-111">This message is useful in conjunction with video stream or waveform-audio stream callback functions that let your application use the video and audio data directly.</span></span>

<span data-ttu-id="6b174-112">Si desea modificar los parámetros que controlan la captura de streaming, use el mensaje de configuración de la secuencia de definición de Cap de WM antes de iniciar la captura. [**\_ \_ \_ \_**](wm-cap-set-sequence-setup.md)</span><span class="sxs-lookup"><span data-stu-id="6b174-112">If you want to alter the parameters controlling streaming capture, use the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message prior to starting the capture.</span></span>

<span data-ttu-id="6b174-113">De forma predeterminada, la ventana de captura no permite que otras aplicaciones sigan ejecutándose durante la captura.</span><span class="sxs-lookup"><span data-stu-id="6b174-113">By default, the capture window does not allow other applications to continue running during capture.</span></span> <span data-ttu-id="6b174-114">Para invalidar esto, establezca el miembro **fYield** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) en **true** o instale una función de devolución de llamada yield.</span><span class="sxs-lookup"><span data-stu-id="6b174-114">To override this, either set the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to **TRUE**, or install a yield callback function.</span></span>

<span data-ttu-id="6b174-115">Durante la captura de streaming, la ventana de captura puede emitir notificaciones de forma opcional a la aplicación de tipos específicos de condiciones.</span><span class="sxs-lookup"><span data-stu-id="6b174-115">During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions.</span></span> <span data-ttu-id="6b174-116">Para instalar los procedimientos de devolución de llamada para estas notificaciones, use los siguientes mensajes:</span><span class="sxs-lookup"><span data-stu-id="6b174-116">To install callback procedures for these notifications, use the following messages:</span></span>

-   [<span data-ttu-id="6b174-117">**\_error de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b174-117">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="6b174-118">**\_Estado de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b174-118">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="6b174-119">**\_rendimiento de \_ devolución de llamada de conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b174-119">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="6b174-120">**\_secuencia de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b174-120">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="6b174-121">**\_WAVESTREAM de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b174-121">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a><span data-ttu-id="6b174-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b174-122">Requirements</span></span>



| <span data-ttu-id="6b174-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b174-123">Requirement</span></span> | <span data-ttu-id="6b174-124">Value</span><span class="sxs-lookup"><span data-stu-id="6b174-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6b174-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b174-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6b174-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6b174-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6b174-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b174-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6b174-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6b174-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6b174-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b174-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b174-130"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b174-130"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b174-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b174-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b174-132">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="6b174-132">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6b174-133">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="6b174-133">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





