---
description: Simulación de Graph building con GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simulación de Graph building con GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375203"
---
# <a name="simulating-graph-building-with-graphedit"></a>Simulación de Graph building con GraphEdit

DirectShow proporciona una utilidad de depuración denominada GraphEdit, que puede usar para crear y probar gráficos de filtro.

GraphEdit es una herramienta visual para crear gráficos de filtro. Con GraphEdit, puede experimentar con un gráfico de filtro antes de escribir cualquier código de aplicación. También puede cargar un gráfico de filtro que crea la aplicación para comprobar que la aplicación está creando el gráfico correcto. Si desarrolla un filtro personalizado, GraphEdit proporciona una manera rápida de probarlo: basta con cargar un gráfico con el filtro personalizado e intentar ejecutar el gráfico. Si no está familiarizado con DirectShow, GraphEdit es una buena manera de familiarizarse con los gráficos de filtro y la arquitectura DirectShow filtros.

En la ilustración siguiente se muestra cómo GraphEdit representa un gráfico de filtro simple.

![gráfico de filtro simple en graphedit](images/gedit09.png)

Cada filtro se representa como un rectángulo. Los cuadrados más pequeños a lo largo de los bordes de los filtros representan alfileres. Los pines de entrada están en el lado izquierdo del filtro y los pines de salida están en el lado derecho. Las flechas representan las conexiones entre los pines.

Con GraphEdit, puede:

-   Cree y modifique gráficos de filtro mediante una interfaz visual, arrastrar y colocar.
-   Simulación de llamadas mediante programación para compilar un gráfico.
-   Ejecute, pause, detenga y busque un grafo.
-   Vea qué filtros están registrados en el equipo y vea la información del Registro para cada filtro.
-   Ver páginas de propiedades de filtro.
-   Ver los tipos de medios de las conexiones de anclado.

Esta sección contiene los siguientes temas:

-   [Uso de GraphEdit](using-graphedit.md)
-   [Cargar un Graph desde un proceso externo](loading-a-graph-from-an-external-process.md)
-   [Guardar un filtro Graph un archivo GraphEdit](saving-a-filter-graph-to-a-graphedit-file.md)
-   [Carga de un archivo GraphEdit mediante programación](loading-a-graphedit-file-programmatically.md)
-   [Formato de archivo GraphEdit](graphedit-file-format.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DirectShow](using-directshow.md)
</dt> </dl>

 

 



