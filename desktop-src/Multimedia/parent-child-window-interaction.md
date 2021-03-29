---
title: Interacción de la ventana de Parent-Child
description: Interacción de la ventana de Parent-Child
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790546"
---
# <a name="parent-child-window-interaction"></a><span data-ttu-id="1de63-103">Interacción de la ventana de Parent-Child</span><span class="sxs-lookup"><span data-stu-id="1de63-103">Parent-Child Window Interaction</span></span>

<span data-ttu-id="1de63-104">Algunos mensajes de nivel de sistema, como [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), solo se envían a ventanas de nivel superior y superpuestas.</span><span class="sxs-lookup"><span data-stu-id="1de63-104">Some system-level messages, such as [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), are sent only to top-level and overlapped windows.</span></span> <span data-ttu-id="1de63-105">Si una ventana de captura es una ventana secundaria, su elemento primario debe reenviar estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="1de63-105">If a capture window is a child window, its parent must forward these messages.</span></span>

<span data-ttu-id="1de63-106">Del mismo modo, si la ventana primaria cambia de tamaño, es posible que tenga que enviar mensajes de notificación a la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="1de63-106">Similarly, if the parent window changes size, it might need to send notification messages to the capture window.</span></span> <span data-ttu-id="1de63-107">Por el contrario, si las dimensiones del vídeo capturado cambian, la ventana de captura podría necesitar enviar mensajes de notificación a la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="1de63-107">Conversely, if the dimensions of the captured video change, the capture window might need to send notification messages to the parent window.</span></span> <span data-ttu-id="1de63-108">La manera más sencilla de administrarlo es mantener siempre las dimensiones de la ventana de captura igual al tamaño de la secuencia de vídeo capturada, notificando al primario cada vez que cambien estas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="1de63-108">The simplest way to manage this is to always keep the capture window dimensions equal to the size of the captured video stream, notifying the parent whenever these dimensions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1de63-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1de63-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1de63-110">Capturar ventanas</span><span class="sxs-lookup"><span data-stu-id="1de63-110">Capture Windows</span></span>](capture-windows.md)
</dt> </dl>

 

 