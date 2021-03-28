---
description: Antes de pintar, el sistema debe preparar el dispositivo de pantalla para las operaciones de dibujo.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Mostrar dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984990"
---
# <a name="display-devices"></a>Mostrar dispositivos

Antes de pintar, el sistema debe preparar el dispositivo de pantalla para las operaciones de dibujo. Un contexto de dispositivo de pantalla define un conjunto de objetos gráficos y sus atributos asociados, así como los modos gráficos que afectan a la salida. El sistema prepara cada contexto de dispositivo de presentación para la salida en una ventana, estableciendo los objetos de dibujo, los colores y los modos de la ventana en lugar del dispositivo de pantalla. Cuando la aplicación proporciona el contexto de mostrar el dispositivo a través de llamadas a funciones GDI, GDI usa la información en el contexto para generar la salida en la ventana especificada sin intrusión en otras ventanas u otras partes de la pantalla.

El sistema proporciona cinco tipos de contextos de dispositivo de pantalla.



| Tipo                                           | Significado                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [normal](common-display-device-contexts.md)   | Permite dibujar en el área de cliente de una ventana especificada.                                                                                                        |
| [class](class-display-device-contexts.md)     | Permite dibujar en el área de cliente de una ventana especificada.                                                                                                        |
| [parent](parent-display-device-contexts.md)   | Permite dibujar en cualquier parte de la ventana. Aunque el contexto de dispositivo primario también permite dibujar en la ventana primaria, no está diseñado para usarse de esta manera. |
| [private](private-display-device-contexts.md) | Permite dibujar en el área de cliente de una ventana especificada.                                                                                                        |
| [periodo](window-display-device-contexts.md)   | Permite dibujar en cualquier parte de la ventana.                                                                                                                          |



 

El sistema proporciona un contexto de dispositivo común, de clase, primario o privado a una ventana basada en el tipo de contexto de dispositivo de pantalla especificado en el estilo de clase de la ventana. El sistema proporciona un contexto de dispositivo de ventana solo cuando la aplicación solicita explícitamente uno, por ejemplo, mediante una llamada a la función [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) . En todos los casos, una aplicación puede usar la función [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) para determinar qué ventana representa un DC de visualización actualmente.

En esta sección se proporciona información sobre los temas siguientes.

-   [Mostrar caché de contexto de dispositivo](display-device-context-cache.md)
-   [Mostrar valores predeterminados de contexto de dispositivo](display-device-context-defaults.md)
-   [Contextos de dispositivo de pantalla comunes](common-display-device-contexts.md)
-   [Contextos de dispositivo de pantalla privada](private-display-device-contexts.md)
-   [Contextos de dispositivo de pantalla primaria](parent-display-device-contexts.md)
-   [La clase muestra contextos de dispositivo](class-display-device-contexts.md)
-   [Ventana Mostrar contextos de dispositivo](window-display-device-contexts.md)
-   [Contextos de dispositivo de pantalla primaria](parent-display-device-contexts.md)

 

 



