---
description: Para que una aplicación pueda representar de manera realista una escena 3D, debe tener en cuenta el efecto que tienen las fuentes de luz en la apariencia de la escena.
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: Asignación de luz con texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705233"
---
# <a name="light-mapping-with-textures-direct3d-9"></a>Asignación de luz con texturas (Direct3D 9)

Para que una aplicación pueda representar de manera realista una escena 3D, debe tener en cuenta el efecto que tienen las fuentes de luz en la apariencia de la escena. Aunque las técnicas como el sombreado plano y Gouraud son herramientas valiosas en este sentido, pueden ser insuficientes para sus necesidades. Direct3D admite Multipass y varias combinaciones de texturas. Estas funcionalidades permiten que la aplicación represente escenas con un aspecto más realista que las escenas representadas únicamente con técnicas de sombreado. Al aplicar una o más asignaciones de luz, la aplicación puede asignar áreas de luz y sombra a sus primitivas.

Un mapa ligero es una textura o un grupo de texturas que contiene información sobre la iluminación en una escena 3D. Puede almacenar la información de iluminación en los valores alfa del mapa de luz, en los valores de color, o en ambos.

Si implementa una asignación ligera mediante la combinación de texturas de Multipass, la aplicación debe representar el mapa de luz en sus primitivas en el primer paso. Debe usar un segundo paso para representar la textura base. La excepción a esto es la asignación de luz especular. En ese caso, represente primero la textura base; a continuación, agregue el mapa de luz.

La combinación de texturas múltiples permite a la aplicación representar el mapa de luz y la textura base en un paso. Si el hardware del usuario proporciona varias combinaciones de texturas, la aplicación debe aprovecharse al realizar una asignación ligera. Esto mejora significativamente el rendimiento de la aplicación.

Mediante el uso de mapas ligeros, una aplicación de Direct3D puede lograr una gran variedad de efectos de iluminación cuando representa primitivas. Puede asignar no solo luz monocroma y de color en una escena, sino que también puede agregar detalles como resaltes especulares e iluminación difusa.

En los temas siguientes se ofrece información sobre el uso de la combinación de texturas de Direct3D para realizar la asignación de luz.

-   [Mapas de luz monocroma (Direct3D 9)](monochrome-light-maps.md)
-   [Mapas de luz de color (Direct3D 9)](color-light-maps.md)
-   [Mapas de luz especular (Direct3D 9)](specular-light-maps.md)
-   [Mapas de luz difusos (Direct3D 9)](diffuse-light-maps.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de texturas](texture-blending.md)
</dt> </dl>

 

 



