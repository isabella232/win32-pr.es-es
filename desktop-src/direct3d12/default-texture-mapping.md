---
title: Optimizaciones de UMA Texturas accesibles de CPU y Swzzle estándar
description: Las GPU de arquitectura de memoria universal (UMA) ofrecen algunas ventajas de eficiencia con respecto a las GPU discretas, especialmente cuando se optimizan para dispositivos móviles.
ms.assetid: 26C41948-9625-4786-BBDF-552D1F8A2437
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47725702676d385d607fa87533680b9ffe0fc0df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359812"
---
# <a name="uma-optimizations-cpu-accessible-textures-and-standard-swizzle"></a>Optimizaciones de UMA: texturas accesibles por CPU y referencias estándar

Las GPU de arquitectura de memoria universal (UMA) ofrecen algunas ventajas de eficiencia con respecto a las GPU discretas, especialmente cuando se optimizan para dispositivos móviles. Proporcionar a los recursos acceso a la CPU cuando la GPU es UMA puede reducir la cantidad de copia que se produce entre la CPU y la GPU. Aunque no se recomienda que las aplicaciones den acceso a la CPU a todos los recursos en los diseños de UMA, hay oportunidades para mejorar la eficacia al proporcionar a los recursos adecuados acceso a la CPU. A diferencia de las GPU discretas, la CPU puede tener técnicamente un puntero a todos los recursos a los que la GPU puede acceder.

-   [Información general sobre las texturas accesibles para LA CPU](#overview-of-cpu-accessible-textures)
-   [Información general de Swzzle estándar](#overview-of-standard-swizzle)
-   [API](#apis)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-cpu-accessible-textures"></a>Información general sobre las texturas accesibles para LA CPU

Las texturas accesibles para la CPU, en la canalización de gráficos, son una característica de la arquitectura UMA, que permite el acceso de lectura y escritura de CPU a las texturas. En las GPU discretas más comunes, la CPU no tiene acceso a texturas en la canalización de gráficos.

El procedimiento recomendado general para las texturas es dar cabida a [](upload-and-readback-of-texture-data.md)GPU discretas, lo que normalmente implica seguir los procesos de Carga de datos de textura a través de búferes, resumidos como:

-   No tener ningún acceso de CPU para la mayoría de las texturas.
-   Establecer el diseño de textura en D3D12 \_ TEXTURE \_ LAYOUT \_ UNKNOWN.
-   Cargar las texturas en la GPU [**con CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

Sin embargo, en determinados casos, la CPU y la GPU pueden interactuar con tanta frecuencia en los mismos datos, que la asignación de texturas resulta útil para ahorrar energía o para acelerar un diseño determinado en determinados adaptadores o arquitecturas. Las aplicaciones deben detectar estos casos y optimizar las copias innecesarias. En este caso, para obtener el mejor rendimiento, tenga en cuenta lo siguiente:

-   Comience a disfrutar del mejor rendimiento de las texturas de asignación cuando [**D3D12 \_ FEATURE \_ DATA \_ ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture)::UMA sea TRUE. A continuación, preste atención *a CacheCoherentUMA si* decide qué propiedades de caché de CPU elegir en el montón.

-   Aprovechar el acceso a la CPU para texturas es más complicado que para los búferes. Los diseños de textura más eficaces para las GPU rara vez son de fila \_ principal. De hecho, algunas GPU solo pueden admitir texturas principales de \_ fila al copiar datos de textura.

-   Las GPU de UMA deben beneficiarse universalmente de una optimización sencilla para reducir los tiempos de carga de nivel. Después de reconocer UMA, la aplicación puede optimizar la [**copyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) inicial para rellenar texturas que la GPU no modificará. En lugar de crear la textura en un montón con D3D12 HEAP TYPE DEFAULT y obtener los datos de textura a través de , la aplicación puede usar \_ \_ \_ [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) para evitar comprender el diseño de textura real.

-   En D3D12, las texturas creadas con D3D12 TEXTURE LAYOUT UNKNOWN y sin acceso de CPU son las más eficaces para la representación y el muestreo frecuentes \_ \_ de \_ GPU. Al realizar pruebas de rendimiento, esas texturas deben compararse con D3D12 TEXTURE LAYOUT UNKNOWN con acceso \_ \_ a \_ CPU, D3D12 TEXTURE LAYOUT STANDARD SW FINES CON ACCESO A LA CPU y \_ \_ \_ \_ D3D12 \_ TEXTURE LAYOUT ROW MAJOR \_ \_ \_ para la compatibilidad entre adaptadores.

-   El uso de D3D12 TEXTURE LAYOUT UNKNOWN con acceso de CPU permite los métodos \_ \_ \_ [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (que excluye el acceso de la aplicación al puntero) y [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap); pero puede sacrificar la eficacia del acceso a GPU.

-   El uso de D3D12 TEXTURE LAYOUT STANDARD SWLINOLE con acceso de CPU habilita \_ \_ \_ \_ [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (que [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)devuelve un puntero válido a la aplicación) y Unmap . También puede sacrificar la eficacia del acceso a GPU más que D3D12 \_ TEXTURE LAYOUT UNKNOWN con acceso a la \_ \_ CPU.

## <a name="overview-of-standard-swizzle"></a>Información general de Swzzle estándar

D3D12 (y D3D11.3) presentan un diseño de datos multidimensional estándar. Esto se hace para permitir que varias unidades de procesamiento funcionen en los mismos datos sin copiar los datos ni deslizarlos entre varios diseños. Un diseño estandarizado permite mejorar la eficacia a través de los efectos de red y permite que los algoritmos realicen cortas reducciones suponiendo un patrón determinado.

Para obtener una descripción detallada de los diseños de textura, consulte [**D3D12 \_ TEXTURE \_ LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

Sin embargo, tenga en cuenta que este swzzle estándar es una característica de hardware y es posible que no sea compatible con todas las GPU.

Para obtener información general sobre el desdobado, consulte [curva de orden Z.](https://en.wikipedia.org/wiki/Z-order_curve)

## <a name="apis"></a>API existentes

A diferencia de D3D11.3, D3D12 admite la asignación de texturas de forma predeterminada, por lo que no es necesario consultar [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Sin embargo, D3D12 no siempre es compatible con swuitle estándar: esta característica deberá consultarse para con una llamada a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) y comprobar el campo *StandardSwzolle64KBSupported* de **D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**.

Las siguientes API hacen referencia a la asignación de texturas:

Enumeraciones

-   [**D3D12 \_ DISEÑO \_ DE TEXTURA:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) controla el patrón swzzle de texturas predeterminadas y habilita la compatibilidad con mapas en texturas accesibles para cpu.

Estructuras

-   [**D3D12 \_ RESOURCE \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) describe un recurso, como una textura, que es una estructura ampliamente usada.
-   [**D3D12 \_ HEAP \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) describe un montón.

Métodos

-   [**ID3D12Device::CreateCommittedResource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) crea un único recurso y un montón de respaldo del tamaño y la alineación correctos.
-   [**ID3D12Device::CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap) : crea un montón para un búfer o textura.
-   [**ID3D12Device::CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) : crea un recurso que se coloca en un montón específico, normalmente un método más rápido para crear un recurso que [**CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap).
-   [**ID3D12Device::CreateReservedResource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource) crea un recurso que está reservado pero que aún no se ha confirmado ni colocado en un montón.
-   [**ID3D12CommandQueue::UpdateTileMappings:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) actualiza las asignaciones de ubicaciones de mosaico de recursos en mosaico a ubicaciones de memoria de un montón de recursos.
-   [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : obtiene un puntero a los datos especificados en el recurso y deniega el acceso de GPU al subrecurso.
-   [**ID3D12Resource::GetDesc**](id3d12resource-getdesc.md) : obtiene las propiedades del recurso.
-   [**ID3D12Heap::GetDesc obtiene**](id3d12heap-getdesc.md) las propiedades del montón.
-   [**ReadFromSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) copia los datos de una textura que se asignó mediante [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).
-   [**WriteToSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) copia los datos en una textura que se asignó mediante [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).

Los recursos y los montones primarios tienen requisitos de alineación:

-   D3D12 \_ DEFAULT \_ MSAA \_ RESOURCE PLACEMENT ALIGNMENT \_ (4MB) for multi-sample textures (ALINEACIÓN PREDETERMINADA DE COLOCACIÓN DE RECURSOS DE MSAA de D3D12[4 \_ MB]) para texturas de varias muestras.
-   D3D12 \_ DEFAULT RESOURCE PLACEMENT ALIGNMENT \_ \_ \_ (64 KB) para texturas y búferes de ejemplo únicos.
-   La copia de subrecursos lineal debe alinearse con D3D12 TEXTURE DATA PLACEMENT ALIGNMENT (512 bytes), con el paso de fila alineado con \_ \_ \_ \_ D3D12 \_ TEXTURE DATA PITCH ALIGNMENT \_ \_ \_ (256 bytes).
-   Las vistas de búfer constante deben alinearse con D3D12 \_ CONSTANT BUFFER DATA PLACEMENT ALIGNMENT \_ \_ \_ \_ (256 bytes).

Las texturas menores de 64 KB se deben procesar a través [**de CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

Con texturas dinámicas (texturas que cambian cada fotograma), la CPU escribirá linealmente en el montón de carga, seguida de una operación de copia de GPU.

Normalmente, para crear recursos dinámicos, cree un búfer grande en un montón de carga (consulte [Suballocation Within Buffers](large-buffers.md)). Para crear recursos de almacenamiento provisional, cree un búfer grande en un montón de readback. Para crear recursos estáticos predeterminados, cree recursos adyacentes en un montón predeterminado. Para crear recursos con alias predeterminados, cree recursos superpuestos en un montón predeterminado.

[**WriteToSubresource y**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) reorganizan los datos de textura entre un diseño principal de fila y un diseño de recursos sin definir. La operación es sincrónica, por lo que la aplicación debe tener en cuenta la programación de CPU. La aplicación siempre puede dividir la copia en regiones más pequeñas o programar esta operación en otra tarea. Estas operaciones de copia de CPU no admiten recursos de MSAA y recursos de galería de símbolos de profundidad con diseños de recursos opacos y provocarán un error. Los formatos que no tienen un tamaño de potencia de dos elementos tampoco se admiten y también provocarán un error. Pueden producirse códigos de retorno de memoria no memoria.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes principales**](constants.md)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

 




