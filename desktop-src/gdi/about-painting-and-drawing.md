---
description: Casi todas las aplicaciones usan la pantalla para mostrar los datos que manipulan.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: Acerca de pintar y dibujar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc0f121ebb2dc87a5cc2a8d767788eef691712c2e03366ef88e74e8ca1b00087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038363"
---
# <a name="about-painting-and-drawing"></a>Acerca de pintar y dibujar

Casi todas las aplicaciones usan la pantalla para mostrar los datos que manipulan. Una aplicación pinta imágenes, dibuja figuras y escribe texto para que el usuario pueda ver los datos a medida que se crean, editan e imprimen. Microsoft Windows proporciona una amplia compatibilidad para pintar y dibujar, pero, debido a la naturaleza de los sistemas operativos multitarea, las aplicaciones deben colaborar entre sí al acceder a la pantalla.

Para mantener todas las aplicaciones funcionando sin problemas y de forma cooperativa, el sistema administra todos los resultados en la pantalla. Las aplicaciones usan Windows como dispositivo de salida principal en lugar de la propia pantalla. El sistema proporciona contextos de dispositivo que se corresponden de forma única con las ventanas. Las aplicaciones usan contextos de dispositivo para mostrar para dirigir su salida a las ventanas especificadas. Dibujar en una ventana (dirigir la salida a ella) evita que una aplicación interfiera con la salida de otras aplicaciones y permite que las aplicaciones coexistan entre sí mientras se siguen aprovechando al máximo las funcionalidades gráficas del sistema.

-   [Cuándo dibujar en una ventana](when-to-draw-in-a-window.md)
-   [El mensaje \_ WM PAINT](the-wm-paint-message.md)
-   [Dibujo sin el mensaje \_ WM PAINT](drawing-without-the-wm-paint-message.md)
-   [Sistema de coordenadas de ventana](window-coordinate-system.md)
-   [Regiones de ventana](window-regions.md)
-   [Fondo de la ventana](window-background.md)
-   [Minimizado Windows](minimized-windows.md)
-   [Cambio de tamaño Windows](resized-windows.md)
-   [Área no cliente](nonclient-area.md)
-   [Región de actualización de ventana secundaria](child-window-update-region.md)
-   [Mostrar dispositivos](display-devices.md)
-   [Bloqueo de actualización de ventana](window-update-lock.md)
-   [Rectángulo delimitador acumulado](accumulated-bounding-rectangle.md)

 

 



