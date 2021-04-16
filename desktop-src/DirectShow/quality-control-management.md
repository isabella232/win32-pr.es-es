---
description: Administración de Quality-Control
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Administración de Quality-Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686270"
---
# <a name="quality-control-management"></a>Administración de Quality-Control

Control de calidad es un mecanismo para ajustar la velocidad del flujo de datos a través del gráfico de filtro en respuesta al rendimiento en tiempo de ejecución. Si un filtro de representador recibe demasiados datos o demasiado pocos, puede enviar un *mensaje de calidad*. El mensaje de calidad solicita un ajuste en la velocidad de datos. De forma predeterminada, los mensajes de calidad viajan hacia arriba desde el representador hasta que llegan a un filtro que puede responder (si lo hubiera). Una aplicación también puede implementar un administrador de calidad personalizado. En ese caso, el representador pasa los mensajes de calidad directamente al administrador de calidad de la aplicación.

Este artículo contiene los siguientes temas.

-   [Mensajes de calidad](quality-messages.md)
-   [Control de calidad predeterminado](default-quality-control.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md)
</dt> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



