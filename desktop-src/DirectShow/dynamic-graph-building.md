---
description: Creación Graph dinámica
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Creación Graph dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c7296b95bc97461eb5a16ee577acb4bd267ee1a25f9be357a00fef7d4bdba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652795"
---
# <a name="dynamic-graph-building"></a>Creación Graph dinámica

Si necesita modificar un gráfico de filtros existente, puede detenerlo, realizar los cambios y reiniciarlo. Este suele ser el mejor enfoque. Sin embargo, en algunas circunstancias, es posible que quiera modificar un gráfico mientras todavía se está ejecutando. Por ejemplo:

-   La aplicación inserta un filtro de efectos de vídeo durante la reproducción.
-   Un filtro de origen cambia los tipos de medios de secuencia media, lo que posiblemente requiera un nuevo filtro de descompresión.
-   La aplicación agrega una nueva secuencia de vídeo al gráfico.

Todos estos son ejemplos de creación *de grafos* dinámicos, un término que cubre cualquier tipo de cambio en un gráfico de filtro mientras el gráfico continúa ejeciendo. La creación de grafos dinámicos se puede iniciar mediante una aplicación o mediante un filtro en el gráfico. Son posibles tres escenarios distintos:

-   [Cambios de formato dinámico:](dynamic-format-changes.md)un filtro puede cambiar los formatos de midstream, sin necesidad de quitar o reemplazar ningún filtro.
-   [Reconexión dinámica:](dynamic-reconnection.md)cambio del gráfico mediante la adición o eliminación de filtros.
-   [Cadenas de](filter-chains.md)filtro: agregar, quitar y controlar cadenas de filtros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de DirectShow](about-directshow.md)
</dt> </dl>

 

 



