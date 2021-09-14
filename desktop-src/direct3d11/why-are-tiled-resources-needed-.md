---
title: ¿Por qué se necesitan recursos en mosaico?
description: Se necesitan recursos en mosaico, por lo que se desperdicia menos memoria de la unidad de procesamiento gráfico (GPU) almacenando regiones de superficies a las que la aplicación sabe que no se accederá y el hardware puede entender cómo filtrar entre iconos adyacentes.
ms.assetid: E2179D65-56D3-481F-A5F3-B9C45A11A179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42ccccf66a73d224d8bab9a9d10c87cc330be43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063760"
---
# <a name="why-are-tiled-resources-needed"></a>¿Por qué se necesitan recursos en mosaico?

Se necesitan recursos en mosaico, por lo que se desperdicia menos memoria de la unidad de procesamiento gráfico (GPU) almacenando regiones de superficies a las que la aplicación sabe que no se accederá y el hardware puede entender cómo filtrar entre iconos adyacentes.

En un sistema de gráficos (es decir, el sistema operativo, el controlador de pantalla y el hardware de gráficos) sin compatibilidad con recursos en mosaico, el sistema de gráficos administra todas las asignaciones de memoria de Direct3D con granularidad de subrecursos. Para un [búfer](overviews-direct3d-11-resources-buffers.md), el búfer completo es el subrecurso. Para una [textura](overviews-direct3d-11-resources-textures.md) (por ejemplo, [**Texture2D),**](/windows/desktop/direct3dhlsl/sm5-object-texture2d)cada nivel mip es un subrecurso; para una matriz de texturas (por ejemplo, [**Texture2DArray),**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray)cada nivel de mip en un segmento de matriz determinado es un subrecurso. El sistema de gráficos solo expone la capacidad de administrar la asignación de asignaciones en esta granularidad de subrecursos. En el contexto de los recursos en mosaico, la "asignación" hace referencia a hacer que los datos sean visibles para la GPU.

Supongamos que una aplicación sabe que una operación de representación determinada solo necesita acceder a una pequeña parte de una cadena de mapa mip de imagen (quizás ni siquiera el área completa de un mapa MIP determinado). Idealmente, la aplicación podría informar al sistema de gráficos sobre esta necesidad. A continuación, el sistema de gráficos solo se preocuparía de asegurarse de que la memoria necesaria está asignada en la GPU sin paginar en demasiada memoria. En realidad, sin compatibilidad con recursos en mosaico, el sistema de gráficos solo se puede informar sobre la memoria que debe asignarse en la GPU con granularidad de subrecursos (por ejemplo, un intervalo de niveles de mapa mip completos a los que se puede acceder). Tampoco hay errores de demanda en el sistema de gráficos, por lo que se debe usar una gran cantidad de memoria de GPU excesiva para asignar recursos secundarios completos antes de que se ejecute un comando de representación que haga referencia a cualquier parte de la memoria. Este es solo un problema que dificulta el uso de grandes asignaciones de memoria en Direct3D sin compatibilidad con recursos en mosaico.

Direct3D 11 admite superficies [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) con hasta 16384 píxeles en un lado determinado. Una imagen de 16384 de ancho por 16384 de alto y 4 bytes por píxel consumiría 1 GB de memoria de vídeo (y agregar mapas MIP duplicaría esa cantidad). En la práctica, rara vez es necesario hacer referencia a todos los 1 GB en una sola operación de representación.

Algunos desarrolladores de juegos modela superficies de terreno de hasta 128 000 por 128 000. La forma en que hacen que esto funcione en las GPU existentes es dividir la superficie en mosaicos lo suficientemente pequeños como para que el hardware lo controle. La aplicación debe averiguar qué iconos pueden ser necesarios y cargarlos en una caché de texturas en la GPU, un sistema de paginación de software. Un inconveniente significativo de este enfoque se debe a que el hardware no sabe nada sobre la paginación que se está haciendo: cuando una parte de una imagen debe mostrarse en la pantalla que se desmarca de los iconos, el hardware no sabe cómo realizar un filtrado de función fija (es decir, eficaz) entre iconos. Esto significa que la aplicación que administra su propio mosaico de software debe recurrir al filtrado manual de texturas en el código del sombreador (que resulta muy costoso si se desea un filtro anisotropico de buena calidad) o a desperdiciar los canales de creación de memoria alrededor de los mosaicos que contienen datos de mosaicos vecinos para que el filtrado de hardware de función fija pueda seguir brindando cierta ayuda.

Si una representación en mosaico de asignaciones de superficie podría ser una característica de primera clase en el sistema de gráficos, la aplicación podría decir al hardware qué iconos deben estar disponibles. De este modo, se desperdicia menos memoria de GPU almacenando regiones de superficies a las que la aplicación sabe que no se accederá y el hardware puede entender cómo filtrar entre iconos adyacentes, lo que mitiga parte del problema que experimentan los desarrolladores que realizan el mosaico de software por sí mismos.

Pero para proporcionar una solución completa, se debe hacer algo para tratar con el hecho de que, independientemente de si se admite el tiling dentro de una superficie, la dimensión de superficie máxima es actualmente 16384, cerca de los más de 128 000 que las aplicaciones ya desean. Requerir que el hardware admita tamaños de textura mayores es un enfoque; sin embargo, hay costos significativos y/o ahorros para ir a esta ruta. La ruta de acceso del filtro de textura y la ruta de representación de Direct3D 11 ya están saturadas en términos de precisión para admitir texturas de 16K con los demás requisitos, como admitir extensiones de ventanilla que se encuentran fuera de la superficie durante la representación o admitir el ajuste de textura fuera del borde de la superficie durante el filtrado. Una posibilidad es definir un ajuste, de modo que, a medida que el tamaño de la textura aumente más allá de 16 000, la funcionalidad o la precisión se desaconsensen de alguna manera. Sin embargo, incluso con esta concesión, es posible que se requieran costos de hardware adicionales en términos de capacidad de direccionamiento en todo el sistema de hardware para pasar a tamaños de textura mayores.

Un problema que entra en juego a medida que las texturas son muy grandes es que las coordenadas de textura de punto flotante de precisión sencilla (y los interpoladores asociados para admitir la rasterización) se ejecutan sin precisión para especificar las ubicaciones de la superficie con precisión. El filtrado de texturas con vibración se crearía. Una opción costosa sería requerir compatibilidad con interpoladores de precisión doble, aunque esto podría ser excesivo dada una alternativa razonable.

Un nombre alternativo para los recursos en mosaico es "textura dispersa". "Disperso" transmite tanto la naturaleza en mosaico de los recursos como quizás la razón principal para mosaicos: que no se espera que todos se asignen a la vez. De hecho, es posible que una aplicación cree un recurso en mosaico en el que no se cree ningún dato para todas las regiones+mips del recurso, intencionadamente. Por lo tanto, el propio contenido podría ser disperso y la asignación del contenido en la memoria de GPU en un momento dado sería un subconjunto de eso (incluso más disperso).

Otro escenario que podrían servir los recursos en mosaico es permitir que varios recursos de diferentes dimensiones o formatos compartan la misma memoria. A veces, las aplicaciones tienen conjuntos exclusivos de recursos que se sabe que no se usan al mismo tiempo, o recursos que se crean solo para un uso muy breve y, a continuación, se destruyen, seguidos de la creación de otros recursos. Una forma de generalidad que puede quedarse fuera de los "recursos en mosaico" es que es posible permitir al usuario señalar varios recursos diferentes en la misma memoria (superpuesta). En otras palabras, la creación y destrucción de "recursos" (que definen una dimensión o formato, entre otras) se puede desacoplar de la administración de la memoria subyacente a los recursos desde el punto de vista de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos en mosaico](tiled-resources.md)
</dt> </dl>

 

 