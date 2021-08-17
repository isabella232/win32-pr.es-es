---
description: El modelo de luz de Direct3D cubre la iluminación ambiental, difusa, especular y emisiva.
ms.assetid: cf870c89-4be0-4b95-92aa-ec7bcdc6d9dd
title: Matemáticas de iluminación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1c6ffa8a1142c1be40993dcd8130b4708f2b509c8a5a1f05e234d0231c3bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728340"
---
# <a name="mathematics-of-lighting-direct3d-9"></a>Matemáticas de iluminación (Direct3D 9)

El modelo de luz de Direct3D cubre la iluminación ambiental, difusa, especular y emisiva. Esta es la flexibilidad suficiente para resolver una amplia gama de situaciones de iluminación. Se hace referencia a la cantidad total de luz de una escena como iluminación global y se calcula mediante la ecuación siguiente.


```
Global Illumination = Ambient Light + Diffuse Light + Specular Light + Emissive Light 
```



[La iluminación ambiental (Direct3D 9)](ambient-lighting.md) es una iluminación constante. Es constante en todas las direcciones y colore todos los píxeles de un objeto de la misma manera. Es rápido calcular, pero deja los objetos con un aspecto plano y poco realista. Para ver cómo se calcula la iluminación ambiente mediante Direct3D, consulte Ambient Lighting (Direct3D 9) (Iluminación ambiental (Direct3D 9).

[La iluminación difusa (Direct3D 9)](diffuse-lighting.md) depende tanto de la dirección de la luz como de la superficie del objeto normal. Varía en la superficie de un objeto como resultado de la dirección de la luz cambiante y el vector numérico de la superficie cambiante. Se tarda más tiempo en calcular la iluminación difusa porque cambia para cada vértice de objeto; sin embargo, la ventaja de usarlo es que sombrea los objetos y les proporciona profundidad tridimensional (3D). Para ver cómo se calcula la iluminación difusa en Direct3D, consulte Iluminación difusa (Direct3D 9).

[La iluminación especular (Direct3D 9)](specular-lighting.md) identifica los resaltados especulares brillantes que se producen cuando la luz llega a una superficie de objeto y se refleja hacia la cámara. Es más intensa que la luz difusa y cae más rápidamente en la superficie del objeto. Se tarda más tiempo en calcular la iluminación especular que la iluminación difusa; sin embargo, la ventaja de usarlo es que agrega detalles significativos a una superficie. Para ver cómo se calcula la iluminación especular en Direct3D, consulte Specular Lighting (Direct3D 9) (Iluminación especular (Direct3D 9).

[La iluminación emisiva (Direct3D 9)](emissive-lighting.md) es la luz que emite un objeto ; por ejemplo, un efecto de efecto de efecto. Para ver cómo se calcula la iluminación emisiva en Direct3D, consulte Iluminación emisiva (Direct3D 9).

La iluminación realista se puede lograr aplicando cada uno de estos tipos de iluminación a una escena 3D. Los valores calculados para los componentes ambiente, emissivo y difuso se emiten como color de vértice difuso; El valor del componente de iluminación especular se genera como el color del vértice especular. Los valores de luz ambiental, difuso y especular pueden verse afectados por la atenuación y el factor de destacado de una luz determinada. Para obtener más información sobre cómo funciona la atenuación, vea [Atenuación y factor spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)

Para lograr un efecto de iluminación más realista, agregue más luces. sin embargo, la escena tarda más tiempo en representarse. Para lograr todos los efectos que un diseñador desea, algunos juegos usan más potencia de CPU de la que está disponible habitualmente. En este caso, es habitual reducir el número de cálculos de iluminación al mínimo mediante mapas de iluminación y mapas de entorno para agregar iluminación a una escena mientras se usan mapas de textura.

La iluminación se calcula en el espacio de la cámara. Para ver cómo se calculan las transformaciones de iluminación, vea Transformaciones de espacio de cámara [(Direct3D 9).](camera-space-transformations.md) La iluminación optimizada se puede calcular en el espacio del modelo, cuando existen condiciones especiales: los vectores normales ya están normalizados (D3DRS NORMALIZENORMALS es True), no se necesita la combinación de vértices, las matrices de transformación son \_ ortogonales, etc.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Luces y materiales](lights-and-materials.md)
</dt> </dl>

 

 



