---
description: Cada vez más, las aplicaciones emplean efectos especiales que se suelen usar en películas y vídeo, como las desmedidas, los deslizamientos y los fundidos.
ms.assetid: 6203922f-9594-4e5c-9baa-8b27ac30978f
title: Se resuelve, atenúa y desliza el dedo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ad837ea846ca43d61102ce426d415270d2f27f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806295"
---
# <a name="dissolves-fades-and-swipes-direct3d-9"></a>Se resuelve, atenúa y desliza el dedo (Direct3D 9)

Cada vez más, las aplicaciones emplean efectos especiales que se suelen usar en películas y vídeo, como las desmedidas, los deslizamientos y los fundidos.

En una resolución, una imagen se reemplaza gradualmente por otra en una secuencia de fotogramas suavizada. Aunque Direct3D proporciona métodos para usar varias combinaciones de texturas para lograr el mismo efecto, las aplicaciones que usan el búfer de estarcido para las discapacidades pueden utilizar las capacidades de combinación de texturas para otros efectos mientras se resuelven.

Cuando la aplicación realiza una resolución, debe representar dos imágenes diferentes. Usa el búfer de estarcido para controlar qué píxeles de cada imagen se dibujan en la superficie de destino de representación. Puede definir una serie de máscaras de estarcido y copiarlas en el búfer de estarcido en fotogramas sucesivos. Como alternativa, puede definir una máscara de galería de símbolos base para el primer fotograma y modificarla incrementalmente.

Al principio de la resolución, la aplicación establece la función de estarcido y la máscara de la galería de símbolos de modo que la mayoría de los píxeles de la imagen inicial pasen la prueba de estarcido. La mayoría de los píxeles de la imagen final deben tener un error en la prueba de estarcido. En fotogramas sucesivos, la máscara de la galería de símbolos se actualiza para que menos y menos de los píxeles de la imagen inicial pasen la prueba. A medida que los fotogramas progresan, se produce un error en la prueba con menos y menos píxeles de la imagen final. De esta manera, la aplicación puede realizar una resolución con cualquier patrón de resolución arbitrario.

La atenuación o el fundido de salida es un caso especial de la solución. Cuando se difumina, el búfer de estarcido se usa para disolver una imagen en blanco o negro en una representación de una escena 3D. La atenuación es lo contrario, la aplicación comienza con una representación de una escena 3D y se resuelve en blanco o negro. La atenuación se puede realizar con cualquier patrón arbitrario que desee emplear.

Las aplicaciones Direct3D usan una técnica similar para los deslizamientos. Por ejemplo, cuando una aplicación realiza un deslizamiento de izquierda a derecha, la imagen final parece deslizarse gradualmente en la parte superior de la imagen inicial de izquierda a derecha. Al igual que en una solución, debe definir una serie de máscaras de galería de símbolos que se cargan en el búfer de estarcido en fotogramas sucesivos o modificar sucesivamente la máscara de la galería de símbolos de inicio. Las máscaras de estarcido se usan para deshabilitar la escritura de píxeles de la imagen inicial y para permitir la escritura de píxeles desde la imagen final.

Un deslizamiento es algo más complejo que resolver en que la aplicación debe leer píxeles de la imagen final en el orden inverso del deslizamiento. Es decir, si el deslizamiento se desplaza de izquierda a derecha, la aplicación debe leer los píxeles de la imagen final de derecha a izquierda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas de búfer de estarcido](stencil-buffer-techniques.md)
</dt> </dl>

 

 



