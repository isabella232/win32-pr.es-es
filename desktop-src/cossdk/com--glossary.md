---
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: Glosario de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5a6cb30529cd8b97b8cf11316347d68003e32c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496121"
---
# <a name="com-glossary"></a>Glosario de COM+

<dl> <dt>

<span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**token de acceso**
</dt> <dd>

Objeto que describe el contexto de seguridad de un proceso o subproceso. La información de un token incluye la identidad y los privilegios de la cuenta de usuario asociada con el proceso o subproceso. Cuando un usuario inicia sesión, el sistema comprueba la contraseña del usuario comparándola con la información almacenada en una base de datos de seguridad. Si la contraseña se autentica, el sistema genera un token de acceso. Cada proceso ejecutado en nombre de este usuario tiene una copia de este token de acceso.

</dd> <dt>

<span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**Propiedades ACID**
</dt> <dd>

Acrónimo acuñó de los pioneros en el procesamiento de transacciones para atomicidad, coherencia, aislamiento y durabilidad. Estas propiedades garantizan un comportamiento predecible, lo que refuerza el rol de las transacciones como proposiciones All-or-None diseñadas para proporcionar resultados coherentes y predecibles en un entorno distribuido cuando se pueden producir errores independientes.

</dd> <dt>

<span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**activación**
</dt> <dd>

Cadena de eventos que tiene como resultado la creación de un objeto COM y la devolución de un puntero válido a una interfaz en ese objeto. En COM+, un objeto se activa en su propio contexto o en el de su creador (un objeto que ha solicitado el objeto que se está activando). Los servicios COM+ dependen de la activación adecuada de un objeto en función de la configuración del objeto. En el transcurso de la activación, el sistema determina el contexto en el que se ejecuta el objeto, inicializa las propiedades de contexto, comprueba los permisos de acceso y establece una identidad de seguridad.

</dd> <dt>

<span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**seguridad de activación**
</dt> <dd>

Forma de protección de seguridad que determina quién puede iniciar un servidor. El administrador de control de servicios (SCM) de un equipo determinado aplica automáticamente la seguridad de activación. Tras recibir una solicitud de un cliente para activar un objeto, el SCM comprueba la solicitud con la información de seguridad de activación almacenada en el registro. También se comprueba la seguridad de activación para las activaciones del mismo equipo. También se denomina *seguridad de inicio*.

</dd> <dt>

<span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**tipo de activación**
</dt> <dd>

Categoría de activación para una aplicación COM+ que indica si la aplicación se ejecuta dentro o fuera del espacio de proceso de su cliente (en función de si se trata de una aplicación de biblioteca o servidor, respectivamente) y de si la aplicación se ejecuta como un servicio.

</dd> <dt>

<span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**proceso**
</dt> <dd>

En COM+, subproceso lógico que consta de una o varias transacciones y que contiene una colección de componentes que se agrupan en una aplicación COM+. Cada objeto COM pertenece a una actividad. No se puede cambiar la asociación entre un objeto y una actividad.

</dd> <dt>

<span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**proceso del modelo de apartamento**
</dt> <dd>

Proceso que tiene dos o más apartamentos de un solo subproceso y sin apartamentos multiproceso.

</dd> <dt>

<span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**proxy de aplicación**
</dt> <dd>

Conjunto de archivos que contiene información de registro que permite a un cliente tener acceso remoto a una aplicación de servidor COM+. Cuando se instala en un equipo cliente, un archivo de proxy de aplicación escribe información acerca de la aplicación de servidor en el equipo cliente. después, el cliente puede tener acceso de forma remota a la aplicación de servidor.

</dd> <dt>

<span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**autenticación**
</dt> <dd>

El proceso de seguridad para determinar que un llamador de una aplicación es realmente quien dice ser: comprobar la autenticidad de una solicitud de identidad. En el caso de las aplicaciones COM+, la autenticación se puede activar y configurar de forma administrativa, después de que funciona de forma transparente en la aplicación.

</dd> <dt>

<span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**on**
</dt> <dd>

El proceso de seguridad que determina si un llamador de una aplicación está autorizado para hacer lo que se le pide.

</dd> <dt>

<span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**almacenamiento en caché de Resource Manager**
</dt> <dd>

Un administrador de recursos que actúa como front-end a otro administrador de recursos y que almacena en caché la información de forma local, lo que reduce el costo de acceso al recurso subyacente. A diferencia de un administrador de recursos convencional, un administrador de recursos de almacenamiento en caché no participa en la recuperación porque nunca almacena permanentemente los datos subyacentes.

</dd> <dt>

<span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**seguridad de llamadas**
</dt> <dd>

Forma de protección de seguridad que ayuda a controlar el acceso a los métodos de un objeto de servidor después de que se haya iniciado un servidor.

</dd> <dt>

<span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**(clase) (COM)**
</dt> <dd>

Una implementación concreta y con nombre de una o más interfaces. Una clase COM se identifica mediante un CLSID y, a veces, un ProgID.

</dd> <dt>

<span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**esconder**
</dt> <dd>

La capacidad de un servidor de enmascarar su propia identidad al realizar llamadas en el nombre de un cliente. Cuando está habilitada la ocultación, las llamadas realizadas por el servidor que suplanta al cliente pueden realizarse en la identidad del cliente. Cuando se deshabilita la ocultación, las llamadas realizadas por el servidor se realizarán en la identidad del servidor.

</dd> <dt>

<span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Aplicación COM+**
</dt> <dd>

La unidad principal de administración y seguridad de servicios de componentes. Una aplicación COM+ es un grupo de componentes COM que, por lo general, realizan funciones relacionadas. Estos componentes se componen además de interfaces y métodos COM.

</dd> <dt>

<span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Agrupación de aplicaciones COM+**
</dt> <dd>

Característica de servicios de componentes que permite escalar los procesos de un solo subproceso y también puede ayudarle a recuperarse de los errores en procesos únicos proporcionando otros procesos en ejecución capaces de controlar las activaciones.

</dd> <dt>

<span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Reciclaje de aplicaciones COM+**
</dt> <dd>

Característica de servicios de componentes que aumenta significativamente la estabilidad general de las aplicaciones, ya que permite cerrar correctamente un proceso asociado a una aplicación y reiniciarlo.

</dd> <dt>

<span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Catálogo de COM+** 
</dt> <dd>

Almacén de datos que contiene los datos de configuración de COM+. El rendimiento de las tareas de administración de COM+ requiere leer y escribir datos almacenados en el catálogo. Solo se puede tener acceso al catálogo a través de la herramienta administrativa Servicios de componentes o a través de la biblioteca COMAdmin.

</dd> <dt>

<span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Eventos COM+**
</dt> <dd>

Los eventos COM+ coinciden y conectan a publicadores y suscriptores a través de un sistema de eventos de acoplamiento flexible. Un publicador realiza la llamada al método para iniciar un evento y un suscriptor recibe estas llamadas a través del sistema de eventos en lugar de hacerlo directamente desde el publicador. El servicio de eventos COM+ mantiene la lista de suscriptores interesados que reciben las llamadas y dirige esas llamadas sin necesidad de conocer el publicador.

</dd> <dt>

<span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Aplicación de biblioteca COM+**
</dt> <dd>

Aplicación COM+ que se ejecuta en el proceso del cliente que la crea. Las aplicaciones de biblioteca pueden utilizar la seguridad basada en roles pero no admiten el acceso remoto o los componentes en cola.

</dd> <dt>

<span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Agrupación de objetos COM+**
</dt> <dd>

Servicio automático proporcionado por COM+ que le permite configurar un componente para que las instancias de se mantengan activas en un grupo, listas para ser utilizadas por cualquier cliente que solicite el componente.

</dd> <dt>

<span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Particiones COM+**
</dt> <dd>

Servicio COM+ que habilita, en un solo equipo, la creación de espacios de ejecución independientes para las aplicaciones.

</dd> <dt>

<span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Conjuntos de particiones COM+**
</dt> <dd>

Grupo de particiones de COM+ que se asigna a un identificador de usuario determinado en Active Directory.

</dd> <dt>

<span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Componentes en cola de COM+**
</dt> <dd>

Un servicio COM+, basado en Microsoft Message Queuing, que proporciona una manera sencilla de invocar y ejecutar componentes de forma asincrónica. El procesamiento de mensajes puede producirse sin tener en cuenta la disponibilidad o la accesibilidad del remitente o del receptor.

</dd> <dt>

<span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**Aplicación de servidor COM+**
</dt> <dd>

Aplicación COM+ que se ejecuta en su propio proceso. Las aplicaciones de servidor pueden admitir todos los servicios COM+.

</dd> <dt>

<span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**SOAP DE COM+**
</dt> <dd>

Característica de servicios de componentes que permite exponer una aplicación COM+ como un servicio Web XML. El protocolo SOAP de COM+ también le permite utilizar un servicio Web XML como componente COM.

</dd> <dt>

<span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**Componente COM**
</dt> <dd>

Unidad binaria de código que incluye el código de empaquetado y de registro y que crea objetos COM. Todas las aplicaciones COM+ constan de uno o varios componentes COM.

</dd> <dt>

<span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**árbol de confirmación**
</dt> <dd>

En un sistema de transacciones distribuidas, representación conceptual de una transacción según las relaciones jerárquicas entre los administradores de transacciones individuales que participan en una transacción distribuida. En esa jerarquía se incluyen los administradores de recursos inscritos asociados a los administradores de transacciones.

</dd> <dt>

<span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**Objeto COM**
</dt> <dd>

En el modelo de programación COM, una estructura de programación que encapsula los datos y la funcionalidad, que se definen y asignan como una sola unidad y para los que el único acceso público se realiza a través de las interfaces de la estructura de programación. Un objeto COM debe admitir, como mínimo, la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , que mantiene la existencia del objeto mientras se usa y proporciona acceso a las demás interfaces del objeto.

</dd> <dt>

<span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Administrador de recursos de compensaciones (CRM)**
</dt> <dd>

Característica de COM+ que permite a los recursos no transaccionales participar en una transacción de confirmación en dos fases con Microsoft Coordinador de transacciones distribuidas (DTC). Normalmente, los CRMs no proporcionan las capacidades de aislamiento de los administradores de recursos completos, pero proporcionan atomicidad y durabilidad transaccional escribiendo en un registro.

</dd> <dt>

<span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Herramienta administrativa Servicios de componentes**
</dt> <dd>

Complemento de interfaz de usuario a través del cual los administradores y programadores pueden crear, configurar y mantener aplicaciones COM+, así como administrar las transacciones distribuidas y las bases de datos residentes en memoria. La herramienta administrativa Servicios de componentes también se puede usar para ver eventos del sistema y administrar servicios del sistema locales en el equipo en el que está instalada la herramienta.

</dd> <dt>

<span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**modelo conceptual**
</dt> <dd>

El primer paso de la fase de diseño de la aplicación COM+, donde el desarrollador define los problemas empresariales que se van a resolver y decide qué componentes y servicios son necesarios.

</dd> <dt>

<span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**simultaneidad**
</dt> <dd>

La capacidad de más de una transacción o proceso para tener acceso a los mismos datos al mismo tiempo. COM+ normalmente administra la simultaneidad a través de la sincronización.

</dd> <dt>

<span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**componente configurado**
</dt> <dd>

Componente COM que se ha instalado en una aplicación COM+. Una vez instalado, el componente se configura en el catálogo de COM+ para que use los servicios COM+ disponibles.

</dd> <dt>

<span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**contexto**
</dt> <dd>

Conjunto de propiedades de tiempo de ejecución asociadas a uno o varios objetos COM que se usan para proporcionar servicios para esos objetos. Cada objeto COM se ejecuta en un contexto único desde la activación hasta la desactivación (siempre dentro del mismo apartamento). Se inicializa cuando se activa un objeto, las propiedades de contexto, como las propiedades de contexto de seguridad, representan las necesidades de tiempo de ejecución de un objeto.

</dd> <dt>

<span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**capa de datos**
</dt> <dd>

En el modelo de arquitectura de tres niveles para aplicaciones empresariales, la capa de acceso de DBMS, a la que se puede tener acceso a través del nivel intermedio o el nivel de servicios empresariales, y en ocasiones a través del nivel de presentación o el nivel de servicios de usuario. La capa de datos consta de componentes de acceso a datos (en lugar de conexiones DBMS sin formato) para ayudar en el uso compartido de recursos y para permitir que los clientes se configuren sin necesidad de instalar las bibliotecas DBMS y los controladores ODBC en cada cliente. También se denomina *capa de servicios de datos*.

</dd> <dt>

<span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**quedó**
</dt> <dd>

En aplicaciones multiproceso, problema de subprocesos que se produce cuando cada miembro de un conjunto de subprocesos está esperando a otro miembro del conjunto.

</dd> <dt>

<span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**Delegado**
</dt> <dd>

Forma de suplantación que autoriza a un servidor a actuar en nombre de un cliente, lo que permite al servidor suplantar a los clientes a través de la red.

</dd> <dt>

<span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**transacción distribuida**
</dt> <dd>

Una transacción que implica varios administradores de recursos, que puede estar en el mismo equipo o en equipos diferentes.

</dd> <dt>

<span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Coordinador de transacciones distribuidas (DTC)**
</dt> <dd>

Servicio del sistema que administra las transacciones y las comunicaciones relacionadas con las transacciones que se distribuyen entre dos o más administradores de recursos en uno o varios sistemas para garantizar las transacciones ACID correctas.

</dd> <dt>

<span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**Cloaking dinámico**
</dt> <dd>

Forma de Cloaking en la que se detecta la identidad del cliente original como el token de acceso del subproceso del servidor en cada llamada al método en el servidor que sigue en la cadena. Aunque la identidad que se presenta se puede determinar de forma dinámica, la sobrecarga necesaria para ello puede ser considerablemente más costosa. En el caso de las aplicaciones COM+, la configuración predeterminada es para la funcionalidad de ocultación dinámica, ya que proporciona la flexibilidad que suele ser necesaria en las circunstancias que requieren el uso de la suplantación en primer lugar.

</dd> <dt>

<span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**objeto Enumerator**
</dt> <dd>

Permite la enumeración de elementos en una colección.

</dd> <dt>

<span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**ceso**
</dt> <dd>

Acción reconocida por un objeto, como hacer clic con el mouse o presionar una tecla, y para la que puede escribir código para responder.

</dd> <dt>

<span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**objeto de clase de evento**
</dt> <dd>

Componente configurado que proporciona un registro persistente en el sistema de eventos COM+ para describir los publicadores y las interfaces de activación asociadas a esos publicadores.

</dd> <dt>

<span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**Event (método)**
</dt> <dd>

Método en una interfaz de COM+ que identifica un evento de COM+. Los métodos de evento deben tener un nombre único y solo pueden contener parámetros de entrada. El valor devuelto debe ser **HRESULT**.

</dd> <dt>

<span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**objeto de evento**
</dt> <dd>

Objeto COM que puede señalar uno o más subprocesos que se ha producido un evento. Cualquier subproceso de un proceso puede crear un objeto de evento.

</dd> <dt>

<span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**excepcional**
</dt> <dd>

Una condición anómala o un error que se produce durante la ejecución de un programa y que requiere la ejecución de software fuera del flujo de control normal.

</dd> <dt>

<span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**muta**
</dt> <dd>

En un sistema de red de clústeres, proceso de reubicación de un recurso sobrecargado o con errores, como un servidor, una unidad de disco o una red, a su componente de copia de seguridad.

</dd> <dt>

<span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**proceso de subprocesamiento libre**
</dt> <dd>

Proceso que tiene un apartamento multiproceso y sin apartamentos de un solo subproceso.

</dd> <dt>

<span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**Coordinador de confirmaciones globales**
</dt> <dd>

En un sistema de transacciones distribuidas basado en Microsoft Windows, el administrador de transacciones raíz del árbol de confirmación. Este Coordinador toma la decisión de confirmar o anular una transacción determinada y nunca está en duda.

</dd> <dt>

<span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**suplantación**
</dt> <dd>

La capacidad de un subproceso de ejecutarse en un contexto de seguridad diferente del proceso que posee el subproceso. El subproceso de servidor utiliza un token de acceso que representa las credenciales del cliente y, con esto, puede tener acceso a los recursos a los que el cliente puede tener acceso.

</dd> <dt>

<span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**nivel de suplantación**
</dt> <dd>

La configuración utilizada por el cliente para conceder al servidor un nivel de autoridad determinado para llevar a cabo acciones en el nombre del cliente. En COM+, solo se puede establecer para aplicaciones de servidor COM+.

</dd> <dt>

<span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**intercepción**
</dt> <dd>

Para un objeto activado en un contexto determinado, el proceso de control de las llamadas a ese objeto a través del límite del contexto. Las llamadas en contexto se controlan con servidores proxy de interfaz ligera que controlarán cualquier mediación necesaria para ajustar el entorno en tiempo de ejecución desde uno que admita al llamador a uno que admita el destinatario.

</dd> <dt>

<span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interfaz**
</dt> <dd>

En la programación basada en COM, colección de funciones públicas relacionadas que proporcionan acceso a un objeto COM. El conjunto de interfaces de un objeto COM se compone de un contrato que especifica cómo los programas y otros objetos pueden interactuar con el objeto COM.

</dd> <dt>

<span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**proxy de interfaz**
</dt> <dd>

Objeto específico de la interfaz que empaqueta (calcula las referencias) de los parámetros de esa interfaz como preparación para una llamada de método remoto y desempaqueta (no calcula las referencias) de los valores devueltos desde el código auxiliar de la interfaz. Un proxy se ejecuta en el espacio de direcciones del remitente y se comunica con el código auxiliar correspondiente en el espacio de direcciones del receptor.

</dd> <dt>

<span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**código auxiliar de la interfaz**
</dt> <dd>

Objeto específico de la interfaz que desempaqueta los parámetros de cálculo de referencias, llama al método necesario y los paquetes (serialización) devuelven valores del método llamado. El código auxiliar se ejecuta en el espacio de direcciones del receptor y se comunica con el proxy de interfaz correspondiente en el espacio de direcciones del remitente.

</dd> <dt>

<span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**interior (objeto)**
</dt> <dd>

En una jerarquía transaccional, cualquier objeto bajo el objeto raíz.

</dd> <dt>

<span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**activación Just-in-Time (JIT)**
</dt> <dd>

Servicio automático proporcionado por COM+ que permite usar de forma más productiva los recursos del servidor inactivos. Cuando un componente se configura como activado JIT, COM+ puede desactivar una instancia de él mientras un cliente todavía mantiene una referencia activa al objeto. La próxima vez que el cliente llame a un método en el objeto, COM+ volverá a activar el objeto de forma transparente para el cliente, justo a tiempo.

</dd> <dt>

<span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**componente heredado**
</dt> <dd>

Componente no configurado que se ha instalado en una aplicación COM+.

</dd> <dt>

<span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**Escucha**
</dt> <dd>

Un elemento arquitectónico del servicio de componentes en cola de COM+. El agente de escucha es un objeto COM que abre la cola de mensajes asociada a su aplicación host y espera a que lleguen los mensajes. A medida que llegan los mensajes, el agente de escucha envía los subprocesos que procesan los mensajes.

</dd> <dt>

<span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**modelo lógico**
</dt> <dd>

El segundo paso de un proceso de diseño de la aplicación COM+, donde el modelo conceptual se divide en los niveles lógicos de la arquitectura de tres niveles, como se indica a continuación: el nivel de presentación o los servicios de usuario; el nivel intermedio o servicios empresariales; y el nivel de datos o Data Services.

</dd> <dt>

<span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**evento de acoplamiento flexible**
</dt> <dd>

Evento cuyo remitente (publicador) y receptor (suscriptor) no están estrechamente enlazados. En un sistema de eventos de acoplamiento flexible, como los eventos COM+, la información de eventos de distintos publicadores se conserva en un almacén de eventos. Los suscriptores consultan este almacén y seleccionan los eventos que desean recibir. La selección de información de eventos del almacén de eventos crea una suscripción. Cuando se produce un evento, el sistema de eventos busca en esta base de datos y busca los suscriptores interesados, crea un nuevo objeto de cada clase interesada y llama a un método en ese objeto.

</dd> <dt>

<span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**serialización**
</dt> <dd>

Proceso de empaquetar y desempaquetar los parámetros de método de interfaz en los límites de subprocesos o procesos para que pueda tener lugar una llamada a procedimiento remoto.

</dd> <dt>

<span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**Movedor de mensajes**
</dt> <dd>

El elemento arquitectónico del servicio de componentes en cola de COM+ que mueve los mensajes con errores a su cola de entrada para que se puedan volver a intentar.

</dd> <dt>

<span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**evento meta**
</dt> <dd>

Tipo de evento utilizado por el sistema de eventos COM+ para notificar a los suscriptores interesados cada vez que se crean, modifican o quitan suscripciones o objetos de clase de eventos.

</dd> <dt>

<span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**forma**
</dt> <dd>

En la programación basada en COM, proceso que realiza un objeto COM cuando recibe un mensaje.

</dd> <dt>

<span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**nivel intermedio**
</dt> <dd>

En el modelo de arquitectura de tres niveles para aplicaciones empresariales, la capa que comprende las reglas de lógica de negocios y de datos. Los componentes que componen el nivel intermedio se pueden usar para aplicar reglas de negocios, como algoritmos de negocio, normativas legales o gubernamentales y reglas de datos, que están diseñadas para mantener la coherencia de las estructuras de datos en bases de datos específicas o varias. Dado que estos componentes de nivel intermedio no están asociados a un cliente específico, pueden ser utilizados por todas las aplicaciones y pueden moverse a ubicaciones diferentes, ya que el tiempo de respuesta y otras reglas requieren. También se denomina *capa de servicios empresariales* o *nivel de lógica de negocios*.

</dd> <dt>

<span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**proceso de modelo mixto**
</dt> <dd>

Proceso que tiene un apartamento multiproceso y uno o más apartamentos de un solo subproceso.

</dd> <dt>

<span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**Nike**
</dt> <dd>

Nombre que identifica de forma única un objeto COM. Del mismo modo que una ruta de acceso identifica un archivo en el sistema de archivos, un moniker identifica un objeto COM en el espacio de nombres de directorio.

</dd> <dt>

<span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**archivo. msi**
</dt> <dd>

Archivo creado por la herramienta administrativa Servicios de componentes cuando se exporta una aplicación COM+ o un proxy de aplicación para su instalación en otro equipo. El archivo. msi se puede instalar en cualquier cliente basado en Windows mediante Windows Installer.

</dd> <dt>

<span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**modelo de Apartamento multiproceso**
</dt> <dd>

Modelo de apartamento en el que todos los subprocesos del proceso que se han inicializado como subproceso libre se encuentran en un único apartamento. Por lo tanto, no hay necesidad de calcular las referencias entre subprocesos. Los subprocesos no necesitan recuperar y enviar mensajes porque COM no utiliza los mensajes de ventana de este modelo.

</dd> <dt>

<span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**transacción anidada**
</dt> <dd>

Una transacción secundaria iniciada desde dentro de un límite de transacción principal o primario existente. La transacción principal no se confirma hasta que se confirman todas las transacciones subordinadas, o anidadas. COM+ no admite transacciones anidadas.

</dd> <dt>

<span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**modelo de Apartamento neutro**
</dt> <dd>

Modelo de subprocesos en el que los objetos siguen las instrucciones para apartamentos multiproceso pero se pueden ejecutar en cualquier tipo de subproceso. El modelo de Apartamento neutro es el modelo de subprocesos recomendado para los componentes COM y las aplicaciones COM+.

</dd> <dt>

<span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**objeto persistente**
</dt> <dd>

Objeto COM que puede guardar su estado interno cuando lo pide un cliente y que se ajusta a los estándares definidos por COM a través de los cuales los clientes pueden solicitar que los objetos se inicialicen, carguen y guarden en un almacén de datos (por ejemplo, archivo sin formato, almacenamiento estructurado o memoria). Es responsabilidad del cliente administrar la ubicación donde se almacenan los datos persistentes del objeto, pero no el formato de los datos.

</dd> <dt>

<span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**interfaz de objeto persistente**
</dt> <dd>

Una interfaz COM implementada por un objeto persistente. Los clientes usan interfaces de objeto persistentes para indicar a esos objetos persistentes Cuándo y dónde almacenar su estado.

</dd> <dt>

<span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**interfaz de notificación de fase cero**
</dt> <dd>

Interfaz COM+ que permite a las aplicaciones detectar cuándo está preparada una transacción para continuar con un protocolo de confirmación en dos fases, de modo que pueda realizar las operaciones de notificación necesarias y comunicarse con el administrador de transacciones cuando se hayan completado las operaciones.

</dd> <dt>

<span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**modelo físico**
</dt> <dd>

El tercer y último paso del proceso de diseño de la aplicación COM+, donde el desarrollador determina dónde residen los componentes físicamente y cómo se van a codificar.

</dd> <dt>

<span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**encargado**
</dt> <dd>

El elemento arquitectónico del servicio de componentes en cola COM+ que recupera el mensaje de una cola y, a continuación, carga el objeto de servidor y los códigos auxiliares de la interfaz estándar para quitar las referencias de los datos e invocar métodos de servidor. El reproductor Anula la serialización del contexto de seguridad del cliente en el lado del servidor y, a continuación, invoca el componente del servidor y realiza las mismas llamadas al método. El reproductor no reproduce las llamadas al método hasta que el componente de cliente finaliza y la transacción que registra el método llama a las confirmaciones.

</dd> <dt>

<span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**nivel de presentación**
</dt> <dd>

En el modelo de arquitectura de tres niveles para aplicaciones empresariales, la capa que presenta los datos al usuario y, opcionalmente, permite la manipulación de datos y la entrada de datos. Los dos tipos principales de interfaz de usuario para el nivel de presentación son la aplicación tradicional y la aplicación basada en Web. También se denomina *nivel de servicios de usuario*.

</dd> <dt>

<span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**token de acceso principal**
</dt> <dd>

Describe el contexto de seguridad de la cuenta de usuario asociada a un proceso.

</dd> <dt>

<span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**Administrador de proxy**
</dt> <dd>

En el cálculo de referencias estándar, componente que administra todos los proxies de interfaz para un solo objeto.

</dd> <dt>

<span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo-objeto**
</dt> <dd>

Un tipo de objeto contenido, como una selección de usuario en un documento, un rango de celdas de una hoja de cálculo o un intervalo de caracteres en un documento de texto. Este tipo de objeto se denomina pseudo objeto porque no se trata como un objeto distinto hasta que un usuario marca la selección.

</dd> <dt>

<span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**publicador**
</dt> <dd>

Remitente de un evento. En la arquitectura de eventos COM+, el publicador hace que la llamada al método inicie un evento.

</dd> <dt>

<span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**moniker de cola**
</dt> <dd>

Moniker utilizado para activar un componente en cola.

</dd> <dt>

<span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**condición de carrera**
</dt> <dd>

En una aplicación multiproceso, condición que se produce cuando varios subprocesos tienen acceso a un elemento de datos sin coordinación, posiblemente produciendo resultados incoherentes, dependiendo del subproceso que llegue primero al elemento de datos. COM proporciona algunas funciones diseñadas específicamente para ayudar a evitar condiciones de carrera en servidores fuera de proceso.

</dd> <dt>

<span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**reproductor**
</dt> <dd>

El elemento arquitectónico del servicio de componentes en cola COM+ que calcula las referencias del contexto de seguridad del cliente en un mensaje y registra todas las llamadas de método para un objeto. La grabadora es un administrador proxy proporcionado por el sistema que selecciona interfaces de las interfaces queuable en el catálogo de COM+.

</dd> <dt>

<span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**dispensador de recursos**
</dt> <dd>

En el modelo de programación COM+, componente que administra el estado compartido no duradero en nombre de los componentes de la aplicación dentro de un proceso. Los distribuidores de recursos son similares a los administradores de recursos, pero sin la garantía de durabilidad.

</dd> <dt>

<span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Administrador de recursos**
</dt> <dd>

Servicio que administra datos persistentes o duraderos en bases de datos, colas de mensajes duraderas o sistemas de archivos transaccionales. Es el administrador de recursos que sabe cómo almacenar datos y realizar la recuperación ante desastres. Las aplicaciones de servidor COM+ usan administradores de recursos para mantener el estado duradero de una aplicación, como el registro de inventario a mano, los pedidos pendientes y las cuentas por cobrar. Los administradores de recursos trabajan en cooperación con Microsoft Coordinador de transacciones distribuidas (DTC) para garantizar la atomicidad y el aislamiento de una aplicación.

</dd> <dt>

<span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**seguridad basada en roles**
</dt> <dd>

Servicio de seguridad COM+ proporcionado para aplicaciones COM+. Un rol representa una categoría de usuarios definidos para una aplicación COM+ con el fin de determinar los permisos de acceso a los recursos de la aplicación. Los roles los asigna un programador a los componentes, interfaces y métodos. Los usuarios son asignados por un administrador a los roles adecuados, lo que permite a un usuario dentro de un rol determinado tener acceso a los recursos a los que está asignado ese rol.

</dd> <dt>

<span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**objeto raíz**
</dt> <dd>

El primer objeto de una transacción, denominado raíz de la transacción, y siempre se coloca en un nuevo límite transaccional. Solo puede haber un objeto raíz en una transacción. Todos los demás objetos de la jerarquía transaccional bajo el objeto raíz se denominan objetos interiores.

</dd> <dt>

<span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**Administrador de transacciones raíz**
</dt> <dd>

Administrador de transacciones en el sistema que inicia una transacción. La transacción no se finaliza hasta que el administrador de transacciones raíz determina el estado de la transacción (confirmada o anulada).

</dd> <dt>

<span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**semáforo**
</dt> <dd>

Objeto de kernel que se usa para arbitrar el acceso a un recurso compartido.

</dd> <dt>

<span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Administrador de control de servicios (SCM)**
</dt> <dd>

Proceso de Microsoft Windows Server que administra todos los servicios del registro de Windows.

</dd> <dt>

<span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**Administrador de propiedades compartidas (SPM)**
</dt> <dd>

En com+, un dispensador de recursos que puede usar para compartir el estado no persistente entre varios objetos dentro de un proceso de servidor.

</dd> <dt>

<span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**proceso de un solo subproceso**
</dt> <dd>

Proceso que consta de un solo apartamento de un solo subproceso, que a su vez consta de exactamente un subproceso. Todos los objetos COM que residen en un contenedor uniproceso pueden recibir llamadas a métodos solo de un subproceso que pertenezca a ese apartamento.

</dd> <dt>

<span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**JABÓN**
</dt> <dd>

Protocolo simple basado en XML para intercambiar información estructurada y de tipos en la Web. El Protocolo no contiene semántica de aplicación o de transporte, lo que hace que sea muy modular y extensible.

</dd> <dt>

<span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**dividir registro**
</dt> <dd>

En el caso de los componentes que ya tienen componentes COM existentes y que se usan en el entorno de servicios COM+, la disposición de registro en la que se almacena el aspecto COM básico del registro en el registro de Windows y los nuevos servicios y atributos de COM+ (por ejemplo, los componentes en cola) se almacenan en la base de datos de registro de COM+. Cada atributo de componente se almacena en el registro de Windows o en la base de datos de registro de COM+. Los nuevos componentes COM se registran exclusivamente en la base de datos de registro de COM+, con algunas duplicaciones en el registro de Windows para que las herramientas existentes puedan utilizarlos.

</dd> <dt>

<span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**con estado**
</dt> <dd>

De o perteneciente a un sistema o proceso que supervisa todos los detalles del estado de una actividad en la que participa.

</dd> <dt>

<span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**sin estado**
</dt> <dd>

De o perteneciente a un sistema o proceso que participa en la actividad sin supervisar todos los detalles de su estado.

</dd> <dt>

<span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**Cloaking estático**
</dt> <dd>

Forma de esconder dónde se puede presentar la identidad del cliente original una vez en un servidor de nivel inferior, estableciendo la identidad del cliente original una vez en el proxy. Esta identidad del cliente se presenta como un token de subproceso de servidor que se usará en las llamadas de método posteriores.

</dd> <dt>

<span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**suscriptor**
</dt> <dd>

Receptor de un evento. En la arquitectura de eventos COM+, el suscriptor recibe las llamadas realizadas por el publicador.

</dd> <dt>

<span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**objeto de suscripción**
</dt> <dd>

En el sistema de eventos COM+, objeto creado por un suscriptor para solicitar y administrar la entrega de eventos.

</dd> <dt>

<span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**sincronización**
</dt> <dd>

En COM+, servicio que fluye del componente al componente y prohíbe que más de un llamador escriba el componente en un momento dado. La sincronización determina si los subprocesos pueden enviar llamadas a un objeto.

</dd> <dt>

<span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**modelo arquitectónico de tres niveles**
</dt> <dd>

El marco fundamental para el modelo de diseño lógico, divide los componentes de una aplicación en tres niveles de servicio de la siguiente manera: el nivel de presentación o los servicios de usuario; el nivel intermedio o servicios empresariales; y el nivel de datos o Data Services. Estos niveles no corresponden necesariamente a ubicaciones físicas en varios equipos de una red, sino a capas lógicas de la aplicación.

</dd> <dt>

<span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**evento estrechamente acoplado**
</dt> <dd>

Evento cuyo remitente (publicador) y receptor (suscriptor) están estrechamente enlazados. En un sistema de eventos estrechamente acoplado, se proporciona al publicador una interfaz en la que llamar a un método cuando se produce un cambio. El Suscriptor sabe a qué publicador debe solicitar la notificación y las interfaces que se exponen. Un sistema de eventos estrechamente acoplado requiere que tanto el publicador como el suscriptor se ejecuten en todo momento.

</dd> <dt>

<span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**registro de seguimiento**
</dt> <dd>

Un archivo de registro generado automáticamente por Microsoft Coordinador de transacciones distribuidas que muestra los datos relacionados con una o varias transacciones distribuidas. Ejemplos de datos en un registro de seguimiento son el identificador de la transacción, el tiempo de la transacción y los mensajes que indican el resultado de la transacción.

</dd> <dt>

<span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**transacción**
</dt> <dd>

Unidad de trabajo en la que se produce una serie de operaciones relacionadas durante un proceso de aplicación. Una transacción se ejecuta exactamente una vez y es atómica, o bien se realiza todo el trabajo o ninguno de ellos.

</dd> <dt>

<span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Protocolo de transacciones de Internet (TIP)**
</dt> <dd>

El protocolo de Internet de transacciones es un protocolo estándar de confirmación en dos fases que permite a los administradores de transacciones heterogéneos coordinar las transacciones distribuidas, especialmente a través de Internet. El protocolo TIP de confirmación en dos fases es fácil de implementar y es independiente del Protocolo de comunicaciones de aplicación a aplicación, de modo que se pueda usar con cualquier protocolo de aplicación, pero especialmente con HTTP.

</dd> <dt>

<span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**Administrador de transacciones**
</dt> <dd>

La parte de Microsoft Coordinador de transacciones distribuidas (DTC) que se ejecuta en cada equipo que participa en una transacción distribuida y administra las actividades relacionadas con la confirmación o anulación de esa parte de la transacción.

</dd> <dt>

<span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**aplicación de procesamiento de transacciones**
</dt> <dd>

Colección de operaciones de transacción que automatizan una tarea empresarial determinada.

</dd> <dt>

<span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**sistema de procesamiento de transacciones**
</dt> <dd>

Un sistema completo, que incluye el hardware y el software del equipo, que hospeda una aplicación de procesamiento de transacciones para realizar las transacciones rutinarias necesarias para llevar a cabo la actividad empresarial.

</dd> <dt>

<span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**Protocolo de confirmación en dos fases**
</dt> <dd>

Un protocolo utilizado únicamente en las transacciones distribuidas garantiza que el resultado de una transacción es coherente en todos los administradores de transacciones que participan en la transacción. El protocolo opera en dos fases distintas para confirmar o anular una transacción en última instancia: la fase uno evalúa la condición de cada administrador de recursos y la fase dos completa la transacción.

</dd> <dt>

<span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**componente no configurado**
</dt> <dd>

Componente COM que no se ha configurado en el catálogo de COM+. Los componentes no configurados no pueden hacer uso de servicios COM+.

</dd> <dt>

<span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**situación**
</dt> <dd>

Para las transacciones DTC, una estructura de datos opaca que representa la dirección del administrador de transacciones del administrador de recursos.

</dd> <dt>

<span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**Interfaces XA**
</dt> <dd>

Conjunto estándar de interfaces de programación que permiten a los desarrolladores de aplicaciones COM+ tener acceso a las bases de datos compatibles con XA y crear administradores de recursos que operan con bases de datos relacionales, Message Queue Server, archivos transaccionales y bases de datos orientadas a objetos. Aunque Microsoft no admite directamente el protocolo XA, Microsoft admite las funciones de traducción entre las transacciones OLE y XA.

</dd> <dt>

<span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**Servicios Web XML**
</dt> <dd>

Unidades de lógica de aplicación que proporcionan datos y servicios a otras aplicaciones. Las aplicaciones obtienen acceso a los servicios Web XML a través de protocolos web estándar, como SOAP.

</dd> </dl>

 

 
