---
title: Estado de la ventana de captura
description: Estado de la ventana de captura
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- Mensaje WM_CAP_GET_STATUS
- capGetStatus (macro)
- Estructura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076116"
---
# <a name="capture-window-status"></a><span data-ttu-id="ef890-106">Estado de la ventana de captura</span><span class="sxs-lookup"><span data-stu-id="ef890-106">Capture Window Status</span></span>

<span data-ttu-id="ef890-107">Puede recuperar el estado actual de una ventana de captura mediante el mensaje [**de \_ \_ \_ Estado de Cap de WM Get**](wm-cap-get-status.md) (o la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) ).</span><span class="sxs-lookup"><span data-stu-id="ef890-107">You can retrieve the current status of a capture window by using the [**WM\_CAP\_GET\_STATUS**](wm-cap-get-status.md) message (or the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro).</span></span> <span data-ttu-id="ef890-108">Este mensaje recupera una copia de la estructura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) con los valores actuales de sus miembros.</span><span class="sxs-lookup"><span data-stu-id="ef890-108">This message retrieves a copy of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure with the current values of its members.</span></span> <span data-ttu-id="ef890-109">La estructura **CAPSTATUS** contiene información relacionada con las dimensiones de la imagen, la posición de desplazamiento y si está habilitada la superposición u vista previa de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ef890-109">The **CAPSTATUS** structure contains information regarding the dimensions of the image, scroll position, and whether overlay or preview of the image is enabled.</span></span> <span data-ttu-id="ef890-110">Dado que la información representada en **CAPSTATUS** es dinámica, la aplicación debe actualizar el contenido de la estructura cada vez que el tamaño o el formato del flujo de vídeo capturado haya cambiado (por ejemplo, después de mostrar el formato de vídeo del controlador de captura).</span><span class="sxs-lookup"><span data-stu-id="ef890-110">Because the information represented in **CAPSTATUS** is dynamic, your application should refresh the contents of the structure whenever the size or format of the captured video stream might have changed (such as after displaying the video format of the capture driver).</span></span>

<span data-ttu-id="ef890-111">Cambiar las dimensiones de la ventana de captura no tiene ningún efecto en las dimensiones de la secuencia de vídeo capturada real.</span><span class="sxs-lookup"><span data-stu-id="ef890-111">Changing the dimensions of the capture window has no effect on the dimensions of the actual captured video stream.</span></span> <span data-ttu-id="ef890-112">El cuadro de diálogo formato mostrado por el controlador de dispositivo de captura de vídeo controla las dimensiones de la secuencia de vídeo capturada.</span><span class="sxs-lookup"><span data-stu-id="ef890-112">The format dialog box displayed by the video capture device driver controls the dimensions of the captured video stream.</span></span>

 

 




