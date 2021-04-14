---
description: Puede usar el mensaje de \_ pintura de WM para llevar a cabo el dibujo necesario para mostrar la información.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Usar el mensaje de WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77246e04effc74de8158aef9bfc4aaf27471c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276452"
---
# <a name="using-the-wm_paint-message"></a>Usar el mensaje de Paint de WM \_

Puede usar el mensaje [**de \_ pintura de WM**](wm-paint.md) para llevar a cabo el dibujo necesario para mostrar la información. Dado que el sistema envía \_ mensajes de WM Paint a la aplicación cuando se debe actualizar la ventana o cuando se solicita explícitamente una actualización, se puede consolidar el código para dibujar en el procedimiento de ventana de la aplicación. Después, puede usar este código cada vez que la aplicación deba dibujar información nueva o existente.

En las secciones siguientes se muestran varias formas de usar el \_ mensaje de Paint de WM para dibujar en una ventana:

-   [Dibujo en el área cliente](drawing-in-the-client-area.md)
-   [Volver a dibujar todo el área cliente](redrawing-the-entire-client-area.md)
-   [Volver a dibujar en la región de actualización](redrawing-in-the-update-region.md)
-   [Invalidar el área de cliente](invalidating-the-client-area.md)
-   [Dibujar una ventana minimizada](drawing-a-minimized-window.md)
-   [Dibujo de un fondo de ventana personalizado](drawing-a-custom-window-background.md)

 

 



