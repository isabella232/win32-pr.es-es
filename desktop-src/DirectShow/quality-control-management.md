---
description: Quality-Control Management
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Quality-Control Management
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824410b697a29ee73fc269748595fdcae91d054a161561b282536a05dcf92ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747715"
---
# <a name="quality-control-management"></a>Quality-Control Management

El control de calidad es un mecanismo para ajustar la velocidad del flujo de datos a través del gráfico de filtro en respuesta al rendimiento en tiempo de ejecución. Si un filtro de representador recibe demasiados datos o demasiados datos, puede enviar un *mensaje de calidad*. El mensaje de calidad solicita un ajuste en la velocidad de datos. De forma predeterminada, los mensajes de calidad viajan en sentido ascendente desde el representador hasta que llegan a un filtro que puede responder (si los hay). Una aplicación también puede implementar un administrador de calidad personalizado. En ese caso, el representador pasa mensajes de calidad directamente al administrador de calidad de la aplicación.

Este artículo contiene los temas siguientes.

-   [Mensajes de calidad](quality-messages.md)
-   [Control de calidad predeterminado](default-quality-control.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Datos Flow para desarrolladores de filtros](data-flow-for-filter-developers.md)
</dt> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



