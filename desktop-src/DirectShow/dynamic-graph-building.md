---
description: Creación de gráficos dinámicos
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Creación de gráficos dinámicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677125"
---
# <a name="dynamic-graph-building"></a>Creación de gráficos dinámicos

Si tiene que modificar un gráfico de filtros existente, puede detener el gráfico, realizar los cambios y reiniciar el gráfico. Este suele ser el mejor enfoque. Sin embargo, en algunas circunstancias, es posible que desee modificar un gráfico mientras se sigue ejecutando. Por ejemplo:

-   La aplicación inserta un filtro de efectos de vídeo durante la reproducción.
-   Un filtro de origen cambia el flujo medio de tipos de medios, posiblemente requiriendo un nuevo filtro de descompresión.
-   La aplicación agrega una nueva secuencia de vídeo al gráfico.

Estos son algunos ejemplos de *creación de gráficos dinámicos*, un término que cubre cualquier tipo de cambio en un gráfico de filtro mientras el gráfico continúa ejecutándose. Una aplicación o un filtro del gráfico pueden iniciar la creación de gráficos dinámicos. Se pueden realizar tres escenarios distintos:

-   [Cambios en el formato dinámico](dynamic-format-changes.md): un filtro puede cambiar los formatos de la secuencia en el nivel más bajo, sin necesidad de quitar o reemplazar ningún filtro.
-   [Reconexión dinámica](dynamic-reconnection.md): cambiar el gráfico agregando o quitando filtros.
-   [Cadenas de filtro](filter-chains.md): agregar, quitar y controlar cadenas de filtros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de DirectShow](about-directshow.md)
</dt> </dl>

 

 



