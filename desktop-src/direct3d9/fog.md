---
description: Agregar niebla a una escena 3D puede mejorar el realismo, proporcionar Ambiance o establecer un ambiente, y los artefactos ocultos a veces se producen cuando la geometría distante entra en la vista.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714677"
---
# <a name="fog-direct3d-9"></a>Niebla (Direct3D 9)

Agregar niebla a una escena 3D puede mejorar el realismo, proporcionar Ambiance o establecer un ambiente, y los artefactos ocultos a veces se producen cuando la geometría distante entra en la vista. Direct3D admite dos modelos de niebla, la niebla de píxeles y la niebla de vértice, cada uno con sus propias características e interfaz de programación.

En esencia, la niebla se implementa mezclando el color de los objetos de una escena con un color de niebla elegido según la profundidad de un objeto en una escena o su distancia desde el punto de vista. A medida que los objetos crecen más lejos, su color original se mezcla más y más con el color de niebla elegido, lo que crea la ilusión de que el objeto está siendo cada vez más oculto por partículas diminutas flotantes en la escena. En la ilustración siguiente se muestra una escena representada sin niebla y una escena similar representada con niebla habilitada.

![Ilustración de la misma escena con y sin niebla](images/fogcomp.png)

En esta ilustración, la escena de la izquierda tiene un horizonte claro, más allá del que no hay ningún escenario visible, aunque sería visible en el mundo real. La escena de la derecha oculta el horizonte mediante el uso de un color de niebla idéntico al color de fondo, lo que hace que los polígonos parezcan atenuados en la distancia. Mediante la combinación de efectos de niebla discretos con el diseño de escenas creativa, puede Agregar el ambiente y suavizar el color de los objetos de una escena.

Direct3D proporciona dos maneras de agregar niebla a una escena: niebla de píxeles y niebla de vértice, con el nombre de cómo se aplican los efectos de niebla. Para obtener más información, consulte [niebla de píxeles (Direct3D 9)](pixel-fog.md) y [niebla de vértice (Direct3D 9)](vertex-fog.md). En Resumen, la niebla de píxel (también llamada niebla de tabla) se implementa en el controlador de dispositivo y la niebla de vértices se implementa en el motor de iluminación de Direct3D. Una aplicación puede implementar la niebla con un sombreador de vértices y la niebla de píxeles simultáneamente si se desea.

> [!Note]  
> Independientemente de si usa la niebla de píxeles o de vértices, la aplicación debe proporcionar una matriz de proyección compatible para asegurarse de que los efectos de niebla se aplican correctamente. Esta restricción se aplica incluso a las aplicaciones que no usan el motor de transformación y luz de Direct3D. Para obtener más información sobre cómo puede proporcionar una matriz adecuada, vea [transformación de proyección (Direct3D 9)](projection-transform.md).

 

En los siguientes temas se presenta la niebla y se presenta información sobre el uso de varias características de niebla en aplicaciones de Direct3D.

-   [Fórmulas de niebla (Direct3D 9)](fog-formulas.md)
-   [Parámetros de niebla (Direct3D 9)](fog-parameters.md)
-   [Combinación de niebla (Direct3D 9)](fog-blending.md)
-   [Color de niebla (Direct3D 9)](fog-color.md)
-   [Niebla de vértices (Direct3D 9)](vertex-fog.md)
-   [Niebla de píxeles (Direct3D 9)](pixel-fog.md)

La combinación de niebla se controla mediante Estados de representación; no forma parte de la canalización de píxeles programable.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación en Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



