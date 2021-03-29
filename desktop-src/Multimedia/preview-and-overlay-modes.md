---
title: Modos de vista previa y superposición
description: Modos de vista previa y superposición
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- Mensaje WM_CAP_SET_PREVIEW
- capPreview (macro)
- Mensaje WM_CAP_SET_PREVIEWRATE
- capPreviewRate (macro)
- Mensaje WM_CAP_SET_SCALE
- capPreviewScale (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4dc293587160d950856fccb15709a11e9533bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994115"
---
# <a name="preview-and-overlay-modes"></a><span data-ttu-id="cb9bb-109">Modos de vista previa y superposición</span><span class="sxs-lookup"><span data-stu-id="cb9bb-109">Preview and Overlay Modes</span></span>

<span data-ttu-id="cb9bb-110">Un controlador de captura puede implementar dos métodos para ver una secuencia de vídeo entrante: modo de vista previa y modo de superposición.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-110">A capture driver can implement two methods for viewing an incoming video stream: preview mode and overlay mode.</span></span> <span data-ttu-id="cb9bb-111">Si un controlador de captura implementa ambos métodos, el usuario puede elegir el método que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-111">If a capture driver implements both methods, the user can choose which method to use.</span></span>

<span data-ttu-id="cb9bb-112">El modo de vista previa transfiere fotogramas digitalizados del hardware de captura a la memoria del sistema y, a continuación, muestra los fotogramas digitalizados en la ventana de captura mediante funciones de la interfaz de dispositivo gráfico (GDI).</span><span class="sxs-lookup"><span data-stu-id="cb9bb-112">Preview mode transfers digitized frames from the capture hardware to system memory and then displays the digitized frames in the capture window by using graphics device interface (GDI) functions.</span></span> <span data-ttu-id="cb9bb-113">Es posible que las aplicaciones disminuyan la velocidad de vista previa cuando la ventana primaria pierde el foco y aumentan la velocidad de vista previa cuando la ventana primaria gana el foco.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-113">Applications might decrease the preview rate when the parent window loses focus, and increase the preview rate when the parent window gains focus.</span></span> <span data-ttu-id="cb9bb-114">Esta acción mejora la capacidad de respuesta del sistema general porque la operación de vista previa es intensiva en el procesador.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-114">This action improves general system responsiveness because the preview operation is processor intensive.</span></span>

<span data-ttu-id="cb9bb-115">Hay tres mensajes para controlar la operación de vista previa.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-115">There are three messages to control the preview operation.</span></span>

-   <span data-ttu-id="cb9bb-116">Use el mensaje de [**\_ \_ \_ vista previa de límite de Cap de WM**](wm-cap-set-preview.md) para habilitar o deshabilitar el modo de vista previa mediante el envío de la (o la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) ) a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-116">Use the [**WM\_CAP\_SET\_PREVIEW**](wm-cap-set-preview.md) message to enable or disable preview mode by sending the (or the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro) to a capture window.</span></span>
-   <span data-ttu-id="cb9bb-117">Use el [**mensaje \_ \_ \_ PREVIEWRATE del conjunto de límites de WM**](wm-cap-set-previewrate.md) (o la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) ) para establecer la velocidad a la que se muestran los fotogramas en el modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-117">Use the [**WM\_CAP\_SET\_PREVIEWRATE**](wm-cap-set-previewrate.md) message (or the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro) to set the rate at which frames are displayed in preview mode</span></span>
-   <span data-ttu-id="cb9bb-118">Use el mensaje de escala del conjunto de Cap de WM (o la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) ) para habilitar o deshabilitar el escalado del vídeo de vista previa. [**\_ \_ \_**](wm-cap-set-scale.md)</span><span class="sxs-lookup"><span data-stu-id="cb9bb-118">Use the [**WM\_CAP\_SET\_SCALE**](wm-cap-set-scale.md) message (or the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro) to enable or disable scaling of the preview video.</span></span>

<span data-ttu-id="cb9bb-119">Cuando se habilitan la vista previa y el escalado, el fotograma de vídeo capturado se ajusta a las dimensiones de la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-119">When preview and scaling are both enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="cb9bb-120">Al habilitar el modo de vista previa se deshabilita automáticamente el modo de superposición.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-120">Enabling preview mode automatically disables overlay mode.</span></span>

<span data-ttu-id="cb9bb-121">El modo de superposición es una función de hardware que muestra el contenido del búfer de captura en el monitor sin usar recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-121">Overlay mode is a hardware function that displays the contents of the capture buffer on the monitor without using CPU resources.</span></span> <span data-ttu-id="cb9bb-122">Puede habilitar y deshabilitar el modo de superposición enviando el mensaje de [**\_ \_ \_ superposición de conjunto de Cap de WM**](wm-cap-set-overlay.md) (o la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) ) a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-122">You can enable and disable overlay mode by sending the [**WM\_CAP\_SET\_OVERLAY**](wm-cap-set-overlay.md) message (or the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro) to a capture window.</span></span> <span data-ttu-id="cb9bb-123">Al habilitar el modo de superposición, se deshabilita automáticamente el modo vista previa.</span><span class="sxs-lookup"><span data-stu-id="cb9bb-123">Enabling overlay mode automatically disables preview mode.</span></span>

<span data-ttu-id="cb9bb-124">También puede establecer la posición de desplazamiento del fotograma de vídeo en el área cliente de la ventana de captura para el modo de vista previa o el modo de superposición enviando el mensaje de desplazamiento del conjunto de límites de WM (o la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) ) a una ventana de captura. [**\_ \_ \_**](wm-cap-set-scroll.md)</span><span class="sxs-lookup"><span data-stu-id="cb9bb-124">You can also set the scroll position of the video frame within the client area of the capture window for preview mode or overlay mode by sending the [**WM\_CAP\_SET\_SCROLL**](wm-cap-set-scroll.md) message (or the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro) to a capture window.</span></span>

 

 




