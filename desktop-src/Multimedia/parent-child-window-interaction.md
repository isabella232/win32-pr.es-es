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
# <a name="parent-child-window-interaction"></a>Interacción de la ventana de Parent-Child

Algunos mensajes de nivel de sistema, como [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), solo se envían a ventanas de nivel superior y superpuestas. Si una ventana de captura es una ventana secundaria, su elemento primario debe reenviar estos mensajes.

Del mismo modo, si la ventana primaria cambia de tamaño, es posible que tenga que enviar mensajes de notificación a la ventana de captura. Por el contrario, si las dimensiones del vídeo capturado cambian, la ventana de captura podría necesitar enviar mensajes de notificación a la ventana primaria. La manera más sencilla de administrarlo es mantener siempre las dimensiones de la ventana de captura igual al tamaño de la secuencia de vídeo capturada, notificando al primario cada vez que cambien estas dimensiones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar ventanas](capture-windows.md)
</dt> </dl>

 

 