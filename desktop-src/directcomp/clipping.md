---
title: Recorte (DirectComposition)
description: En este tema se describe la compatibilidad de Microsoft DirectComposition con los objetos visuales de recorte.
ms.assetid: B6E0D8F5-B6B9-40CC-B079-850AC8F2D538
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4feb537dfb41053dd1099eca7f122b3284dce95
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421881"
---
# <a name="clipping-directcomposition"></a>Recorte (DirectComposition)

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

El recorte proporciona una manera de revelar solo una parte de un árbol visual o visual limitando la representación del árbol visual o del árbol a un área rectangular determinada. En este tema se describe la compatibilidad de Microsoft DirectComposition con los objetos visuales de recorte. Se incluyen las secciones siguientes:

-   [Rectángulo de recorte](#clip-rectangle)
-   [Clip (objeto)](#clip-object)
-   [Rectángulo de recorte animado](#animated-clip-rectangle)
-   [Temas relacionados](#related-topics)

## <a name="clip-rectangle"></a>Rectángulo de recorte

Un objeto visual tiene una propiedad clip que define una región rectangular, o un *rectángulo de recorte*, dentro del contenido del mapa de bits del objeto visual. Cuando el visual se representa en la pantalla, solo la parte del contenido del mapa de bits que se encuentra dentro del rectángulo de recorte se dibuja en la pantalla, mientras que el contenido que se extiende fuera del rectángulo de recorte se recorta (no se dibuja). De forma predeterminada, la propiedad clip incluye todo el contenido del mapa de bits.

La propiedad clip de un elemento visual se aplica a todos los objetos visuales secundarios y descendientes. Es decir, cualquier contenido secundario o descendiente que se encuentre fuera de los límites del rectángulo de recorte del elemento primario también se recorta.

DirectComposition aplica la propiedad clip antes de aplicar las propiedades de transformación OffsetX, offsetY y 2D, pero después de aplicar las propiedades Effect y transformación 3D. Esto significa que las transformaciones 2D, OffsetX y PosiciónInicial, afectarán tanto al contenido visual como al rectángulo de recorte. Mientras que las transformaciones y los efectos 3D no se aplicarán al rectángulo de recorte.

Por ejemplo, al aplicar un desplazamiento o una transformación 2D, el rectángulo de recorte se ve afectado por la matriz de transformación. Por tanto, si se agrega un desplazamiento y un giro 2D (45 grados) junto con un rectángulo de recorte de esquinas redondeadas, se producirá lo siguiente:

![diagrama que muestra el efecto de una transformación 2D en un rectángulo de recorte.](images/clipping2dtransform.png)

Al aplicar una transformación 3D "dentro" del rectángulo de recorte, el rectángulo de recorte no se ve afectado por la matriz de transformación. Incluso cuando se aplica un giro alrededor del eje Z (en realidad, lo mismo que el ejemplo anterior), el siguiente diagrama es el resultado:

![diagrama que muestra que una transformación 3D no afecta al clip del rectángulo (el visual gira dentro del clip).](images/clipping3dtransform.png)

Tenga en cuenta que el visual girado en el clip porque la matriz 3D no se aplica al propio clip.

Si la propiedad clip está establecida en un rectángulo vacío, el visual se recorta completamente; es decir, el elemento visual se incluye en el árbol visual, pero no representa nada. Si no desea incluir un visual determinado en una composición, quite el visual del árbol visual en lugar de establecer un rectángulo de recorte vacío. Quitar el resultado visual mejora el rendimiento.

La propiedad clip de un visual se establece mediante el método [**IDCompositionVisual:: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) . Este método incluye sobrecargas que permiten establecer el valor de la propiedad clip en un rectángulo estático o en un objeto clip. Use un rectángulo estático si no necesita cambiar las dimensiones del rectángulo de recorte mientras dure el visual. Si necesita cambiar las dimensiones o animar el rectángulo de recorte, use un objeto de clip.

## <a name="clip-object"></a>Clip (objeto)

Un objeto de recorte es un objeto de modelo de objetos componentes (COM) que representa un rectángulo de recorte. Cree un objeto clip mediante el método [**IDCompositionDevice:: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) y, a continuación, use la interfaz [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) del objeto para establecer las propiedades del objeto. Un objeto de recorte recién creado tiene los valores mínimos posibles para las propiedades Left y Top, y los valores máximos posibles para las propiedades derecha e inferior, lo que lo convierte en un objeto de clip no operativo. En otras palabras, el objeto representa un rectángulo de recorte que incluiría todo el contenido del mapa de bits de un objeto visual.

Un objeto clip incluye un conjunto de propiedades que le permiten especificar esquinas redondeadas para el objeto clip. Las propiedades permiten establecer el radio x e y de cada esquina del objeto de recorte.

## <a name="animated-clip-rectangle"></a>Rectángulo de recorte animado

Puede animar un rectángulo de recorte aplicando objetos de animación a las propiedades izquierda, superior, derecha e inferior de un objeto de clip. Use el método sobrecargado [**IDCompositionVisual:: SetClip (IDCompositionClip)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) para aplicar el rectángulo de recorte animado a la propiedad clip de un visual.

Para obtener más información sobre los objetos de animación, vea [animación](animation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> <dt>

[Cómo recortar con un objeto de recorte de rectángulo](how-to--set-the-clip-rectangle-for-a-visual.md)
</dt> </dl>

 

 
