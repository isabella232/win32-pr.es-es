---
title: Cuadros de diálogo de vídeo
description: Cuadros de diálogo de vídeo
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- Mensaje WM_CAP_DLG_VIDEOSOURCE
- capDlgVideoSource (macro)
- Mensaje WM_CAP_DLG_VIDEOFORMAT
- capDlgVideoFormat (macro)
- Mensaje WM_CAP_DLG_VIDEODISPLAY
- capDlgVideoDisplay (macro)
- Mensaje WM_CAP_DLG_VIDEOCOMPRESSION
- capDlgVideoCompression (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665611"
---
# <a name="video-dialog-boxes"></a><span data-ttu-id="8406e-111">Cuadros de diálogo de vídeo</span><span class="sxs-lookup"><span data-stu-id="8406e-111">Video Dialog Boxes</span></span>

<span data-ttu-id="8406e-112">Cada controlador de captura puede proporcionar hasta cuatro cuadros de diálogo para controlar aspectos del proceso de captura y digitalización de vídeo, y para definir los atributos de compresión que se usan para reducir el tamaño de los datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8406e-112">Each capture driver can provide up to four dialog boxes to control aspects of the video digitization and capture process, and to define compression attributes used in reducing the size of the video data.</span></span> <span data-ttu-id="8406e-113">El contenido de estos cuadros de diálogo se define mediante el controlador de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8406e-113">The contents of these dialog boxes are defined by the video capture driver.</span></span>

<span data-ttu-id="8406e-114">El cuadro de diálogo origen de vídeo controla la selección de canales de entrada de vídeo y los parámetros que afectan a la imagen de vídeo que se está digitalizando en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="8406e-114">The Video Source dialog box controls the selection of video input channels and parameters affecting the video image being digitized in the frame buffer.</span></span> <span data-ttu-id="8406e-115">En este cuadro de diálogo se enumeran los tipos de señales que conectan el origen de vídeo con la tarjeta de captura (normalmente SVHS y las entradas compuestas) y se proporcionan controles para cambiar el matiz, el contraste o la saturación.</span><span class="sxs-lookup"><span data-stu-id="8406e-115">This dialog box enumerates the types of signals that connect the video source to the capture card (typically SVHS and composite inputs), and provides controls to change hue, contrast, or saturation.</span></span> <span data-ttu-id="8406e-116">Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje de [**\_ \_ \_ videosource Dlg Cap de WM**](wm-cap-dlg-videosource.md) (o la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) ).</span><span class="sxs-lookup"><span data-stu-id="8406e-116">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOSOURCE**](wm-cap-dlg-videosource.md) message (or the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro).</span></span>

<span data-ttu-id="8406e-117">El cuadro de diálogo formato de vídeo controla la selección de las dimensiones del fotograma de vídeo digitalizado y la profundidad de imagen, así como las opciones de compresión del vídeo capturado.</span><span class="sxs-lookup"><span data-stu-id="8406e-117">The Video Format dialog box controls selection of the digitized video frame dimensions and image-depth, and compression options of the captured video.</span></span> <span data-ttu-id="8406e-118">Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje de [**\_ \_ \_ videoformat de Cap Cap Dlg**](wm-cap-dlg-videoformat.md) (o la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ).</span><span class="sxs-lookup"><span data-stu-id="8406e-118">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro).</span></span>

<span data-ttu-id="8406e-119">El cuadro de diálogo presentación en vídeo controla la apariencia del vídeo en el monitor durante la captura.</span><span class="sxs-lookup"><span data-stu-id="8406e-119">The Video Display dialog box controls the appearance of the video on the monitor during capture.</span></span> <span data-ttu-id="8406e-120">Los controles de este cuadro de diálogo no tienen ningún efecto en los datos de vídeo digitalizados, pero podrían afectar a la presentación de la señal digitalizada.</span><span class="sxs-lookup"><span data-stu-id="8406e-120">The controls in this dialog box have no effect on the digitized video data, but they might affect the presentation of the digitized signal.</span></span> <span data-ttu-id="8406e-121">Por ejemplo, los dispositivos de captura que admiten la superposición pueden permitir la modificación del matiz y la saturación, el color de la clave o la alineación de la superposición.</span><span class="sxs-lookup"><span data-stu-id="8406e-121">For example, capture devices that support overlay might allow altering hue and saturation, key color, or alignment of the overlay.</span></span> <span data-ttu-id="8406e-122">Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje de vídeo de [**\_ \_ \_ presentación de Cap de WM Cap**](wm-cap-dlg-videodisplay.md) (o la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) ).</span><span class="sxs-lookup"><span data-stu-id="8406e-122">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) message (or the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro).</span></span>

<span data-ttu-id="8406e-123">El cuadro de diálogo compresión de vídeo controla los atributos de compresión de vídeo posteriores a la captura.</span><span class="sxs-lookup"><span data-stu-id="8406e-123">The Video Compression dialog box controls the post-capture video compression attributes.</span></span> <span data-ttu-id="8406e-124">Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje de [**\_ \_ \_ compresión**](wm-cap-dlg-videocompression.md) de vídeo del Cap de WM (o la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) ).</span><span class="sxs-lookup"><span data-stu-id="8406e-124">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) message (or the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro).</span></span>

 

 




