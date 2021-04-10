---
description: La asignación de rugosidad es una forma especial de asignación de entorno especular o difusor que simula los reflejos de objetos con una teselación precisa sin necesidad de recuentos de polígonos extremadamente altos.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Asignación de rugosidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dba4621568f595eae965941168ad6930e183f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153382"
---
# <a name="bump-mapping-direct3d-9"></a>Asignación de rugosidad (Direct3D 9)

La asignación de rugosidad es una forma especial de asignación de entorno especular o difusor que simula los reflejos de objetos con una teselación precisa sin necesidad de recuentos de polígonos extremadamente altos. La asignación de rugosidad implementada por Direct3D se puede describir con precisión como Perturbation de coordenadas de textura por píxel de las asignaciones de entorno especulares o difusas, ya que proporciona información sobre el contorno del mapa de rugosidad en términos de valores Delta, que el sistema aplica a las coordenadas de textura de ti y v de un mapa de entorno en la siguiente fase de textura. Los valores Delta se codifican en el formato de píxel de la superficie del mapa de rugosidad (vea [formatos de píxeles de mapa de rugosidad](bump-map-pixel-formats.md)).

La asignación de rugosidad se basa en la combinación de varias texturas. Esto significa que el dispositivo debe admitir al menos dos fases de fusión; uno para el mapa de rugosidad y otro para un mapa de entorno. Se requiere un mínimo de tres fases de fusión de texturas para aplicar un mapa de textura base adicional, que es el caso más común. En el diagrama siguiente se muestran las relaciones entre la textura base, el mapa de rugosidad y el mapa de entorno en cascada de fusión de texturas.

![diagrama de la mezcla en cascada de la combinación de texturas](images/bumpmap-tcascade.png)

Debe preparar las fases de textura correctamente para habilitar la asignación de rugosidad. En los siguientes temas se presenta la asignación de rugosidad y se proporcionan detalles sobre cómo se puede usar en las aplicaciones:

-   [Formatos de píxeles de mapa de rugosidad](bump-map-pixel-formats.md)
-   [Fórmulas de asignación de rugosidad](bump-mapping-formulas.md)
-   [Usar la asignación de rugosidad](using-bump-mapping.md)

Direct3D no admite de forma nativa mapas de altura; son simplemente un formato cómodo en el que se almacenan y visualizan los datos del perfil. La aplicación puede almacenar información de perfil en cualquier formato o incluso generar un mapa de rugosidad de procedimientos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 



