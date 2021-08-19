---
title: El Administrador de ventanas de escritorio
description: El Administrador de ventanas de escritorio
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99585a75bf2b25b086f09a17a0d8d93391b1f94f5018c5d4f83f90937fde620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896894"
---
# <a name="the-desktop-window-manager"></a>El Administrador de ventanas de escritorio

Antes Windows Vista, un Windows programa se dibujaba directamente en la pantalla. En otras palabras, el programa escribiría directamente en el búfer de memoria que muestra la tarjeta de vídeo. Este enfoque puede provocar artefactos visuales si una ventana no se vuelve a dibujar correctamente. Por ejemplo, si el usuario arrastra una ventana sobre otra ventana y la ventana debajo no se vuelve a dibujar lo suficientemente rápido, la ventana superior puede dejar un final:

![captura de pantalla en la que se muestran los artefactos de repintado.](images/graphics04.png)

El final se debe a que ambas ventanas pintan en la misma área de memoria. A medida que se arrastra la ventana superior, se debe volver a dibujar la ventana debajo de ella. Si el repintado es demasiado lento, provoca los artefactos que se muestran en la imagen anterior.

Windows Vista cambió fundamentalmente la forma en que se dibujan las ventanas, al introducir Administrador de ventanas de escritorio (DWM). Cuando el DWM está habilitado, una ventana ya no se dibuja directamente en el búfer de presentación. En su lugar, cada ventana se dibuja en un búfer de memoria fuera de pantalla, también denominado *superficie fuera de pantalla*. A continuación, el DWM compone estas superficies en la pantalla.

![diagrama que muestra cómo el dwm compone el escritorio.](images/graphics05.png)

DwM proporciona varias ventajas con respecto a la arquitectura de gráficos antigua.

-   Menos mensajes de repintado. Cuando una ventana está obstruida por otra ventana, no es necesario volver a dibujarla.
-   Artefactos reducidos. Anteriormente, arrastrar una ventana podía crear artefactos visuales, como se describe.
-   Efectos visuales. Dado que dwm se encarga de componer la pantalla, puede representar áreas translúcidas y desenfoque de la ventana.
-   Escalado automático para valores altos de PPP. Aunque el escalado no es la manera ideal de controlar valores altos de PPP, es una reserva viable para aplicaciones anteriores que no se diseñaron para la configuración de valores altos de PPP. (Volveremos a este tema más adelante, en la sección [PPP y Device-Independent píxeles).](dpi-and-device-independent-pixels.md)
-   Vistas alternativas. DwM puede usar las superficies fuera de la pantalla de varias maneras interesantes. Por ejemplo, DWM es la tecnología detrás de Windows Flip 3D, miniaturas y transiciones animadas.

Sin embargo, tenga en cuenta que no se garantiza que el DWM esté habilitado. Es posible que la tarjeta gráfica no admita los requisitos del sistema DWM y que los usuarios puedan deshabilitarlo a través del panel de control **Propiedades** del sistema. Esto significa que el programa no debe basarse en el comportamiento de volver a dibujar del DWM. Pruebe el programa con DWM deshabilitado para asegurarse de que se vuelve a dibujar correctamente.

## <a name="next"></a>Siguientes

[Modo retenido frente al modo inmediato](retained-mode-versus-immediate-mode.md)

 

 




