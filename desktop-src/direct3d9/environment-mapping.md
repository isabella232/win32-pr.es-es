---
description: La asignación de entorno es una técnica que simula superficies altamente reflectantes sin usar el seguimiento de rayos.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Asignación de entorno (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a07d53028e200d273206f149ea12c07afa6dbc4ad47f8232e64cddf7582a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122232"
---
# <a name="environment-mapping-direct3d-9"></a>Asignación de entorno (Direct3D 9)

La asignación de entorno es una técnica que simula superficies altamente reflectantes sin usar el seguimiento de rayos. En la práctica, la asignación de entorno aplica un mapa de textura especial que contiene una imagen de la escena que rodea un objeto al propio objeto. El resultado se aproxima a la apariencia de una superficie reflectante, lo suficientemente cercana como para aterse el ojo, sin incurrir en ninguno de los cálculos complejos implicados en el seguimiento de rayos.

En la ilustración siguiente se muestra un tipo de asignación de entorno denominada asignación de entorno esférica. Para obtener más información, consulte [Asignación de entorno esférica.](spherical-environment-mapping.md)

![ilustración de una cafetera con una textura aplicada que refleja el entorno](images/spheremapped-teapot.png)

La cafetera de esta imagen parece reflejar su entorno; se trata realmente de una textura que se aplica al objeto . Dado que la asignación de entorno usa una textura, combinada con coordenadas de textura calculadas especialmente, se puede realizar en tiempo real.

En esta sección se proporciona información sobre cómo realizar dos tipos comunes de asignación de entorno con Direct3D. Hay muchos tipos de asignación de entorno en uso en todo el sector gráfico, pero los temas siguientes tienen como destino las dos formas más comunes: asignación de entorno cúbico y asignación de entorno esférica.

-   [Asignación de entorno cúbica](cubic-environment-mapping.md)
-   [Asignación de entorno esférica](spherical-environment-mapping.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 



