---
description: Imágenes 3D tempranas generadas por el equipo, aunque por lo general son avanzadas para su tiempo, con lo que se tiende a tener un aspecto plástico brillante.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Conceptos básicos de la texturización (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696122"
---
# <a name="basic-texturing-concepts-direct3d-9"></a>Conceptos básicos de la texturización (Direct3D 9)

Imágenes 3D tempranas generadas por el equipo, aunque por lo general son avanzadas para su tiempo, con lo que se tiende a tener un aspecto plástico brillante. Carecía de los tipos de marcas, como scuffs, grietas, huellas digitales y manchas, que proporcionan a los objetos 3D una complejidad visual realista. En los últimos años, las texturas han ganado popularidad entre los desarrolladores como una herramienta para mejorar el realismo de las imágenes 3D generadas por el equipo.

En su uso cotidiano, la palabra Texture hace referencia a la suavidad o la rugosidad de un objeto. En los gráficos de equipos, sin embargo, una textura es un mapa de bits de colores de píxeles que proporcionan a un objeto la apariencia de la textura.

Dado que las texturas de Direct3D son mapas de bits, cualquier mapa de bits se puede aplicar a un primitivo de Direct3D. Por ejemplo, las aplicaciones pueden crear y manipular objetos que parezcan tener un patrón de grano de madera en ellos. Hierba, suciedad y Rocks se pueden aplicar a un conjunto de primitivas 3D que forman un máximo. El resultado es una Hillside de aspecto realista. También puede usar la texturización para crear efectos como signos a lo largo de una carretera, Rock estratos en un acantilado o la apariencia de Marble en un piso.

Además, Direct3D admite técnicas de texturización más avanzadas, como la combinación de texturas, con o sin la asignación de transparencia y ligera. Para obtener más información, vea [combinación de texturas (Direct3D 9)](texture-blending.md) y [asignación de luz con texturas (Direct3D 9)](light-mapping-with-textures.md).

Si la aplicación crea un dispositivo de capa de abstracción de hardware (HAL) o un dispositivo de software, puede usar texturas de 8, 16, 24, 32, 64 o 128 bits.

En los temas siguientes se incluye información adicional.

-   [Modos de direccionamiento de textura (Direct3D 9)](texture-addressing-modes.md)
-   [Regiones desfasadas de textura (Direct3D 9)](texture-dirty-regions.md)
-   [Paletas de texturas (Direct3D 9)](texture-palettes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 



