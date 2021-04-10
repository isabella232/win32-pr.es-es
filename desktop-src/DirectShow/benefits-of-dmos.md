---
description: Ventajas de DMOs
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Ventajas de DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274770"
---
# <a name="benefits-of-dmos"></a>Ventajas de DMOs

DMOs ofrecen las siguientes ventajas:

-   Suelen ser más pequeñas y más sencillas que los filtros de DirectShow, ya que admiten menos funcionalidad.
-   Son más flexibles que los filtros de DirectShow porque no requieren un gráfico de filtros. Puede usarlos con DirectShow cuando necesite los servicios que proporciona DirectShow, como la sincronización, la conexión inteligente, el control automático del flujo de datos y la administración de subprocesos. Los clientes que no necesitan estos servicios pueden acceder a DMOs directamente.
-   DMOs siempre realiza el procesamiento de datos sincrónicos, lo que elimina muchos de los problemas de subprocesos que debe tener en cuenta si escribe un filtro.
-   A diferencia de los códecs ACM y VCM tradicionales, los DMOs se basan en el modelo de objetos componentes (COM), por lo que se pueden extender a través de **QueryInterface**.
-   DMOs admite un modelo de streaming más generalizado que los códecs ACM o VCM. Al igual que los filtros DirectShow, DMOs puede admitir varias entradas y varias salidas.

Por estos motivos, ahora se recomienda DMOs como solución para escribir codificadores, descodificadores y efectos de audio. También son posibles muchos otros escenarios, en función de las necesidades de la aplicación.

Diferencias entre DMOs y filtros de DirectShow

Los filtros de DirectShow no funcionan fuera de un gráfico de filtros de DirectShow. En DirectShow, el administrador de gráficos de filtros media entre la aplicación y los filtros. Los filtros de DirectShow realizan la mayor parte del trabajo necesario para transmitir datos, entre los que se incluyen:

-   Asignación de búferes.
-   Negociar tipos de medios y conexiones con otros filtros.
-   Insertar datos a través del gráfico de filtro.
-   Envío de eventos al administrador de gráficos de filtro.
-   Sincronización de varios subprocesos.

En cambio, una DMO no realiza ninguna de estas acciones. En su lugar, estos tipos de tareas son responsabilidad del cliente mediante DMO. El cliente asigna búferes, los rellena con datos y los entrega a DMO. DMO procesa los datos y el cliente recupera los búferes de salida resultantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de DMOs](about-dmos.md)
</dt> </dl>

 

 



