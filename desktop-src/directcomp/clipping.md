---
title: Recorte (DirectComposition)
description: En este tema se describe la compatibilidad de Microsoft DirectComposition con objetos visuales de recorte.
ms.assetid: B6E0D8F5-B6B9-40CC-B079-850AC8F2D538
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446dda9cc95341dcce041dbfbfd32a9d0368e74b2a67aabe1a8b1c4856165ea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043412"
---
# <a name="clipping-directcomposition"></a>Recorte (DirectComposition)

> [!NOTE]
> Para las aplicaciones de Windows 10, se recomienda usar Windows.UI.Composition API en lugar de DirectComposition. Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

El recorte proporciona una manera de mostrar solo una parte de un árbol visual o visual limitando la representación del objeto visual o árbol a un área rectangular determinada. En este tema se describe la compatibilidad de Microsoft DirectComposition con objetos visuales de recorte. Se incluyen las secciones siguientes:

-   [Rectángulo de recorte](#clip-rectangle)
-   [Clip (objeto)](#clip-object)
-   [Rectángulo de clip animado](#animated-clip-rectangle)
-   [Temas relacionados](#related-topics)

## <a name="clip-rectangle"></a>Rectángulo de recorte

Un objeto visual tiene una propiedad Clip que define una región rectangular, o *rectángulo de recorte,* dentro del contenido de mapa de bits del objeto visual. Cuando el objeto visual se representa en la pantalla, solo se dibuja en la pantalla la parte del contenido del mapa de bits que está dentro del rectángulo de recorte, mientras que el contenido que se extiende fuera del rectángulo de recorte se recorta (no se dibuja). De forma predeterminada, la propiedad Clip incluye todo el contenido del mapa de bits.

La propiedad Clip de un objeto visual se aplica a todos los objetos visuales secundarios y descendientes. En otras palabras, también se recorta cualquier contenido secundario o descendiente que se encuentra fuera de los límites del rectángulo de recorte del elemento primario.

DirectComposition aplica la propiedad Clip antes de aplicar las propiedades OffsetX, OffsetY y 2D Transform, pero después de aplicar las propiedades Efecto y Transformación 3D. Esto significa que las transformaciones 2D, OffsetX y OffsetY afectarán tanto al contenido visual como al rectángulo de recorte. Mientras que las transformaciones y los efectos 3D no se aplicarán al rectángulo de recorte.

Por ejemplo, al aplicar un desplazamiento o una transformación 2D, la matriz de transformación afecta al rectángulo de recorte. Por lo tanto, agregar un desplazamiento y una rotación 2D (45 grados) junto con un rectángulo de recorte de esquina redondeado dará como resultado lo siguiente:

![diagrama de que muestra el efecto de una transformación 2d en un rectángulo de recorte.](images/clipping2dtransform.png)

Al aplicar una transformación 3D "dentro" del rectángulo de recorte, la matriz de transformación no afecta al rectángulo de recorte. Incluso cuando se aplica una rotación alrededor del eje Z (de forma eficaz igual que en el ejemplo anterior), el siguiente diagrama es el resultado:

![diagrama que muestra que una transformación 3d no afecta al clip del rectángulo (el objeto visual gira dentro del clip).](images/clipping3dtransform.png)

Tenga en cuenta que el objeto visual gira dentro del clip porque la matriz 3D no se aplica al propio clip.

Si la propiedad Clip se establece en un rectángulo vacío, el objeto visual se recorta completamente; es decir, el objeto visual se incluye en el árbol visual, pero no representa nada. Si no desea incluir un objeto visual determinado en una composición, quite el objeto visual del árbol visual en lugar de establecer un rectángulo de recorte vacío. Al quitar el objeto visual, se mejora el rendimiento.

La propiedad Clip de un objeto visual se establece mediante el [**método IDCompositionVisual::SetClip.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) Este método incluye sobrecargas que permiten establecer el valor de la propiedad Clip en un rectángulo estático o en un objeto clip. Use un rectángulo estático si no necesita cambiar las dimensiones del rectángulo de recorte durante la vigencia del objeto visual. Si necesita cambiar las dimensiones o animar el rectángulo de recorte, use un objeto clip.

## <a name="clip-object"></a>Clip (objeto)

Un objeto clip es un objeto De modelo de objetos componentes (COM) que representa un rectángulo de recorte. Para crear un objeto clip, use el método [**IDCompositionDevice::CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) y, a continuación, use la interfaz [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) del objeto para establecer las propiedades del objeto. Un objeto de recorte recién creado tiene los valores mínimos posibles para las propiedades Left y Top, y los valores máximos posibles para las propiedades Right e Bottom, lo que lo hace un objeto de recorte sin operación. En otras palabras, el objeto representa un rectángulo de recorte que incluiría todo el contenido de mapa de bits de un objeto visual.

Un objeto de recorte incluye un conjunto de propiedades que permiten especificar esquinas redondeadas para el objeto de recorte. Las propiedades permiten establecer el radio x y el radio de cada esquina del objeto de recorte.

## <a name="animated-clip-rectangle"></a>Rectángulo de clip animado

Puede animar un rectángulo de recorte aplicando objetos de animación a las propiedades Izquierda, Superior, Derecha e Inferior de un objeto clip. Use el [**método sobrecargado IDCompositionVisual::SetClip(IDCompositionClip)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) para aplicar el rectángulo de clip animado a la propiedad Clip de un objeto visual.

Para obtener más información sobre los objetos de animación, vea [Animation](animation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> <dt>

[Cómo recortar con un objeto de recorte de rectángulo](how-to--set-the-clip-rectangle-for-a-visual.md)
</dt> </dl>

 

 
