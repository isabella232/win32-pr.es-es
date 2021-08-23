---
description: Un recurso es un área en memoria a la que puede acceder la canalización de Direct3D.
ms.assetid: 24859fbc-b5e1-4963-baf8-4f083f41f39a
title: Recursos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93448fadd14d1a0849c9b730d34030b70d42a8cbc0926743e7059e222a6ea9c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567055"
---
# <a name="resources-direct3d-10"></a>Recursos (Direct3D 10)

Un recurso es un área en memoria a la que puede acceder la canalización de Direct3D. Para que la canalización acceda a la memoria de forma eficaz, los datos que se proporcionan a la canalización (como geometría de entrada, recursos de sombreador, texturas, etc.) deben almacenarse en un recurso. Hay dos tipos de recursos de los que derivan todos los recursos de Direct3D: un búfer o una textura. Se pueden activar hasta 128 recursos para cada fase de la canalización.

Cada aplicación normalmente creará muchos recursos. Algunos ejemplos de recursos son: búferes de vértices, búfer de índice, búfer constante, texturas y recursos de sombreador. Hay varias opciones que determinan cómo se pueden usar los recursos. Puede crear recursos fuertemente con tipo o que escriban menos; puede controlar si los recursos tienen acceso de lectura y escritura. puede hacer que los recursos solo puedan acceder a la CPU, LA GPU o ambos. Por supuesto, habrá una comparación de velocidad frente a funcionalidad: entre más funcionalidad permita que tenga un recurso, menor será el rendimiento que debería esperar.

Puesto que una aplicación suele usar muchas texturas, Direct3D también introduce el concepto de una matriz de texturas para simplificar la administración de texturas. Una matriz de texturas contiene una o varias texturas (todas del mismo tipo y dimensiones) que se pueden indexar desde dentro de una aplicación o mediante sombreadores. Las matrices de textura permiten usar una sola interfaz con varios índices para acceder a muchas texturas. Puede crear tantas matrices de texturas para administrar los distintos tipos de textura que necesite.

Una vez que haya creado los recursos que usará la aplicación, conecte o enlace cada recurso a las fases de canalización que los usarán. Esto se logra mediante una llamada a una API de enlace, que toma un puntero al recurso. Puesto que más de una fase de canalización puede necesitar acceso al mismo recurso, Direct3D 10 presenta el concepto de una vista de recursos. Una vista identifica la parte de un recurso al que se puede acceder. Puede crear vistas m o un recurso y enlazarlas a n fases de canalización, suponiendo que siga las reglas de enlace para el recurso compartido (el tiempo de ejecución generará errores en tiempo de compilación si no lo hace).

Una vista de recursos proporciona un modelo general para el acceso a un recurso (texturas, búferes, etc.). Dado que puede usar una vista para decir al tiempo de ejecución a qué datos acceder y cómo acceder a ellos, las vistas de recursos permiten crear menos recursos de tipo. Es decir, puede crear recursos para un tamaño determinado en tiempo de compilación y, a continuación, declarar el tipo de datos dentro del recurso cuando el recurso se enlaza a la canalización. Las vistas exponen muchas funcionalidades nuevas para usar recursos, como la capacidad de leer superficies de profundidad o galería de símbolos en el sombreador, generar mapas de cubo dinámicos en un solo paso y representarse simultáneamente en varios segmentos de un volumen.

Para más información sobre los tipos de recursos básicos, las matrices de texturas y cómo crear y usar recursos, consulte estos otros temas:

-   [Tipos de recursos](d3d10-graphics-programming-guide-resources-types.md)
-   [Elección de un recurso](d3d10-graphics-programming-guide-resources-choosing-basic.md)
-   [Creación de recursos de búfer](d3d10-graphics-programming-guide-resources-creating.md)
-   [Creación de recursos de textura](d3d10-graphics-programming-guide-resources-creating-textures.md)
-   [Copia y acceso a datos de recursos](d3d10-graphics-programming-guide-resources-mapping.md)
-   [Estructura y vistas de memoria](d3d10-graphics-programming-guide-resources-access-views.md)
-   [Compresión de bloques](d3d10-graphics-programming-guide-resources-block-compression.md)
-   [Tabla de límites de recursos](d3d10-graphics-programming-guide-resources-limits.md)
-   [Sistemas de coordenadas](d3d10-graphics-programming-guide-resources-coordinates.md)
-   [Reglas de punto flotante](d3d10-graphics-programming-guide-resources-float-rules.md)
-   [Reglas de conversión de tipos de datos](d3d10-graphics-programming-guide-resources-data-conversion.md)
-   [Asignar formatos heredados](d3d10-graphics-programming-guide-resources-legacy-formats.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



