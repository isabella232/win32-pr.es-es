---
description: Las primeras imágenes 3D generadas por el equipo, aunque generalmente avanzadas para su tiempo, tendían a tener un aspecto de plástico brillante.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Conceptos básicos de texturing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 799504d2bb7f57952d55ca541155be09d10fed1a03a038d50d98069c2f1c1243
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952605"
---
# <a name="basic-texturing-concepts-direct3d-9"></a>Conceptos básicos de texturing (Direct3D 9)

Las primeras imágenes 3D generadas por el equipo, aunque generalmente avanzadas para su tiempo, tendían a tener un aspecto de plástico brillante. Les faltaban los tipos de marcas (como scuffs, cracks, fingerprints y smudges) que dan a los objetos 3D una complejidad visual realista. En los últimos años, las texturas han adquirido popularidad entre los desarrolladores como una herramienta para mejorar el realismo de las imágenes 3D generadas por equipos.

En su uso diario, la palabra textura hace referencia a la subilidad o aspersividad de un objeto. Sin embargo, en los gráficos de equipo, una textura es un mapa de bits de colores de píxeles que dan a un objeto la apariencia de textura.

Dado que las texturas de Direct3D son mapas de bits, cualquier mapa de bits se puede aplicar a una primitiva de Direct3D. Por ejemplo, las aplicaciones pueden crear y manipular objetos que parecen tener un patrón de grano de bosque en ellos. El pasto, las rocas y las rocas se pueden aplicar a un conjunto de primitivas 3D que forman un monte. El resultado es una visión realista. También puede usar texturing para crear efectos como signos a lo largo de una carretera, estratagenos de roca en un borde o la apariencia de la canica en un suelo.

Además, Direct3D admite técnicas de texturizado más avanzadas, como la combinación de texturas (con o sin transparencia) y la asignación de luz. Para obtener más información, vea [Mezcla de texturas (Direct3D 9)](texture-blending.md) y Asignación de luz con [texturas (Direct3D 9).](light-mapping-with-textures.md)

Si la aplicación crea un dispositivo de capa de abstracción de hardware (HAN) o un dispositivo de software, puede usar texturas de 8, 16, 24, 32, 64 o 128 bits.

En los temas siguientes se incluye información adicional.

-   [Modos de direccionamiento de textura (Direct3D 9)](texture-addressing-modes.md)
-   [Regiones de textura desaseadas (Direct3D 9)](texture-dirty-regions.md)
-   [Paletas de textura (Direct3D 9)](texture-palettes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 



