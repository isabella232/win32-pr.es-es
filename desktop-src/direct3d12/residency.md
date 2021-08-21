---
title: Residencia
description: Se considera que un objeto es residentes cuando la GPU puede acceder a él.
ms.assetid: 956F80D7-EEC8-4D88-B251-EE325614F31E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257af2526120df5509a38fcc0c81984aa53a954f8eed6a8ce9194fa2aadb020a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989464"
---
# <a name="residency"></a>Residencia

Se considera que un objeto es *residentes cuando* la GPU puede acceder a él.

-   [Presupuesto de residencia](#residency-budget)
-   [Recursos del montón](#heap-resources)
-   [Prioridades de residencia](#residency-priorities)
    -   [Algoritmo de prioridad predeterminado](#default-priority-algorithm)
-   [Administración de residencias de programación](#programming-residency-management)
-   [Temas relacionados](#related-topics)

## <a name="residency-budget"></a>Presupuesto de residencia

Las GPU aún no admiten errores de página, por lo que las aplicaciones deben confirmar datos en la memoria física mientras la GPU podría acceder a ellos. Este proceso se conoce como "hacer algo residentes" y debe realizarse tanto para la memoria del sistema físico como para la memoria de vídeo discreta física. En D3D12, la mayoría de los objetos de API encapsulan cierta cantidad de memoria accesible para GPU. Esa memoria accesible para GPU se hace residentes durante la creación del objeto de API y se expulsa al destruir objetos de API.

La cantidad de memoria física disponible para el proceso se conoce como presupuesto de memoria de vídeo. El presupuesto puede fluctuar notablemente a medida que el fondo procesa la reactivación y la suspensión. y fluctúan drásticamente cuando el usuario cambia a otra aplicación. Se puede notificar a la aplicación cuando cambia el presupuesto y sondear tanto el presupuesto actual como la cantidad de memoria consumida actualmente. Si una aplicación no permanece dentro de su presupuesto, el proceso se inmovilizará intermitentemente para permitir que otras aplicaciones se ejecuten o las API de creación devolverán errores. La [**interfaz IDXGIAdapter3**](/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) proporciona los métodos que pertenecen a esta funcionalidad, en particular [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) y [**RegisterVideoMemoryBudgetChangeNotificationEvent.**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent)

Se recomienda a las aplicaciones usar una reserva para indicar la cantidad de memoria sin la que no pueden pasar. Lo ideal es que la configuración de gráficos "baja" especificada por el usuario, o algo incluso inferior, sea el valor adecuado para dicha reserva. Establecer una reserva nunca dará a una aplicación un presupuesto mayor del que normalmente recibiría. En su lugar, la información de reserva ayuda al kernel del sistema operativo a minimizar rápidamente el impacto de situaciones de presión de memoria de gran tamaño. Ni siquiera se garantiza que la reserva esté disponible para la aplicación cuando la aplicación no es la aplicación en primer plano.

## <a name="heap-resources"></a>Recursos del montón

Aunque muchos objetos de API encapsulan parte de la memoria accesible para GPU, se espera que los montones & recursos sean la manera más significativa en que las aplicaciones consumen y administran la memoria física. Un montón es la unidad de nivel más bajo para administrar la memoria física, por lo que es bueno estar familiarizado con sus propiedades de residencia.

-   Los montones no se pueden convertir en parcialmente residentes, pero existen soluciones alternativas con recursos reservados.
-   Los montones se deben presupuestar como parte de un grupo determinado. Los adaptadores UMA tienen un grupo, mientras que los adaptadores discretos tienen dos grupos. Aunque es cierto que el kernel puede cambiar algunos montones en adaptadores discretos de memoria de vídeo a memoria del sistema, solo lo hace como último recurso extremo. Las aplicaciones no deben basarse en el comportamiento de exceso de presupuesto del kernel y deben centrarse en una buena administración de presupuestos en su lugar.
-   Los montones se pueden expulsar de la residencia, lo que permite que su contenido se pueda paginar en el disco. Pero la destrucción de montones es una técnica más confiable para liberar residencia en todas las arquitecturas de adaptadores. En los adaptadores en los que el *campoMaxGPUVirtualAddressBitsPerProcess* de [**D3D12 \_ FEATURE DATA GPU VIRTUAL ADDRESS \_ \_ \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support) está cerca del tamaño del presupuesto, [**Evict**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict) no reclamará de forma confiable la residencia.
-   La creación del montón puede ser lenta; pero está optimizado para el procesamiento de subprocesos en segundo plano. Se recomienda crear montones en subprocesos en segundo plano para evitar problemas en el subproceso de representación. En D3D12, varios subprocesos pueden llamar de forma segura a las rutinas de creación simultáneamente.

D3D12 introduce más flexibilidad y ortogonalidad en su modelo de recursos para habilitar más opciones para las aplicaciones. Hay tres tipos de recursos de alto nivel en D3D12: confirmado, colocado y reservado.

-   Los recursos confirmados crean un recurso y un montón al mismo tiempo. El montón es implícito y no se puede acceder a él directamente. El montón tiene el tamaño adecuado para localizar todo el recurso dentro del montón.
-   Los recursos colocados permiten la colocación de un recurso en un desplazamiento distinto de cero dentro de un montón. Normalmente, los desplazamientos deben alinearse con 64 KB; pero existen algunas excepciones en ambas direcciones. Los recursos de MSAA requieren una alineación de desplazamiento de 4 MB y la alineación de desplazamiento de 4 KB está disponible para texturas pequeñas. Los recursos colocados no se pueden reubicar ni reasignar directamente a otro montón; pero permiten la reubicación simple de los datos de recursos entre montones. Después de crear un nuevo recurso colocado en un montón diferente y copiar los datos del recurso, se tendrán que usar nuevos descriptores de recursos para la nueva ubicación de datos de recursos.
-   Los recursos reservados solo están disponibles cuando el adaptador admite recursos en mosaico de nivel 1 o superior. Cuando están disponibles, ofrecen las técnicas de administración de residencia más avanzadas disponibles. pero no todos los adaptadores los admiten actualmente. Permiten volver a crear un recurso sin necesidad de regenerar descriptores de recursos, residencia parcial de nivel mip y escenarios de textura dispersa, etc. No todos los tipos de recursos se admiten incluso cuando los recursos reservados están disponibles, por lo que aún no es factible un administrador de residencias basado en páginas totalmente general.

## <a name="residency-priorities"></a>Prioridades de residencia

La Windows 10 Creators Update permite a los desarrolladores influir en qué montones y recursos se prefiere que permanezcan residentes cuando la presión de memoria requiera que algunos de sus recursos se degradan. Esto ayuda a los desarrolladores a crear aplicaciones de mejor rendimiento al aprovechar el conocimiento de que el tiempo de ejecución no puede deducir del uso de la API. Se espera que los desarrolladores se sientan más cómodos y capaces de especificar prioridades a medida que se pasa de usar recursos comprometidos a recursos reestados y en mosaico.

La aplicación de estas prioridades debe ser más fácil que administrar dos presupuestos de memoria dinámica, degradar y promover manualmente los recursos, ya que las aplicaciones ya pueden hacerlo. Por lo tanto, el diseño de la API de prioridad de residencia está por supuesto específico con prioridades predeterminadas razonables asignadas a cada montón o recurso a medida que se crea. Para obtener más información, [**vea ID3D12Device1::SetResidencyPriority**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority) y la [**enumeración D3D12 \_ RESIDENCY \_ PRIORITY.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority)

Con las prioridades, se espera que los desarrolladores:

-   Aumentar la prioridad de algunos montones excepcionales para mitigar mejor el impacto experimentado en el rendimiento de estos montones que se degradan antes o con más frecuencia de lo que sus patrones de acceso natural exigirían. Se espera que este enfoque lo aprovechen las aplicaciones portadas desde API de gráficos como Direct3D 11 o OpenGL, que el modelo de administración de recursos es significativamente diferente al de Direct3D 12.
-   Invalide casi todas las prioridades del montón con el propio esquema de bucketización de la aplicación, ya sea fijo, en función del conocimiento del programador de la frecuencia de acceso o dinámico; un esquema fijo es más sencillo de administrar que uno dinámico, pero puede ser menos eficaz y requerir la intervención del programador a medida que los patrones de uso cambian en el transcurso del desarrollo. Se espera que este enfoque lo aprovechen las aplicaciones que se han creado teniendo en cuenta la administración de recursos de estilo 12 de Direct3D, como las que usan la biblioteca de residencia (especialmente los esquemas dinámicos).

### <a name="default-priority-algorithm"></a>Algoritmo de prioridad predeterminado

Una aplicación no puede especificar prioridades útiles para ningún montón que intente administrar sin necesidad de subsociar primero el algoritmo de prioridad predeterminado. Esto se debe a que el valor de asignar una prioridad determinada a un montón se deriva de su prioridad relativa a otros montones con prioridad que compiten por la misma memoria.

La estrategia elegida para generar prioridades predeterminadas es clasificar los montones en dos cubos, favoreciendo (dando mayor prioridad a) montones que se supone que la GPU escribe con frecuencia sobre montones que no lo están.

El cubo de alta prioridad contiene montones y recursos que se crean con marcas que los identifican como destinos de representación, búferes de galería de símbolos de profundidad o vistas de acceso desordenadas (UAV). Se les asignan valores de prioridad en el intervalo a partir de **D3D12 \_ RESIDENCY \_ PRIORITY \_ HIGH;** para priorizar aún más entre estos montones y recursos, los 16 bits más bajos de la prioridad se establecen en el tamaño del montón o recurso dividido entre 10 MB (saturación a 0xFFFF para montones extremadamente grandes). Esta priorización adicional favorece los montones y recursos más grandes.

El cubo de prioridad baja contiene todos los demás montones y recursos, a los que se les asigna un valor de prioridad **de D3D12 \_ RESIDENCY \_ PRIORITY \_ NORMAL**. No se intenta priorizar más entre estos montones y recursos.

## <a name="programming-residency-management"></a>Administración de residencias de programación

Es posible que las aplicaciones sencillas puedan obtener simplemente creando recursos confirmados hasta experimentar errores de memoria fuera de memoria. En caso de error, la aplicación puede destruir otros recursos o objetos de API confirmados para permitir que las creaciones de recursos adicionales se puedan realizar correctamente. Sin embargo, incluso las aplicaciones sencillas se recomiendan encarecidamente que estén atentos a los cambios de presupuesto negativos y que destruyan objetos de API sin usar aproximadamente una vez un fotograma.

La complejidad de un diseño de administración de residencias subirá al intentar optimizar las arquitecturas de adaptadores o incorporar prioridades de residencia. Presupuestar y administrar discretamente dos grupos de memoria discreta será más complejo que administrar solo uno, y asignar prioridades fijas a gran escala puede convertirse en una carga de mantenimiento si los patrones de uso evolucionan. El desbordamiento de texturas en la memoria del sistema agrega más complejidad, ya que el recurso incorrecto en la memoria del sistema puede afectar gravemente a la velocidad de fotogramas. Además, no hay ninguna funcionalidad sencilla que ayude a identificar los recursos que se beneficiarían de un mayor ancho de banda de GPU o tolerarían un menor ancho de banda de GPU.

Los diseños aún más complicados consultarán las características del adaptador actual. Esta información está disponible en [**D3D12 \_ FEATURE DATA GPU VIRTUAL ADDRESS \_ \_ \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support), [**D3D12 \_ FEATURE DATA \_ \_ ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture), [**D3D12 \_ TILED RESOURCES \_ \_ TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)y [**D3D12 \_ RESOURCE \_ HEAP \_ TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier).

Es probable que varias partes de una aplicación se desasoyerán mediante distintas técnicas. Por ejemplo, algunas texturas grandes y rutas de acceso de código que rara vez se han ejercicio pueden usar recursos confirmados, mientras que muchas texturas se pueden designar con una propiedad de streaming y usar una técnica general de recursos colocados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Administración de memoria](memory-management.md)
</dt> </dl>

 

 