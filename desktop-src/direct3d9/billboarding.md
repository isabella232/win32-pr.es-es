---
description: Al crear escenas 3D, una aplicación a veces puede obtener ventajas de rendimiento al representar objetos 2D de forma que parezcan objetos 3D. Esta es la idea básica que hay detrás de la técnica de la técnica de sobresaliendo.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Resalte (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02624a3172df7a36f4d38bb2bc6d613ded26faab8ac6d4f4b37668f0868cd16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123412"
---
# <a name="billboarding-direct3d-9"></a>Resalte (Direct3D 9)

Al crear escenas 3D, una aplicación a veces puede obtener ventajas de rendimiento al representar objetos 2D de forma que parezcan objetos 3D. Esta es la idea básica que hay detrás de la técnica de la técnica de sobresaliendo.

Un símbolo en el sentido normal de la palabra es un signo a lo largo de un camino. Las aplicaciones de Microsoft Direct3D pueden crear y representar este tipo de paneles definiendo un sólido rectangular y aplicando una textura. El diseño en el sentido más especializado de los gráficos 3D es una extensión de esto. El objetivo es hacer que los objetos 2D parezcan 3D. La técnica consiste en aplicar una textura que contiene la imagen del objeto a una primitiva rectangular. La primitiva se gira para que siempre se enfrenta al usuario. No importa si la imagen del objeto no es rectangular. Las partes de los paneles se pueden hacer transparentes, por lo que las partes de la imagen de la foto que no desea ver no son visibles.

Muchos juegos emplean juegos para sprites animados. Por ejemplo, cuando el usuario se mueve a través de un mundo 3D, es posible que vea las recompensas o las recompensas que se pueden recoger. Normalmente se trata de imágenes 2D con textura en una primitiva rectangular. A menudo se usa en juegos para representar imágenes de árboles, árboles, árboles y nubes.

Cuando se aplica una imagen a un reloj, la primitiva rectangular debe girarse primero para que la imagen resultante se enfrenta al usuario. A continuación, la aplicación debe traducirla en su posición. A continuación, la aplicación puede aplicar una textura a la primitiva.

El diseño de desplazamiento funciona mejor para los objetos simétricos, especialmente los objetos que son simétricos a lo largo del eje vertical. También requiere que la altitud del punto de vista no aumente demasiado. Si el usuario puede ver el contenido de arriba, resulta evidente que el objeto es 2D en lugar de 3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos alfa](alpha-examples.md)
</dt> </dl>

 

 



