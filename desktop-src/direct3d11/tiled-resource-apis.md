---
title: API de recursos en mosaico
description: Las API descritas en esta sección funcionan con recursos en mosaico y un grupo de mosaicos.
ms.assetid: 02DCF9BA-F9EA-4176-AD6F-AA620CE968BA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f433b6c70d475d4da511b85fdcc2b1c273de1efa8e1186215b25ce6b9b95d0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894395"
---
# <a name="tiled-resource-apis"></a>API de recursos en mosaico

Las API descritas en esta sección funcionan con recursos en mosaico y un grupo de mosaicos.

-   [Asignación de iconos de un grupo de iconos a un recurso](#assigning-tiles-from-a-tile-pool-to-a-resource)
-   [Consulta de la compatibilidad y el uso de tilings de recursos](#querying-resource-tiling-and-support)
-   [Copia de datos en mosaico](#copying-tiled-data)
-   [Redimensionamiento del grupo de mosaicos](#resizing-tile-pool)
-   [Barrera de recursos en mosaico](#tiled-resource-barrier)
-   [Temas relacionados](#related-topics)

## <a name="assigning-tiles-from-a-tile-pool-to-a-resource"></a>Asignación de iconos de un grupo de iconos a un recurso

Las [**API ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) e [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) manipulan y consultan asignaciones de mosaicos. Las llamadas de actualización solo afectan a los iconos identificados en la llamada y otras se quedan como se definió anteriormente.

Cualquier icono determinado de un grupo de mosaicos se puede asignar a varias ubicaciones de un recurso e incluso a varios recursos. Esta asignación incluye iconos en un recurso que tienen un diseño elegido por la implementación (empaquetado de[Mipmap)](mipmap-packing.md)donde varios mapas MIP se empaquetan juntos en un solo icono. El problema es que si los datos se escriben en el icono a través de una asignación, pero se leen a través de una asignación configurada de forma diferente, los resultados no están definidos. Sin embargo, usar cuidadosamente esta flexibilidad puede ser útil para una aplicación, como compartir un icono entre recursos que no se usarán simultáneamente, donde el contenido del icono siempre se inicializa a través de la misma asignación de recursos desde la que se leerán posteriormente. De forma similar, un icono asignado para contener los mapas MIP empaquetados de varios recursos diferentes con las mismas dimensiones de superficie funcionará correctamente: los datos aparecerán iguales en ambas asignaciones.

Los cambios en las asignaciones de mosaicos de un recurso se pueden realizar en cualquier momento en un contexto inmediato o diferido.

## <a name="querying-resource-tiling-and-support"></a>Consulta de la compatibilidad y el uso de tilings de recursos

Para consultar el etiquetado de recursos, use [**ID3D11Device2::GetResourceTiling.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)

Para otra compatibilidad con el uso de tilings de recursos, use [**ID3D11Device2::CheckMultisampleQualityLevels1**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-checkmultisamplequalitylevels1).

## <a name="copying-tiled-data"></a>Copia de datos en mosaico

Los métodos de Direct3D para mover datos funcionan con recursos en mosaico igual que si no se hubieran en mosaico, salvo que las escrituras en áreas sin asociar se descartan y las lecturas de áreas no recortadas generan 0. Si una operación de copia implica escribir varias veces en la misma ubicación de memoria porque varias ubicaciones del recurso de destino están asignadas a la misma memoria de mosaico, las escrituras resultantes en iconos multiasignados no son deterministas ni repetibles. Es decir, los accesos se produce en el orden en que el hardware ejecuta la copia.

Direct3D 11.2 presenta métodos para estas formas adicionales de copiar:

-   Copiar entre iconos de un recurso en mosaico (con una granularidad de mosaico de 64 KB) y (hacia y desde) un búfer en memoria de unidad de procesamiento gráfico (GPU) (o recurso de almacenamiento provisional) - [ **ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   Copia de la memoria proporcionada por la aplicación en iconos de un recurso en mosaico: [ **ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)

Estos métodos sw fax/desw fax según sea necesario y permiten una marca D3D11 TILE COPY NO OVERWRITE cuando el autor de la llamada prometa que el trabajo de GPU que está en marcha no hace referencia a la memoria de \_ \_ \_ \_ destino.

Los iconos implicados en la copia no pueden incluir iconos que contengan mapas MIP empaquetados o que tengan resultados que no estén definidos. Para transferir datos hacia y desde mipmaps que los paquetes de hardware empaquetan en un icono, debe usar las API de copia/actualización estándar (no específicas del icono) o [**ID3D11DeviceContext::GenerateMips para**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) toda la cadena mip.

**Nota en [**GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips):** Using [**ID3D11DeviceContext::GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) on a resource with partially mapped tiles will produce results that simply follow the rules for reading and writing **NULL** applied to whatever algorithm the hardware and display driver happen to use to **GenerateMips**. Por lo tanto, no es especialmente útil para una aplicación preocuparse de hacerlo a menos que, de algún modo, las áreas con asignaciones **NULL** (y su efecto en otros mips durante la fase de generación) no tengan ninguna consecuencia en las partes de la superficie que sí le importan a la aplicación.

Copiar datos de mosaico desde una superficie de almacenamiento provisional o desde la memoria de la aplicación sería la manera de cargar iconos que pueden haber sido transmitidos fuera del disco, por ejemplo. Una variación al transmitir fuera del disco es cargar algún tipo de datos comprimidos en la memoria de GPU y, a continuación, decodificar en la GPU. El destino de descodificación podría ser un recurso de búfer en memoria de GPU, desde el que [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) copia en el recurso en mosaico real. Este paso de copia permite que la GPU se desvía cuando no se conoce el patrón sw fax. No es necesario deslizar el dedo si el propio recurso en mosaico es un recurso de búfer (por ejemplo, en lugar de una textura).

El diseño de memoria de los iconos en el lado del recurso de búfer no en mosaico de la copia es simplemente lineal en memoria dentro de los mosaicos de 64 KB, que el hardware y el controlador de pantalla deslizarían o desconsejaban por icono según corresponda al transferir a o desde un recurso en mosaico. En el caso de las superficies de suavizado de contorno de múltiples muestras (MSAA), las muestras de cada píxel se recorren en orden de índice de muestra antes de pasar al píxel siguiente. En el caso de los mosaicos que se rellenan parcialmente en el lado derecho (para una superficie que tiene un ancho distinto de un múltiplo de ancho de mosaico en píxeles), el paso o el paso para bajar una fila es el tamaño completo en bytes de los píxeles de número que caben en el mosaico si el icono estaba lleno. Por lo tanto, puede haber un intervalo entre cada fila de píxeles en la memoria. Para simplificar las especificaciones, los mapas MIP más pequeños que un icono no se empaquetan juntos en el diseño lineal. Parece ser una pérdida de espacio de memoria, pero como se mencionó al copiar en mips que los paquetes de hardware juntos no se permiten a través de [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) [**o UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles). La aplicación solo puede usar las API UpdateSubresource () o CopySubresource () genéricas para copiar mips pequeños individualmente, aunque en el caso de CopySubresource (), esto significa que la memoria lineal tiene que ser la misma dimensión que el recurso en mosaico: CopySubresource () no puede copiar desde un recurso de búfer \* \* a \* \* texture2D, por ejemplo.

Si se define un swzzle estándar de hardware, se podrían agregar marcas para indicar que los datos del búfer se van a interpretar en ese formato (no es necesario deslizar nada en la transferencia), aunque los enfoques alternativos para cargar datos también pueden tener sentido en ese caso, como permitir que las aplicaciones accedan directamente a la memoria del grupo de mosaicos.

Las operaciones de copia se pueden realizar en un contexto inmediato o diferido.

## <a name="resizing-tile-pool"></a>Redimensionamiento del grupo de mosaicos

Para cambiar el tamaño de un grupo de mosaicos, use [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool).

## <a name="tiled-resource-barrier"></a>Barrera de recursos en mosaico

Para especificar una restricción de ordenación de acceso a datos entre varios recursos en mosaico, use [**ID3D11DeviceContext2::TiledResourceBardevice .**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos en mosaico](tiled-resources.md)
</dt> </dl>

 

 




