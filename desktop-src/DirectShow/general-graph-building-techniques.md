---
description: Técnicas de Graph-Building generales
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Técnicas de Graph-Building generales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061159"
---
# <a name="general-graph-building-techniques"></a>Técnicas de Graph-Building generales

Cada DirectShow aplicación se inicia mediante la creación de un gráfico de filtros. A medida que lea los temas de información general de DirectShow documentación, verá que la mayoría empieza por describir qué tipo de gráfico de filtro necesita. En algunos casos, hay un método o un objeto auxiliar diseñado específicamente para compilar ese tipo de grafo. Por ejemplo, el [objeto DVD Graph Builder](dvd-graph-builder.md) compila gráficos de reproducción de DVD. En otros casos, la aplicación debe construir el gráfico agregando filtros y conectándolos.

En esta sección se presentan algunas funciones auxiliares que implementan operaciones básicas de creación de grafos. Se pueden usar en cualquier aplicación DirectShow que necesite compilar o modificar un gráfico de filtros. Esta sección contiene los siguientes temas:

-   [Agregar un filtro por CLSID](add-a-filter-by-clsid.md)
-   [Buscar un pin no desconectado en un filtro](find-an-unconnected-pin-on-a-filter.md)
-   [Conectar Dos filtros](connect-two-filters.md)
-   [Buscar una interfaz en un filtro o anclar](find-an-interface-on-a-filter-or-pin.md)
-   [Buscar el elemento del mismo nivel de un filtro](find-a-filters-peer.md)
-   [Quitar todos los filtros de la Graph](remove-all-the-filters-in-the-graph.md)
-   [Creación de gráficos con capture Graph Builder](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas DirectShow básicas](basic-directshow-tasks.md)
</dt> <dt>

[Enumeración de dispositivos y filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Enumerar objetos en un filtro Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Inteligencia Conectar](intelligent-connect.md)
</dt> </dl>

 

 



