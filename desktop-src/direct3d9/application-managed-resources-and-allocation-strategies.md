---
description: Los recursos de búfer de vértices administrados o de búfer de índice no se pueden declarar de forma dinámica mediante la especificación de D3DUSAGE \_ Dynamic en el momento de la creación.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed de recursos y estrategias de asignación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705257"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a>Application-Managed de recursos y estrategias de asignación (Direct3D 9)

Los recursos de búfer de vértices administrados o de búfer de índice no se pueden declarar de forma dinámica mediante la especificación de D3DUSAGE \_ Dynamic en el momento de la creación. Esto requeriría una copia adicional para cada modificación del contenido del búfer de vértices. Los búferes de vértices dinámicos están pensados para representar geometría dinámica y datos extraídos de árboles con particiones de espacio binario u otras estructuras de datos de visibilidad. Esto puede realizarse mediante la asignación previa de búferes del formato deseado. A continuación, estos recursos se empaquetan para admitir las necesidades de la aplicación por parte de un administrador de recursos dentro de la aplicación. El número total de búferes dinámicos de vértices es pequeño porque una aplicación usará simultáneamente solo unos cuantos distintos vértices y, por tanto, solo se necesita un búfer de vértices diferente para los grandes progresos. Al administrar recursos dinámicos de esta manera, asegúrese de que las demandas de alta frecuencia de los recursos no disminuyan significativamente el rendimiento de la aplicación.

Al usar recursos administrados por Direct3D y aplicaciones, asigne recursos administrados por la aplicación en la \_ memoria predeterminada de D3DPOOL antes de crear recursos administrados por Direct3D. Esto permite al administrador de memoria mantener un recuento preciso de la memoria disponible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



