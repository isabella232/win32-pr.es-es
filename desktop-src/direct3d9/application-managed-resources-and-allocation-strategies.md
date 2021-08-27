---
description: Los recursos administrados de búfer de vértices o búfer de índice no se pueden declarar dinámicos especificando D3DUSAGE \_ DYNAMIC en el momento de la creación.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed recursos y estrategias de asignación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86eabccde7fef025c952c869a30fdeff8cf5316ceb0316b513692175d8581a01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119435"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a>Application-Managed recursos y estrategias de asignación (Direct3D 9)

Los recursos administrados de búfer de vértices o búfer de índice no se pueden declarar dinámicos especificando D3DUSAGE \_ DYNAMIC en el momento de la creación. Esto requeriría una copia adicional para cada modificación en el contenido del búfer de vértices. Los búferes de vértice dinámicos están diseñados para representar la geometría dinámica y los datos que se extrayó de árboles con particiones de espacio binario u otras estructuras de datos de visibilidad. Esto se puede lograr mediante la asignación previa de búferes del formato deseado. A continuación, estos recursos se entregan para satisfacer las necesidades de la aplicación por parte de un administrador de recursos dentro de la aplicación. El número total de búferes de vértices dinámicos es pequeño porque una aplicación usará simultáneamente solo algunos pasos de vértice diferentes y porque solo se requiere un búfer de vértices diferente para los avances únicos. Al administrar recursos dinámicos de esta manera, asegúrese de que las demandas de alta frecuencia en los recursos no reduzcan significativamente el rendimiento de la aplicación.

Al usar recursos administrados por Direct3D y aplicaciones, asigne recursos administrados por la aplicación en la memoria predeterminada de D3DPOOL antes de crear \_ recursos administrados por Direct3D. Esto permite al administrador de memoria mantener un recuento preciso de la memoria disponible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



