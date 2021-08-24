---
description: La adición de artefactos a una escena 3D puede mejorar el realismo, proporcionar un ambiente o establecer un ambiente, y ocultar artefactos a veces causados cuando la geometría lejana se ve.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Brumoso (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f06f9ff25c132feaed4ada291e7f063fcbfb3f4f1129cf934b43795b79b20aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026944"
---
# <a name="fog-direct3d-9"></a>Brumoso (Direct3D 9)

La adición de artefactos a una escena 3D puede mejorar el realismo, proporcionar un ambiente o establecer un ambiente, y ocultar artefactos a veces causados cuando la geometría lejana se ve. Direct3D admite dos modelos de bruma, píxeles y vértices, cada uno con sus propias características e interfaz de programación.

Básicamente, la bruma se implementa combinando el color de los objetos de una escena con un color de color de punta elegido en función de la profundidad de un objeto de una escena o su distancia desde el punto de vista. A medida que los objetos crecen más lejos, su color original se mezcla cada vez más con el color de la paleta elegido, lo que crea la sensación de que el objeto está cada vez más oculto por pequeñas partículas que flotan en la escena. En la ilustración siguiente se muestra una escena que se representa sin ningún efecto, y una escena similar que se representa con la zona habilitada.

![ilustración de la misma escena con y sin sentido](images/fogcomp.png)

En esta ilustración, la escena de la izquierda tiene un horizonte claro, más allá del cual no se puede ver ningún ambiente, aunque sea visible en el mundo real. La escena de la derecha oculta el horizonte mediante un color de color idéntico al color de fondo, lo que hace que los polígonos parezcan atenuarse a la distancia. Mediante la combinación de efectos discretos de color rojo con el diseño de escena creativo, puede agregar ambiente y suavizar el color de los objetos de una escena.

Direct3D proporciona dos maneras de agregar más sonidos a una escena: píxeles y vértices, con el nombre de cómo se aplican los efectos de efecto de color. Para obtener más información, vea [Pixel Pixel (Direct3D 9)](pixel-fog.md) y [Vertex Vertex Vertex (Direct3D 9) ( Vértices de vértice [Direct3D 9]).](vertex-fog.md) En resumen, los píxeles de píxeles , también denominados ángulos de tabla, se implementan en el controlador del dispositivo y el vértice de vértice se implementa en el motor de iluminación de Direct3D. Una aplicación puede implementar el sombreador con un sombreador de vértices y pixelar simultáneamente si lo desea.

> [!Note]  
> Independientemente de si usa píxeles o vértices de vértice, la aplicación debe proporcionar una matriz de proyección compatible para asegurarse de que los efectos de efecto de efecto de color se aplican correctamente. Esta restricción se aplica incluso a las aplicaciones que no usan el motor de iluminación y transformación de Direct3D. Para obtener más información sobre cómo puede proporcionar una matriz adecuada, vea [Projection Transform (Direct3D 9) (Transformación de proyección [Direct3D 9]).](projection-transform.md)

 

En los temas siguientes se presenta información sobre el uso de diversas características de la nube en aplicaciones de Direct3D.

-   [Fórmulas Desmaes (Direct3D 9)](fog-formulas.md)
-   [Parámetros de parámetros de parámetros de parámetros de destino (Direct3D 9)](fog-parameters.md)
-   [Blending de Blend (Direct3D 9)](fog-blending.md)
-   [Color azulado (Direct3D 9)](fog-color.md)
-   [Vértices de vértice (Direct3D 9)](vertex-fog.md)
-   [Píxeles de píxeles (Direct3D 9)](pixel-fog.md)

La mezcla de fusión se controla mediante estados de representación; no forma parte de la canalización de píxeles programable.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



