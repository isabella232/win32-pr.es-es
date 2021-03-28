---
title: Comportamiento SRV con iconos sin asignar
description: El comportamiento de las lecturas de vista de recursos del sombreador (SRV) que impliquen mosaicos no asignados depende del nivel de compatibilidad de hardware.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268244"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a>Comportamiento SRV con iconos sin asignar

El comportamiento de las lecturas de vista de recursos del sombreador (SRV) que impliquen mosaicos no asignados depende del nivel de compatibilidad de hardware. Para ver un desglose de los requisitos, consulte el comportamiento de lectura de [los recursos en mosaico características de las capas](tiled-resources-features-tiers.md). En esta sección se resume el comportamiento ideal, que requiere el [nivel 2](tier-2.md) .

Considere una operación de filtro de textura que lee de un conjunto de textura en un SRV. Los textura que se encuentran en mosaicos no asignados contribuyen a 0 en todos los componentes que no faltan del formato (y el valor predeterminado para los componentes que faltan) en la operación de filtro general junto con las contribuciones de textura asignados. Los textura están todos ponderados y combinados juntos, independientemente de si los datos proceden de mosaicos asignados o no asignados.

Parte del hardware de nivel [2](tier-2.md) de primera generación no cumple este requisito de especificación y devuelve 0 con los valores predeterminados descritos anteriormente como resultado de filtro general si cualquier textura (con un peso distinto de cero) se encuentra en mosaicos no asignados. No se permitirá que ningún otro hardware pierda el requisito de incluir todos los textura (sin peso) en el filtro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




