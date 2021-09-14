---
description: Dynamic Graph Building
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Dynamic Graph Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061216"
---
# <a name="dynamic-graph-building"></a>Dynamic Graph Building

Si necesita modificar un gráfico de filtros existente, puede detener el gráfico, realizar los cambios y reiniciar el gráfico. Este suele ser el mejor enfoque. Sin embargo, en algunas circunstancias, es posible que quiera modificar un gráfico mientras todavía se está ejecutando. Por ejemplo:

-   La aplicación inserta un filtro de efectos de vídeo durante la reproducción.
-   Un filtro de origen cambia los tipos de medios de la secuencia media, lo que posiblemente requiera un nuevo filtro de descompresión.
-   La aplicación agrega una nueva secuencia de vídeo al gráfico.

Todos estos son ejemplos de *creación* dinámica de grafos, un término que abarca cualquier tipo de cambio en un gráfico de filtro mientras el gráfico continúa ejeciendo. La creación de grafos dinámicos se puede iniciar mediante una aplicación o mediante un filtro en el gráfico. Son posibles tres escenarios distintos:

-   [Cambios de formato dinámico:](dynamic-format-changes.md)un filtro puede cambiar los formatos de midstream, sin necesidad de quitar o reemplazar ningún filtro.
-   [Reconexión dinámica:](dynamic-reconnection.md)cambio del gráfico mediante la adición o eliminación de filtros.
-   [Cadenas de](filter-chains.md)filtro: agregar, quitar y controlar cadenas de filtros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de DirectShow](about-directshow.md)
</dt> </dl>

 

 



