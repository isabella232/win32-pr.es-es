---
title: Glosario de Direct3D 12
description: Estos términos son distintivos de Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549167"
---
# <a name="direct3d-12-glossary"></a>Glosario de Direct3D 12

Estos términos son distintivos de Direct3D 12.

<dl> <dt>

<span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**enlace**
</dt> <dd>

Proceso de adjuntar memoria a la canalización de gráficos. Por ejemplo, el enlace de recursos implica el enlace de un recurso, como una textura a la canalización, para su uso en la representación de un objeto.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**búfer**
</dt> <dd>

Un tipo de recurso D3D que es sinónimo de una asignación de memoria contigua.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**lotes**
</dt> <dd>

Un búfer de comandos que la unidad de procesamiento de gráficos (GPU) puede ejecutar solo directamente a través de una *lista de comandos directa*. Una agrupación hereda todo el estado de la GPU (excepto el *objeto de estado de la canalización* establecido actualmente y la topología primitiva).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**Asignador de comandos**
</dt> <dd>

Las asignaciones de memoria subyacentes en las que se almacenan los comandos de GPU. El objeto de asignador de comandos se aplica tanto a *las listas de comandos directas* como a las *agrupaciones*.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**lista de comandos**
</dt> <dd>

Una lista de comandos corresponde a un conjunto de comandos que se ejecutan en la GPU. Estos incluyen comandos como para establecer el estado, dibujar, borrar y copiar. La interfaz de la lista de comandos D3D12 es significativamente diferente de la interfaz de la lista de comandos de D3D11. La interfaz de la lista de comandos de D3D12 contiene API similares a las API de representación de contexto de dispositivo D3D11.

Una lista de comandos D3D12 no asigna ni anula la asignación de recursos, cambia las asignaciones de iconos, cambia el tamaño de los grupos de mosaicos, obtiene los datos de la consulta ni envía implícitamente comandos a la GPU para su ejecución.

A diferencia de los contextos diferidos de D3D11, las listas de comandos de D3D12 solo admiten dos niveles de direccionamiento indirecto. Una *lista de comandos directa* corresponde a un búfer de comandos que la GPU puede ejecutar. Un *paquete* solo puede ejecutarse directamente a través de una lista de comandos directa.

Una lista de comandos directa no hereda ningún estado de GPU. Una agrupación hereda todo el estado de la GPU (excepto el objeto de estado de la canalización establecido actualmente y la topología primitiva).

El *asignador de comandos* establece la memoria para una lista de comandos. El propósito de las listas de comandos es que se pueden enviar a una GPU como una única solicitud de representación.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**cola de comandos**
</dt> <dd>

Una cola de *comandos enumera* que la GPU se ejecuta sucesivamente. Las aplicaciones deben enviar explícitamente *listas de comandos* a una cola de comandos para su ejecución. Normalmente hay tres colas de comandos: gráficos 3D, proceso y copia, que se corresponden con la canalización de gráficos 3D, el motor de proceso y uno o varios motores de copia, en la GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**rasterización conservadora**
</dt> <dd>

La rasterización conservadora es un modo de funcionamiento para la fase de rasterización de la canalización de gráficos Direct3D. Deshabilita la rasterización estándar basada en muestras y, en su lugar, rasteriza un píxel que está incluido en cualquier cantidad por parte de una primitiva. Una diferencia importante es que, mientras que cualquier cobertura produce un píxel rasterizado, esa cobertura no se puede caracterizar por el hardware, por lo que la cobertura siempre aparece como binario en un sombreador de píxeles: totalmente cubierto o no cubierto. Se deja en el código del sombreador de píxeles para determinar de forma analítica la cobertura real.

La rasterización conservadora puede ayudar a resolver estos problemas como colisiones y detección de aciertos, discretización y eliminación de la oclusión, donde el color de un píxel es más cierto y se pueden eliminar los casos extremos. Vea [rasterización conservadora](conservative-rasterization.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Vista de búfer de constantes (CBV)**
</dt> <dd>

Los búferes de constantes contienen datos de constantes del sombreador, como una vista de cámara, matrices de proyección y matrices mundiales. Una "vista de búfer de constantes" es la vista específica del formato del búfer tal como la muestra la canalización de gráficos.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**montón predeterminado**
</dt> <dd>

Un montón de modo de usuario que se centra en admitir tipos de recursos de GPU persistentes, incluidos los recursos escritos por GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**scripto**
</dt> <dd>

Los descriptores son la unidad principal de enlace para un único recurso de D3D12. Un descriptor es un bloque de datos relativamente pequeño que describe por completo un objeto para la GPU, en un formato específico de GPU. Hay muchos tipos diferentes de descriptores: las vistas de recursos del sombreador (SRVs), las vistas de acceso desordenado (UAVs), las vistas de búfer de constantes (CBVs) y los muestreadores son algunos ejemplos.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**montón de descriptores**
</dt> <dd>

Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor. El punto principal de un montón de descriptores consiste en abarcar la mayor parte de la asignación de memoria necesaria para almacenar las especificaciones de descriptor de tipos de objeto a los que los sombreadores hacen referencia para el tamaño de una ventana de representación lo más grande posible (lo ideal es un marco completo de representación o más).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**tabla de descriptores**
</dt> <dd>

Una tabla de descriptores es lógicamente una matriz de descriptores. Cada tabla de descriptores almacena descriptores de uno o varios tipos, incluidos SRVs, UAVe, CBVs y muestreadores. Una tabla de descriptores no es una asignación de memoria, sino simplemente un desplazamiento y una longitud en un montón de descriptores.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**lista de comandos directos**
</dt> <dd>

Un búfer de comandos que la GPU puede ejecutar. Una lista de comandos directa no hereda ningún estado de GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**barrera**
</dt> <dd>

Un mecanismo para sincronizar la GPU y la CPU. Se puede indicar a la GPU y la CPU que esperen a una barrera, esperando en vigor para que el otro procesador se ponga al día. Consulte [sincronización de varios motores](./user-mode-heap-synchronization.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**riesgo, seguimiento de peligros**
</dt> <dd>

Se produce un riesgo cuando se ha usado un recurso para un propósito y la aplicación intenta volver a usarlo para otro propósito. Para poder usar el recurso de nuevo, es necesario vaciar o invalidar las memorias caché intermedias, los requisitos de compresión deben ser coherentes con el segundo uso y el recurso debe estar en el Estado requerido para evitar la lectura del recurso una vez que se ha escrito e invalidado para el propósito previsto.

El proceso de mantenimiento de los recursos y la prevención de estos problemas de sincronización se conoce como seguimiento de peligros. Si el controlador no realiza ningún seguimiento de los peligros, la aplicación es responsable de ello. En la mayoría de las versiones anteriores de DirectX, el seguimiento del riesgo lo controlaba el controlador. Para mejorar el rendimiento, los métodos sin seguimiento de peligros están disponibles en DirectX 12.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**Lenguaje de sombreador de alto nivel (HLSL)**
</dt> <dd>

Un lenguaje informático, similar pero distinto en muchas formas de C, que se usa para escribir código de sombreador. Todos los sombreadores de vértices, píxeles, Geometry, compute, Domain y casco se escriben con HLSL. Un compilador convierte el origen de HLSL en un formato binario para que lo consuma la GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multimotor**
</dt> <dd>

Las distintas instancias y tipos de motores en una sola GPU. Los tipos de motores incluyen: gráficos, proceso y copia.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**
</dt> <dd>

Una configuración de hardware donde hay más de un adaptador de gráficos. A veces, a los adaptadores independientes se les denomina nodos. El hecho de tener varias GPU puede hacer que la tarea de sincronizarlas con la CPU y entre ellas sea considerablemente más compleja que con una sola GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Objeto de estado de canalización (PSO)**
</dt> <dd>

Una parte significativa del estado de la GPU. Este estado incluye todos los sombreadores establecidos actualmente y determinados objetos de estado de función fija. La única manera de cambiar los Estados contenidos en el objeto de canalización es cambiar el objeto de canalización enlazado actualmente.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predication**
</dt> <dd>

Predication es una característica que permite que la GPU en lugar de la CPU determine no dibujar, copiar o enviar un objeto. Por ejemplo, si un cuadro de límite de un objeto es totalmente ocluidos por otro objeto o la perspectiva ha reducido el objeto a un tamaño menor que el de un píxel, puede que no haya ningún punto intentando dibujar el objeto oculto. Vea [Predication](predication.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Vista de orden de rasterizador (ROV)**
</dt> <dd>

Las canalizaciones de gráficos estándar pueden tener problemas al componer varias texturas que contienen transparencias correctamente. Los objetos como las barreras de alambres, humos, incendios, vegetación y vidrio en color usan transparencia para obtener el efecto deseado. Surgen problemas cuando varias texturas que contienen transparencias están alineadas entre sí (humo delante de una barrera delante de un edificio de vidrio que contiene vegetación, por ejemplo). Las vistas ordenadas de rasterizador (ROVs) permiten que los algoritmos subyacentes de transparencia independiente de orden (OIT) usen características del hardware para intentar resolver el orden de transparencia correctamente. El sombreador de píxeles controla la transparencia.

Las vistas ordenadas de rasterizador (ROVs) permiten que el código del sombreador de píxeles marque los enlaces de vista de acceso desordenado (UAV) con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para UAVs.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**montón readback**
</dt> <dd>

Un montón de modo de usuario que se centra en la transferencia de datos desde la GPU de vuelta a la CPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**recurso**
</dt> <dd>

Una entidad que proporciona datos a la canalización y define lo que se representa durante la escena. Los recursos se pueden cargar desde el medio de juego o se pueden crear dinámicamente en tiempo de ejecución. Normalmente, los recursos incluyen datos de textura, datos de vértices y datos de sombreador. La mayoría de las aplicaciones de Direct3D crean y destruyen los recursos mucho a lo largo de su duración.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**barrera de recursos**
</dt> <dd>

Una barrera de recursos notifica al controlador que se puede requerir la sincronización de varios accesos a un único recurso, por ejemplo, para leer y escribir en la misma textura.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**enlace de recursos**
</dt> <dd>

El enlace de recursos es el proceso de vinculación de recursos (texturas, búferes de vértices, búferes de índice, etc.) a la canalización de gráficos, lo que permite a los sombreadores de la canalización procesar el recurso correcto.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**montones de recursos**
</dt> <dd>

Los montones de recursos son un término genérico para los montones que son búferes de memoria que se reservan para contener recursos a medida que se transfieren hacia y desde la GPU. Una transferencia a la GPU requiere un montón de carga, de la GPU a la CPU requiere un montón de Readback y un montón persistente para que la GPU se mantenga en varios fotogramas de representación se denomina montón predeterminado.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**firma raíz**
</dt> <dd>

Las signaturas raíz definen todos los recursos que se van a enlazar a las canalizaciones de gráficos o de proceso. Las listas de comandos de la aplicación y de vínculos configuran una firma raíz para los recursos que los sombreadores requieren normalmente, hay un gráfico y una firma de raíz de proceso por aplicación.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**muestras**
</dt> <dd>

Una muestra es el código que lee de una textura.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Sombreador Vista de recursos (SRV)**
</dt> <dd>

Una forma específica del formato de ver los datos de un recurso de sombreador, como una textura.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**montón estático**
</dt> <dd>

Un montón de modo de usuario que se centra en varios recursos de solo lectura de GPU que se usan normalmente al mismo tiempo y que no cambian con frecuencia.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**cadena de intercambio**
</dt> <dd>

Las cadenas de intercambio controlan la rotación del búfer de reserva, formando la base de la animación de gráficos. Las cadenas de intercambio se controlan mediante el conjunto de API de bajo nivel de DXGI (consulte [información general sobre dxgi](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**
</dt> <dd>

Técnica de ubicación de datos multidimensionales en memoria de modo que los datos de la dimensionalidad cercana suelen tener direcciones cercanas. En concreto, todos los datos de una fila no se colocan de forma contigua delante de los datos de la fila siguiente. Un "Swizzle con parámetros" describe una forma estandarizada de describir patrones de swizzle.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**degrada**
</dt> <dd>

Un tipo de recurso D3D que es multidimensional y tiene un diseño de memoria que está optimizado para el acceso multidimensional desde la GPU. Las texturas suelen contener la imagen sin procesar necesaria para representarla en una superficie, antes de que tenga lugar la iluminación y la fusión, pero puede contener otras formas de datos, como degradados de color y colores de referencia. Direct3D 12 admite texturas de una, dos y tres dimensiones.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**posición**
</dt> <dd>

Página de memoria de vídeo, similar a una página de CPU/sistema de memoria. La notación de mosaico ayuda a distinguir el subsistema de memoria virtual de GPU del subsistema de memoria virtual de CPU. Las GPU proporcionan capacidades de memoria virtual similares como memoria virtual del sistema. Algunas GPU tienen capacidades de memoria virtual compartidas, que permiten el uso compartido de algunas páginas del subsistema de memoria virtual con la CPU y la GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**recursos en mosaico**
</dt> <dd>

Los recursos en mosaico son necesarios, por lo que no se podrá tener acceso a la memoria de GPU, y el hardware puede comprender cómo filtrar por los mosaicos adyacentes. Los recursos en mosaico son recursos lógicos de gran tamaño, pero requieren pequeñas cantidades de memoria física.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Vista de acceso desordenado (UAV)**
</dt> <dd>

Una vista de acceso desordenado en un recurso (que incluye búferes, texturas y matrices de texturas, sin muestreo múltiple), permite el acceso de lectura y escritura desordenado temporal desde varios subprocesos. Esto significa que varios subprocesos pueden leer o escribir este tipo de recurso simultáneamente sin generar conflictos de memoria.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**cargar montón**
</dt> <dd>

Un montón de modo de usuario que se centra en la transferencia de datos desde la CPU a la GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**montón de modo de usuario**
</dt> <dd>

Colección de asignaciones de memoria grandes y contiguas que se reciclan sin ningún conocimiento del componente kernel: los métodos de asignación y destrucción no llaman a los métodos de asignación y destrucción del kernel durante el estado estable. Los montones de carga, Readback y predeterminado son variantes de montones de modo de usuario.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**recursos en mosaico de volumen**
</dt> <dd>

[Recursos en mosaico](/windows)tridimensionales.

</dd> </dl>

 

 