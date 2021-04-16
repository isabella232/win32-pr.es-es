---
description: Simular la compilación de gráficos con GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simular la compilación de gráficos con GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495227"
---
# <a name="simulating-graph-building-with-graphedit"></a>Simular la compilación de gráficos con GraphEdit

DirectShow proporciona una utilidad de depuración denominada GraphEdit, que puede usar para crear y probar gráficos de filtros.

GraphEdit es una herramienta visual para crear gráficos de filtros. Con GraphEdit, puede experimentar con un gráfico de filtros antes de escribir código de aplicación. También puede cargar un gráfico de filtro que cree la aplicación, para comprobar que la aplicación está compilando el gráfico correcto. Si desarrolla un filtro personalizado, GraphEdit proporciona una forma rápida de probarla: simplemente cargue un grafo con el filtro personalizado y pruebe a ejecutar el gráfico. Si no está familiarizado con DirectShow, GraphEdit es una buena manera de familiarizarse con los gráficos de filtro y la arquitectura de DirectShow.

En la ilustración siguiente se muestra cómo GraphEdit representa un gráfico de filtro simple.

![gráfico de filtro simple en GraphEdit](images/gedit09.png)

Cada filtro se representa como un rectángulo. Los cuadrados más pequeños a lo largo de los bordes de los filtros representan PIN. Los pines de entrada están en el lado izquierdo del filtro y los pin de salida están en el lado derecho. Las flechas representan las conexiones entre los pines.

Con GraphEdit, puede:

-   Cree y modifique gráficos de filtro con una interfaz visual, de arrastrar y colocar.
-   Simular llamadas mediante programación para compilar un grafo.
-   Ejecutar, pausar, detener y buscar un grafo.
-   Vea qué filtros están registrados en el equipo y vea la información del registro para cada filtro.
-   Ver las páginas de propiedades de filtro.
-   Ver los tipos de medios de las conexiones del PIN.

Esta sección contiene los siguientes temas:

-   [Usar GraphEdit](using-graphedit.md)
-   [Cargar un grafo desde un proceso externo](loading-a-graph-from-an-external-process.md)
-   [Guardar un gráfico de filtro en un archivo GraphEdit](saving-a-filter-graph-to-a-graphedit-file.md)
-   [Cargar un archivo GraphEdit mediante programación](loading-a-graphedit-file-programmatically.md)
-   [Formato de archivo GraphEdit](graphedit-file-format.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar DirectShow](using-directshow.md)
</dt> </dl>

 

 



