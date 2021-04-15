---
title: ¿Por qué son necesarios los recursos en mosaico?
description: Los recursos en mosaico son necesarios, por lo que no se podrá tener acceso a la memoria de la unidad de procesamiento de gráficos (GPU), y el hardware puede comprender cómo filtrar por los mosaicos adyacentes.
ms.assetid: E2179D65-56D3-481F-A5F3-B9C45A11A179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42ccccf66a73d224d8bab9a9d10c87cc330be43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983987"
---
# <a name="why-are-tiled-resources-needed"></a>¿Por qué son necesarios los recursos en mosaico?

Los recursos en mosaico son necesarios, por lo que no se podrá tener acceso a la memoria de la unidad de procesamiento de gráficos (GPU), y el hardware puede comprender cómo filtrar por los mosaicos adyacentes.

En un sistema de gráficos (es decir, el sistema operativo, el controlador de pantalla y el hardware de gráficos) sin compatibilidad con recursos en mosaico, el sistema de gráficos administra todas las asignaciones de memoria de Direct3D en la granularidad de los recursos. En el caso de un [búfer](overviews-direct3d-11-resources-buffers.md), todo el búfer es el subrecurso. En el caso de una [textura](overviews-direct3d-11-resources-textures.md) (por ejemplo, [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d)), cada nivel de MIP es un subrecurso; en el caso de una matriz de textura (por ejemplo, [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray)), cada nivel de MIP en un segmento de matriz determinado es un subrecurso. El sistema de gráficos solo expone la capacidad de administrar la asignación de asignaciones en esta granularidad de Subrecursos. En el contexto de los recursos en mosaico, la "asignación" hace referencia a hacer que los datos sean visibles para la GPU.

Supongamos que una aplicación sabe que una operación de representación determinada solo necesita tener acceso a una pequeña parte de una cadena de mipmap de imagen (quizás no incluso al área completa de un mipmap determinado). Idealmente, la aplicación podría informar al sistema de gráficos sobre esta necesidad. El sistema de gráficos solo se molestaría para asegurarse de que la memoria necesaria está asignada en la GPU sin paginación en demasiada memoria. En realidad, sin compatibilidad con recursos en mosaico, solo se puede informar al sistema de gráficos sobre la memoria que debe asignarse a la GPU en la granularidad de los Subrecursos (por ejemplo, un intervalo de niveles de mipmap completo a los que se puede tener acceso). No hay ningún error de demanda en el sistema de gráficos, por lo que es posible que se use una gran cantidad de memoria de GPU para hacer que se asignen Subrecursos completos antes de que se ejecute un comando de representación que haga referencia a cualquier parte de la memoria. Esto es solo un problema que dificulta el uso de grandes asignaciones de memoria en Direct3D sin compatibilidad con recursos en mosaico.

Direct3D 11 admite superficies [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) con hasta 16384 píxeles en un lado determinado. Una imagen de 16384 de ancho a 16384 de alto y 4 bytes por píxel consumirá 1 GB de memoria de vídeo (y la adición de mapas de bits duplicaría esa cantidad). En la práctica, no es necesario hacer referencia a todos los 1 GB en una sola operación de representación.

Algunos desarrolladores de juegos muestran superficies del terreno tan grandes como 128 KB. La forma en que lo hacen para trabajar en GPU existentes es dividir la superficie en mosaicos que son lo suficientemente pequeños como para controlar el hardware. La aplicación debe averiguar qué mosaicos podrían ser necesarios y cargarlos en una caché de texturas en el sistema de paginación de software GPU-a. Una desventaja importante de este enfoque es que el hardware no está informando sobre la paginación que se está llevando a cabo: cuando es necesario mostrar una parte de una imagen en la pantalla que ocupa los mosaicos, el hardware no sabe cómo realizar el filtrado de función fija (es decir, eficaz) en los mosaicos. Esto significa que la aplicación que administra su propia segmentación de software debe recurrir al filtrado manual de texturas en el código del sombreador (lo que resulta muy caro si se desea un filtro anisotrópico de buena calidad) o desperdiciar los márgenes de la creación de memoria alrededor de los mosaicos que contienen datos de mosaicos contiguos, de modo que el filtrado de hardware de función fija pueda seguir proporcionando

Si una representación en mosaico de las asignaciones de superficie puede ser una característica de primera clase en el sistema de gráficos, la aplicación podría indicar al hardware qué mosaicos debe poner a disposición. De esta manera, se desperdicia menos memoria de GPU al almacenar regiones de superficies que la aplicación sabe que no se tendrá acceso a ella, y el hardware puede entender cómo filtrar por los mosaicos adyacentes, lo que evitará que se detecten algunos de los problemas de los desarrolladores que realizan el mosaico de software por su cuenta.

Pero para proporcionar una solución completa, se debe hacer algo para tratar con el hecho de que, independientemente de si se admite la disposición en mosaico dentro de una superficie, la dimensión de superficie máxima es actualmente de 16384-no está cerca de las 128K + que las aplicaciones ya quieren. Simplemente requerir el hardware para admitir tamaños de textura mayores es un enfoque, sin embargo, hay costos y/o contrapartidas significativos para pasar a esta ruta. La ruta de acceso de la representación y la ruta de acceso del filtro de textura de Direct3D 11 ya están saturadas en términos de precisión en la compatibilidad con texturas de 16K con los demás requisitos, como la compatibilidad de las extensiones de la ventanilla que caen fuera de la superficie durante la representación o la compatibilidad con el ajuste de textura del borde de la superficie durante el filtrado. Una posibilidad es definir un equilibrio de forma que, a medida que el tamaño de la textura aumente más allá de 16 k, la funcionalidad/precisión se proporcione de alguna manera. Sin embargo, incluso con esta concesión, es posible que se requieran costos de hardware adicionales en cuanto a la capacidad de direccionamiento en todo el sistema de hardware para ir a tamaños de textura más grandes.

Un problema que se reproduce como texturas es muy grande es que las coordenadas de textura de punto flotante de precisión sencilla (y los interpoladores asociados para admitir la rasterización) se agotan sin precisión para especificar las ubicaciones en la superficie de forma precisa. El filtrado de textura de vibración surgiría. Una opción costosa sería requerir compatibilidad con el interpolador de precisión doble, aunque esto podría ser exageración dada una alternativa razonable.

Un nombre alternativo para los recursos en mosaico es "Texture SParte". "Disperso" transmite tanto la naturaleza en mosaico de los recursos como la principal razón para su disposición en mosaico, de modo que no se espera que se asignen todos ellos a la vez. De hecho, una aplicación puede crear un recurso en mosaico en el que no se crean datos para todas las regiones y MIPS del recurso, de forma intencionada. Por lo tanto, el propio contenido podría ser disperso y la asignación del contenido de la memoria de GPU en un momento dado sería un subconjunto de eso (más disperso).

Otro escenario que podrían atender los recursos en mosaico es habilitar varios recursos de diferentes dimensiones y formatos para compartir la misma memoria. A veces, las aplicaciones tienen conjuntos exclusivos de recursos que se sabe que no se usan al mismo tiempo, o recursos que se crean solo para un uso muy breve y, a continuación, se destruyen, seguido de la creación de otros recursos. Una forma de generalización que puede salir de "recursos en mosaico" es que es posible permitir que el usuario señale a varios recursos distintos en la misma memoria (superpuestas). En otras palabras, la creación y destrucción de "recursos" (que definen una dimensión o formato, etc.) se pueden desacoplar de la administración de la memoria subyacente a los recursos desde el punto de vista de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos en mosaico](tiled-resources.md)
</dt> </dl>

 

 