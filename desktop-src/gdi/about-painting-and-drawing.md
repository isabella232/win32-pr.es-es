---
description: Casi todas las aplicaciones usan la pantalla para mostrar los datos que manipulan.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: Acerca del dibujo y el dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997297"
---
# <a name="about-painting-and-drawing"></a>Acerca del dibujo y el dibujo

Casi todas las aplicaciones usan la pantalla para mostrar los datos que manipulan. Una aplicación pinta imágenes, dibuja figuras y escribe texto para que el usuario pueda ver los datos a medida que se crean, editan e imprimen. Microsoft Windows proporciona una amplia compatibilidad para dibujar y dibujar, pero, debido a la naturaleza de los sistemas operativos de multitarea, las aplicaciones deben cooperar entre sí al tener acceso a la pantalla.

Para mantener todas las aplicaciones en funcionamiento sin problemas y de forma cooperativa, el sistema administra todos los resultados en la pantalla. Las aplicaciones usan Windows como dispositivo de salida principal en lugar de la propia pantalla. El sistema proporciona los contextos de dispositivo de pantalla que se corresponden de forma única a las ventanas. Las aplicaciones usan contextos de dispositivo de pantalla para dirigir su salida a las ventanas especificadas. Dibujar en una ventana (dirigir la salida a ella) impide que una aplicación interfiera con la salida de otras aplicaciones y permite que las aplicaciones coexistan entre sí mientras se sigue aprovechando al máximo las capacidades de gráficos del sistema.

-   [Cuándo dibujar en una ventana](when-to-draw-in-a-window.md)
-   [Mensaje de \_ dibujo de WM](the-wm-paint-message.md)
-   [Dibujo sin el mensaje de pintura de WM \_](drawing-without-the-wm-paint-message.md)
-   [Sistema de coordenadas de ventana](window-coordinate-system.md)
-   [Regiones de ventana](window-regions.md)
-   [Fondo de la ventana](window-background.md)
-   [Ventanas minimizadas](minimized-windows.md)
-   [Ventanas cambiadas de tamaño](resized-windows.md)
-   [Área no cliente](nonclient-area.md)
-   [Región de actualización de la ventana secundaria](child-window-update-region.md)
-   [Mostrar dispositivos](display-devices.md)
-   [Bloqueo de actualización de ventana](window-update-lock.md)
-   [Rectángulo delimitador acumulado](accumulated-bounding-rectangle.md)

 

 



