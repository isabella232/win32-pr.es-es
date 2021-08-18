---
description: Antes de pintar, el sistema debe preparar el dispositivo de presentación para las operaciones de dibujo.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Mostrar dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd71b943d294bf89e932f965b023ecbce7f4e594044fe96b70bb84d41a27f777
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038123"
---
# <a name="display-devices"></a>Mostrar dispositivos

Antes de pintar, el sistema debe preparar el dispositivo de presentación para las operaciones de dibujo. Un contexto de dispositivo de presentación define un conjunto de objetos gráficos y sus atributos asociados, así como los modos gráficos que afectan a la salida. El sistema prepara cada contexto de dispositivo de presentación para la salida en una ventana, estableciendo los objetos, colores y modos de dibujo para la ventana en lugar del dispositivo de visualización. Cuando la aplicación proporciona el contexto del dispositivo de presentación a través de llamadas a funciones GDI, GDI usa la información del contexto para generar la salida en la ventana especificada sin interrumpir en otras ventanas u otras partes de la pantalla.

El sistema proporciona cinco tipos de contextos de dispositivo de visualización.



| Tipo                                           | Significado                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Común](common-display-device-contexts.md)   | Permite dibujar en el área cliente de una ventana especificada.                                                                                                        |
| [class](class-display-device-contexts.md)     | Permite dibujar en el área cliente de una ventana especificada.                                                                                                        |
| [parent](parent-display-device-contexts.md)   | Permite dibujar en cualquier parte de la ventana. Aunque el contexto del dispositivo primario también permite dibujar en la ventana primaria, no está pensado para usarse de esta manera. |
| [private](private-display-device-contexts.md) | Permite dibujar en el área cliente de una ventana especificada.                                                                                                        |
| [Ventana](window-display-device-contexts.md)   | Permite dibujar en cualquier parte de la ventana.                                                                                                                          |



 

El sistema proporciona un contexto de dispositivo común, de clase, primario o privado a una ventana en función del tipo de contexto de dispositivo de presentación especificado en el estilo de clase de esa ventana. El sistema proporciona un contexto de dispositivo de ventana solo cuando la aplicación solicita explícitamente uno, por ejemplo, mediante una llamada a la [**función GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx.**](/windows/desktop/api/Winuser/nf-winuser-getdcex) En todos los casos, una aplicación puede usar la [**función WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) para determinar qué ventana representa actualmente un controlador de dominio de pantalla.

En esta sección se proporciona información sobre los temas siguientes.

-   [Mostrar caché de contexto de dispositivo](display-device-context-cache.md)
-   [Mostrar valores predeterminados de contexto de dispositivo](display-device-context-defaults.md)
-   [Contextos comunes del dispositivo de visualización](common-display-device-contexts.md)
-   [Contextos de dispositivo de pantalla privada](private-display-device-contexts.md)
-   [Contextos de dispositivos de visualización primarios](parent-display-device-contexts.md)
-   [Contextos de dispositivo de presentación de clases](class-display-device-contexts.md)
-   [Contextos de dispositivo de visualización de ventana](window-display-device-contexts.md)
-   [Contextos de dispositivos de visualización primarios](parent-display-device-contexts.md)

 

 



