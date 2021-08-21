---
title: Comportamiento UAV con iconos sin asignar
description: El comportamiento de las lecturas y escrituras de la vista de acceso no ordenado (UAV) depende del nivel de compatibilidad con hardware.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed676403e5eb1fdc838ac080b8be530b5004e6734fedc5674664f4d75304ee37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857665"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a>Comportamiento UAV con iconos sin asignar

El comportamiento de las lecturas y escrituras de la vista de acceso no ordenado (UAV) depende del nivel de compatibilidad con hardware. Para ver un desglose de los requisitos, consulte comportamiento general de lectura y escritura para niveles de características [de recursos en mosaico.](tiled-resources-features-tiers.md) En esta sección se resume el comportamiento ideal.

Las operaciones de sombreador que leen de un icono no asignado en un UAV devuelven 0 en todos los componentes que no faltan del formato y el valor predeterminado para los componentes que faltan.

Las operaciones de sombreador que intentan escribir en un icono no asignado no hacen que no se escriba nada en el área no asignada (mientras las escrituras en un área asignada prosiga). Esta definición ideal para el control de escritura no es necesaria para [el nivel 2;](tier-2.md) Las escrituras en iconos no asignados pueden acabar en una caché que las lecturas posteriores podrían recoger.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




