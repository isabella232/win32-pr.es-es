---
title: Cambio del tamaño de los grupos de iconos
description: Use la API ResizeTilePool ID3D11DeviceContext2 para aumentar el tamaño de un grupo de mosaicos si la aplicación necesita más espacio de trabajo para la asignación de recursos en mosaico en él o para reducir si se necesita menos espacio.
ms.assetid: 529E874E-650B-4BFD-97F6-E66E743564A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86368da46f7c2219f42b5ecbc122b79fee19e72c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966871"
---
# <a name="tile-pool-resizing"></a>Cambio del tamaño de los grupos de iconos

Use la API [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) para aumentar el tamaño de un grupo de mosaicos si la aplicación necesita más espacio de trabajo para la asignación de recursos en mosaico en él o para reducir si se necesita menos espacio. Otra opción para las aplicaciones es asignar grupos de mosaicos adicionales para nuevos recursos en mosaico. Pero si un único recurso en mosaico necesita más espacio del que está disponible inicialmente en su grupo de mosaicos, el crecimiento del grupo de mosaicos es una buena opción. Un recurso en mosaico no puede tener asignaciones en varios grupos de mosaicos al mismo tiempo.

Cuando se crece un grupo de mosaicos, el controlador de pantalla agrega iconos adicionales al final mediante una o varias asignaciones nuevas. Este desglose de las asignaciones no es visible para la aplicación. La memoria existente en el grupo de mosaicos se deja intacta y las asignaciones de recursos en mosaico existentes en esa memoria permanecen intactas.

Cuando se encoge un grupo de mosaicos, los iconos se quitan del final. Los iconos se quitan incluso por debajo del tamaño de asignación inicial, hasta 0, lo que significa que no se pueden realizar nuevas asignaciones más allá del nuevo tamaño. Sin embargo, las asignaciones existentes más allá del final del nuevo tamaño permanecen intactas y se pueden usar. El controlador para mostrar conservará la memoria mientras permanezcan las asignaciones a cualquier parte de las asignaciones que el controlador usa para la memoria del grupo de mosaicos. Si después de reducir parte de la memoria se ha mantenido activo porque las asignaciones de mosaicos apuntan a ella y, a continuación, el grupo de mosaicos vuelve a crecer (en cualquier cantidad), la memoria existente se reutiliza primero antes de que se produzcan asignaciones adicionales para dar servicio al tamaño de la operación de crecimiento.

Para poder ahorrar memoria, una aplicación no solo debe reducir un grupo de mosaicos, sino también quitar o reasignar las asignaciones existentes más allá del final del nuevo tamaño de grupo de mosaicos más pequeño.

El hecho de reducir (y quitar asignaciones) no genera necesariamente un ahorro inmediato de memoria. La liberar memoria depende de la granularidad de las asignaciones subyacentes del controlador de pantalla para el grupo de mosaicos. Cuando la reducción resulta ser suficiente para que una asignación de controladores de pantalla no se utilice, el controlador de pantalla puede liberarla. Si se ha aumentado un grupo de mosaicos, es más probable que la reducción a tamaños anteriores (y la eliminación o reapping de asignaciones de mosaicos correspondientes) produjese un ahorro de memoria, aunque no se garantiza en el caso de que los tamaños no se alineen exactamente con los tamaños de asignación subyacentes elegidos por el controlador de pantalla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mapas en un grupo de iconos](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




