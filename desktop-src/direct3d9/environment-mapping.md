---
description: La asignación de entorno es una técnica que simula superficies muy reflectantes sin usar el seguimiento de Ray.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Asignación de entorno (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805612"
---
# <a name="environment-mapping-direct3d-9"></a>Asignación de entorno (Direct3D 9)

La asignación de entorno es una técnica que simula superficies muy reflectantes sin usar el seguimiento de Ray. En la práctica, la asignación de entorno aplica un mapa de textura especial que contiene una imagen de la escena que rodea un objeto al propio objeto. El resultado se aproxima a la apariencia de una superficie reflectante, lo suficientemente cerca como para engañar, sin incurrir en ningún cálculo complejo implicado en el seguimiento de Ray.

En la ilustración siguiente se muestra un tipo de asignación de entorno denominada asignación de entorno esférico. Para obtener más información, consulte [asignación de entorno esférico](spherical-environment-mapping.md).

![Ilustración de un tetera con una textura aplicada que refleja el entorno](images/spheremapped-teapot.png)

El tetera de esta imagen parece reflejar su entorno; en realidad, se aplica una textura al objeto. Dado que la asignación de entorno utiliza una textura, combinada con coordenadas de textura de cálculo especial, se puede realizar en tiempo real.

En esta sección se proporciona información sobre cómo realizar dos tipos comunes de asignación de entorno con Direct3D. Hay muchos tipos de asignación de entorno en uso en toda la industria de gráficos, pero los temas siguientes se destinan a las dos formas más comunes: asignación de entorno cúbica y asignación de entorno esférico.

-   [Asignación de entorno cúbica](cubic-environment-mapping.md)
-   [Asignación de entorno esférico](spherical-environment-mapping.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 



