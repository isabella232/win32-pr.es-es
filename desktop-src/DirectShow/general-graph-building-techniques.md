---
description: Técnicas generales de Graph-Building
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Técnicas generales de Graph-Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274631"
---
# <a name="general-graph-building-techniques"></a>Técnicas generales de Graph-Building

Cada aplicación de DirectShow se inicia mediante la creación de un gráfico de filtro. A medida que lea los temas de información general de la documentación de DirectShow, encontrará que la mayor parte de los pasos es describir el tipo de gráfico de filtro que necesita. En algunos casos, hay un método o un objeto auxiliar específicamente diseñados para compilar ese tipo de gráfico. Por ejemplo, el objeto [generador de gráficos de DVD](dvd-graph-builder.md) crea gráficos de reproducción de DVD. En otros casos, la aplicación debe construir el gráfico agregando filtros y conectándolos.

En esta sección se presentan algunas funciones auxiliares que implementan operaciones básicas de creación de gráficos. Se pueden usar en cualquier aplicación de DirectShow que necesite crear o modificar un gráfico de filtro. Esta sección contiene los siguientes temas:

-   [Agregar un filtro por CLSID](add-a-filter-by-clsid.md)
-   [Buscar un PIN no conectado en un filtro](find-an-unconnected-pin-on-a-filter.md)
-   [Conectar dos filtros](connect-two-filters.md)
-   [Buscar una interfaz en un filtro o un PIN](find-an-interface-on-a-filter-or-pin.md)
-   [Buscar el elemento del mismo nivel de un filtro](find-a-filters-peer.md)
-   [Quitar todos los filtros del gráfico](remove-all-the-filters-in-the-graph.md)
-   [Generar gráficos con el generador de gráficos de captura](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas básicas de DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[Enumerar dispositivos y filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Enumerar objetos en un gráfico de filtros](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Conexión inteligente](intelligent-connect.md)
</dt> </dl>

 

 



