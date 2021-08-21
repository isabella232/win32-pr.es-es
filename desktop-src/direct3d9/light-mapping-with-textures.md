---
description: Para que una aplicación represente de forma realista una escena 3D, debe tener en cuenta el efecto que tienen las fuentes de luz en la apariencia de la escena.
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: Asignación de luz con texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de583f7cd7f29404fd627811b0df22d584e8c752133d9e4cfc246a4b52157f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092913"
---
# <a name="light-mapping-with-textures-direct3d-9"></a>Asignación de luz con texturas (Direct3D 9)

Para que una aplicación represente de forma realista una escena 3D, debe tener en cuenta el efecto que tienen las fuentes de luz en la apariencia de la escena. Aunque técnicas como el sombreado plano y gouraud son herramientas valiosas en este sentido, pueden ser insuficientes para sus necesidades. Direct3D admite la combinación multipass y de varias texturas. Estas funcionalidades permiten a la aplicación representar escenas con una apariencia más realista que las escenas que se representan solo con técnicas de sombreado. Al aplicar uno o varios mapas claros, la aplicación puede asignar áreas de luz y sombra a sus primitivas.

Un mapa claro es una textura o un grupo de texturas que contiene información sobre la iluminación en una escena 3D. Puede almacenar la información de iluminación en los valores alfa del mapa claro, en los valores de color o en ambos.

Si implementa la asignación de luz mediante la combinación de texturas multipass, la aplicación debe representar el mapa de luz en sus primitivas en el primer paso. Debe usar un segundo paso para representar la textura base. La excepción a esto es la asignación de luz especular. En ese caso, represente primero la textura base; a continuación, agregue el mapa claro.

La combinación de varias texturas permite que la aplicación represente el mapa claro y la textura base en un solo paso. Si el hardware del usuario proporciona la combinación de varias texturas, la aplicación debe aprovecharlo al realizar la asignación de luz. Esto mejora significativamente el rendimiento de la aplicación.

Con mapas claros, una aplicación de Direct3D puede lograr diversos efectos de iluminación cuando representa primitivas. No solo puede asignar luces monocromáticas y coloreadas en una escena, sino que también puede agregar detalles como resaltados especulares e iluminación difusa.

En los temas siguientes se ofrece información sobre el uso de la combinación de texturas de Direct3D para realizar la asignación de luz.

-   [Monocromática Light Mapas (Direct3D 9)](monochrome-light-maps.md)
-   [Color Light Mapas (Direct3D 9)](color-light-maps.md)
-   [Specular Light Mapas (Direct3D 9)](specular-light-maps.md)
-   [Difuso de Mapas (Direct3D 9)](diffuse-light-maps.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mezcla de texturas](texture-blending.md)
</dt> </dl>

 

 



