---
title: Comportamiento UAV con iconos sin asignar
description: El comportamiento de las lecturas y escrituras de la vista de acceso desordenado (UAV) depende del nivel de compatibilidad de hardware.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9909f8faecd3345761ae26e60835c77aae9ab3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993981"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a>Comportamiento UAV con iconos sin asignar

El comportamiento de las lecturas y escrituras de la vista de acceso desordenado (UAV) depende del nivel de compatibilidad de hardware. Para ver un desglose de los requisitos, consulte el comportamiento general de lectura y escritura para [los niveles de características de los recursos en mosaico](tiled-resources-features-tiers.md). En esta sección se resume el comportamiento ideal.

Las operaciones del sombreador que leen de un mosaico no asignado en una UAV devuelven 0 en todos los componentes que no faltan del formato y el valor predeterminado para los componentes que faltan.

Las operaciones del sombreador que intentan escribir en un mosaico no asignado no provocan que se escriba nada en el área no asignada (mientras se escribe en un área asignada). Esta definición ideal para el control de escritura no es necesaria en el [nivel 2](tier-2.md); las escrituras en mosaicos no asignados pueden acabar en una memoria caché que las lecturas posteriores podrían recogerse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




