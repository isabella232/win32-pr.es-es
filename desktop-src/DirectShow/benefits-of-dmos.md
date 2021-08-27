---
description: Ventajas de las DDO
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Ventajas de las DDO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b13a9ef7f91446d03732b935648b689ab65a33c9d10dcfca26051d9284404db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103375"
---
# <a name="benefits-of-dmos"></a>Ventajas de las DDO

Las DDO ofrecen las siguientes ventajas:

-   Por lo general, son más pequeños y más sencillos que DirectShow, porque admiten menos funcionalidad.
-   Son más flexibles que DirectShow filtros porque no requieren un gráfico de filtros. Puede usarlos con DirectShow cuando necesite los servicios que proporciona DirectShow, como la sincronización, la conexión inteligente, el control automático del flujo de datos y la administración de subprocesos. Los clientes que no necesitan estos servicios pueden acceder directamente a las DDO.
-   Las DDO siempre realizan un procesamiento de datos sincrónico, lo que elimina muchos de los problemas de subprocesos que debe tener en cuenta si escribe un filtro.
-   A diferencia de los códecs ACM y VCM tradicionales, las DDO se basan en el modelo de objetos componentes (COM), por lo que se pueden extender a través **de QueryInterface**.
-   Las DDO admiten un modelo de streaming más generalizado que los códecs ACM o VCM. Al DirectShow filtros, las DDO pueden admitir varias entradas y varias salidas.

Por estos motivos, ahora se recomiendan las DDO como solución para escribir codificadores, descodificadores y efectos de audio. Muchos otros escenarios también son posibles, en función de las necesidades de la aplicación.

Diferencias entre las DDO y DirectShow filtros

DirectShow filtros no pueden funcionar fuera de un gráfico DirectShow filtro. En DirectShow, filter Graph Manager media entre la aplicación y los filtros. DirectShow filtros hacen la mayor parte del trabajo necesario para transmitir datos, incluidos:

-   Asignación de búferes.
-   Negociación de tipos de medios y conexiones a otros filtros.
-   Insertar datos a través del gráfico de filtros.
-   Envío de eventos al administrador de Graph filtro.
-   Sincronizar varios subprocesos.

Por el contrario, DMO realiza ninguna de estas cosas. En su lugar, estos tipos de tareas son responsabilidad del cliente mediante el DMO. El cliente asigna búferes, los rellena con datos y los entrega al DMO. El DMO procesa los datos y el cliente recupera los búferes de salida resultantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las DDO](about-dmos.md)
</dt> </dl>

 

 



