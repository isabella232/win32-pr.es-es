---
description: Cada vez más, las aplicaciones emplean efectos especiales que se usan habitualmente en películas y vídeos, como desenlace, deslizamientos y atenuaciones.
ms.assetid: 6203922f-9594-4e5c-9baa-8b27ac30978f
title: Conexiones, atenuaciones y deslizamientos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d6df834ad19fa4b00b6e4706d0884227bc4af33c6a25ec09cba14757e1248
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607474"
---
# <a name="dissolves-fades-and-swipes-direct3d-9"></a>Conexiones, atenuaciones y deslizamientos (Direct3D 9)

Cada vez más, las aplicaciones emplean efectos especiales que se usan habitualmente en películas y vídeos, como desenlace, deslizamientos y atenuaciones.

En una escena, una imagen se reemplaza gradualmente por otra en una secuencia suave de fotogramas. Aunque Direct3D proporciona métodos de uso de la combinación de varias texturas para lograr el mismo efecto, las aplicaciones que usan el búfer de galería de símbolos para las desatenciones pueden usar funcionalidades de mezcla de textura para otros efectos mientras se desenvuelven.

Cuando la aplicación realiza una disolver, debe representar dos imágenes diferentes. Usa el búfer de galería de símbolos para controlar qué píxeles de cada imagen se dibujan en la superficie de destino de representación. Puede definir una serie de máscaras de galería de símbolos y copiarlas en el búfer de galería de símbolos en fotogramas sucesivos. Como alternativa, puede definir una máscara de galería de símbolos base para el primer fotograma y modificarla incrementalmente.

Al principio de la distensión, la aplicación establece la función de galería de símbolos y la máscara de galería de símbolos para que la mayoría de los píxeles de la imagen inicial pasen la prueba de galería de símbolos. La mayoría de los píxeles de la imagen final deben producir un error en la prueba de galería de símbolos. En los fotogramas sucesivos, la máscara de galería de símbolos se actualiza para que cada vez menos píxeles de la imagen inicial pasen la prueba. A medida que los fotogramas progresan, cada vez menos píxeles de la imagen final no se completan con la prueba. De esta manera, la aplicación puede realizar una dislación mediante cualquier patrón arbitrario de dislate.

La desvanección o la desvanección es un caso especial de disolver. Al desvanecirse, el búfer de la galería de símbolos se usa para desaparecer de una imagen en blanco o negro a una representación de una escena 3D. La desvanecha es lo contrario, la aplicación comienza con una representación de una escena 3D y se disuelve en blanco o negro. La atenuación se puede realizar con cualquier patrón arbitrario que desee emplear.

Las aplicaciones de Direct3D usan una técnica similar para deslizar rápidamente. Por ejemplo, cuando una aplicación realiza un deslizamiento de izquierda a derecha, la imagen final parece deslizarse gradualmente sobre la imagen inicial de izquierda a derecha. Como en un período, debe definir una serie de máscaras de galería de símbolos que se cargan en el búfer de galería de símbolos en marcos sucesivos o modificar sucesivamente la máscara de galería de símbolos inicial. Las máscaras de galería de símbolos se usan para deshabilitar la escritura de píxeles de la imagen inicial y para habilitar la escritura de píxeles a partir de la imagen final.

Un deslizamiento es algo más complejo que un desenlace, ya que la aplicación debe leer píxeles de la imagen final en el orden inverso del deslizamiento. Es decir, si el deslizamiento se mueve de izquierda a derecha, la aplicación debe leer píxeles de la imagen final de derecha a izquierda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas de búfer de galería de símbolos](stencil-buffer-techniques.md)
</dt> </dl>

 

 



