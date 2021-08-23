---
title: Glosario de Direct3D 12
description: Estos términos son distintivos de Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a7ad8d9c925d4bd3b82a3c7dd177a58afd7f50fb82836bed56fac6a20c8f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496885"
---
# <a name="direct3d-12-glossary"></a>Glosario de Direct3D 12

Estos términos son distintivos de Direct3D 12.

<dl> <dt>

<span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**Vinculante**
</dt> <dd>

Proceso de adjuntar memoria a la canalización de gráficos. El enlace de recursos, por ejemplo, implica el enlace de un recurso, como una textura, a la canalización, para su uso en la representación de un objeto.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**Búfer**
</dt> <dd>

Tipo de recurso D3D que es sinónimo de una asignación de memoria contigua.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**Paquete**
</dt> <dd>

Búfer de comandos que la unidad de procesamiento gráfico (GPU) solo puede ejecutar directamente a través de una *lista de comandos directos.* Un conjunto hereda todo el estado de GPU (excepto el objeto de estado de canalización establecido actualmente *y* la topología primitiva).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**asignador de comandos**
</dt> <dd>

Asignaciones de memoria subyacentes en las que se almacenan los comandos de GPU. El objeto de asignador de comandos se aplica tanto a listas *de comandos directos* como *a agrupaciones.*

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**lista de comandos**
</dt> <dd>

Una lista de comandos corresponde a un conjunto de comandos que ejecuta la GPU. Estos incluyen comandos como para establecer el estado, dibujar, borrar y copiar. La interfaz de lista de comandos D3D12 es significativamente diferente de la interfaz de lista de comandos D3D11. La interfaz de lista de comandos D3D12 contiene API similares a las API de representación del contexto de dispositivo D3D11.

Una lista de comandos D3D12 no asigna ni desa asigna recursos, cambia las asignaciones de mosaicos, cambia el tamaño de los grupos de mosaicos, obtiene datos de consulta ni nunca envía implícitamente comandos a la GPU para su ejecución.

A diferencia de los contextos diferidos de D3D11, las listas de comandos D3D12 solo admiten dos niveles de direccionamiento indirecto. Una *lista de comandos directos* corresponde a un búfer de comandos que la GPU puede ejecutar. Una *agrupación* solo se puede ejecutar directamente a través de una lista de comandos directos.

Una lista de comandos directos no hereda ningún estado de GPU. Un conjunto hereda todo el estado de GPU (excepto el objeto de estado de canalización establecido actualmente y la topología primitiva).

El asignador de comandos establece la memoria de una lista *de comandos.* El propósito de las listas de comandos es que se pueden enviar a una GPU como una única solicitud de representación.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**cola de comandos**
</dt> <dd>

Una cola de *comandos muestra* que la GPU se ejecuta sucesivamente. Las aplicaciones deben enviar explícitamente *listas de comandos* a una cola de comandos para su ejecución. Normalmente hay tres colas de comandos: gráficos 3D, proceso y copia, correspondientes a la canalización de gráficos 3D, el motor de proceso y uno o varios motores de copia, en la GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**rasterización conservadora**
</dt> <dd>

La rasterización conservadora es un modo de operación para la fase de rasterizador de la canalización de gráficos de Direct3D. Deshabilita la rasterización basada en muestras estándar y, en su lugar, rasteriza un píxel cubierto por cualquier cantidad por una primitiva. Una distinción importante es que, aunque cualquier cobertura en absoluto genera un píxel rasterizado, esa cobertura no se puede caracterizar por el hardware, por lo que la cobertura siempre parece binaria para un sombreador de píxeles: totalmente cubierta o no cubierta. Se deja en el código del sombreador de píxeles para determinar analíticamente la cobertura real.

La rasterización conservadora puede ayudar con problemas como la detección de colisiones y impactos, la detección de colisiones y oclusión, donde el color de un píxel es más seguro y se pueden eliminar los casos perimetrales. Consulte [Rasterización conservadora.](conservative-rasterization.md)

</dd> <dt>

<span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Vista búfer constante (CBV)**
</dt> <dd>

Los búferes constantes contienen datos constantes del sombreador, como una vista de cámara, matrices de proyección y matrices de mundo. Una "vista de búfer constante" es la vista específica del formato del búfer, tal como la canalización de gráficos ve.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**montón predeterminado**
</dt> <dd>

Un montón en modo de usuario que se centra en admitir tipos de recursos de GPU persistentes, incluidos los recursos escritos por GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**Descriptor**
</dt> <dd>

Los descriptores son la unidad principal de enlace para un único recurso en D3D12. Un descriptor es un bloque de datos relativamente pequeño que describe completamente un objeto para la GPU, en un formato específico de GPU. Hay muchos tipos diferentes de descriptores: Vistas de recursos de sombreador (SRV), Vistas de acceso desordenado (UAV), Vistas de búfer constante (CBV) y Muestreadores son algunos ejemplos.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**montón de descriptores**
</dt> <dd>

Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor. El punto principal de un montón de descriptores es abarcar la mayor parte de la asignación de memoria necesaria para almacenar las especificaciones de descriptor de tipos de objeto a los que hacen referencia los sombreadores para el mayor tamaño posible de una ventana de representación (idealmente un marco completo de representación o más).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**tabla de descriptores**
</dt> <dd>

Una tabla de descriptores es lógicamente una matriz de descriptores. Cada tabla de descriptores almacena descriptores de uno o varios tipos, incluidos SRV, UAVe, CBV y Samplers. Una tabla de descriptores no es una asignación de memoria, simplemente es un desplazamiento y una longitud en un montón de descriptores.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**direct command list**
</dt> <dd>

Búfer de comandos que la GPU puede ejecutar. Una lista de comandos directos no hereda ningún estado de GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**Cerca**
</dt> <dd>

Mecanismo para sincronizar la GPU y la CPU. Se puede indicar a la GPU y a la CPU que esperen en una barrera, esperando en vigor a que el otro procesador se pueda ponerse al día. Consulte [Sincronización de varios motores.](./user-mode-heap-synchronization.md)

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**peligro, seguimiento de riesgos**
</dt> <dd>

Un peligro se produce cuando se ha usado un recurso para un propósito y la aplicación pretende reutilizarlo para otro propósito. Para volver a usar el recurso, las memorias caché intermedias deberán vaciarse o invalidarse, los requisitos de compresión deberán ser coherentes con el segundo uso y el recurso debe estar en el estado necesario para evitar leer el recurso después de que se haya escrito e invalidado para el propósito previsto.

El proceso de mantener los recursos y evitar estos problemas de sincronización se conoce como seguimiento de riesgos. Si no hay ningún seguimiento de riesgos por parte del controlador, la aplicación es responsable de esto. En la mayoría de las versiones anteriores de DirectX, el controlador controló el seguimiento de riesgos. Para mejorar el rendimiento, los métodos sin seguimiento de riesgos están disponibles en DirectX 12.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**Lenguaje de sombreador de alto nivel (HLSL)**
</dt> <dd>

Un lenguaje informático, similar pero distinto en muchos sentidos de C, que se usa para escribir código de sombreador. Los sombreadores de vértice, píxel, geometría, proceso, dominio y casco se escriben mediante HLSL. Un compilador convierte el origen HLSL en un formato binario para que lo consuma la GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**
</dt> <dd>

Las distintas instancias y tipos de motores en una sola GPU. Los tipos de motores incluyen: gráficos, proceso y copia.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**
</dt> <dd>

Una configuración de hardware donde hay más de un adaptador de gráficos. Los adaptadores independientes a veces se conocen como nodos. Tener varias GPU puede hacer que la tarea de sincronizarlas con la CPU y entre sí sea considerablemente más compleja que con una sola GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Objeto Pipeline State (PSO)**
</dt> <dd>

Una parte significativa del estado de la GPU. Este estado incluye todos los sombreadores establecidos actualmente y determinados objetos de estado de función fija. La única manera de cambiar los estados contenidos en el objeto de canalización es cambiar el objeto de canalización enlazado actualmente.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**Predicación**
</dt> <dd>

Predication es una característica que permite que la GPU en lugar de la CPU determine que no se debe dibujar, copiar ni enviar un objeto. Por ejemplo, si un rectángulo delimitador de un objeto está totalmente ocluido por otro objeto o perspectiva ha reducido el objeto a menos del tamaño de un píxel, puede que no tenga sentido intentar dibujar el objeto oculto en absoluto. Vea [Predication](predication.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Vista de orden de rasterizador (ROV)**
</dt> <dd>

Las canalizaciones de gráficos estándar pueden tener problemas para componer correctamente varias texturas que contienen transparencia. Los objetos como las barreras de cable, el humo, el incendio, la humedad y el cristal coloreado usan la transparencia para obtener el efecto deseado. Los problemas surgen cuando varias texturas que contienen transparencia están en línea entre sí (por ejemplo, el humo delante de una barrera delante de un edificio de cristal que contiene humedad). Las vistas ordenadas por rasterizador (ROV) permiten que los algoritmos subyacentes de transparencia independiente de pedidos (RSA) usen características del hardware para intentar resolver el orden de transparencia correctamente. El sombreador de píxeles controla la transparencia.

Las vistas ordenadas por rasterizador (ROV) permiten que el código del sombreador de píxeles marque los enlaces de vista de acceso desordenado (UAV) con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para los UAV.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**montón de readback**
</dt> <dd>

Un montón en modo de usuario que se centra en la transferencia de datos desde la GPU de vuelta a la CPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**Recursos**
</dt> <dd>

Entidad que proporciona datos a la canalización y define lo que se representa durante la escena. Los recursos se pueden cargar desde los medios del juego o crearse dinámicamente en tiempo de ejecución. Normalmente, los recursos incluyen datos de textura, datos de vértices y datos de sombreador. La mayoría de las aplicaciones de Direct3D crean y destruyen recursos ampliamente a lo largo de su vida útil.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**barrera de recursos**
</dt> <dd>

Una barrera de recursos notifica al controlador que puede ser necesaria la sincronización de varios accesos a un único recurso, por ejemplo, leer y escribir en la misma textura.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**enlace de recursos**
</dt> <dd>

El enlace de recursos es el proceso de vincular recursos (texturas, búferes de vértices, búferes de índice, entre otros) a la canalización de gráficos, lo que permite que los sombreadores de la canalización procese el recurso correcto.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**montones de recursos**
</dt> <dd>

Los montones de recursos son un término genérico para los montones que son búferes de memoria reservados para contener los recursos a medida que se transfieren a y desde la GPU. Una transferencia a la GPU requiere un montón de Upload, desde la GPU a la CPU requiere un montón de readback y un montón persistente para que la GPU mantenga en varios fotogramas de representación se denomina montón predeterminado.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**firma raíz**
</dt> <dd>

Las firmas raíz definen todos los recursos que se van a enlazar a las canalizaciones de gráficos o proceso. La aplicación configura una firma raíz y vincula listas de comandos a los recursos que los sombreadores requieren Normalmente, hay un gráfico y una firma raíz de proceso por aplicación.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**Sampler**
</dt> <dd>

Un sampler es código que lee de una textura.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Sombreador Vista de recursos (SRV)**
</dt> <dd>

Una manera específica del formato de ver los datos de un recurso de sombreador, como una textura.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**montón estático**
</dt> <dd>

Un montón en modo de usuario que se centra en varios recursos de solo lectura de GPU que normalmente se usan al mismo tiempo y no se cambian con frecuencia.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**cadena de intercambio**
</dt> <dd>

Las cadenas de intercambio controlan la rotación del búfer de reserva, formando la base de la animación gráfica. Las cadenas de intercambio se controlan mediante el conjunto de API de bajo nivel DXGI (consulte [Información general de DXGI).](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**Swizzle**
</dt> <dd>

Técnica de localización de datos multidimensionales en memoria, de modo que los datos de dimensionalidad cercana tienden a tener direcciones cercanas. En concreto, todos los datos de una fila no se encuentran de forma contigua antes de los datos de la fila siguiente. Un "Swzzle con parámetros" describe una manera estandarizada de describir patrones swzzle.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**Textura**
</dt> <dd>

Tipo de recurso D3D que es multidimensional y tiene un diseño de memoria optimizado para el acceso multidimensional desde la GPU. Las texturas suelen contener la imagen sin formato necesaria para representarse en una superficie, antes de que se lleve a cabo la iluminación y la mezcla, pero pueden contener otras formas de datos, como degradados de color y colores de referencia. Direct3D 12 admite una, dos y texturas tridimensionales.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**Azulejo**
</dt> <dd>

Una página de memoria de vídeo, similar a una página cpu/sistema de memoria. La notación de mosaico ayuda a distinguir el subsistema de memoria virtual de GPU del subsistema de memoria virtual de CPU. Las GPU proporcionan funcionalidades de memoria virtual similares a la memoria virtual del sistema. Algunas GPU tienen funcionalidades de memoria virtual compartida, que permiten compartir algunas páginas del subsistema de memoria virtual con la CPU y la GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**recursos en mosaico**
</dt> <dd>

Se necesitan recursos en mosaico, por lo que se desperdicia menos memoria de GPU almacenando regiones de superficies a las que la aplicación sabe que no se accederá y el hardware puede entender cómo filtrar entre iconos adyacentes. Los recursos en mosaico son recursos lógicos grandes, pero requieren pequeñas cantidades de memoria física.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Vista de acceso sin ordenar (UAV)**
</dt> <dd>

Una vista de acceso desordenado en un recurso (que incluye búferes, texturas y matrices de texturas, sin muestreo múltiple), permite el acceso de lectura y escritura desordenado temporalmente desde varios subprocesos. Esto significa que varios subprocesos pueden leer o escribir simultáneamente este tipo de recurso sin generar conflictos de memoria.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**carga del montón**
</dt> <dd>

Un montón en modo de usuario que se centra en la transferencia de datos desde la CPU a la GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**montón en modo de usuario**
</dt> <dd>

Colección de asignaciones de memoria grandes y contiguas que se reciclan sin el reconocimiento de ningún componente de kernel: los métodos de asignación y destrucción no llaman a los métodos de asignación y destrucción del kernel durante el estado estable. Upload, Readback y Default heaps son variantes de montones de modo de usuario.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**recursos en mosaico de volumen**
</dt> <dd>

Recursos en [mosaico tridimensionales](/windows).

</dd> </dl>

 

 