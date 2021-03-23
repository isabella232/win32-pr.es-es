---
title: Residencia
description: Un objeto se considera residente cuando es accesible para la GPU.
ms.assetid: 956F80D7-EEC8-4D88-B251-EE325614F31E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b842ce5b3e89c3877f50036e747a90f14104bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549146"
---
# <a name="residency"></a>Residencia

Un objeto se considera *residente* cuando es accesible para la GPU.

-   [Presupuesto de residencia](#residency-budget)
-   [Recursos del montón](#heap-resources)
-   [Prioridades de residencia](#residency-priorities)
    -   [Algoritmo de prioridad predeterminado](#default-priority-algorithm)
-   [Administración de la residencia de programación](#programming-residency-management)
-   [Temas relacionados](#related-topics)

## <a name="residency-budget"></a>Presupuesto de residencia

Las GPU todavía no admiten errores de página, por lo que las aplicaciones deben confirmar los datos en la memoria física mientras la GPU podría acceder a ella. Este proceso se conoce como "crear un elemento residente" y debe realizarse tanto para la memoria física del sistema como para la memoria física de vídeo independiente. En D3D12, la mayoría de los objetos de API encapsulan cierta cantidad de memoria accesible desde GPU. Esa memoria accesible mediante GPU se hace residente durante la creación del objeto de API y se expulsa en la destrucción de objetos de la API.

La cantidad de memoria física disponible para el proceso se conoce como el presupuesto de memoria de vídeo. El presupuesto puede fluctuar notablemente a medida que los procesos en segundo plano se reactivan y suspenden. y fluctúan drásticamente cuando el usuario cambia a otra aplicación. Se puede notificar a la aplicación cuando el presupuesto cambie y sondee el presupuesto actual y la cantidad de memoria consumida actualmente. Si una aplicación no se mantiene dentro de su presupuesto, el proceso se inmovilizará intermitentemente para permitir que se ejecuten otras aplicaciones y/o las API de creación devolverán un error. La interfaz [**IDXGIAdapter3**](/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) proporciona los métodos que pertenecen a esta funcionalidad, en particular [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) y [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Se recomienda que las aplicaciones usen una reserva para denotar la cantidad de memoria a la que no pueden ir. Idealmente, la configuración de gráficos "Low" especificada por el usuario, o algo más baja, es el valor correcto para dicha reserva. La configuración de una reserva no proporcionará nunca a una aplicación un presupuesto superior al que normalmente recibiría. En su lugar, la información de reserva ayuda al kernel del sistema operativo a minimizar rápidamente el impacto de las situaciones de presión de memoria de gran tamaño. Incluso no se garantiza que la reserva esté disponible para la aplicación cuando la aplicación no es la aplicación en primer plano.

## <a name="heap-resources"></a>Recursos del montón

Aunque muchos objetos de API encapsulan algunas memoria accesible por GPU, se espera que los montones & recursos sean la forma más significativa de usar y administrar la memoria física. Un montón es la unidad de nivel más bajo para administrar la memoria física, por lo que es conveniente estar familiarizado con sus propiedades de residencia.

-   Los montones no se pueden hacer residentes parcialmente, pero existen soluciones con recursos reservados.
-   Los montones deben presupuestarse como parte de un grupo determinado. Los adaptadores de UMA tienen un grupo, mientras que los adaptadores discretos tienen dos grupos. Aunque es cierto que el kernel puede desplazar algunos montones en adaptadores discretos de la memoria de vídeo a la memoria del sistema, solo lo hace como último recurso. Las aplicaciones no deben basarse en el comportamiento de exceso de presupuesto del kernel y deben centrarse en la buena administración del presupuesto.
-   Los montones se pueden desalojar de la residencia, lo que permite que el contenido se desproteja en el disco. Sin embargo, la destrucción de montones es una técnica más confiable para liberar la residencia en todas las arquitecturas de adaptador. En los adaptadores en los que el campo *theMaxGPUVirtualAddressBitsPerProcess* de la [**\_ \_ \_ \_ \_ \_ compatibilidad de dirección virtual de GPU de datos de características de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support) está cerca del tamaño de presupuesto, la [**expulsión**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict) no reclamará de manera confiable la residencia.
-   La creación del montón puede ser lenta; pero está optimizado para el procesamiento de subprocesos en segundo plano. Se recomienda crear montones en subprocesos en segundo plano para evitar el problema del subproceso de representación. En D3D12, varios subprocesos pueden llamar a las rutinas de creación de forma segura simultáneamente.

D3D12 introduce más flexibilidad y ortogonalidad en su modelo de recursos con el fin de habilitar más opciones para las aplicaciones. Hay tres tipos de recursos de alto nivel en D3D12: confirmados, colocados y reservados.

-   Los recursos confirmados crean un recurso y un montón al mismo tiempo. El montón es implícito y no se puede tener acceso a él directamente. El tamaño del montón es el adecuado para buscar el recurso completo en el montón.
-   Los recursos colocados permiten la colocación de un recurso en un desplazamiento distinto de cero dentro de un montón. Los desplazamientos se deben alinear normalmente a 64 KB; pero existen algunas excepciones en ambas direcciones. Los recursos de MSAA requieren una alineación de desplazamiento de 4 MB y la alineación de desplazamiento de 4 KB está disponible para las texturas pequeñas. Los recursos colocados no se pueden reubicar o volver a asignar a otro montón directamente; pero habilitan la reubicación simple de los datos de recursos entre montones. Después de crear un nuevo recurso colocado en otro montón y copiar los datos de recursos, se tendrán que usar nuevos descriptores de recursos para la nueva ubicación de datos de recursos.
-   Los recursos reservados solo están disponibles cuando el adaptador admite los recursos en mosaico nivel 1 o superior. Cuando está disponible, ofrecen las técnicas de administración de residencia más avanzadas disponibles; pero no todos los adaptadores los admiten actualmente. Permiten volver a asignar un recurso sin necesidad de la regeneración de descriptores de recursos, la residencia parcial del nivel de MIP y escenarios de textura dispersos, etc. No se admiten todos los tipos de recursos, aunque los recursos reservados estén disponibles, por lo que todavía no es posible un administrador de residencia totalmente basado en páginas.

## <a name="residency-priorities"></a>Prioridades de residencia

Windows 10 Creators Update permite a los desarrolladores influir en qué montones y recursos serán preferibles para permanecer residentes cuando la presión de memoria requiere que algunos de sus recursos se degraden. Esto ayuda a los desarrolladores a crear aplicaciones de mejor rendimiento al aprovechar el conocimiento que el runtime no puede deducir del uso de la API. Se espera que los desarrolladores sean más cómodos y puedan especificar prioridades a medida que pasan por el uso de recursos confirmados para reservada y los recursos en mosaico.

La aplicación de estas prioridades debe ser más fácil que la administración de dos presupuestos de memoria dinámica, la degradación manual y la promoción de recursos bettween, ya que las aplicaciones ya pueden hacerlo. Por lo tanto, el diseño de la API de prioridad de residencia es muy específico con prioridades razonables predeterminadas asignadas a cada montón o recurso como se creó. Para obtener más información, vea [**ID3D12Device1:: SetResidencyPriority**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority) y la enumeración de [**prioridad de \_ residencia \_ de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority) .

Con las prioridades, se espera que los desarrolladores:

-   Aumente la prioridad de algunos montones excepcionales para mitigar mejor el impacto en el rendimiento experimentado de estos montones al disminuir de nivel antes o con mayor frecuencia que sus patrones de acceso natural. Se espera que este enfoque sea aprovechado por aplicaciones que se portan desde API de gráficos como Direct3D 11 o OpenGL, cuyo modelo de administración de recursos es significativamente diferente del de Direct3D 12.
-   Invalide casi todas las prioridades del montón con el esquema de depósito propio de la aplicación, ya sea fijo, según el conocimiento del programador de la frecuencia de acceso o dinámica. un esquema fijo es más fácil de administrar que uno dinámico, pero puede ser menos eficaz y requerir que los pendiente"Styles de programador cambien en el transcurso del desarrollo. Se espera que este enfoque sea aprovechado por aplicaciones compiladas con la administración de recursos de estilo de Direct3D 12 en mente, como las que usan la biblioteca de residencia (especialmente los esquemas dinámicos).

### <a name="default-priority-algorithm"></a>Algoritmo de prioridad predeterminado

Una aplicación no puede especificar prioridades útiles para cualquier montón que intente administrar sin deshacer primero el algoritmo de prioridad predeterminado. Esto se debe a que el valor de asignar una prioridad determinada a un montón se deriva de su prioridad relativa a otros montones con prioridad que compiten por la misma memoria.

La estrategia elegida para generar las prioridades predeterminadas es categorizar los montones en dos cubos, con lo que se favorece el uso de los montones (lo que da prioridad más) a los montones que no se suelen escribir con frecuencia en los montones.

El depósito de alta prioridad contiene montones y recursos creados con marcas que los identifican como destinos de representación, búferes de estarcido de profundidad o vistas de acceso desordenado (UAVs). A estos se les asignan los valores de prioridad en el intervalo que empieza en la **prioridad de residencia de D3D12 \_ \_ \_ alto**; para dar mayor prioridad entre estos montones y recursos, los 16 bits más bajos de la prioridad se establecen en el tamaño del montón o recurso dividido entre 10 MB (saturando a 0xFFFF para montones extremadamente grandes). Esta priorización adicional favorece montones y recursos más grandes.

El depósito de prioridad baja contiene el resto de montones y recursos, a los que se asigna un valor de prioridad de la **prioridad de residencia de D3D12 \_ \_ \_ normal**. No se intenta establecer una priorización adicional entre estos montones y recursos.

## <a name="programming-residency-management"></a>Administración de la residencia de programación

Las aplicaciones sencillas pueden obtener simplemente la creación de recursos confirmados hasta que se produzcan errores de memoria insuficiente. En caso de error, la aplicación puede destruir otros recursos confirmados o objetos de API para permitir que se realicen más creaciones de recursos. Sin embargo, se recomienda encarecidamente que las aplicaciones simples inspeccionen los cambios de presupuesto negativos y destruyan los objetos de API no usados aproximadamente una vez al fotograma.

La complejidad de un diseño de la administración de las residencias se producirá al intentar optimizar las arquitecturas del adaptador o incorporar prioridades de residencia. La presupuestación discreta y la administración de dos grupos de memoria discreta serán más complejas que la administración de una sola y la asignación de prioridades fijas en una escala amplia puede suponer una carga de mantenimiento si evolucionan los patrones de uso. El desbordamiento de texturas en la memoria del sistema aumenta la complejidad, ya que el recurso equivocado en la memoria del sistema puede afectar gravemente a la velocidad de fotogramas. Además, no hay ninguna funcionalidad sencilla que ayude a identificar los recursos que pueden beneficiarse del ancho de banda de la GPU superior o tolerar un ancho de banda menor de la GPU.

Incluso en diseños más complicados, se consultan las características del adaptador actual. Esta información está disponible en [**D3D12 \_ características \_ compatibilidad de la \_ \_ \_ dirección \_ virtual de GPU**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support), [**\_ \_ \_ arquitectura de datos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture), D3D12 de [**\_ \_ recursos en mosaico \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)y [**\_ \_ \_ nivel de montón de recursos de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier).

Es probable que varias partes de una aplicación se desenreden con distintas técnicas. Por ejemplo, algunas texturas de gran tamaño y rutas de acceso de código poco empleadas pueden usar recursos confirmados, mientras que muchas texturas se pueden designar con una propiedad de streaming y usar una técnica de recursos colocados general.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Administración de memoria](memory-management.md)
</dt> </dl>

 

 