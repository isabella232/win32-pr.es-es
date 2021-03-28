---
title: Cambio del tamaño de los grupos de iconos
description: Use la API de ID3D11DeviceContext2 ResizeTilePool para aumentar el tamaño de un grupo de mosaicos si la aplicación necesita más espacio de trabajo para los recursos en mosaico asignados a él o para reducir si se necesita menos espacio.
ms.assetid: 529E874E-650B-4BFD-97F6-E66E743564A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86368da46f7c2219f42b5ecbc122b79fee19e72c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903178"
---
# <a name="tile-pool-resizing"></a>Cambio del tamaño de los grupos de iconos

Use la API [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) para aumentar el tamaño de un grupo de mosaicos si la aplicación necesita más espacio de trabajo para los recursos en mosaico asignados a él o para reducir si se necesita menos espacio. Otra opción para las aplicaciones es asignar grupos de mosaicos adicionales para los nuevos recursos en mosaico. Sin embargo, si un único recurso en mosaico necesita más espacio que el disponible inicialmente en el grupo de mosaicos, el crecimiento del grupo de mosaicos es una buena opción. Un recurso en mosaico no puede tener asignaciones en varios grupos de mosaicos al mismo tiempo.

Cuando se aumenta un grupo de mosaicos, el controlador de pantalla agrega iconos adicionales al final a través de una o varias asignaciones nuevas. Este desglose en las asignaciones no es visible para la aplicación. La memoria existente en el grupo de mosaicos se deja intacta y las asignaciones de recursos en mosaico existentes en esa memoria permanecen intactas.

Cuando se reduce un grupo de mosaicos, los mosaicos se quitan del final. Los mosaicos se quitan incluso por debajo del tamaño de asignación inicial, hasta 0, lo que significa que no se pueden realizar nuevas asignaciones más allá del nuevo tamaño. Sin embargo, las asignaciones existentes más allá del final del nuevo tamaño permanecen intactas y utilizables. El controlador de pantalla mantendrá la memoria siempre que permanezcan las asignaciones a cualquier parte de las asignaciones que el controlador utiliza para la memoria del grupo de mosaicos. Si después de reducir la cantidad de memoria se mantiene activa, ya que las asignaciones de iconos apuntan a ella y, a continuación, el grupo de mosaicos vuelve a crecer (en cualquier cantidad), la memoria existente se reutiliza en primer lugar antes de que se produzcan asignaciones adicionales para dar servicio al tamaño de la operación de crecimiento.

Para poder ahorrar memoria, una aplicación no solo debe reducir un grupo de mosaicos sino también quitar o reasignar las asignaciones existentes más allá del final del nuevo tamaño de grupo de mosaicos más pequeño.

El hecho de reducir (y quitar asignaciones) no produce necesariamente un ahorro de memoria inmediato. La liberación de memoria depende de la granularidad de las asignaciones subyacentes del controlador de la pantalla para el grupo de mosaicos. Cuando la reducción es suficiente para que una asignación de controlador de pantalla no se use, el controlador de pantalla puede liberarla. Si se aumentó un grupo de mosaicos, la reducción de los tamaños anteriores (y la eliminación o reasignación de las asignaciones de iconos correspondientes) es más probable que se produzca un ahorro de memoria, aunque no se garantiza en el caso de que los tamaños no se alineen exactamente con los tamaños de asignación subyacentes elegidos por el controlador de pantalla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mapas en un grupo de iconos](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




