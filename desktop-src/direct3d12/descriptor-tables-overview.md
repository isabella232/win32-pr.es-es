---
title: Información general sobre tablas de descriptores
description: 'Cada tabla de descriptores almacena descriptores de uno o más tipos: SRVs, UAVe, CBVs y Samplers. Una tabla de descriptores no es una asignación de memoria; es simplemente un desplazamiento y una longitud en un montón de descriptores.'
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105185"
---
# <a name="descriptor-tables-overview"></a>Información general sobre tablas de descriptores

Cada tabla de descriptores almacena descriptores de uno o más tipos: SRVs, UAVe, CBVs y Samplers. Una tabla de descriptores no es una asignación de memoria; es simplemente un desplazamiento y una longitud en un montón de descriptores.

-   [Referencia a tablas de descriptores](#referencing-descriptor-tables)
-   [Temas relacionados](#related-topics)

## <a name="referencing-descriptor-tables"></a>Referencia a tablas de descriptores

La canalización de gráficos, a través de la firma raíz, obtiene acceso a los recursos haciendo referencia a las tablas de descriptores por índice.

Una tabla de descriptores es en realidad solo un subintervalo de un montón de descriptores. Los montones descriptores representan la asignación de memoria subyacente para una colección de descriptores. Dado que la asignación de memoria es una propiedad de la creación de un montón de descriptores, se garantiza que la definición de una tabla de descriptores fuera de uno es tan barata como identificar una región del montón en el hardware. No es necesario crear ni destruir tablas de descriptores en el nivel de API: simplemente se identifican como un desplazamiento y el tamaño de un montón cuando se hace referencia a ellos.

En realidad, una aplicación puede definir tablas de descriptores muy grandes cuando sus sombreadores quieren tener la libertad de seleccionar entre un amplio conjunto de descriptores disponibles (a menudo, hacer referencia a texturas) sobre la marcha (quizás controlado por datos materiales).

La firma raíz hace referencia a la entrada de la tabla de descriptores con una referencia al montón, la ubicación inicial de la tabla (un desplazamiento desde el inicio del montón) y la longitud (en entradas) de la tabla. En la imagen siguiente se muestran estos conceptos: los punteros de tabla del descriptor de la firma raíz y los descriptores dentro del montón del descriptor que hace referencia a los datos de búfer o textura completos en un montón de carga.

![tablas de descriptores](images/descriptor-table.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tablas de descriptores](descriptor-tables.md)
</dt> </dl>

 

 




