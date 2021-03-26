---
title: API de recursos en mosaico
description: Las API descritas en esta sección funcionan con los recursos en mosaico y el grupo de mosaicos.
ms.assetid: 02DCF9BA-F9EA-4176-AD6F-AA620CE968BA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0d97f5272f4f96db56e6e89b871951de035105
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418424"
---
# <a name="tiled-resource-apis"></a>API de recursos en mosaico

Las API descritas en esta sección funcionan con los recursos en mosaico y el grupo de mosaicos.

-   [Asignar iconos de un grupo de mosaicos a un recurso](#assigning-tiles-from-a-tile-pool-to-a-resource)
-   [Consultar el mosaico de recursos y el soporte técnico](#querying-resource-tiling-and-support)
-   [Copiar datos en mosaico](#copying-tiled-data)
-   [Cambiar el tamaño del grupo de mosaicos](#resizing-tile-pool)
-   [Barrera de recursos en mosaico](#tiled-resource-barrier)
-   [Temas relacionados](#related-topics)

## <a name="assigning-tiles-from-a-tile-pool-to-a-resource"></a>Asignar iconos de un grupo de mosaicos a un recurso

Las API [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) y [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) manipulan y consultan asignaciones de iconos. Las llamadas de actualización solo afectan a los iconos identificados en la llamada y otros se quedan como se definieron anteriormente.

Cualquier mosaico determinado de un grupo de mosaicos se puede asignar a varias ubicaciones de un recurso e incluso a varios recursos. Esta asignación incluye mosaicos en un recurso que tienen un diseño elegido por la implementación ([empaquetado de mipmap](mipmap-packing.md)) en el que varios mapas de bits se empaquetan juntos en un solo mosaico. La captura es que, si los datos se escriben en el icono mediante una asignación, pero se leen a través de una asignación configurada de forma diferente, los resultados son indefinidos. Sin embargo, el uso meticuloso de esta flexibilidad puede seguir siendo útil para una aplicación, como el uso compartido de un icono entre recursos que no se usarán simultáneamente, donde el contenido del icono siempre se inicializa a través de la misma asignación de recursos, ya que se leerán posteriormente. Del mismo modo, un icono asignado para contener los mapas de bits empaquetados de varios recursos diferentes con las mismas dimensiones de superficie funcionará correctamente: los datos aparecerán de la misma forma en ambas asignaciones.

Los cambios en las asignaciones de mosaicos de un recurso se pueden realizar en cualquier momento en un contexto inmediato o diferido.

## <a name="querying-resource-tiling-and-support"></a>Consultar el mosaico de recursos y el soporte técnico

Para consultar el mosaico de recursos, use [**ID3D11Device2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling).

Para la compatibilidad con otros mosaicos de recursos, use [**ID3D11Device2:: CheckMultisampleQualityLevels1**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-checkmultisamplequalitylevels1).

## <a name="copying-tiled-data"></a>Copiar datos en mosaico

Cualquier método de Direct3D para mover los datos en torno al trabajo con recursos en mosaico es como si no estuvieran en mosaico, con la excepción de que las escrituras en áreas sin asignar se quitan y las lecturas de áreas sin asignar producen 0. Si una operación de copia implica la escritura en la misma ubicación de memoria varias veces, ya que se asignan varias ubicaciones en el recurso de destino a la misma memoria de mosaico, las escrituras resultantes en mosaicos multiasignados son no deterministas y no repetibles. Es decir, los accesos se producen en cualquier orden en el que se produzca el hardware para ejecutar la copia.

Direct3D 11,2 presenta métodos para estas otras maneras de copiar:

-   Copiar entre mosaicos en un recurso en mosaico (con granularidad de mosaico de 64 KB) y (hacia/desde) un búfer en memoria de la unidad de procesamiento de gráficos (GPU) (o recurso de almacenamiento provisional)- [ **ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   Copia de la memoria proporcionada por la aplicación en mosaicos en un recurso en mosaico: [ **ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)

Estos métodos swizzle/deswizzle según sea necesario y permiten que una \_ \_ copia \_ en mosaico de D3D11 no \_ sobrescriba la marca cuando el autor de la llamada promete que el trabajo de GPU no hace referencia a la memoria de destino en el vuelo.

Los mosaicos implicados en la copia no pueden incluir mosaicos que contengan mapas MIP empaquetados o que tengan resultados sin definir. Para transferir datos hacia y desde los mapas de hardware a un mosaico, debe usar las API de copia/actualización estándar (no específicas del mosaico) o [**ID3D11DeviceContext:: GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) para toda la cadena de MIP.

**Nota en [**GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips):** el uso de [**ID3D11DeviceContext:: GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) en un recurso con mosaicos parcialmente asignados producirá resultados que simplemente siguen las reglas de lectura y escritura de **valores NULL** aplicados a cualquier algoritmo que el hardware y el controlador de pantalla tengan que usar para **GenerateMips**. Por lo tanto, no es especialmente útil para que una aplicación se moleste en hacer esto, a menos que las áreas con asignaciones **null** (y su efecto en otro MIPS durante la fase de generación) no tengan ninguna consecuencia en las partes de la superficie sobre las que la aplicación se preocupa.

La copia de los datos del icono desde una superficie de ensayo o desde la memoria de la aplicación sería la manera de cargar los mosaicos que se pueden haber transmitido fuera del disco, por ejemplo. Una variación cuando la transmisión fuera del disco es la carga de algún tipo de datos comprimidos en la memoria de GPU y, después, la descodificación en la GPU. El destino de descodificación podría ser un recurso de búfer en la memoria de GPU, desde el que [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) copia en el recurso en mosaico real. Este paso de copia permite que la GPU se swizzle cuando no se conoce el patrón swizzle. Permutación no es necesario si el propio recurso en mosaico es un recurso de búfer (por ejemplo, en lugar de una textura).

El diseño de memoria de los mosaicos en el lado del recurso de búfer no en mosaico de la copia es simplemente lineal en la memoria en los mosaicos de 64 KB, que el hardware y el controlador de pantalla swizzlen/deswizzle por cada mosaico según corresponda al transferirlos a un recurso en mosaico o desde este. En el caso de las superficies de suavizado de contorno de muestreo múltiple (MSAA), los ejemplos de cada píxel se recorren en orden de índice de muestra antes de pasar al siguiente píxel. En el caso de los mosaicos que se rellenan parcialmente en el lado derecho (para una superficie que tenga un ancho que no sea un múltiplo del ancho del mosaico en píxeles), el paso o el paso para bajar una fila es el tamaño total en bytes del número de píxeles que cabrían en el mosaico si el icono estaba lleno. Por lo tanto, puede haber un intervalo entre cada fila de píxeles en la memoria. Para simplificar la especificación, los mapas de tiempo menores que un mosaico no se empaquetan en el diseño lineal. Esto parece ser un desperdicio de espacio en memoria, pero como se mencionó en la copia a MIPS que los paquetes de hardware juntos no se permiten a través de [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) o [**UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles). La aplicación puede usar simplemente las \* API UpdateSubresource () o CopySubresource \* () genéricas para copiar Small MIPS de forma individual, aunque en el caso de CopySubresource \* (), lo que significa que la memoria lineal debe ser la misma dimensión que el recurso en mosaico-CopySubresource \* () no puede copiar desde un recurso de búfer a una Texture2D por ejemplo.

Si se define un swizzle estándar de hardware, se pueden agregar marcas para indicar que los datos del búfer deben interpretarse en ese formato (no swizzle necesario en la transferencia), aunque los enfoques alternativos para cargar datos también pueden tener sentido en ese caso, como permitir que las aplicaciones tengan acceso directo a la memoria del grupo de mosaicos.

Las operaciones de copia se pueden realizar en un contexto inmediato o diferido.

## <a name="resizing-tile-pool"></a>Cambiar el tamaño del grupo de mosaicos

Para cambiar el tamaño de un grupo de mosaicos, use [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool).

## <a name="tiled-resource-barrier"></a>Barrera de recursos en mosaico

Para especificar una restricción de ordenación de acceso a datos entre varios recursos en mosaico, use [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos en mosaico](tiled-resources.md)
</dt> </dl>

 

 




