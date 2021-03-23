---
title: Optimizaciones de la CPU de las texturas accesibles y estándar swizzle
description: Las GPU de arquitectura de memoria universal (UMA) ofrecen algunas ventajas de eficiencia frente a las GPU discretas, especialmente cuando se optimizan para dispositivos móviles.
ms.assetid: 26C41948-9625-4786-BBDF-552D1F8A2437
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47725702676d385d607fa87533680b9ffe0fc0df
ms.sourcegitcommit: 294c5ab750c46b5100bb2c84ef6c33ef7266c54b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "104549137"
---
# <a name="uma-optimizations-cpu-accessible-textures-and-standard-swizzle"></a>Optimizaciones de UMA: texturas accesibles por CPU y swizzle estándar

Las GPU de arquitectura de memoria universal (UMA) ofrecen algunas ventajas de eficiencia frente a las GPU discretas, especialmente cuando se optimizan para dispositivos móviles. La concesión de recursos de acceso de CPU cuando la GPU es UMA puede reducir la cantidad de copia que se produce entre la CPU y la GPU. Aunque no se recomienda que las aplicaciones proporcionen acceso a la CPU a todos los recursos de los diseños de UMA, existen oportunidades para mejorar las eficiencias proporcionando el acceso a la CPU de los recursos correctos. A diferencia de las GPU discretas, la CPU puede tener técnicamente un puntero a todos los recursos a los que puede tener acceso la GPU.

-   [Información general sobre las texturas accesibles de la CPU](#overview-of-cpu-accessible-textures)
-   [Información general de swizzle estándar](#overview-of-standard-swizzle)
-   [API](#apis)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-cpu-accessible-textures"></a>Información general sobre las texturas accesibles de la CPU

Las texturas accesibles por CPU, en la canalización de gráficos, son una característica de la arquitectura UMA, lo que permite que las CPU tengan acceso de lectura y escritura a las texturas. En las GPU discretas más comunes, la CPU no tiene acceso a las texturas de la canalización de gráficos.

El Consejo de prácticas recomendadas generales para las texturas es dar cabida a las GPU discretas, lo que suele implicar seguir los procesos de [carga de datos de textura a través de búferes](upload-and-readback-of-texture-data.md), resumidos como:

-   No tener acceso a la CPU para la mayoría de las texturas.
-   Establecer el diseño de textura en el \_ diseño de textura D3D12 \_ \_ desconocido.
-   Carga de las texturas en la GPU con [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

Sin embargo, en algunos casos, la CPU y la GPU pueden interactuar con tanta frecuencia en los mismos datos, que las texturas de asignación resultan útiles para ahorrar energía o para acelerar un diseño determinado en adaptadores o arquitecturas determinados. Las aplicaciones deben detectar estos casos y optimizar las copias innecesarias. En este caso, para obtener el mejor rendimiento, considere lo siguiente:

-   Solo empiece a entretener el mejor rendimiento de la asignación de texturas cuando la arquitectura de datos de características de D3D12:: Uma sea TRUE. [**\_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) A continuación, preste atención a *CacheCoherentUMA* si decide qué propiedades de la memoria caché de la CPU elegir en el montón.

-   Aprovechar el acceso a la CPU para las texturas es más complicado que en el caso de los búferes. Los diseños de textura más eficaces para las GPU no suelen ser principales de las filas \_ . De hecho, algunas GPU solo pueden admitir \_ texturas principales de fila al copiar los datos de textura.

-   Las GPU de UMA deben beneficiarse universalmente de una optimización simple para reducir los tiempos de carga de nivel. Después de reconocer UMA, la aplicación puede optimizar el [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) inicial para rellenar las texturas que la GPU no va a modificar. En lugar de crear la textura en un montón con el \_ tipo de montón D3D12 \_ \_ predeterminado y calcular las referencias de los datos de textura a través de, la aplicación puede usar [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) para evitar comprender el diseño de textura real.

-   En D3D12, las texturas creadas con \_ diseño de texturas de D3D12 \_ \_ desconocidos y sin acceso de CPU son las más eficaces para la representación y el muestreo frecuente de la GPU. Cuando se prueba el rendimiento, esas texturas se deben comparar con el \_ diseño de textura D3D12 \_ \_ desconocido con el acceso a la CPU y con el \_ estándar D3D12 \_ \_ de diseño de textura \_ SWIZZLE con acceso a la CPU y la \_ \_ \_ fila de diseño de textura D3D12 \_ principal para la compatibilidad entre adaptadores.

-   El uso \_ \_ del diseño de textura D3D12 \_ desconocido con el acceso a la CPU habilita los métodos [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource), Map (lo que impide [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)el acceso a la aplicación al puntero) y se anula la [**asignación**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) , pero puede sacrificar la eficacia del acceso a la GPU.

-   El uso \_ de D3D12 Texture \_ layout \_ estándar \_ SWIZZLE con acceso de CPU habilita [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource), [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (que devuelve un puntero válido a la [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)aplicación) y se puede desasignar. También puede sacrificar la eficacia del acceso a GPU más que el diseño de textura de D3D12 \_ \_ \_ desconocido con el acceso a la CPU.

## <a name="overview-of-standard-swizzle"></a>Información general de swizzle estándar

D3D12 (y D3D 11.3) introducen un diseño estándar de datos multidimensionales. Esto se hace para permitir que varias unidades de procesamiento operen en los mismos datos sin copiar los datos ni permutación los datos entre varios diseños. Un diseño normalizado permite mejorar la eficacia a través de los efectos de la red y permite que los algoritmos realicen cortes cortos suponiendo un patrón determinado.

Para obtener una descripción detallada de los diseños de texturas, consulte [**D3D12 \_ Texture \_ layout**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

No obstante, tenga en cuenta que esta swizzle estándar es una característica de hardware y puede que no sea compatible con todas las GPU.

Para obtener información general sobre permutación, consulte [la curva de orden Z](https://en.wikipedia.org/wiki/Z-order_curve).

## <a name="apis"></a>API

A diferencia de D3D 11.3, D3D12 admite la asignación de texturas de forma predeterminada, por lo que no es necesario consultar [**\_ \_ \_ \_ las opciones D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)de los datos de la característica D3D12. Sin embargo, D3D12 no siempre admite swizzle estándar: para consultar esta característica, se necesitará una llamada a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) y se comprobará el campo *StandardSwizzle64KBSupported* de **D3D12 \_ \_ \_ \_ Opciones** de D3D12 de datos de características.

Las siguientes API hacen referencia a la asignación de textura:

Enumeraciones

-   [**D3D12 \_ \_Diseño de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) : controla el patrón swizzle de las texturas predeterminadas y habilita la compatibilidad con asignaciones en texturas accesibles de la CPU.

Estructuras

-   [**D3D12 \_ \_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) . del recurso: describe un recurso, como una textura, que es una estructura que se usa con mucha frecuencia.
-   [**D3D12 \_ HEAP \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) : describe un montón.

Métodos

-   [**ID3D12Device:: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) : crea un único recurso y un montón de respaldo del tamaño y la alineación correctos.
-   [**ID3D12Device:: CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap) : crea un montón para un búfer o textura.
-   [**ID3D12Device:: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) : crea un recurso que se coloca en un montón específico, normalmente un método más rápido para crear un recurso que [**CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap).
-   [**ID3D12Device:: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource) : crea un recurso que está reservado pero que todavía no se ha confirmado ni colocado en un montón.
-   [**ID3D12CommandQueue:: UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : actualiza las asignaciones de ubicaciones de iconos en recursos en mosaico a ubicaciones de memoria en un montón de recursos.
-   [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : obtiene un puntero a los datos especificados en el recurso y deniega el acceso de la GPU al subrecurso.
-   [**ID3D12Resource:: GetDesc**](id3d12resource-getdesc.md) : obtiene las propiedades del recurso.
-   [**ID3D12Heap:: GetDesc**](id3d12heap-getdesc.md) obtiene las propiedades del montón.
-   [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copia datos de una textura que se asignó mediante [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).
-   [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copia los datos en una textura que se asignó mediante [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).

Los recursos y los montones primarios tienen requisitos de alineación:

-   D3D12 \_ \_ \_ \_ \_ : alineación de ubicación de recursos de MSAA predeterminada (4MB) para texturas de varios ejemplos.
-   D3D12 \_ \_ \_ \_ : alineación de ubicación de recursos predeterminada (64 KB) para texturas y búferes de ejemplo únicos.
-   La copia de Subrecursos lineal debe estar alineada con la alineación de colocación de datos de textura de D3D12 \_ \_ \_ \_ (512 bytes), con un paso de fila alineado con la alineación de tono de datos de D3D12 \_ \_ \_ \_ (256 bytes).
-   Las vistas de búfer de constantes se deben alinear con la \_ alineación de colocación de datos de búfer constante D3D12 \_ \_ \_ \_ (256 bytes).

Las texturas menores que 64 KB se deben procesar a través de [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

Con las texturas dinámicas (texturas que cambian cada fotograma), la CPU escribirá linealmente en el montón de carga, seguida de una operación de copia de GPU.

Normalmente, para crear recursos dinámicos, cree un búfer grande en un montón de carga (consulte [subasignación dentro de búferes](large-buffers.md)). Para crear recursos de almacenamiento provisional, cree un búfer grande en un montón de readback. Para crear recursos estáticos predeterminados, cree recursos adyacentes en un montón predeterminado. Para crear recursos con alias predeterminados, cree recursos superpuestos en un montón predeterminado.

[**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) y [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) reorganizan los datos de textura entre un diseño de fila principal y un diseño de recursos sin definir. La operación es sincrónica, por lo que la aplicación debe tener en cuenta la programación de la CPU. La aplicación siempre puede dividir la copia en regiones más pequeñas o programar esta operación en otra tarea. Las operaciones de copia de la CPU no admiten los recursos de MSAA y los recursos de estarcido de profundidad con diseños de recursos opacos y se producirá un error. Tampoco se admiten los formatos que no tienen un tamaño de elemento de potencia de dos y también producirán un error. Se pueden producir códigos de retorno de memoria insuficiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes básicas**](constants.md)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

 




