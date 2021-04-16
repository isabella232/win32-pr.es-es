---
description: El modelo Direct3D Light cubre la iluminación ambiente, difuso, especular y emisor.
ms.assetid: cf870c89-4be0-4b95-92aa-ec7bcdc6d9dd
title: Matemáticas de iluminación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683e320788d720883702ebfa56941b1a3a5cf090
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494573"
---
# <a name="mathematics-of-lighting-direct3d-9"></a>Matemáticas de iluminación (Direct3D 9)

El modelo Direct3D Light cubre la iluminación ambiente, difuso, especular y emisor. Esta es la flexibilidad suficiente para resolver una amplia gama de situaciones de iluminación. Se hace referencia a la cantidad total de luz de una escena como iluminación global y se calcula con la siguiente ecuación.


```
Global Illumination = Ambient Light + Diffuse Light + Specular Light + Emissive Light 
```



La [iluminación ambiente (Direct3D 9)](ambient-lighting.md) es una iluminación constante. Es constante en todas las direcciones y colorea todos los píxeles de un objeto. Es rápido calcular pero deja objetos que parezcan planos e impropios. Para ver cómo Direct3D calcula la iluminación ambiente, vea iluminación ambiente (Direct3D 9).

La [iluminación difusa (Direct3D 9)](diffuse-lighting.md) depende tanto de la dirección luminosa como de la superficie del objeto normal. Varía en la superficie de un objeto como resultado de la dirección de la luz cambiante y del vector de numeración de superficie cambiante. Se tarda más tiempo en calcular la iluminación difusa porque cambia para cada vértice del objeto; sin embargo, la ventaja de utilizarlo es que sombrea objetos y les proporciona profundidad tridimensional (3D). Para ver cómo se calcula la iluminación difusa en Direct3D, vea iluminación difusa (Direct3D 9).

La [iluminación especular (Direct3D 9)](specular-lighting.md) identifica los reflejos especulares brillantes que se producen cuando la luz alcanza una superficie de objeto y se refleja de nuevo hacia la cámara. Es más intenso que la luz difusa y se cae más rápidamente en la superficie del objeto. Se tarda más tiempo en calcular la iluminación especular que la iluminación difusa; sin embargo, la ventaja de utilizarla es que agrega un detalle significativo a una superficie. Para ver cómo se calcula la iluminación especular en Direct3D, vea iluminación especular (Direct3D 9).

La [iluminación emisor (Direct3D 9)](emissive-lighting.md) es una luz que emite un objeto. por ejemplo, un resplandor. Para ver cómo se calcula la iluminación emisor en Direct3D, vea iluminación de emisor (Direct3D 9).

La iluminación realista puede realizarse aplicando cada uno de estos tipos de iluminación a una escena 3D. Los valores calculados para los componentes de ambiente, emisor y difuso se muestran como el color de vértice difuso; el valor del componente de iluminación especular se genera como el color del vértice especular. Los valores de las luces de ambiente, difusas y especulares se pueden ver afectados por la atenuación y el factor destacados de una luz determinada. Para obtener más información sobre cómo funciona la atenuación, vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).

Para lograr un efecto de iluminación más realista, agregue más luces. sin embargo, la escena tarda más tiempo en representarse. Para lograr todos los efectos que un diseñador desea, algunos juegos usan más potencia de CPU de la que suele estar disponible. En este caso, es habitual reducir el número de cálculos de iluminación a un mínimo mediante mapas de iluminación y mapas de entorno para agregar iluminación a una escena mientras se usan mapas de textura.

La iluminación se calcula en el espacio de la cámara. Para ver cómo se calculan las transformaciones de iluminación, vea [transformaciones del espacio de la cámara (Direct3D 9)](camera-space-transformations.md). La iluminación optimizada se puede calcular en el espacio del modelo cuando existen condiciones especiales: los vectores normales ya están normalizados (D3DRS \_ NORMALIZENORMALS es true), no se necesita la combinación de vértices, las matrices de transformación son ortogonales y así sucesivamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Luces y materiales](lights-and-materials.md)
</dt> </dl>

 

 



