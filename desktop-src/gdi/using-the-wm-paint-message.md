---
description: Puede usar el mensaje WM \_ PAINT para llevar a cabo el dibujo necesario para mostrar información.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Uso del WM_PAINT mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1969d5aae7e64ad74d8070c7515daa6e9e782135ce0af54b49c7faab07f5d34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037453"
---
# <a name="using-the-wm_paint-message"></a>Uso del mensaje \_ WM PAINT

Puede usar el mensaje [**WM \_ PAINT**](wm-paint.md) para llevar a cabo el dibujo necesario para mostrar información. Dado que el sistema envía mensajes WM PAINT a la aplicación cuando se debe actualizar la ventana o cuando se solicita explícitamente una actualización, puede consolidar el código para dibujar en el procedimiento de ventana de \_ la aplicación. A continuación, puede usar este código siempre que la aplicación deba dibujar información nueva o existente.

En las secciones siguientes se muestran varias maneras de usar el mensaje \_ WM PAINT para dibujar en una ventana:

-   [Dibujo en el área cliente](drawing-in-the-client-area.md)
-   [Volver a dibujar todo el área de cliente](redrawing-the-entire-client-area.md)
-   [Volver a dibujar en la región de actualización](redrawing-in-the-update-region.md)
-   [Invalidación del área cliente](invalidating-the-client-area.md)
-   [Dibujar una ventana minimizada](drawing-a-minimized-window.md)
-   [Dibujar un fondo de ventana personalizado](drawing-a-custom-window-background.md)

 

 



