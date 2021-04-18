---
description: Al crear escenas 3D, una aplicación a veces puede obtener ventajas de rendimiento al representar objetos 2D de forma que parezcan objetos 3D. Esta es la idea básica detrás de la técnica de la cartelera.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Cartelera (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705385"
---
# <a name="billboarding-direct3d-9"></a>Cartelera (Direct3D 9)

Al crear escenas 3D, una aplicación a veces puede obtener ventajas de rendimiento al representar objetos 2D de forma que parezcan objetos 3D. Esta es la idea básica detrás de la técnica de la cartelera.

Una cartelera en el sentido normal de la palabra es un signo a lo largo de un Roadway. Las aplicaciones de Microsoft Direct3D pueden crear y representar este tipo de cartelera definiendo un sólido rectangular y aplicándole una textura. La cartelera en el sentido más especializado de los gráficos 3D es una extensión de este. El objetivo es hacer que los objetos 2D parezcan 3D. La técnica consiste en aplicar una textura que contenga la imagen del objeto a un primitivo rectangular. La primitiva se gira para que siempre enfrente al usuario. No importa si la imagen del objeto no es rectangular. Las partes de la cartelera pueden hacerse transparentes, por lo que las partes de la imagen de la cartelera que no desea ver no son visibles.

Muchos juegos emplean la cartelera de sprites animados. Por ejemplo, cuando el usuario está pasando por un laberinto 3D, puede ver armas o recompensas que se pueden seleccionar. Suelen ser imágenes 2D con textura en un primitivo rectangular. La cartelera se usa a menudo en juegos para representar imágenes de árboles, casquillos y nubes.

Cuando se aplica una imagen a una cartelera, primero se debe girar el primitivo rectangular para que la imagen resultante se enfrente al usuario. A continuación, la aplicación debe convertirla en posición. A continuación, la aplicación puede aplicar una textura a la primitiva.

La cartelera funciona mejor para objetos simétricos, especialmente los objetos que son simétricos a lo largo del eje vertical. También requiere que la altitud del punto de vista no aumente demasiado. Si el usuario tiene permiso para ver la cartelera anterior, se hace evidente de forma fácil que el objeto es 2D en lugar de 3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de alfa](alpha-examples.md)
</dt> </dl>

 

 



