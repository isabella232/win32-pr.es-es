---
description: Al crear escenas 3D, una aplicación a veces puede obtener ventajas de rendimiento mediante la representación de objetos 2D de forma que parezcan ser objetos 3D. Esta es la idea básica que se encuentra detrás de la técnica de la tecnología de diseño de paneles.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Afición (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359372"
---
# <a name="billboarding-direct3d-9"></a>Afición (Direct3D 9)

Al crear escenas 3D, una aplicación a veces puede obtener ventajas de rendimiento mediante la representación de objetos 2D de forma que parezcan ser objetos 3D. Esta es la idea básica que se encuentra detrás de la técnica de la tecnología de diseño de paneles.

Un pancarte en el sentido normal de la palabra es un signo a lo largo de un camino. Las aplicaciones de Microsoft Direct3D pueden crear y representar este tipo de paneles si definen un sólido rectangular y le aplican una textura. La formación de paneles en el sentido más especializado de los gráficos 3D es una extensión de esto. El objetivo es hacer que los objetos 2D parezcan 3D. La técnica consiste en aplicar una textura que contiene la imagen del objeto a una primitiva rectangular. La primitiva se gira para que siempre se enfrenta al usuario. No importa si la imagen del objeto no es rectangular. Las partes de la galería se pueden hacer transparentes, por lo que las partes de la imagen de color azul azul que no desea ver no son visibles.

Muchos juegos emplean juegos para sprites animados. Por ejemplo, cuando el usuario se mueve a través de un mundo 3D, es posible que vea las recompensas o las recompensas que se pueden recoger. Normalmente se trata de imágenes 2D con textura en una primitiva rectangular. A menudo se usa la marcación en juegos para representar imágenes de árboles, árboles, árboles y nubes.

Cuando se aplica una imagen a un rectángulo, primero se debe girar la primitiva rectangular para que la imagen resultante se enfrenta al usuario. A continuación, la aplicación debe traducirla en su posición. A continuación, la aplicación puede aplicar una textura a la primitiva.

La señalización funciona mejor para los objetos simétricos, especialmente los objetos simétricos a lo largo del eje vertical. También requiere que la altitud del punto de vista no aumente demasiado. Si el usuario puede ver el contenido de arriba, se hace evidente que el objeto es 2D en lugar de 3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos alfa](alpha-examples.md)
</dt> </dl>

 

 



