---
title: El Administrador de ventanas de escritorio
description: .
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73167b762a9952eb508f09e70f3d4183b3b7a018
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357051"
---
# <a name="the-desktop-window-manager"></a>El Administrador de ventanas de escritorio

Antes de Windows Vista, un programa de Windows dibujaría directamente en la pantalla. En otras palabras, el programa escribiría directamente en el búfer de memoria que muestra la tarjeta de vídeo. Este enfoque puede producir artefactos visuales si una ventana no se vuelve a dibujar correctamente. Por ejemplo, si el usuario arrastra una ventana sobre otra ventana y la ventana inferior no vuelve a dibujarse lo suficiente rápidamente, la ventana de nivel superior puede dejar un rastro:

![captura de pantalla que muestra los artefactos Repaint.](images/graphics04.png)

El rastro se debe a que las ventanas se dibujan en la misma área de memoria. A medida que se arrastra la ventana de nivel superior, se debe volver a dibujar la ventana siguiente. Si el repintado es demasiado lento, provoca los artefactos mostrados en la imagen anterior.

Windows Vista ha cambiado fundamentalmente el modo en que se dibujan las ventanas, introduciendo el Administrador de ventanas de escritorio (DWM). Cuando DWM está habilitado, una ventana ya no se dibuja directamente en el búfer de pantalla. En su lugar, cada ventana se dibuja en un búfer de memoria fuera de la pantalla, también denominado *superficie fuera* de la pantalla. A continuación, el DWM compone estas superficies en la pantalla.

![diagrama que muestra cómo el DWM compone el escritorio.](images/graphics05.png)

DWM proporciona varias ventajas con respecto a la antigua arquitectura de gráficos.

-   Menos mensajes Repaint. Cuando una ventana está obstruida por otra ventana, no es necesario volver a dibujar la ventana obstruida.
-   Artefactos reducidos. Anteriormente, arrastrar una ventana podía crear artefactos visuales, tal como se describe.
-   Efectos visuales. Dado que DWM se encarga de componer la pantalla, puede representar áreas translúcidas y borrosas de la ventana.
-   Escalado automático para altos ppp. Aunque el escalado no es la manera ideal de administrar valores altos de PPP, se trata de una reserva viable para aplicaciones más antiguas que no se diseñaron para la configuración de PPP alta. (Volveremos a este tema más adelante, en la sección de [PPP y Device-Independent píxeles](dpi-and-device-independent-pixels.md)).
-   Vistas alternativas. El DWM puede usar las superficies de la ocultación de varias formas interesantes. Por ejemplo, el DWM es la tecnología que subyace a Windows Flip 3D, las miniaturas y las transiciones animadas.

Sin embargo, tenga en cuenta que no se garantiza que el DWM esté habilitado. Es posible que la tarjeta gráfica no admita los requisitos del sistema DWM y que los usuarios puedan deshabilitar DWM a través del panel de control **propiedades del sistema** . Esto significa que el programa no debe basarse en el comportamiento de repintado de DWM. Pruebe el programa con DWM deshabilitado para asegurarse de que se vuelve a dibujar correctamente.

## <a name="next"></a>Siguientes

[Modo retenido frente al modo inmediato](retained-mode-versus-immediate-mode.md)

 

 




