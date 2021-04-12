---
description: Enumerar objetos en un gráfico de filtros
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: Enumerar objetos en un gráfico de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152298"
---
# <a name="enumerating-objects-in-a-filter-graph"></a>Enumerar objetos en un gráfico de filtros

Es posible que una aplicación necesite buscar un filtro determinado en el gráfico de filtros, o incluso un PIN determinado en un filtro. Por ejemplo, podría utilizar una interfaz que expone un filtro determinado. O bien, puede crear un gráfico de filtros especializado y tener que llamar a métodos en PIN individuales para conectar los filtros. Para este propósito, DirectShow proporciona varios métodos para enumerar los objetos de un gráfico de filtro.

Los enumeradores descritos en esta sección siguen el formato estándar que utilizan las interfaces de enumeración COM. Para obtener más información, vea el tema "IEnumXXXX" en el SDK de la plataforma. Para obtener información sobre la enumeración de filtros que están registrados en el equipo del usuario, pero que aún no están en el gráfico de filtros, consulte [enumeración de dispositivos y filtros](enumerating-devices-and-filters.md).

Ese artículo contiene los siguientes temas:

-   [Enumerar filtros](enumerating-filters.md)
-   [Enumerar PIN](enumerating-pins.md)
-   [Enumerar tipos de medios](enumerating-media-types.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas básicas de DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 



