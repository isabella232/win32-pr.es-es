---
title: Parent-Child interacción de la ventana de Parent-Child
description: Parent-Child interacción de la ventana de Parent-Child
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b2ea050fda4cbc6ffc54e318a6a7d01e63db6ace0f1d71e3847f46b68b94ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136754"
---
# <a name="parent-child-window-interaction"></a>Parent-Child interacción de la ventana de Parent-Child

Algunos mensajes de nivel de sistema, como [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE,**](/windows/desktop/gdi/wm-querynewpalette)solo se envían a las ventanas de nivel superior y superpuestas. Si una ventana de captura es una ventana secundaria, su elemento primario debe reenviar estos mensajes.

De forma similar, si la ventana primaria cambia de tamaño, es posible que tenga que enviar mensajes de notificación a la ventana de captura. Por el contrario, si las dimensiones del vídeo capturado cambian, es posible que la ventana de captura tenga que enviar mensajes de notificación a la ventana primaria. La manera más sencilla de administrar esto es mantener siempre las dimensiones de la ventana de captura iguales al tamaño de la secuencia de vídeo capturada, notificando al elemento primario cada vez que cambian estas dimensiones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar Windows](capture-windows.md)
</dt> </dl>

 

 