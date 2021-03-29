---
title: Procedimientos recomendados para la administración de recursos
description: En este artículo se describen los procedimientos recomendados para trabajar con los recursos en general, cómo se comportan los recursos administrados y no administrados, y se proporciona información detallada sobre cómo los controladores y el tiempo de ejecución suelen controlar los recursos.
ms.assetid: 265ae0b2-f268-a4a4-551e-9d3dae886517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cdadb8cee3cb57f4208657054784937ecd1ea2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359214"
---
# <a name="resource-management-best-practices"></a>Procedimientos recomendados para la administración de recursos

Las texturas administradas, también conocidas como administración automática de texturas, están disponibles en DirectX desde la versión 6, con varias revisiones y mejoras realizadas en las versiones posteriores. A partir del lanzamiento de la API de Direct3D 9, la administración automática de recursos incluye compatibilidad con texturas, búferes de vértices y búferes de índice, todo ello con una interfaz compartida coherente. Con el administrador de recursos de Direct3D, las aplicaciones pueden simplificar en gran medida el control de las situaciones de dispositivos perdidos y pueden basarse en el sistema para controlar una cantidad razonable de sobrecompromiso de recursos de memoria de vídeo.

A veces, los desarrolladores tienen dificultades para usar recursos administrados, en parte debido a la naturaleza abstracta del sistema. Aunque muchos escenarios comunes para los recursos son una buena opción para los recursos administrados, algunos casos funcionan mejor cuando se usan recursos no administrados. En este artículo se describen los procedimientos recomendados para trabajar con los recursos en general, cómo se comportan los recursos administrados y no administrados, y se proporciona información detallada sobre cómo los controladores y el tiempo de ejecución suelen controlar los recursos.

En este artículo se tratan estos conceptos:

-   [Memoria de vídeo](#video-memory)
-   [Recursos administrados](#managed-resources)
-   [Recursos administrados por controladores](#driver-managed-resources)
-   [Recursos predeterminados](#default-resources)
    -   [Usar recursos administrados y predeterminados](#using-both-managed-and-default-resources)
    -   [Recursos predeterminados dinámicos](#dynamic-default-resources)
-   [Recursos de memoria del sistema](#system-memory-resources)
-   [Recomendaciones generales](#general-recommendations)
-   [Temas relacionados](#related-topics)

## <a name="video-memory"></a>Memoria de vídeo

Para que el sistema de vídeo haga uso de un recurso, debe encontrarse en memoria que sea accesible para la GPU. La memoria de vídeo local proporciona el mejor rendimiento para la GPU y ciertos recursos (como destinos de representación y búferes de profundidad y estarcido) deben encontrarse en la memoria de vídeo local. Con la llegada de AGP, la GPU también puede tener acceso a una parte de la memoria del sistema directamente. Este área de memoria, conocida como la abertura AGP, se conoce como memoria de vídeo no local y no está disponible para otros fines. La CPU puede leer y escribir en la memoria de vídeo no local, que normalmente no tiene acceso de alto rendimiento a la memoria de vídeo local y, por tanto, es ideal para su uso como un recurso de memoria compartida. Una cuestión clave que hay que recordar sobre la memoria AGP es que, al igual que la memoria de vídeo local, se invalida en situaciones de dispositivo perdido y se deben restaurar los recursos persistentes que se encuentran allí.

**Figura 1. Relación de la GPU, la CPU, la RAM de vídeo y la RAM del sistema**

![relación de la GPU, la CPU, la RAM de vídeo y la RAM del sistema](images/managingresources1.gif)

Algunas soluciones de vídeo integradas hacen uso de una arquitectura de memoria unificada (UMA), donde la memoria principal es direccionable por todos los componentes de los sistemas. Direct3D admite la UMA sin necesidad de realizar ningún cambio en la aplicación, con las mismas sugerencias que para las configuraciones de memoria de vídeo local. En estos sistemas, los recursos siempre se encuentran en la memoria del sistema y el controlador es responsable de garantizar que los recursos funcionen de forma muy similar a como lo hacen en una arquitectura más tradicional, al mismo tiempo que se aprovechan las propiedades del UMA y cualquier comportamiento específico de la implementación de hardware.

**Figura 2. GPU y CPU tienen el mismo acceso a la memoria RAM del sistema en una arquitectura de memoria unificada**

![GPU y CPU tienen el mismo acceso a la memoria RAM del sistema en una arquitectura de memoria unificada](images/managingresources2.gif)

## <a name="managed-resources"></a>Recursos administrados

La mayoría de los recursos debe crearse como recursos administrados en el grupo \_ administrado. Todos los recursos se crearán en la memoria del sistema y, a continuación, se copiarán según sea necesario en la memoria de vídeo. Las situaciones de dispositivo perdido se administrarán automáticamente desde la copia de la memoria del sistema. Puesto que no es necesario que todos los recursos administrados quepan en la memoria de vídeo de una sola vez, puede sobrecargar la memoria en la que todo el espacio de trabajo de memoria de vídeo es el que se requiere para representar en cualquier fotograma determinado. Tenga en cuenta que es probable que la mayoría de la memoria del sistema de almacenamiento de respaldo se desproteja en el disco a lo largo del tiempo, por lo que la operación de restablecimiento puede ser lenta debido a la necesidad de volver a paginar los datos para restaurar la memoria de vídeo perdida.

El tiempo de ejecución mantiene una marca de tiempo para la última vez que se utiliza un recurso y, cuando se produce un error en la asignación de memoria de vídeo para cargar un recurso administrado necesario, libera los recursos según esta marca de tiempo de forma LRU. El uso de [**SetPriority**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) tiene prioridad sobre la marca de tiempo, por lo que los recursos usados más comúnmente deben establecerse en un valor de prioridad más alto. Direct3D 9,0 tiene información limitada sobre la memoria de vídeo administrada por el controlador, por lo que el tiempo de ejecución puede necesitar expulsar varios recursos para crear una región lo suficientemente grande como para que la asignación se realice correctamente. Las prioridades adecuadas pueden ayudar a eliminar situaciones en las que algo se expulsa y, a continuación, se vuelven a necesitar poco después. La aplicación también puede llamar a [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) para forzar la eliminación de todos los recursos administrados. De nuevo, esto puede ser una operación que requiere mucho tiempo para volver a cargar todos los recursos necesarios para el siguiente fotograma, pero es muy útil para las transiciones de nivel en las que el espacio de trabajo cambia significativamente y para quitar la fragmentación de la memoria de vídeo.

También se mantiene un recuento de fotogramas para permitir que el motor en tiempo de ejecución detecte si el recurso que acaba de retirar se usó antes del fotograma actual, lo que implica una situación de hiperpaginación en la que se usan más recursos en un solo fotograma que en la memoria de vídeo. Esto desencadena la Directiva de reemplazo para cambiar a un modo de MRU en lugar de LRU para el resto del fotograma, ya que esto tiende a realizarse ligeramente mejor en esas condiciones. Este comportamiento de hiperpaginación afectará significativamente al rendimiento de la representación. Tenga en cuenta que la noción del marco actual está ligada a [**EndScene**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene), por lo que cualquier aplicación que use recursos administrados debe realizar llamadas regulares a este método.

Los desarrolladores que deseen encontrar más información sobre cómo se comportan los recursos administrados en su aplicación pueden usar la consulta de eventos de RESOURCEMANAGER a través de la interfaz [**IDirect3DQuery9**](/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9) . Esto solo funciona cuando se usan los tiempos de ejecución de depuración, por lo que la aplicación no puede depender de esta información, pero proporciona detalles profundos sobre los recursos administrados por el tiempo de ejecución.

A la hora de comprender cómo funciona el administrador de recursos puede ayudarle a optimizar y depurar las aplicaciones, es importante no asociar la aplicación a los detalles de implementación del motor en tiempo de ejecución o los controladores actuales. Las revisiones del controlador o los cambios en el hardware pueden cambiar significativamente el comportamiento, y las versiones futuras de Direct3D tendrán una administración de recursos muy mejorada y sofisticada.

## <a name="driver-managed-resources"></a>Recursos de Driver-Managed

Los controladores de Direct3D son gratuitos para implementar la funcionalidad de texturas administradas de controladores, indicada por D3DCAPS2 \_ CANMANAGERESOURCE, que permite que el controlador controle la administración de recursos en lugar del tiempo de ejecución. En el caso del controlador (poco frecuente) que implementa esta característica, el comportamiento exacto del administrador de recursos del controlador puede variar considerablemente y debe ponerse en contacto con el proveedor del controlador para obtener más detalles sobre cómo funciona para su implementación. Como alternativa, puede asegurarse de que el administrador en tiempo de ejecución siempre se usa en su lugar mediante la especificación de D3DCREATE \_ deshabilitar la \_ \_ Administración de controladores al crear el dispositivo.

## <a name="default-resources"></a>Recursos predeterminados

Aunque los recursos administrados son sencillos, eficientes y fáciles de usar, hay ocasiones en las que es preferible usar la memoria de vídeo directamente o incluso se requiere. Estos recursos se crean en la \_ categoría predeterminado del grupo. El uso de estos recursos produce complicaciones adicionales para la aplicación. El código es necesario para hacer frente a la situación de dispositivo perdido para todos los \_ recursos predeterminados de grupo y se deben tener en cuenta las consideraciones de rendimiento cuando se copian datos en ellas. Si no se especifica USAGE \_ WRITEONLY o se hace que un destino de representación se pueda bloquear, también se pueden imponer penalizaciones de rendimiento graves.

Llamar al **bloqueo** en un \_ recurso predeterminado de grupo es más probable que la GPU se detenga en lugar de trabajar con un \_ recurso administrado de grupo, a menos que se usen ciertas marcas de sugerencia. Dependiendo de la ubicación del recurso, el puntero devuelto podría ser a un búfer de memoria temporal del sistema o puede ser un puntero directamente a la memoria AGP. Si es un búfer de memoria temporal del sistema, los datos deberán transferirse a la memoria de vídeo después de la llamada de **desbloqueo** . Si el recurso de vídeo no es de solo escritura, los datos deberán transferirse al búfer temporal durante el **bloqueo**. Si se trata de un área de memoria AGP, se evitan las copias temporales, pero el comportamiento de la memoria caché necesario puede dar lugar a un rendimiento lento.

Se debe tener cuidado para escribir una línea de datos de la memoria caché completa en cualquier puntero a la memoria de abertura AGP para evitar la penalización del barrido de escritura, que induce un ciclo de lectura y escritura, y se prefiere el acceso secuencial del área de memoria. Si la aplicación necesita realizar un acceso aleatorio a los datos durante la creación y no desea usar un recurso administrado para el búfer, debe trabajar con una copia de la memoria del sistema en su lugar. Una vez creados los datos, puede transmitir el resultado a la memoria de recursos bloqueados para evitar el pago de una penalización alta para la operación de combinación de escritura en la memoria caché.

La \_ marca Lock NOOVERWRITE se puede usar para anexar datos de una manera eficaz para algunos recursos, pero idealmente, se pueden evitar varias llamadas de **bloqueo** y **desbloqueo** al mismo recurso. Es importante hacer un uso correcto de las distintas marcas de bloqueo para obtener un rendimiento óptimo, como es el uso de un patrón de acceso a datos que se puede almacenar en caché al rellenar la memoria bloqueada.

### <a name="using-both-managed-and-default-resources"></a>Usar recursos administrados y predeterminados

La combinación de asignaciones de recursos predeterminados administrados y AGRUPAdos \_ puede provocar la fragmentación de la memoria de vídeo y confundir la vista del tiempo de ejecución de la memoria de vídeo disponible para los recursos administrados. Idealmente, debe crear todos los \_ recursos predeterminados de grupo antes de usar los \_ recursos administrados de grupo o hacer uso de la llamada [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) antes de asignar recursos no administrados. Recuerde que todas las asignaciones realizadas desde el \_ valor predeterminado del grupo que residen en la memoria de vídeo ocupan la memoria para la vida del recurso que no está disponible para su uso por parte del administrador de recursos o para cualquier otro propósito.

Tenga en cuenta que, a diferencia de las versiones anteriores de Direct3D, el tiempo de ejecución de la versión 9 expulsa automáticamente algunos recursos administrados antes de generar una asignación de recursos no administrada con errores para la falta de memoria de vídeo, pero esto puede crear una fragmentación adicional e incluso forzar un recurso en una ubicación poco óptima (por ejemplo, tener una textura estática en la memoria de vídeo De nuevo, es mejor asignar todos los recursos no administrados necesarios por adelantado y antes de usar los recursos administrados.

### <a name="dynamic-default-resources"></a>Recursos predeterminados dinámicos

Los datos que se generan y se actualizan con una frecuencia alta no necesitan el almacenamiento de copia de seguridad, ya que toda la información se volverá a crear al restaurar el dispositivo. Normalmente, estos datos se crean mejor en \_ el grupo de forma predeterminada, especificando la \_ sugerencia dinámica Usage, de modo que el controlador pueda tomar decisiones de optimización al colocar el recurso, sabiendo que se actualizará con frecuencia. Normalmente, esto significa poner el recurso en memoria de vídeo no local y, por lo tanto, suele ser mucho más lento para que la GPU tenga acceso a la memoria de vídeo local. En el caso de las arquitecturas UMA, el controlador puede elegir una ubicación determinada para que los recursos dinámicos optimicen el acceso de escritura de la CPU.

Este uso es típico para las soluciones de la división de software y los sistemas de partículas basados en CPU que rellenan los búferes de vértices/índices, y la \_ marca de descartar bloqueo garantizará que no se creen paradas en los casos en los que el recurso todavía esté en uso desde el fotograma anterior. En este caso, el uso de un recurso administrado actualizaría un búfer de memoria del sistema, que luego se copiaría en la memoria de vídeo y, a continuación, se usaría solo para un marco o dos antes de ser reemplazado. En sistemas con memoria de vídeo no local, la copia adicional se elimina mediante el uso correcto de este patrón dinámico.

Las texturas estándar no se pueden bloquear y solo se pueden actualizar a través de [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) o [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture). Algunos sistemas admiten texturas dinámicas, que se pueden bloquear y usan el \_ patrón de descartar bloqueo, pero se debe comprobar un bit de funcionalidad (D3DCAPS2 \_ DYNAMICTEXTURES) antes de usar dichos recursos. En el caso de las texturas muy dinámicas (vídeo o procedimiento), la aplicación podría crear recursos coincidentes \_ predeterminados y SYSTEMMEM del grupo \_ y controlar las actualizaciones de la memoria de vídeo mediante **UpdateTexture**. En el caso de las actualizaciones parciales y muy frecuentes, el paradigma **UpdateTexture** es probablemente la mejor opción.

Como es útil para los recursos dinámicos, tenga cuidado al diseñar sistemas que se basen en gran medida en el envío dinámico. Los recursos estáticos deben colocarse en \_ un grupo administrado para garantizar un uso correcto de la memoria de vídeo local y para hacer un uso más eficaz del ancho de banda de la memoria y del bus limitado. En el caso de los recursos que son semiestáticos, es posible que el costo de una carga ocasional en la memoria de vídeo local sea mucho menor que el tráfico de bus constante generado haciéndolos dinámicos.

## <a name="system-memory-resources"></a>Recursos de memoria del sistema

Los recursos también se pueden crear en el grupo \_ SYSTEMMEM. Aunque la canalización de gráficos no puede usarlos, se pueden usar como orígenes para actualizar \_ los recursos predeterminados del grupo mediante [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) o [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture). Su comportamiento de bloqueo es sencillo, aunque se pueden producir paradas si están en uso por uno de los métodos mencionados anteriormente.

Aunque residen en la memoria del sistema, los recursos de SYSTEMMEM de grupo \_ se limitan a los mismos formatos y capacidades (como el tamaño máximo) que admite el controlador de dispositivo. El \_ tipo de recurso Scratch de grupo es otra forma de recurso de memoria del sistema que puede usar todos los formatos y capacidades admitidos por el tiempo de ejecución, pero el dispositivo no puede tener acceso a él. Los recursos de memoria temporal están pensados principalmente para su uso por parte de las herramientas de contenido.

**Figura 3. Recursos de memoria en RAM de vídeo, abertura AGP y RAM del sistema**

![recursos de memoria en RAM de vídeo, abertura AGP y RAM del sistema](images/managingresources3.gif)

## <a name="general-recommendations"></a>Recomendaciones generales

Obtener los detalles de la implementación técnica de la correcta administración de recursos será una forma larga de lograr los objetivos de rendimiento de la aplicación. La planeación de la presentación de los recursos en Direct3D y el diseño arquitectónico en torno a la obtención de los datos de manera oportuna es una tarea más complicada. Recomendamos una serie de prácticas recomendadas al tomar estas decisiones para su aplicación:

-   Procese previamente todos los recursos. La dependencia de la mejora de la conversión y la optimización en tiempo de carga para los recursos resulta útil durante el desarrollo, pero esto supone una gran carga de rendimiento en los equipos de los usuarios. Los recursos preprocesados son más rápidos de cargar, más rápidos de usar y ofrecen la opción de realizar un trabajo sin conexión sofisticado.
-   Evite crear muchos recursos por fotograma. Las interacciones del controlador necesarias pueden serializar la CPU y la GPU, y las operaciones implicadas son pesadas, ya que a menudo requieren transiciones del kernel. Distribuir la creación en varios marcos o reutilizar recursos sin crearlos o liberarlos. Idealmente, debe esperar varias tramas antes de bloquear o liberar los recursos que se usaron recientemente para su presentación.
-   Al final del marco, asegúrese de desenlazar todos los canales de recursos (es decir, los orígenes de flujo, las fases de textura y los índices actuales). De este modo, se asegurará de que las referencias pendientes a los recursos se quitan antes de que el administrador de recursos Mantenga los recursos residentes que realmente ya no están en uso.
-   En el caso de las texturas, use formatos comprimidos (por ejemplo, DXTn) con mapas MIP y considere la posibilidad de usar un Atlas de textura. Esto reduce en gran medida los requisitos de ancho de banda y pueden reducir el tamaño total de los recursos, por lo que son más eficientes.
-   En el caso de Geometry, haga uso de la geometría indizada como ayuda para comprimir los recursos de búfer de vértices y el hardware de vídeo moderno está muy optimizado en torno a la reutilización de vértices. Mediante el uso de sombreadores de vértices programables, puede comprimir la información de vértices y expandirla durante el procesamiento de vértices. De nuevo, esto ayuda a reducir los requisitos de ancho de banda y facilita los recursos de búfer de vértices.
-   Evite la optimización de la administración de recursos. Las revisiones futuras de los controladores, el hardware y el sistema operativo pueden causar problemas de compatibilidad si la aplicación se ajusta demasiado a una combinación especialmente. Dado que la mayoría de las aplicaciones están enlazadas a la CPU, la administración basada en CPU es costosa, por lo general, genera más problemas de rendimiento de los que resuelve.

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

 

 