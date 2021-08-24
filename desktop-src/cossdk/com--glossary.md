---
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: Glosario de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda1c62c8edee1e15df33b63a9d4894639dd9e5637ed3e87a747d724f9e9040e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638725"
---
# <a name="com-glossary"></a>Glosario de COM+

<dl> <dt>

<span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**token de acceso**
</dt> <dd>

Objeto que describe el contexto de seguridad de un proceso o subproceso. La información de un token incluye la identidad y los privilegios de la cuenta de usuario asociada al proceso o subproceso. Cuando un usuario inicia sesión, el sistema comprueba la contraseña del usuario comparándolo con la información almacenada en una base de datos de seguridad. Si se autentica la contraseña, el sistema genera un token de acceso. Cada proceso ejecutado en nombre de este usuario tiene una copia de este token de acceso.

</dd> <dt>

<span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**Propiedades ACID**
</dt> <dd>

Acrónimo acuñado por los procesos de procesamiento de transacciones para ser atómico, coherente, aislado y duradero. Estas propiedades garantizan un comportamiento predecible, lo que refuerza el rol de las transacciones como propuestas todas o ninguna diseñadas para proporcionar resultados coherentes y predecibles en un entorno distribuido cuando se pueden producir errores independientes.

</dd> <dt>

<span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**Activación**
</dt> <dd>

Cadena de eventos que da como resultado la creación de un objeto COM y la devolución de un puntero válido a una interfaz en ese objeto. En COM+, un objeto se activa en su propio contexto o en el de su creador (un objeto que ha solicitado que se active el objeto). Los servicios COM+ se basan en la activación adecuada de un objeto en función de la configuración del objeto. Durante la activación, el sistema determina el contexto en el que se ejecuta el objeto, inicializa las propiedades de contexto, comprueba los permisos de acceso y establece una identidad de seguridad.

</dd> <dt>

<span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**seguridad de activación**
</dt> <dd>

Una forma de protección de seguridad que determina quién puede iniciar un servidor. El Administrador de control de servicios (SCM) de un equipo determinado aplica automáticamente la seguridad de activación. Tras recibir una solicitud de un cliente para activar un objeto, el SCM comprueba la solicitud con la información de seguridad de activación almacenada en su registro. También se comprueba la seguridad de activación para las activaciones en el mismo equipo. También se denomina *iniciar seguridad*.

</dd> <dt>

<span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**tipo de activación**
</dt> <dd>

Categoría de activación para una aplicación COM+ que indica si la aplicación se ejecuta dentro o fuera del espacio de proceso de su cliente (dependiendo de si es una aplicación de servidor o biblioteca, respectivamente), así como si la aplicación se ejecuta como un servicio.

</dd> <dt>

<span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**Actividad**
</dt> <dd>

En COM+, un subproceso lógico que consta de una o varias transacciones y que contiene una colección de componentes que se agrupan en una aplicación COM+. Cada objeto COM pertenece a una actividad. No se puede cambiar la asociación entre un objeto y una actividad.

</dd> <dt>

<span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**proceso de modelo de apartamento**
</dt> <dd>

Un proceso que tiene dos o más departamentos de un solo subproceso y sin departamentos multiproceso.

</dd> <dt>

<span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**proxy de aplicación**
</dt> <dd>

Conjunto de archivos que contienen información de registro que permite a un cliente acceder de forma remota a una aplicación de servidor COM+. Cuando se instala en un equipo cliente, un archivo proxy de aplicación escribe información sobre la aplicación de servidor en el equipo cliente; A continuación, el cliente puede acceder de forma remota a la aplicación de servidor.

</dd> <dt>

<span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**Autenticación**
</dt> <dd>

El proceso de seguridad de determinar que un llamador de una aplicación es realmente quien dice ser, comprobando la autenticidad de una notificación de identidad. En el caso de las aplicaciones COM+, la autenticación puede estar activada y configurada administrativamente, después de lo cual funciona de forma transparente para la aplicación.

</dd> <dt>

<span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**Autorización**
</dt> <dd>

El proceso de seguridad de determinar si un llamador de una aplicación está autorizado para hacer lo que pide.

</dd> <dt>

<span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**Administrador de recursos de almacenamiento en caché**
</dt> <dd>

Un administrador de recursos que actúa como front-end para otro administrador de recursos y que almacena en caché la información localmente, lo que reduce el costo de acceso al recurso subyacente. A diferencia de un administrador de recursos convencional, un administrador de recursos de almacenamiento en caché no participa en la recuperación porque nunca almacena permanentemente los datos subyacentes.

</dd> <dt>

<span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**llamar a seguridad**
</dt> <dd>

Una forma de protección de seguridad que ayuda a controlar el acceso a los métodos de un objeto de servidor una vez iniciado un servidor.

</dd> <dt>

<span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**clase (COM)**
</dt> <dd>

Una implementación concreta con nombre de una o varias interfaces. Una clase COM se identifica mediante un CLSID y, a veces, un ProgID.

</dd> <dt>

<span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**Ocultación**
</dt> <dd>

La capacidad de un servidor para enmascarar su propia identidad al realizar llamadas en nombre de un cliente. Cuando se habilita la protección, las llamadas realizadas por el servidor que suplanta al cliente se pueden realizar en la identidad del cliente. Cuando la protección está deshabilitada, las llamadas realizadas por el servidor se realizarán en la identidad del servidor.

</dd> <dt>

<span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Aplicación COM+**
</dt> <dd>

Unidad principal de administración y seguridad para Servicios de componentes. Una aplicación COM+ es un grupo de componentes COM que, por lo general, realizan funciones relacionadas. Estos componentes constan además de interfaces y métodos COM.

</dd> <dt>

<span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Agrupación de aplicaciones COM+**
</dt> <dd>

Una característica de Servicios de componentes que permite escalar los procesos de un solo subproceso y también puede ayudarle a recuperarse de errores en procesos únicos proporcionando otros procesos en ejecución capaces de controlar las activaciones.

</dd> <dt>

<span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Reciclaje de aplicaciones COM+**
</dt> <dd>

Una característica de Servicios de componentes que aumenta significativamente la estabilidad general de las aplicaciones al permitirle cerrar correctamente un proceso asociado a una aplicación y reiniciarlo.

</dd> <dt>

<span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Catálogo de COM+** 
</dt> <dd>

Almacén de datos que contiene los datos de configuración de COM+. El rendimiento de las tareas de administración de COM+ requiere la lectura y escritura de los datos almacenados en el catálogo. Solo se puede acceder al catálogo a través de la herramienta administrativa Servicios de componentes o a través de la biblioteca COMAdmin.

</dd> <dt>

<span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Eventos COM+**
</dt> <dd>

Eventos COM+ coincide y conecta publicadores y suscriptores a través de un sistema de eventos de acoplamiento flexible. Un publicador realiza la llamada al método para iniciar un evento y un suscriptor recibe estas llamadas a través del sistema de eventos en lugar de directamente desde el publicador. El servicio eventos COM+ mantiene la lista de suscriptores interesados que reciben las llamadas y dirige esas llamadas sin necesidad de que el publicador lo sepa.

</dd> <dt>

<span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Aplicación de biblioteca COM+**
</dt> <dd>

Una aplicación COM+ que se ejecuta en el proceso del cliente que la crea. Las aplicaciones de biblioteca pueden usar la seguridad basada en roles, pero no admiten el acceso remoto ni los componentes en cola.

</dd> <dt>

<span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Agrupación de objetos COM+**
</dt> <dd>

Un servicio automático proporcionado por COM+ que permite configurar un componente para que las instancias de sí mismos se mantienen activas en un grupo, listas para que las utilice cualquier cliente que solicite el componente.

</dd> <dt>

<span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Particiones COM+**
</dt> <dd>

Un servicio COM+ que permite, en un solo equipo, la creación de espacios de ejecución independientes para las aplicaciones.

</dd> <dt>

<span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Conjuntos de particiones COM+**
</dt> <dd>

Un grupo de particiones COM+ que se asigna a un identificador de usuario determinado en Active Directory.

</dd> <dt>

<span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Componentes en cola de COM+**
</dt> <dd>

Un servicio COM+, basado en Microsoft Message Queuing, que proporciona una manera sencilla de invocar y ejecutar componentes de forma asincrónica. El procesamiento de mensajes puede producirse sin tener en cuenta la disponibilidad o accesibilidad del remitente o del receptor.

</dd> <dt>

<span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**Aplicación de servidor COM+**
</dt> <dd>

Una aplicación COM+ que se ejecuta en su propio proceso. Las aplicaciones de servidor pueden admitir todos los servicios COM+.

</dd> <dt>

<span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM+ SOAP**
</dt> <dd>

Una característica servicios de componentes que permite exponer una aplicación COM+ como un servicio web XML. SOAP de COM+ también permite usar un servicio web XML como componente COM.

</dd> <dt>

<span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**Componente COM**
</dt> <dd>

Unidad binaria de código que incluye el empaquetado y el código de registro y que crea objetos COM. Todas las aplicaciones COM+ constan de uno o varios componentes COM.

</dd> <dt>

<span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**árbol de confirmación**
</dt> <dd>

En un sistema de transacciones distribuidas, la representación conceptual de una transacción en función de las relaciones jerárquicas entre los administradores de transacciones individuales que participan en una transacción distribuida. En esa jerarquía se incluyen los administradores de recursos inscritos asociados a los administradores de transacciones.

</dd> <dt>

<span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**Objeto COM**
</dt> <dd>

En el modelo de programación COM, una estructura de programación que encapsula los datos y la funcionalidad, que se definen y asignan como una sola unidad y para la que el único acceso público es a través de las interfaces de la estructura de programación. Un objeto COM debe admitir, como mínimo, la interfaz [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) que mantiene la existencia del objeto mientras se usa y proporciona acceso a las otras interfaces del objeto.

</dd> <dt>

<span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Compensación Resource Manager (CRM)**
</dt> <dd>

Una característica com+ que permite a los recursos no transaccionales participar en una transacción de confirmación en dos fases con el Microsoft DTC (Coordinador de transacciones distribuidas) (DTC). Normalmente, las CRM no proporcionan las capacidades de aislamiento de administradores de recursos completos, pero proporcionan atomicidad transaccional y durabilidad escribiendo en un registro.

</dd> <dt>

<span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Herramienta administrativa servicios de componentes**
</dt> <dd>

Complemento de interfaz de usuario a través del cual los administradores y desarrolladores pueden crear, configurar y mantener aplicaciones COM+, así como administrar transacciones distribuidas y bases de datos residentes en memoria. La herramienta administrativa Servicios de componentes también se puede usar para ver eventos del sistema y administrar servicios del sistema locales en el equipo en el que está instalada la herramienta.

</dd> <dt>

<span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**modelo conceptual**
</dt> <dd>

Primer paso de la fase de diseño de aplicaciones COM+, donde el desarrollador define los problemas empresariales que se van a resolver y decide qué componentes y servicios son necesarios.

</dd> <dt>

<span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**Concurrencia**
</dt> <dd>

La capacidad de más de una transacción o proceso para acceder a los mismos datos al mismo tiempo. COM+ generalmente administra la simultaneidad a través de la sincronización.

</dd> <dt>

<span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**componente configurado**
</dt> <dd>

Componente COM que se ha instalado en una aplicación COM+. Una vez instalado, el componente se configura en el catálogo de COM+ para usar los servicios COM+ disponibles.

</dd> <dt>

<span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**Contexto**
</dt> <dd>

Conjunto de propiedades en tiempo de ejecución asociadas a uno o varios objetos COM que se usan para proporcionar servicios para esos objetos. Cada objeto COM se ejecuta en un único contexto desde la activación hasta la desactivación (siempre dentro del mismo apartamento). Inicializado cuando se activa un objeto, las propiedades de contexto, como las propiedades de contexto de seguridad, representan las necesidades en tiempo de ejecución de un objeto.

</dd> <dt>

<span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**capa de datos**
</dt> <dd>

En el modelo de arquitectura de tres niveles para aplicaciones empresariales, la capa de acceso de DBMS, a la que se puede acceder a través del nivel intermedio, o la capa de servicios empresariales, y en ocasiones a través del nivel de presentación o de servicios de usuario. La capa de datos consta de componentes de acceso a datos (en lugar de conexiones DBMS sin procesar) para ayudar en el uso compartido de recursos y para permitir que los clientes se configuren sin instalar las bibliotecas de DBMS y los controladores ODBC en cada cliente. También se denomina *capa de servicios de datos*.

</dd> <dt>

<span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**Interbloqueo**
</dt> <dd>

En aplicaciones multiproceso, un problema de subprocesos que se produce cuando cada miembro de un conjunto de subprocesos está esperando otro miembro del conjunto.

</dd> <dt>

<span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**Delegación**
</dt> <dd>

Forma de suplantación que autoriza a un servidor a actuar en nombre de un cliente, lo que da al servidor la capacidad de suplantar clientes a través de la red.

</dd> <dt>

<span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**transacción distribuida**
</dt> <dd>

Transacción que implica varios administradores de recursos, que pueden estar en el mismo equipo o en equipos diferentes.

</dd> <dt>

<span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Coordinador de transacciones distribuidas (DTC)**
</dt> <dd>

Un servicio del sistema que administra transacciones y comunicaciones relacionadas con transacciones que se distribuyen entre dos o más administradores de recursos en uno o varios sistemas para garantizar las transacciones ACID correctas.

</dd> <dt>

<span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**dinámica**
</dt> <dd>

Una forma de ocultación en la que se detecta la identidad de cliente original como el token de acceso a subprocesos del servidor en cada llamada de método al servidor de bajada. Aunque la identidad que se presenta se puede determinar dinámicamente, la sobrecarga necesaria para ello puede ser considerablemente más costosa. En el caso de las aplicaciones COM+, la configuración predeterminada es para la funcionalidad de aplanamiento dinámico, ya que proporciona la flexibilidad que normalmente requieren las circunstancias que requieren el uso de la suplantación en primer lugar.

</dd> <dt>

<span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**Objeto enumerador**
</dt> <dd>

Permite la enumeración de elementos en una colección.

</dd> <dt>

<span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**Evento**
</dt> <dd>

Acción reconocida por un objeto, como hacer clic con el mouse o presionar una tecla, y para la que puede escribir código para responder.

</dd> <dt>

<span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**objeto de clase de evento**
</dt> <dd>

Componente configurado que proporciona un registro persistente en el sistema de eventos COM+ para describir los publicadores y las interfaces de activación asociadas a esos publicadores.

</dd> <dt>

<span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**método de evento**
</dt> <dd>

Método de una interfaz COM+ que identifica un evento COM+. Los métodos de evento deben tener un nombre único y solo pueden contener parámetros de entrada. El valor devuelto debe ser **HRESULT.**

</dd> <dt>

<span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**objeto event**
</dt> <dd>

Objeto COM que puede indicar uno o varios subprocesos que indica que se ha producido un evento. Cualquier subproceso dentro de un proceso puede crear un objeto de evento.

</dd> <dt>

<span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**Excepción**
</dt> <dd>

Condición o error anómalo que se produce durante la ejecución de un programa y que requiere la ejecución de software fuera del flujo normal de control.

</dd> <dt>

<span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**Failover**
</dt> <dd>

En un sistema de red de clúster, el proceso de reubicación de un recurso sobrecargado o con errores,como un servidor, una unidad de disco o una red, a su componente de copia de seguridad.

</dd> <dt>

<span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**proceso de subproceso libre**
</dt> <dd>

Un proceso que tiene un apartamento multiproceso y ningún apartamento de un solo subproceso.

</dd> <dt>

<span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**coordinador global de confirmaciones**
</dt> <dd>

En un sistema de transacciones distribuidas Windows basado en microsoft, el administrador de transacciones raíz del árbol de confirmación. Este coordinador toma la decisión de confirmar o anular una transacción determinada y nunca duda.

</dd> <dt>

<span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**Suplantación**
</dt> <dd>

La capacidad de un subproceso para ejecutarse en un contexto de seguridad diferente del del proceso que posee el subproceso. El subproceso de servidor usa un token de acceso que representa las credenciales del cliente y, con esto, puede acceder a los recursos a los que el cliente puede acceder.

</dd> <dt>

<span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**nivel de suplantación**
</dt> <dd>

La configuración utilizada por el cliente para conceder al servidor un nivel de autoridad determinado para llevar a cabo acciones en nombre del cliente. En COM+, esto solo se puede establecer para aplicaciones de servidor COM+.

</dd> <dt>

<span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**Interceptación**
</dt> <dd>

Para un objeto activado en un contexto determinado, el proceso de control de llamadas a ese objeto desde el límite de contexto. Las llamadas en todo el contexto se controlan con servidores proxy de interfaz ligera que controlarán cualquier mediación necesaria para ajustar el entorno en tiempo de ejecución de uno que aloje al autor de la llamada a uno que aloje al destinatario.

</dd> <dt>

<span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**Interfaz**
</dt> <dd>

En la programación basada en COM, una colección de funciones públicas relacionadas que proporcionan acceso a un objeto COM. El conjunto de interfaces de un objeto COM compone un contrato que especifica cómo los programas y otros objetos pueden interactuar con el objeto COM.

</dd> <dt>

<span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**proxy de interfaz**
</dt> <dd>

Objeto específico de la interfaz que empaqueta (serializa) parámetros para esa interfaz como preparación para una llamada de método remoto y desempaquete (unmarshals) los valores devueltos del código auxiliar de la interfaz. Un proxy se ejecuta en el espacio de direcciones del remitente y se comunica con un código auxiliar correspondiente en el espacio de direcciones del receptor.

</dd> <dt>

<span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**código auxiliar de interfaz**
</dt> <dd>

Objeto específico de la interfaz que desempaquete los parámetros serializados, llama al método necesario y los paquetes (serializaciones) devuelven valores del método llamado. El código auxiliar se ejecuta en el espacio de direcciones del receptor y se comunica con un proxy de interfaz correspondiente en el espacio de direcciones del remitente.

</dd> <dt>

<span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**objeto interior**
</dt> <dd>

En una jerarquía transaccional, cualquier objeto bajo el objeto raíz.

</dd> <dt>

<span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**Activación Just-In-Time (JIT)**
</dt> <dd>

Un servicio automático proporcionado por COM+ que permite que los recursos de servidor inactivos se utilicen de forma más productiva. Cuando un componente se configura como JIT activado, COM+ puede desactivar una instancia de él mientras un cliente todavía contiene una referencia activa al objeto. La próxima vez que el cliente llame a un método en el objeto , COM+ reactivará el objeto de forma transparente al cliente, justo a tiempo.

</dd> <dt>

<span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**componente heredado**
</dt> <dd>

Componente no configurado que se ha instalado en una aplicación COM+.

</dd> <dt>

<span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**Oyente**
</dt> <dd>

Elemento arquitectónico del servicio componentes en cola de COM+. El agente de escucha es un objeto COM que abre la cola de mensajes asociada a su aplicación host y espera a que lleguen los mensajes. A medida que llegan los mensajes, el agente de escucha envía subprocesos que procesan los mensajes.

</dd> <dt>

<span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**modelo lógico**
</dt> <dd>

El segundo paso de un proceso de diseño de aplicaciones COM+, donde el modelo conceptual se divide en los niveles lógicos de la arquitectura de tres niveles, como se muestra a continuación: el nivel de presentación o los servicios de usuario. el nivel intermedio, o servicios empresariales; y la capa de datos o los servicios de datos.

</dd> <dt>

<span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**evento de acoplamiento flexible**
</dt> <dd>

Evento cuyo remitente (publicador) y receptor (suscriptor) no están estrechamente enlazados. En un sistema de eventos de acoplamiento flexible, como eventos COM+, la información de eventos de distintos publicadores se conserva en un almacén de eventos. Los suscriptores consultan este almacén y seleccionan los eventos que desean recibir. Al seleccionar información de eventos del almacén de eventos, se crea una suscripción. Cuando se produce un evento, el sistema de eventos busca en esta base de datos y busca los suscriptores interesados, crea un nuevo objeto de cada clase interesada y llama a un método en ese objeto.

</dd> <dt>

<span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**Cálculo**
</dt> <dd>

Proceso de empaquetado y desempaquete de parámetros de método de interfaz a través de los límites de subprocesos o procesos para que se pueda realizar una llamada a procedimiento remoto.

</dd> <dt>

<span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**motor de mensajes**
</dt> <dd>

Elemento de arquitectura del servicio componentes en cola de COM+ que vuelve a mover los mensajes con error a su cola de entrada para que se puedan reinterír.

</dd> <dt>

<span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-event**
</dt> <dd>

Tipo de evento utilizado por el sistema de eventos COM+ para notificar a los suscriptores interesados cada vez que se crean, modifican o quitan objetos o suscripciones de clase de eventos.

</dd> <dt>

<span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**Método**
</dt> <dd>

En la programación basada en COM, un proceso realizado por un objeto COM cuando recibe un mensaje.

</dd> <dt>

<span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**nivel intermedio**
</dt> <dd>

En el modelo de arquitectura de tres niveles para aplicaciones empresariales, la capa que comprende la lógica de negocios y las reglas de datos. Los componentes que son el nivel intermedio se pueden usar para aplicar reglas de negocio, como algoritmos empresariales, regulaciones legales o gubernamentales, y reglas de datos, que están diseñadas para mantener la coherencia de las estructuras de datos dentro de bases de datos específicas o en varias bases de datos. Dado que estos componentes de nivel intermedio no están vinculados a un cliente específico, todas las aplicaciones pueden usar estos componentes y se pueden mover a diferentes ubicaciones a medida que el tiempo de respuesta y otras reglas requieran. También se denomina *capa de servicios empresariales* *o nivel de lógica de negocios.*

</dd> <dt>

<span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**proceso de modelo mixto**
</dt> <dd>

Proceso que tiene un apartamento multiproceso y uno o varios departamentos de un solo subproceso.

</dd> <dt>

<span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**Moniker**
</dt> <dd>

Nombre que identifica de forma única un objeto COM. Del mismo modo que una ruta de acceso identifica un archivo en el sistema de archivos, un moniker identifica un objeto COM en el espacio de nombres del directorio.

</dd> <dt>

<span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi archivo**
</dt> <dd>

Un archivo creado por la herramienta administrativa Servicios de componentes al exportar una aplicación COM+ o un proxy de aplicación para su instalación en otro equipo. El .msi puede instalarse en cualquier cliente basado en Windows mediante Windows instalador.

</dd> <dt>

<span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**modelo de apartamento multiproceso**
</dt> <dd>

Modelo de apartamento en el que todos los subprocesos del proceso que se han inicializado como subprocesos libres residen en un único apartamento. Por lo tanto, no es necesario serializar entre subprocesos. Los subprocesos no necesitan recuperar y enviar mensajes porque COM no usa mensajes de ventana en este modelo.

</dd> <dt>

<span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**transacción anidada**
</dt> <dd>

Transacción secundaria iniciada desde un límite de transacción principal o primario existente. La transacción principal no se confirma hasta que se confirman todas sus transacciones subordinadas o anidadas. COM+ no admite transacciones anidadas.

</dd> <dt>

<span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**modelo de apartamento neutro**
</dt> <dd>

Modelo de subprocesos en el que los objetos siguen las instrucciones para los departamentos multiproceso, pero se pueden ejecutar en cualquier tipo de subproceso. El modelo de apartamento neutro es el modelo de subprocesos recomendado para componentes COM y aplicaciones COM+.

</dd> <dt>

<span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**objeto persistente**
</dt> <dd>

Objeto COM que puede guardar su estado interno cuando un cliente lo solicita y que cumple los estándares definidos por COM a través del cual los clientes pueden solicitar que los objetos se inicialicen, carguen y guarden en y desde un almacén de datos (por ejemplo, archivo plano, almacenamiento estructurado o memoria). Es responsabilidad del cliente administrar la ubicación donde se almacenan los datos persistentes del objeto, pero no el formato de los datos.

</dd> <dt>

<span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**interfaz de objeto persistente**
</dt> <dd>

Interfaz COM implementada por un objeto persistente. Los clientes usan interfaces de objetos persistentes para decir a esos objetos persistentes cuándo y dónde almacenar su estado.

</dd> <dt>

<span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**interfaz de notificación de fase cero**
</dt> <dd>

Interfaz COM+ que permite a las aplicaciones detectar cuándo una transacción está lista para continuar con un protocolo de confirmación en dos fases para que pueda realizar las operaciones de notificación necesarias y comunicarse con el administrador de transacciones cuando se hayan completado las operaciones.

</dd> <dt>

<span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**modelo físico**
</dt> <dd>

Tercer y último paso del proceso de diseño de aplicaciones COM+, donde el desarrollador determina dónde residen físicamente los componentes y cómo se van a codificar.

</dd> <dt>

<span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**Jugador**
</dt> <dd>

Elemento arquitectónico del servicio componentes en cola de COM+ que recupera el mensaje de una cola y, a continuación, carga el objeto de servidor y los códigos auxiliares de interfaz estándar para desmarshal datos e invocar métodos de servidor. El reproductor desmarshals el contexto de seguridad del cliente en el lado servidor y, a continuación, invoca el componente de servidor y realiza las mismas llamadas de método. El reproductor no reproduce las llamadas al método hasta que se completa el componente de cliente y se confirma la transacción que registró las llamadas al método.

</dd> <dt>

<span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**nivel de presentación**
</dt> <dd>

En el modelo de arquitectura de tres niveles para aplicaciones empresariales, la capa que presenta los datos al usuario y, opcionalmente, permite la manipulación de datos y la entrada de datos. Los dos tipos principales de interfaz de usuario para el nivel de presentación son la aplicación tradicional y la aplicación basada en web. También se denomina *capa de servicios de usuario*.

</dd> <dt>

<span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**token de acceso principal**
</dt> <dd>

Describe el contexto de seguridad de la cuenta de usuario asociada a un proceso.

</dd> <dt>

<span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**administrador de proxy**
</dt> <dd>

En la serialización estándar, componente que administra todos los servidores proxy de interfaz para un único objeto.

</dd> <dt>

<span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo object**
</dt> <dd>

Tipo de objeto contenido, como una selección de usuario en un documento, un intervalo de celdas en una hoja de cálculo o un intervalo de caracteres en un documento de texto. Este tipo de objeto se denomina pseudo object porque no se trata como un objeto distinto hasta que un usuario marca la selección.

</dd> <dt>

<span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**Editor**
</dt> <dd>

Remitente de un evento. En la arquitectura de eventos COM+, el publicador realiza la llamada al método para iniciar un evento.

</dd> <dt>

<span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**moniker de cola**
</dt> <dd>

Moniker usado para activar un componente en cola.

</dd> <dt>

<span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**condición de carrera**
</dt> <dd>

En una aplicación multiproceso, una condición que se produce cuando varios subprocesos acceden a un elemento de datos sin coordinación, lo que puede provocar resultados incoherentes, en función de qué subproceso llegue primero al elemento de datos. COM proporciona algunas funciones diseñadas específicamente para ayudar a evitar condiciones de carrera en servidores fuera de proceso.

</dd> <dt>

<span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**Grabadora**
</dt> <dd>

Elemento arquitectónico del servicio componentes en cola de COM+ que serializa el contexto de seguridad del cliente en un mensaje y registra todas las llamadas de método para un objeto . La grabadora es un administrador de proxy proporcionado por el sistema que selecciona interfaces de las interfaces que se pueden usar en el catálogo de COM+.

</dd> <dt>

<span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**dispensador de recursos**
</dt> <dd>

En el modelo de programación COM+, componente que administra el estado compartido no legible en nombre de los componentes de la aplicación dentro de un proceso. Los dispensadores de recursos son similares a los administradores de recursos, pero sin la garantía de durabilidad.

</dd> <dt>

<span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Resource Manager**
</dt> <dd>

Un servicio que administra datos persistentes o duraderos en bases de datos, colas de mensajes durables o sistemas de archivos transaccionales. Es el administrador de recursos el que sabe cómo almacenar datos y realizar la recuperación ante desastres. Las aplicaciones de servidor COM+ usan administradores de recursos para mantener el estado duradero de una aplicación, como el registro de inventario disponible, los pedidos pendientes y las cuentas que se pueden cobrar. Los administradores de recursos trabajan en cooperación con Microsoft DTC (Coordinador de transacciones distribuidas) (DTC) para garantizar la atomicidad y el aislamiento de una aplicación.

</dd> <dt>

<span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**seguridad basada en roles**
</dt> <dd>

Un servicio de seguridad COM+ proporcionado para aplicaciones COM+. Un rol representa una categoría de usuarios definida para una aplicación COM+ con el fin de determinar los permisos de acceso a los recursos de la aplicación. Un desarrollador asigna roles a componentes, interfaces y métodos. Un administrador asigna a los usuarios los roles adecuados, lo que permite que un usuario dentro de un rol determinado acceda a los recursos a los que se asigna ese rol.

</dd> <dt>

<span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**objeto raíz**
</dt> <dd>

Primer objeto de una transacción, denominado raíz de la transacción y siempre colocado en un nuevo límite transaccional. Solo puede haber un objeto raíz en una transacción. Todos los demás objetos de la jerarquía transaccional bajo el objeto raíz se denominan objetos interiores.

</dd> <dt>

<span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**administrador de transacciones raíz**
</dt> <dd>

Administrador de transacciones del sistema que inicia una transacción. La transacción no se finalizará hasta que el administrador de transacciones raíz determine el estado de la transacción (confirmado o anulado).

</dd> <dt>

<span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**Semáforo**
</dt> <dd>

Objeto de kernel que se usa para evitar el acceso a un recurso compartido.

</dd> <dt>

<span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Service Control Manager (SCM)**
</dt> <dd>

Un proceso Windows servidor de Microsoft que administra todos los servicios del Windows registro.

</dd> <dt>

<span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**administrador de propiedades compartidas (SPM)**
</dt> <dd>

En Com+, un dispensador de recursos que puede usar para compartir el estado no persistente entre varios objetos dentro de un proceso de servidor.

</dd> <dt>

<span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**proceso de un solo subproceso**
</dt> <dd>

Un proceso que consta de un solo apartamento de un solo subproceso, que a su vez consta de exactamente un subproceso. Todos los objetos COM que se encuentra en un apartamento de un solo subproceso pueden recibir llamadas de método de solo el subproceso que pertenece a ese apartamento.

</dd> <dt>

<span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**Jabón**
</dt> <dd>

Un protocolo sencillo basado en XML para intercambiar información estructurada y de tipo en la Web. El protocolo no contiene ninguna semántica de aplicación o transporte, lo que lo hace muy modular y extensible.

</dd> <dt>

<span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**división del registro**
</dt> <dd>

Para los componentes que ya son componentes COM existentes y se usan en el entorno de servicios COM+, la disposición de registro en la que el aspecto COM básico del registro se almacena en el registro de Windows y los nuevos servicios y atributos de COM+ (por ejemplo, componentes en cola) se almacenan en la base de datos de registro de COM+. Cada atributo de componente se almacena en el registro Windows o en la base de datos de registro de COM+. Los nuevos componentes COM se registran exclusivamente en la base de datos de registro de COM+, con alguna duplicación en el registro de Windows para que las herramientas existentes puedan usarlas.

</dd> <dt>

<span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**Stateful**
</dt> <dd>

De o perteneciente a un sistema o proceso que supervisa todos los detalles del estado de una actividad en la que participa.

</dd> <dt>

<span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**Apátridas**
</dt> <dd>

De o perteneciente a un sistema o proceso que participa en la actividad sin supervisar todos los detalles de su estado.

</dd> <dt>

<span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**estática**
</dt> <dd>

Una forma de crear un escenario en el que la identidad de cliente original se puede presentar una vez en un servidor de bajada, estableciendo la identidad de cliente original una vez en el proxy. Esta identidad de cliente se presenta como un token de subproceso de servidor que se usará en llamadas de método posteriores.

</dd> <dt>

<span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**Suscriptor**
</dt> <dd>

Receptor de un evento. En la arquitectura de eventos COM+, el suscriptor recibe las llamadas realizadas por el publicador.

</dd> <dt>

<span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**objeto de suscripción**
</dt> <dd>

En el sistema de eventos COM+, un objeto creado por un suscriptor para solicitar y administrar la entrega de eventos.

</dd> <dt>

<span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**Sincronización**
</dt> <dd>

En COM+, un servicio que fluye de componente a componente y prohíbe que más de un llamador entre en el componente en un momento dado. La sincronización determina cuándo los subprocesos pueden enviar llamadas a un objeto .

</dd> <dt>

<span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**Modelo de arquitectura de tres niveles**
</dt> <dd>

El marco fundamental para el modelo de diseño lógico, segmenta los componentes de una aplicación en tres niveles de servicios como se muestra a continuación: el nivel de presentación o los servicios de usuario. el nivel intermedio, o servicios empresariales; y la capa de datos o los servicios de datos. Estos niveles no se corresponden necesariamente con ubicaciones físicas en varios equipos de una red, sino con capas lógicas de la aplicación.

</dd> <dt>

<span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**evento estrechamente acoplado**
</dt> <dd>

Evento cuyo remitente (publicador) y receptor (suscriptor) están estrechamente enlazados. En un sistema de eventos estrechamente acoplado, se proporciona al publicador una interfaz en la que llamar a un método cuando se produce un cambio. El suscriptor sabe desde qué publicador se va a solicitar la notificación y las interfaces que se exponen. Un sistema de eventos estrechamente acoplado requiere que tanto el publicador como el suscriptor se ejecuten en todo momento.

</dd> <dt>

<span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**registro de seguimiento**
</dt> <dd>

Un archivo de registro generado automáticamente por el Microsoft DTC (Coordinador de transacciones distribuidas) que muestra los datos relacionados con una o varias transacciones distribuidas. Algunos ejemplos de datos de un registro de seguimiento son el identificador de transacción, el tiempo de transacción y los mensajes que indican el resultado de la transacción.

</dd> <dt>

<span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**Transacción**
</dt> <dd>

Unidad de trabajo en la que se produce una serie de operaciones relacionadas durante un proceso de aplicación. Una transacción se ejecuta exactamente una vez y es atómica: todo el trabajo se realiza o ninguno de ellos.

</dd> <dt>

<span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Protocolo de Internet de transacciones (TIP)**
</dt> <dd>

Protocolo de Internet de transacciones es un protocolo estándar de confirmación en dos fases que permite a los administradores de transacciones heterogéneos coordinar las transacciones distribuidas, especialmente a través de Internet. El protocolo de confirmación en dos fases tip es fácil de implementar y es independiente del protocolo de comunicaciones de aplicación a aplicación, de modo que se puede usar con cualquier protocolo de aplicación, pero especialmente con HTTP.

</dd> <dt>

<span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**administrador de transacciones**
</dt> <dd>

Parte del Microsoft DTC (Coordinador de transacciones distribuidas) (DTC) que se ejecuta en cada equipo que participa en una transacción distribuida y administra las actividades relacionadas con confirmar o anular esa parte de la transacción.

</dd> <dt>

<span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**aplicación de procesamiento de transacciones**
</dt> <dd>

Colección de operaciones de transacción que automatizan una tarea empresarial determinada.

</dd> <dt>

<span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**sistema de procesamiento de transacciones**
</dt> <dd>

Un sistema completo, que incluye hardware y software de equipo, que hospeda una aplicación de procesamiento de transacciones para realizar las transacciones rutinarias necesarias para llevar a cabo el negocio.

</dd> <dt>

<span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**Protocolo de confirmación en dos fases**
</dt> <dd>

Un protocolo que solo se usa en transacciones distribuidas garantiza que el resultado de una transacción sea coherente entre todos los administradores de transacciones que participan en la transacción. El protocolo funciona en dos fases distintas para confirmar o anular una transacción en última instancia: la primera evalúa la condición de cada administrador de recursos y la segunda completa la transacción.

</dd> <dt>

<span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**componente no configurado**
</dt> <dd>

Componente COM que no se ha configurado en el catálogo de COM+. Los componentes no configurados no pueden usar servicios COM+.

</dd> <dt>

<span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**Paradero**
</dt> <dd>

Para las transacciones DTC, una estructura de datos opaca que representa la dirección del administrador de transacciones del administrador de recursos.

</dd> <dt>

<span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**Interfaces XA**
</dt> <dd>

Un conjunto estándar de interfaces de programación que permiten a los desarrolladores de aplicaciones COM+ acceder a bases de datos compatibles con XA y crear administradores de recursos que funcionan con bases de datos relacionales, colas de mensajes, archivos transaccionales y bases de datos orientadas a objetos. Aunque Microsoft no admite directamente el protocolo XA, Microsoft admite las instalaciones de traducción entre transacciones OLE y XA.

</dd> <dt>

<span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**Servicios web XML**
</dt> <dd>

Unidades de lógica de aplicación que proporcionan datos y servicios a otras aplicaciones. Las aplicaciones acceden a servicios web XML a través de protocolos web estándar, como SOAP.

</dd> </dl>

 

 
