---
title: Procedimientos recomendados de administración de recursos
description: En este artículo se de tratan los procedimientos recomendados para tratar con los recursos por lo general, cómo se comportan los recursos administrados y no administrados, y se proporcionan algunos detalles sobre cómo los recursos se controlan normalmente mediante el tiempo de ejecución y los controladores.
ms.assetid: 265ae0b2-f268-a4a4-551e-9d3dae886517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf57c33ef765596ffa660ba884708ee000dd370c90edd3fcd158a9c526a7ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213239"
---
# <a name="resource-management-best-practices"></a>Procedimientos recomendados de administración de recursos

Las texturas administradas, también conocidas como administración automática de texturas, están disponibles en DirectX desde la versión 6, con varias revisiones y mejoras realizadas en versiones posteriores. A partir del lanzamiento de la API de Direct3D 9, la administración automática de recursos incluye compatibilidad con texturas, búferes de vértices y búferes de índice, todo ello con una interfaz compartida coherente. Mediante el uso del administrador de recursos de Direct3D, las aplicaciones pueden simplificar en gran medida el control de situaciones de dispositivo perdido y pueden confiar en el sistema para controlar una cantidad razonable de exceso de compromiso de los recursos de memoria de vídeo.

A veces, los desarrolladores tienen dificultades para usar recursos administrados, en parte debido a la naturaleza abstracta del sistema. Aunque muchos escenarios comunes para los recursos son una buena opción para los recursos administrados, algunos casos tienen un mejor rendimiento cuando se usan recursos no administrados. En este artículo se de tratan los procedimientos recomendados para tratar con los recursos por lo general, cómo se comportan los recursos administrados y no administrados, y se proporcionan algunos detalles sobre cómo los recursos se controlan normalmente mediante el tiempo de ejecución y los controladores.

En este artículo se tratan estos conceptos:

-   [Memoria de vídeo](#video-memory)
-   [Recursos administrados](#managed-resources)
-   [Recursos administrados por el controlador](#driver-managed-resources)
-   [Recursos predeterminados](#default-resources)
    -   [Uso de recursos administrados y predeterminados](#using-both-managed-and-default-resources)
    -   [Recursos predeterminados dinámicos](#dynamic-default-resources)
-   [Recursos de memoria del sistema](#system-memory-resources)
-   [Información general Recomendaciones](#general-recommendations)
-   [Temas relacionados](#related-topics)

## <a name="video-memory"></a>Memoria de vídeo

Para que el sistema de vídeo use un recurso, debe encontrarse en la memoria accesible para la GPU. La memoria de vídeo local proporciona el mejor rendimiento para la GPU y determinados recursos (como destinos de representación y búferes de profundidad o galería de símbolos) deben encontrarse en la memoria de vídeo local. Con la llegada de AGP, la GPU también puede acceder directamente a una parte de la memoria del sistema. Esta área de memoria, conocida como apertura de AGP, se conoce como memoria de vídeo no local y no está disponible para otros fines. La CPU puede leer y escribir en la memoria de vídeo no local, que normalmente no tiene acceso de alto rendimiento a la memoria de vídeo local y, por tanto, es ideal para su uso como recurso de memoria compartida. Un aspecto clave que hay que recordar sobre la memoria de AGP es que, al igual que la memoria de vídeo local, se invalida en situaciones de dispositivo perdido y se deben restaurar los recursos persistentes ubicados allí.

**Figura 1. Relación de la GPU, la CPU, la RAM de vídeo y la RAM del sistema**

![relación de la GPU, cpu, ram de vídeo y ram del sistema](images/managingresources1.gif)

Algunas soluciones de vídeo integradas usan una arquitectura de memoria unificada (UMA), donde la memoria principal es direccionable por todos los componentes de los sistemas. Direct3D admite UMA sin necesidad de ningún cambio en la aplicación, utilizando las mismas sugerencias que para las configuraciones de memoria de vídeo local. Para estos sistemas, los recursos siempre se encuentran en la memoria del sistema y el controlador es responsable de garantizar que los recursos funcionen de forma muy parecido a como lo hacen en una arquitectura más tradicional, al tiempo que se aprovechan las propiedades de UMA y cualquier comportamiento específico de la implementación de hardware.

**Figura 2. Gpu y CPU tienen el mismo acceso a la RAM del sistema en una arquitectura de memoria unificada**

![Gpu y CPU tienen el mismo acceso a la ram del sistema en una arquitectura de memoria unificada](images/managingresources2.gif)

## <a name="managed-resources"></a>Recursos administrados

La mayoría de los recursos deben crearse como recursos administrados en POOL \_ MANAGED. Todos los recursos se crearán en la memoria del sistema y, a continuación, se copiarán según sea necesario en la memoria de vídeo. Las situaciones de dispositivo perdido se controlarán automáticamente desde la copia de memoria del sistema. Puesto que no todos los recursos administrados son necesarios para caber en la memoria de vídeo a la vez, puede realizar una confirmación en exceso de la memoria donde un conjunto de trabajo de memoria de vídeo más pequeño de recursos es todo lo que se necesita para representar en cualquier fotograma determinado. Tenga en cuenta que es probable que la mayoría de esta memoria del sistema de almacenamiento de respaldo se paginará en el disco a lo largo del tiempo, por lo que la operación de restablecimiento puede ser lenta debido a la necesidad de volver a paginar estos datos para restaurar la memoria de vídeo perdida.

El tiempo de ejecución mantiene una marca de tiempo para la última vez que se usa un recurso y, cuando se produce un error en la asignación de memoria de vídeo para cargar un recurso administrado necesario, liberará los recursos en función de esta marca de tiempo de forma LRU. El uso [**de SetPriority**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) tiene prioridad sobre la marca de tiempo, por lo que los recursos más usados deben establecerse en un valor de prioridad más alto. Direct3D 9.0 tiene información limitada sobre la memoria de vídeo administrada por el controlador, por lo que el tiempo de ejecución puede necesitar expulsar varios recursos para crear una región lo suficientemente grande como para que la asignación se haga correctamente. Las prioridades adecuadas pueden ayudar a eliminar situaciones en las que se expulsa algo y, a continuación, se requiere de nuevo poco después. La aplicación también puede llamar [**a EvictManagedResources para**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) forzar la eliminación de todos los recursos administrados. Una vez más, puede ser una operación que tarda mucho tiempo en volver a cargar todos los recursos necesarios para el siguiente fotograma, pero es muy útil para las transiciones de nivel en las que el espacio de trabajo cambia significativamente y para quitar la fragmentación de la memoria de vídeo.

También se mantiene un recuento de fotogramas para permitir que el tiempo de ejecución detecte si el recurso que acaba de expulsar se usó al principio del fotograma actual, lo que implica una situación de gran tamaño en la que hay más recursos en uso en un único fotograma de los que caben en la memoria de vídeo. Esto desencadena que la directiva de reemplazo cambie a un modo de MRU en lugar de LRU durante el resto del fotograma, ya que esto tiende a mejorar ligeramente en tales condiciones. Este comportamiento de reducción del nivel afectará significativamente al rendimiento de la representación. Tenga en cuenta que la noción de marco actual está vinculada a [**EndScene,**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene)por lo que cualquier aplicación que use recursos administrados debe realizar llamadas periódicas a este método.

Los desarrolladores que buscan más información sobre cómo se comportan los recursos administrados en su aplicación pueden usar la consulta de eventos RESOURCEMANAGER a través de la interfaz [**IDirect3DQuery9.**](/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9) Esto solo funciona cuando se usan los tiempos de ejecución de depuración, por lo que la aplicación no puede depender de esta información, pero proporciona detalles detallados sobre los recursos administrados por el runtime.

Aunque comprender cómo funciona resource manager puede ayudar a optimizar y depurar las aplicaciones, es importante no vincular la aplicación demasiado estrechamente a los detalles de implementación del runtime o los controladores actuales. Las revisiones del controlador o los cambios en el hardware pueden cambiar significativamente el comportamiento y las versiones futuras de Direct3D tendrán una administración de recursos significativamente mejorada y sofisticada.

## <a name="driver-managed-resources"></a>Driver-Managed recursos

Los controladores de Direct3D pueden implementar la funcionalidad de texturas administradas por el controlador, indicada por D3DCAPS2 CANMANAGERESOURCE, que permite al controlador controlar la administración de recursos en lugar del tiempo de \_ ejecución. En el caso del controlador (poco frecuente) que implementa esta característica, el comportamiento exacto del administrador de recursos del controlador puede variar ampliamente y debe ponerse en contacto con el proveedor del controlador para obtener más información sobre cómo funciona esto para su implementación. Como alternativa, puede asegurarse de que siempre se usa el administrador en tiempo de ejecución especificando D3DCREATE \_ DISABLE DRIVER MANAGEMENT al crear el \_ \_ dispositivo.

## <a name="default-resources"></a>Recursos predeterminados

Aunque los recursos administrados son sencillos, eficaces y fáciles de usar, hay ocasiones en las que se prefiere o incluso se requiere el uso directo de la memoria de vídeo. Estos recursos se crean en la categoría POOL \_ DEFAULT. El uso de estos recursos provoca complicaciones adicionales para la aplicación. El código es necesario para hacer frente a la situación de dispositivo perdido para todos los recursos DE POOL DEFAULT, y se deben tener en cuenta las consideraciones de rendimiento al copiar datos \_ en ellos. Si no se especifica USAGE WRITEONLY o se puede bloquear un destino de representación, también se pueden imponer graves \_ penalizaciones de rendimiento.

Llamar **a Lock** en un recurso POOL DEFAULT es más probable que cause que la GPU se detener que trabajar con un recurso ADMINISTRADO POR GRUPO, a menos que se utilicen \_ \_ determinadas marcas de sugerencias. Dependiendo de la ubicación del recurso, el puntero devuelto podría ser a un búfer de memoria temporal del sistema o puede ser un puntero directamente a la memoria de AGP. Si es un búfer de memoria temporal del sistema, los datos se deben transferir a la memoria de vídeo después de la **llamada de** desbloqueo. Si el recurso de vídeo no es de solo escritura, los datos tendrán que transferirse al búfer temporal durante el **bloqueo**. Si se trata de un área de memoria AGP, se evitan las copias temporales, pero el comportamiento de caché necesario puede provocar un rendimiento lento.

Se debe tener cuidado de escribir una línea de datos de caché completa en cualquier puntero a la memoria de apertura de AGP para evitar la penalización de la combinación de escritura, lo que induce un ciclo de lectura y escritura, y se prefiere el acceso secuencial del área de memoria. Si la aplicación necesita realizar acceso aleatorio a los datos durante la creación y no desea usar un recurso administrado para el búfer, debe trabajar con una copia de memoria del sistema en su lugar. Una vez creados los datos, puede transmitir el resultado a la memoria de recursos bloqueada para evitar pagar una penalización elevada por la operación de combinación de escritura de caché.

La marca LOCK NOOVERWRITE se puede usar para anexar datos de una manera eficaz para algunos recursos, pero lo ideal es que se puedan evitar varias llamadas lock y unlock al \_ mismo recurso.   El uso adecuado de las distintas marcas de bloqueo es importante para obtener un rendimiento óptimo, al igual que el uso de un patrón de acceso a datos descriptivo para la memoria caché al rellenar la memoria bloqueada.

### <a name="using-both-managed-and-default-resources"></a>Uso de recursos administrados y predeterminados

La combinación de asignaciones de recursos administrados y POOL DEFAULT puede provocar la fragmentación de la memoria de vídeo y confundir la vista del entorno de ejecución de la memoria de vídeo disponible para \_ los recursos administrados. Idealmente, debe crear todos los recursos DE POOL DEFAULT antes de usar los recursos ADMINISTRADOs de GRUPO o hacer uso de la llamada \_ \_ [**AvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) antes de asignar recursos no administrados. Recuerde que todas las asignaciones realizadas a partir de POOL DEFAULT que residen en la memoria de vídeo vinculan la memoria durante la vida útil de ese recurso que no está disponible para su uso por parte del administrador de recursos o para \_ cualquier otro propósito.

Tenga en cuenta que, a diferencia de las versiones anteriores de Direct3D, el entorno de ejecución de la versión 9 expulsa automáticamente algunos recursos administrados antes de dejar de asignar recursos no administrados por una falta de memoria de vídeo, pero esto puede crear una fragmentación adicional e incluso forzar un recurso a una ubicación poco óptima (por ejemplo, tener una textura estática en la memoria de vídeo no local). De nuevo, es mejor asignar todos los recursos no administrados necesarios por adelantado y antes de usar los recursos administrados.

### <a name="dynamic-default-resources"></a>Recursos predeterminados dinámicos

Los datos que se generan y actualizan con una frecuencia alta no necesitan el almacenamiento de respaldo, ya que toda la información se volverá a crear al restaurar el dispositivo. Normalmente, estos datos se crean mejor en POOL DEFAULT, especificando la sugerencia USAGE DYNAMIC, para que el controlador pueda tomar decisiones de optimización al colocar el recurso, sabiendo que se actualizará \_ \_ con frecuencia. Esto suele significar colocar el recurso en memoria de vídeo no local y, por tanto, suele ser mucho más lento para la GPU acceder a ella que la memoria de vídeo local. En el caso de las arquitecturas de UMA, el controlador puede elegir una ubicación determinada para los recursos dinámicos a fin de optimizar el acceso de escritura de CPU.

Este uso es típico para las soluciones de descacharrización de software y los sistemas de partícula basados en CPU que rellenan búferes de vértices o índices, y la marca LOCK DISCARD garantizará que no se crean retenciones en los casos en los que el recurso sigue en uso desde el fotograma \_ anterior. En este caso, el uso de un recurso administrado actualizaría un búfer de memoria del sistema, que luego se copiaría en la memoria de vídeo y, a continuación, se usaría solo para un fotograma o dos antes de reemplazarse. Para los sistemas con memoria de vídeo no local, la copia adicional se elimina mediante el uso adecuado de este patrón dinámico.

Las texturas estándar no se pueden bloquear y solo se pueden actualizar a través de [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) o [**UpdateTexture.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture) Algunos sistemas admiten texturas dinámicas, que se pueden bloquear, y usan el patrón LOCK DISCARD, pero se debe comprobar un bit de funcionalidad \_ (D3DCAPS2 DYNAMICTEXTURES) antes de usar dichos \_ recursos. Para texturas altamente dinámicas (vídeo o procedimientos), la aplicación podría crear recursos POOL DEFAULT y POOL SYSTEMMEM correspondientes y controlar las actualizaciones de memoria de vídeo mediante \_ \_ **UpdateTexture**. En el caso de las actualizaciones muy frecuentes y parciales, es probable que el paradigma **UpdateTexture** sea la mejor opción.

Tan útil como pueden ser los recursos dinámicos, tenga cuidado al diseñar sistemas que dependen en gran medida del envío dinámico. Los recursos estáticos deben colocarse en POOL MANAGED para garantizar el buen uso de la memoria de vídeo local y para hacer un uso más eficaz del bus limitado y el ancho de \_ banda de memoria principal. En el caso de los recursos semiestáticos, es posible que encuentre que el costo de una carga ocasional en la memoria de vídeo local es mucho menor que el tráfico de bus constante generado al hacer que sean dinámicos.

## <a name="system-memory-resources"></a>Recursos de memoria del sistema

Los recursos también se pueden crear en POOL \_ SYSTEMMEM. Aunque la canalización de gráficos no los puede usar, se pueden usar como orígenes para actualizar los recursos DE POOL DEFAULT mediante \_ [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) [**o UpdateTexture.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture) Su comportamiento de bloqueo es sencillo, aunque pueden producirse retenciones si están en uso por uno de los métodos mencionados anteriormente.

Aunque residen en la memoria del sistema, los recursos DE POOL SYSTEMMEM se limitan a los mismos formatos y funcionalidades (como el tamaño máximo) admitidos \_ por el controlador de dispositivo. El tipo de recurso POOL SCRATCH es otra forma de recurso de memoria del sistema que puede usar todos los formatos y funcionalidades admitidos por el entorno de ejecución, pero al que el dispositivo no \_ puede acceder. Los recursos de scratch están pensados principalmente para su uso por parte de las herramientas de contenido.

**Figura 3. Recursos de memoria en ram de vídeo, apertura de AGP y RAM del sistema**

![recursos de memoria en ram de vídeo, apertura agp y ram del sistema](images/managingresources3.gif)

## <a name="general-recommendations"></a>Recomendaciones generales

La obtención de los detalles de implementación técnica de la administración de recursos correcta irá mucho más allá para lograr los objetivos de rendimiento de la aplicación. Planear cómo se presentan los recursos a Direct3D y el diseño arquitectónico en torno a la carga oportuna de los datos es una tarea más complicada. Se recomiendan varios procedimientos recomendados al tomar estas decisiones para la aplicación:

-   Procese previamente todos los recursos. Confiar en la conversión y optimización en tiempo de carga costosos de los recursos es conveniente durante el desarrollo, pero hacerlo supone una gran carga de rendimiento en los equipos de los usuarios. Los recursos procesados previamente son más rápidos de cargar, más rápidos de usar y le dan la opción de realizar un trabajo sofisticado fuera de línea.
-   Evite crear muchos recursos por fotograma. Las interacciones del controlador necesarias pueden serializar la CPU y la GPU, y las operaciones implicadas son pesadas, ya que a menudo requieren transiciones de kernel. Reparta la creación en varios fotogramas o reutiliza recursos sin crearlos ni liberarlos. Lo ideal es esperar varios fotogramas antes de bloquear o liberar recursos que se usaron recientemente para representar.
-   Al final del fotograma, asegúrese de desenlabinar todos los canales de recursos (es decir, orígenes de secuencias, fases de textura e índices actuales). Si lo hace, se asegurará de que se quiten las referencias de dominio a los recursos antes de hacer que el administrador de recursos mantenga los recursos residentes que en realidad ya no están en uso.
-   En el caso de las texturas, use formatos comprimidos (por ejemplo, DXTn) con mapas mip y considere la posibilidad de usar un atlas de textura. Estos requisitos reducen considerablemente los requisitos de ancho de banda y pueden reducir el tamaño total de los recursos, lo que los hace más eficientes.
-   En el caso de la geometría, use geometría indexada, ya que ayuda a comprimir los recursos del búfer de vértices y el hardware de vídeo moderno está muy optimizado en torno a la reutilización de vértices. Al usar sombreadores de vértices programables, puede comprimir la información del vértice y expandirla durante el procesamiento de vértices. De nuevo, esto ayuda a reducir los requisitos de ancho de banda y hace que los recursos del búfer de vértices sea más eficaz.
-   Evite optimizar en exceso la administración de recursos. Las revisiones futuras de los controladores, el hardware y el sistema operativo pueden causar problemas de compatibilidad si la aplicación está demasiado ajustada a una combinación concreta. Dado que la mayoría de las aplicaciones están enlazadas a la CPU, la administración costosa basada en CPU suele provocar más problemas de rendimiento de los que resuelve.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de recursos](/windows/desktop/direct3d9/managing-resources)
</dt> <dt>

[Dispositivos perdidos](/windows/desktop/direct3d9/lost-devices)
</dt> <dt>

[Optimizaciones de rendimiento](/windows/desktop/direct3d9/performance-optimizations)
</dt> <dt>

[Recursos de textura comprimidos](/windows/desktop/direct3d9/compressed-texture-resources)
</dt> <dt>

[Consultas](/windows/desktop/direct3d9/queries)
</dt> <dt>

[**D3DUSAGE**](/windows/desktop/direct3d9/d3dusage)
</dt> <dt>

[**D3DPOOL**](/windows/desktop/direct3d9/d3dpool)
</dt> <dt>

[D3DCREATE](/windows/desktop/direct3d9/d3dcreate)
</dt> </dl>

 

 