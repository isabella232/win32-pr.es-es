---
description: Cambios de formato dinámico
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Cambios de formato dinámico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061220"
---
# <a name="dynamic-format-changes"></a>Cambios de formato dinámico

Cuando se conectan dos filtros, se ponen de acuerdo en un tipo de medio, que describe el formato de los datos que el filtro ascendente va a entregar. En la mayoría de los casos, el tipo de medio se fija durante la conexión. Sin embargo, DirectShow ofrece compatibilidad limitada con filtros para cambiar el tipo de medio. Cuando un filtro cambia los tipos de medios, se denomina cambio *de formato dinámico.* Si está escribiendo un filtro DirectShow, debe tener en cuenta los mecanismos para los cambios de formato dinámico. Incluso si el filtro no admite estos cambios, debe responder correctamente si otro filtro solicita un nuevo formato.

DirectShow define varios mecanismos distintos para los cambios de formato dinámico, según el estado del gráfico de filtro y el tipo de cambio necesario.

-   Si se detiene el gráfico, los pines pueden volver a conectarse y volver a negociar el tipo de medio. Para obtener más información, vea [Volver a conectar los pines.](reconnecting-pins.md)
-   Algunos filtros pueden volver a conectar los pines incluso mientras el gráfico está activo (en ejecución o en pausa). Para obtener más información sobre este mecanismo, vea [Reconexión dinámica.](dynamic-reconnection.md)

De lo contrario, si el gráfico está activo, pero los filtros en cuestión no admiten reconexiones dinámicas de pin, hay tres mecanismos posibles para cambiar el formato:

-   [QueryAccept (bajada)](queryaccept--downstream.md) se usa cuando si un pin de salida propone un cambio de formato a su elemento del mismo nivel de bajada, pero solo si el nuevo formato no requiere un búfer mayor.
-   [QueryAccept (upstream) se](queryaccept--upstream.md) usa cuando un pin de entrada propone un cambio de formato a su par ascendente. El nuevo formato puede tener el mismo tamaño o puede ser mayor.
-   [ReceiveConnection](receiveconnection.md) se usa cuando un pin de salida propone un cambio de formato a su elemento del mismo nivel de bajada y el nuevo formato requiere un búfer mayor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de cambios de formato desde el representador de vídeo](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



