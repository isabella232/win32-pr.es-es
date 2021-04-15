---
description: Un recurso es un área en memoria a la que puede acceder la canalización de Direct3D.
ms.assetid: 24859fbc-b5e1-4963-baf8-4f083f41f39a
title: Recursos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bb064bc771e36335527d68891bc76a1ce4df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496445"
---
# <a name="resources-direct3d-10"></a>Recursos (Direct3D 10)

Un recurso es un área en memoria a la que puede acceder la canalización de Direct3D. Para que la canalización tenga acceso a la memoria de forma eficaz, los datos que se proporcionan a la canalización (como la geometría de entrada, los recursos del sombreador, las texturas, etc.) deben almacenarse en un recurso. Hay dos tipos de recursos de los que derivan todos los recursos de Direct3D: un búfer o una textura. Se pueden activar hasta 128 recursos para cada fase de la canalización.

Cada aplicación creará normalmente muchos recursos. Entre los ejemplos de recursos se incluyen: búferes de vértices, búfer de índice, búfer de constantes, texturas y recursos de sombreador. Hay varias opciones que determinan cómo se pueden usar los recursos. Puede crear recursos fuertemente tipados o tipos menos; puede controlar si los recursos tienen acceso de lectura y escritura. puede hacer que los recursos sean accesibles solo para la CPU, la GPU o ambos. Naturalmente, habrá equilibrio entre la velocidad y la funcionalidad: la mayor funcionalidad que permite que tenga un recurso, el menor rendimiento que debería esperar.

Dado que una aplicación suele usar muchas texturas, Direct3D también presenta el concepto de una matriz de textura para simplificar la administración de texturas. Una matriz de textura contiene una o varias texturas (todas del mismo tipo y dimensiones) que se pueden indizar desde dentro de una aplicación o mediante sombreadores. Las matrices de textura permiten usar una sola interfaz con varios índices para tener acceso a muchas texturas. Puede crear tantas matrices de texturas para administrar distintos tipos de texturas según sea necesario.

Una vez que haya creado los recursos que va a usar la aplicación, conecte o enlace cada recurso a las fases de canalización que los usarán. Esto se logra mediante una llamada a una API de enlace, que toma un puntero al recurso. Dado que es posible que más de una fase de canalización necesite tener acceso al mismo recurso, Direct3D 10 presenta el concepto de una vista de recursos. Una vista identifica la parte de un recurso al que se puede tener acceso. Puede crear vistas m o un recurso y enlazarlos a las fases de canalización n, suponiendo que sigue las reglas de enlace para recursos compartidos (el tiempo de ejecución generará errores en tiempo de compilación si no lo está).

Una vista de recursos proporciona un modelo general para el acceso a un recurso (texturas, búferes, etc.). Dado que puede usar una vista para indicar al tiempo de ejecución los datos a los que acceder y cómo obtener acceso a ellos, las vistas de recursos le permiten crear tipos menos recursos. Es decir, puede crear recursos para un tamaño determinado en tiempo de compilación y, a continuación, declarar el tipo de datos dentro del recurso cuando el recurso se enlaza a la canalización. Las vistas exponen muchas funciones nuevas para el uso de recursos, como la capacidad de leer las superficies de fondo o de la galería de símbolos en el sombreador, generar cubemaps dinámicos en un solo paso y representar simultáneamente en varios segmentos de un volumen.

Para obtener más información sobre los tipos de recursos básicos, las matrices de texturas y cómo crear y usar recursos, consulte estos otros temas:

-   [Tipos de recursos](d3d10-graphics-programming-guide-resources-types.md)
-   [Elección de un recurso](d3d10-graphics-programming-guide-resources-choosing-basic.md)
-   [Crear recursos de búfer](d3d10-graphics-programming-guide-resources-creating.md)
-   [Crear recursos de textura](d3d10-graphics-programming-guide-resources-creating-textures.md)
-   [Copiar y obtener acceso a los datos de recursos](d3d10-graphics-programming-guide-resources-mapping.md)
-   [Estructura y vistas de memoria](d3d10-graphics-programming-guide-resources-access-views.md)
-   [Compresión de bloque](d3d10-graphics-programming-guide-resources-block-compression.md)
-   [Tabla de límites de recursos](d3d10-graphics-programming-guide-resources-limits.md)
-   [Sistemas de coordenadas](d3d10-graphics-programming-guide-resources-coordinates.md)
-   [Reglas de punto flotante](d3d10-graphics-programming-guide-resources-float-rules.md)
-   [Reglas de conversión de tipos de datos](d3d10-graphics-programming-guide-resources-data-conversion.md)
-   [Asignar formatos heredados](d3d10-graphics-programming-guide-resources-legacy-formats.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



