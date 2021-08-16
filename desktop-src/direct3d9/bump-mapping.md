---
description: La asignación de cambios es una forma especial de asignación de entorno especular o difuso que simula las reflexión de objetos con teselación fina sin necesidad de recuentos de polígonos extremadamente altos.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Asignación de protuberancias (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb10a3a01ff3b7989cd7c44f95d6980cb08a86c00b3e9a0fc02173e349d4968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805840"
---
# <a name="bump-mapping-direct3d-9"></a>Asignación de protuberancias (Direct3D 9)

La asignación de cambios es una forma especial de asignación de entorno especular o difuso que simula las reflexión de objetos con teselación fina sin necesidad de recuentos de polígonos extremadamente altos. La asignación de incrementos implementada por Direct3D se puede describir con precisión como la alteración de coordenadas de textura por píxel de los mapas de entorno especular o difuso, ya que proporciona información sobre el contorno del mapa de incrementos en términos de valores delta, que el sistema aplica a las coordenadas de textura usted y v de un mapa de entorno en la siguiente fase de textura. Los valores delta se codifican en el formato de píxel de la superficie del mapa de incrementos (consulte [Formatos de píxeles de mapa de incremento).](bump-map-pixel-formats.md)

La asignación de relieves se basa en la combinación de varias texturas. Esto significa que el dispositivo debe admitir al menos dos fases de mezcla; uno para el mapa de protuberancias y otro para un mapa de entorno. Se requiere un mínimo de tres fases de mezcla de textura para aplicar un mapa de textura base adicional, que es el caso más común. En el diagrama siguiente se muestran las relaciones entre la textura base, el mapa de protuberancias y el mapa de entorno en la cascada de mezcla de textura.

![diagrama de la textura que se mezcla en cascada](images/bumpmap-tcascade.png)

Debe preparar las fases de textura correctamente para habilitar la asignación de protuberancias. En los temas siguientes se presenta la asignación de cambios y se proporcionan detalles sobre cómo se puede usar en las aplicaciones:

-   [Formatos de píxeles de mapa de protuberancia](bump-map-pixel-formats.md)
-   [Fórmulas de asignación de protuberancias](bump-mapping-formulas.md)
-   [Uso de la asignación de protuberancias](using-bump-mapping.md)

Direct3D no admite de forma nativa mapas de altura; son simplemente un formato cómodo en el que almacenar y visualizar datos de contorno. La aplicación puede almacenar información de contorno en cualquier formato o incluso generar un mapa de cambios de procedimientos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 



