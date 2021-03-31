---
title: Mensaje de WM_CAP_SEQUENCE (VFW. h)
description: El mensaje de secuencia de Cap de WM \_ inicia la \_ captura de audio y vídeo de streaming a un archivo. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSequence.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- Mensaje de WM_CAP_SEQUENCE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996535"
---
# <a name="wm_cap_sequence-message"></a><span data-ttu-id="5bdae-105">Mensaje de secuencia de \_ Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="5bdae-105">WM\_CAP\_SEQUENCE message</span></span>

<span data-ttu-id="5bdae-106">El mensaje de **\_ \_ secuencia de Cap de WM** inicia la captura de audio y vídeo de streaming a un archivo.</span><span class="sxs-lookup"><span data-stu-id="5bdae-106">The **WM\_CAP\_SEQUENCE** message initiates streaming video and audio capture to a file.</span></span> <span data-ttu-id="5bdae-107">Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) .</span><span class="sxs-lookup"><span data-stu-id="5bdae-107">You can send this message explicitly or by using the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro.</span></span>


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="5bdae-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bdae-108">Return Value</span></span>

<span data-ttu-id="5bdae-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5bdae-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="5bdae-110">Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="5bdae-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bdae-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bdae-111">Remarks</span></span>

<span data-ttu-id="5bdae-112">Si desea modificar los parámetros que controlan la captura de streaming, use el mensaje de configuración de la secuencia de definición de Cap de WM antes de iniciar la captura. [**\_ \_ \_ \_**](wm-cap-set-sequence-setup.md)</span><span class="sxs-lookup"><span data-stu-id="5bdae-112">If you want to alter the parameters controlling streaming capture, use the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message prior to starting the capture.</span></span>

<span data-ttu-id="5bdae-113">De forma predeterminada, la ventana de captura no permite que otras aplicaciones sigan ejecutándose durante la captura.</span><span class="sxs-lookup"><span data-stu-id="5bdae-113">By default, the capture window does not allow other applications to continue running during capture.</span></span> <span data-ttu-id="5bdae-114">Para invalidar esto, establezca el miembro **fYield** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) en **true** o instale una función de devolución de llamada yield.</span><span class="sxs-lookup"><span data-stu-id="5bdae-114">To override this, either set the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to **TRUE**, or install a yield callback function.</span></span>

<span data-ttu-id="5bdae-115">Durante la captura de streaming, la ventana de captura puede emitir notificaciones de forma opcional a la aplicación de tipos específicos de condiciones.</span><span class="sxs-lookup"><span data-stu-id="5bdae-115">During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions.</span></span> <span data-ttu-id="5bdae-116">Para instalar los procedimientos de devolución de llamada para estas notificaciones, use los siguientes mensajes:</span><span class="sxs-lookup"><span data-stu-id="5bdae-116">To install callback procedures for these notifications, use the following messages:</span></span>

-   [<span data-ttu-id="5bdae-117">**\_error de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="5bdae-117">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="5bdae-118">**\_Estado de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="5bdae-118">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="5bdae-119">**\_rendimiento de \_ devolución de llamada de conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="5bdae-119">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="5bdae-120">**\_secuencia de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="5bdae-120">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="5bdae-121">**\_WAVESTREAM de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="5bdae-121">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a><span data-ttu-id="5bdae-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bdae-122">Requirements</span></span>



| <span data-ttu-id="5bdae-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bdae-123">Requirement</span></span> | <span data-ttu-id="5bdae-124">Value</span><span class="sxs-lookup"><span data-stu-id="5bdae-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5bdae-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bdae-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5bdae-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5bdae-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5bdae-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bdae-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5bdae-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5bdae-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5bdae-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bdae-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bdae-130"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bdae-130"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bdae-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bdae-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bdae-132">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="5bdae-132">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="5bdae-133">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="5bdae-133">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





