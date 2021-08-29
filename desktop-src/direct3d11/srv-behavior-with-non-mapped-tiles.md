---
title: Comportamiento SRV con iconos sin asignar
description: El comportamiento de las lecturas de vista de recursos de sombreador (SRV) que implican iconos no asignados depende del nivel de compatibilidad con hardware.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edb1dd6e291fb1bdeb691349a74b8483773cf3fbb5a49fb2ee1a5e950fab452
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850875"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a>Comportamiento SRV con iconos sin asignar

El comportamiento de las lecturas de vista de recursos de sombreador (SRV) que implican iconos no asignados depende del nivel de compatibilidad con hardware. Para ver un desglose de los requisitos, consulte Comportamiento de lectura de los niveles [de características de recursos en mosaico.](tiled-resources-features-tiers.md) En esta sección se resume el comportamiento ideal, que [requiere el nivel 2.](tier-2.md)

Considere una operación de filtro de textura que lee de un conjunto de elementos de textura en un SRV. Los elementos de textura que se incluyen en iconos no asignados contribuyen a 0 en todos los componentes que no faltan del formato (y el valor predeterminado para los componentes que faltan) en la operación de filtro general junto con las contribuciones de los elementos de textura asignados. Todos los elementos de textura se ponderan y combinan juntos independientemente de si los datos provenían de iconos asignados o no asignados.

Algún hardware de nivel [2](tier-2.md) de primera generación no cumple este requisito de especificación y devuelve el 0 con los valores predeterminados descritos anteriormente como resultado del filtro general si algún elemento de textura (con un peso distinto de cero) se encuentra en mosaicos no asignados. No se permitirá que ningún otro hardware pierda el requisito de incluir todos los elementos de textura (peso distinto de cero) en el filtro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




