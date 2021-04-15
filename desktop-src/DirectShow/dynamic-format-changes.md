---
description: Cambios en el formato dinámico
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Cambios en el formato dinámico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677126"
---
# <a name="dynamic-format-changes"></a>Cambios en el formato dinámico

Cuando dos filtros se conectan, coinciden con un tipo de medio, que describe el formato de los datos que proporcionará el filtro de nivel superior. En la mayoría de los casos, el tipo de medio es fijo para la duración de la conexión. Sin embargo, DirectShow ofrece compatibilidad limitada para los filtros con el fin de cambiar el tipo de medio. Cuando un filtro cambia los tipos de medios, se denomina *cambio de formato dinámico*. Si está escribiendo un filtro de DirectShow, debe tener en cuenta los mecanismos para los cambios de formato dinámico. Incluso si el filtro no admite estos cambios, debe responder correctamente si otro filtro solicita un nuevo formato.

DirectShow define varios mecanismos distintos para los cambios de formato dinámico, según el estado del gráfico de filtro y el tipo de cambio necesario.

-   Si se detiene el gráfico, los pin pueden volver a conectarse y negociar el tipo de medio. Para obtener más información, consulte [reconexión de PIN](reconnecting-pins.md).
-   Algunos filtros pueden volver a conectar los pin incluso mientras el gráfico esté activo (en ejecución o en pausa). Para obtener más información sobre este mecanismo, vea [reconexión dinámica](dynamic-reconnection.md).

De lo contrario, si el gráfico está activo, pero los filtros en cuestión no admiten las reconexiones dinámicas de PIN, existen tres mecanismos posibles para cambiar el formato:

-   [QueryAccept (Downstream)](queryaccept--downstream.md) se usa cuando un terminal de salida propone un cambio de formato a su elemento inferior del mismo nivel, pero solo si el nuevo formato no requiere un búfer mayor.
-   [QueryAccept (upstream)](queryaccept--upstream.md) se usa cuando un PIN de entrada propone un cambio de formato a su par de nivel superior. El nuevo formato puede tener el mismo tamaño o puede ser mayor.
-   [ReceiveConnection](receiveconnection.md) se usa cuando un terminal de salida propone un cambio de formato a su par inferior y el nuevo formato requiere un búfer mayor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de los cambios de formato del representador de vídeo](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



