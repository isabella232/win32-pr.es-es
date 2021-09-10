---
title: Parent-Child interacción de la ventana de Parent-Child
description: Parent-Child interacción de la ventana de Parent-Child
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372427"
---
# <a name="parent-child-window-interaction"></a>Parent-Child interacción de la ventana de Parent-Child

Algunos mensajes de nivel de sistema, como [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE,**](/windows/desktop/gdi/wm-querynewpalette)solo se envían a las ventanas de nivel superior y superpuestas. Si una ventana de captura es una ventana secundaria, su elemento primario debe reenviar estos mensajes.

De forma similar, si la ventana primaria cambia de tamaño, es posible que tenga que enviar mensajes de notificación a la ventana de captura. Por el contrario, si las dimensiones del vídeo capturado cambian, es posible que la ventana de captura tenga que enviar mensajes de notificación a la ventana primaria. La manera más sencilla de administrar esto es mantener siempre las dimensiones de la ventana de captura iguales al tamaño de la secuencia de vídeo capturada, notificando al elemento primario cada vez que cambian estas dimensiones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de Windows](capture-windows.md)
</dt> </dl>

 

 