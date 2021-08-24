---
title: Glosario COM
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0c4c1aa78c81484666311dfcdd6bae8b4e6daaa45581af98f50171f48b4b58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048513"
---
# <a name="com-glossary"></a>Glosario COM

<dl> <dt>

<span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**Activación**
</dt> <dd>

Proceso de carga de un objeto en memoria, que lo coloca en estado en ejecución.

</dd> <dt>

<span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**estado activo**
</dt> <dd>

Objeto COM que se encuentra en estado de ejecución y tiene una interfaz de usuario visible.

</dd> <dt>

<span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**moniker absoluto**
</dt> <dd>

moniker que especifica la ubicación absoluta de un objeto . Un moniker absoluto es análogo a una ruta de acceso completa.

</dd> <dt>

<span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**titular de asesoramiento**
</dt> <dd>

Objeto COM que almacena en caché, administra y envía notificaciones de cambios en los receptores de aviso de las aplicaciones de contenedor.

</dd> <dt>

<span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**receptor de aviso**
</dt> <dd>

Objeto COM que puede recibir notificaciones de cambios en un objeto incrustado o un objeto vinculado porque implementa la interfaz [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) o [**IAdviseSink2.**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) Los contenedores que deben recibir una notificación de los cambios en los objetos implementan un receptor de aviso. Las notificaciones se originan en el servidor, que usa un objeto de titular de aviso para almacenar en caché y administrar notificaciones en contenedores.

</dd> <dt>

<span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**aggregate (objeto)**
</dt> <dd>

Un objeto COM que está hecho de uno o varios otros objetos COM. Un objeto del agregado se designa como objeto de control, que controla qué interfaces del agregado se exponen y cuáles son privadas. Este objeto de control tiene una implementación especial de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) denominada **IUnknown de control.** Todos los objetos del agregado deben pasar llamadas a **métodos IUnknown** a través del **control IUnknown**.

</dd> <dt>

<span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**Agregación**
</dt> <dd>

Técnica de composición para implementar objetos COM. Permite compilar un nuevo objeto mediante la utilización de una o varias implementaciones de interfaz de objetos existentes. El objeto de agregado elige las interfaces que se van a exponer a los clientes y las interfaces se exponen como si las hubiera implementado el objeto agregado. Los clientes del objeto agregado solo se comunican con el objeto agregado.

</dd> <dt>

<span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**propiedad ambient**
</dt> <dd>

Propiedad en tiempo de ejecución administrada y expuesta por el contenedor. Normalmente, una propiedad ambiente representa una característica de una forma, como el color de fondo, que debe comunicarse con un control para que el control pueda asumir la apariencia de su entorno circundante.

</dd> <dt>

<span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**antimoniker**
</dt> <dd>

Inverso de un moniker de archivo, elemento o puntero. Se agrega un antimoniker al final de un moniker de archivo, elemento o puntero para anularlo. Los anti monikers se usan en la construcción de monikers relativos.

</dd> <dt>

<span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**recuento de referencias artificiales**
</dt> <dd>

Técnica que se usa para ayudar a proteger un objeto antes de llamar a una función o método que podría destruirlo prematuramente. Un programa llama **a IUnknown::AddRef para** incrementar el recuento de referencias del objeto antes de realizar la llamada que podría liberar el objeto. Una vez que se devuelve la función, el programa llama **a IUnknown::Release para** disminuir el recuento.

</dd> <dt>

<span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**enlace asincrónico**
</dt> <dd>

Tipo de enlace en el que es necesario que el proceso se produzca de forma asincrónica para evitar la degradación del rendimiento del usuario final. Normalmente, el enlace asincrónico se usa en entornos distribuidos, como el World Wide Web. OLE admite clases de moniker asincrónicas y mecanismos de devolución de llamada que permiten que el proceso de localización e inicialización de un objeto en un entorno distribuido se produzca mientras se llevan a cabo otras operaciones.

</dd> <dt>

<span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**llamada asincrónica**
</dt> <dd>

Una llamada a una función que se ejecuta por separado para que el autor de la llamada pueda seguir procesando instrucciones sin esperar a que se devuelva la función.

</dd> <dt>

<span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**moniker asincrónico**
</dt> <dd>

Un moniker que admite el enlace asincrónico. Por ejemplo, las instancias de la clase moniker url proporcionada por el sistema son monikers asincrónicos.

</dd> <dt>

<span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**Automatización**
</dt> <dd>

Una manera de manipular los objetos de una aplicación desde fuera de la aplicación. La automatización se usa normalmente para crear aplicaciones que exponen objetos a herramientas de programación y lenguajes de macros, crear y manipular objetos de una aplicación desde otras aplicaciones, o para crear herramientas para acceder a objetos y manipularlos.

</dd> <dt>

<span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**contexto de enlace**
</dt> <dd>

Objeto COM que implementa la [**interfaz IBindCtx.**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) Los contextos de enlace se usan en operaciones de moniker para contener referencias a los objetos activados cuando se enlaza un moniker. El contexto de enlace contiene parámetros que se aplican a todas las operaciones durante el enlace de un moniker compuesto genérico y proporciona a la implementación del moniker acceso a información sobre su entorno.

</dd> <dt>

<span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**Vinculante**
</dt> <dd>

Asociar un nombre a su referencia. En concreto, buscar el objeto denominado por un moniker, colocarlo en su estado en ejecución si aún no lo está y devolverle un puntero de interfaz. Los objetos se pueden enlazar en tiempo de ejecución (también denominado enlace en tiempo de ejecución o enlace dinámico) o en tiempo de compilación (también denominado enlace estático).

</dd> <dt>

<span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**Caché**
</dt> <dd>

Un almacén local (normalmente temporal) de información. En OLE, una caché contiene información que define la presentación de un objeto vinculado o incrustado cuando se abre el contenedor.

</dd> <dt>

<span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**inicialización de caché**
</dt> <dd>

Rellenar la memoria caché de un objeto vinculado o incrustado con datos de presentación. La [**interfaz IOleCache proporciona**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) métodos a los que un contenedor puede llamar para controlar los datos que se almacenan en caché para objetos vinculados o incrustados.

</dd> <dt>

<span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**Clase**
</dt> <dd>

Definición de un objeto en el código. En C++, la clase de un objeto se define como un tipo de datos, pero este no es el caso en otros lenguajes. Dado que OLE se puede codificar en cualquier lenguaje, la clase se usa para hacer referencia a la definición de objeto general.

</dd> <dt>

<span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**generador de clases**
</dt> <dd>

Objeto COM que implementa la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) y que crea una o varias instancias de un objeto identificado por un identificador de clase determinado (CLSID).

</dd> <dt>

<span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**Identificador de clase (CLSID)**
</dt> <dd>

Identificador único global (GUID) asociado a un objeto de clase OLE. Si se va a usar un objeto de clase para crear más de una instancia de un objeto , la aplicación de servidor asociada debe registrar su CLSID en el registro del sistema para que los clientes puedan buscar y cargar el código ejecutable asociado a los objetos. Cada servidor OLE o contenedor que permita la vinculación a sus objetos incrustados debe registrar un CLSID para cada definición de objeto compatible.

</dd> <dt>

<span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**objeto de clase**
</dt> <dd>

En la programación orientada a objetos, un objeto cuyo estado comparten todos los objetos de una clase y cuyo comportamiento actúa sobre esos datos de estado de toda la clase. En COM, los objetos de clase se denominan generadores de clases y normalmente no tienen ningún comportamiento excepto para crear nuevas instancias de la clase .

</dd> <dt>

<span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**Cliente**
</dt> <dd>

Objeto COM que solicita servicios de otro objeto .

</dd> <dt>

<span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**sitio cliente**
</dt> <dd>

Sitio para mostrar de un objeto incrustado o vinculado dentro de un documento compuesto. El sitio cliente es el medio principal por el que un objeto solicita servicios desde su contenedor.

</dd> <dt>

<span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**Clsid**
</dt> <dd>

Identificador único global (GUID) asociado a un objeto de clase OLE. Si se va a usar un objeto de clase para crear más de una instancia de un objeto , la aplicación de servidor asociada debe registrar su CLSID en el registro del sistema para que los clientes puedan buscar y cargar el código ejecutable asociado a los objetos. Cada servidor OLE o contenedor que permita la vinculación a sus objetos incrustados debe registrar un CLSID para cada definición de objeto compatible.

</dd> <dt>

<span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**Cometer**
</dt> <dd>

Para guardar de forma persistente los cambios realizados en un objeto de almacenamiento o flujo desde que se abrió o se guardaron por última vez los cambios.

</dd> <dt>

<span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**Componente**
</dt> <dd>

Objeto que encapsula los datos y el código, y proporciona un conjunto bien especificado de servicios disponibles públicamente.

</dd> <dt>

<span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Modelo de objetos componentes (COM)**
</dt> <dd>

Modelo de programación orientado a objetos OLE que define cómo interactúan los objetos dentro de un único proceso o entre procesos. En COM, los clientes tienen acceso a un objeto a través de interfaces implementadas en el objeto .

</dd> <dt>

<span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**barra de menús compuesta**
</dt> <dd>

Una barra de menús compartida formada por grupos de menús de una aplicación contenedora y una aplicación de servidor activada localmente.

</dd> <dt>

<span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**moniker compuesto**
</dt> <dd>

Un moniker que consta de dos o más monikers que se tratan como una unidad. Un moniker compuesto puede no ser genérico, lo que significa que sus monikers componentes tienen conocimientos especiales entre sí, o genéricos, lo que significa que sus monikers componentes no saben nada entre sí, excepto que son monikers.

</dd> <dt>

<span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**documento compuesto**
</dt> <dd>

Documento que incluye objetos vinculados o incrustados, así como sus propios datos nativos.

</dd> <dt>

<span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**archivo compuesto**
</dt> <dd>

Una implementación de structured Storage proporcionada por OLE.

</dd> <dt>

<span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**Objeto COM**
</dt> <dd>

Objeto que se ajusta al modelo de objetos de componente OLE (COM). Un objeto COM es una instancia de una definición de objeto, que especifica los datos del objeto y una o varias implementaciones de interfaces en el objeto. Los clientes interactúan con un objeto COM solo a través de sus interfaces.

</dd> <dt>

<span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**objeto conectable**
</dt> <dd>

Objeto COM que implementa, como mínimo, la interfaz [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) para la administración de objetos de punto de conexión. Los objetos conectables admiten la comunicación desde el servidor al cliente. Un objeto conectable crea y administra uno o varios subobjetos de punto de conexión, que reciben eventos de interfaces implementadas en otros objetos y los envían al cliente.

</dd> <dt>

<span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**objeto de punto de conexión**
</dt> <dd>

Objeto COM administrado por un objeto conectable y que implementa la [**interfaz IConnectionPoint.**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) Un objeto conectable puede crear y administrar uno o varios objetos de punto de conexión. Cada objeto de punto de conexión administra los eventos entrantes desde una interfaz específica en otro objeto y los envía al cliente.

</dd> <dt>

<span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**aplicación contenedora**
</dt> <dd>

Una aplicación que admite documentos compuestos. La aplicación contenedora proporciona almacenamiento para un objeto incrustado o vinculado, un sitio para su presentación, acceso al sitio para mostrar y un receptor de aviso para recibir notificaciones de cambios en el objeto.

</dd> <dt>

<span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**Contención**
</dt> <dd>

Técnica de composición para implementar objetos COM. Permite que un objeto reutilice algunas o todas las implementaciones de interfaz de uno o varios objetos. El objeto externo actúa como cliente de los demás objetos, delegando la implementación cuando desea usar los servicios de uno de los objetos contenidos.

</dd> <dt>

<span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**Contexto**
</dt> <dd>

En COM+, un conjunto de propiedades en tiempo de ejecución asociadas a uno o varios objetos COM que se usan para proporcionar servicios para esos objetos.

</dd> <dt>

<span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**Control**
</dt> <dd>

Objeto COM reutilizable e insertable que admite, como mínimo, la [**interfaz IOleControl.**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) Normalmente, los controles están asociados a la interfaz de usuario. También admiten la comunicación con un contenedor y varios clientes pueden reutilizarlos, en función de los criterios de licencia.

</dd> <dt>

<span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**contenedor de control**
</dt> <dd>

Una aplicación que admite la inserción de controles mediante la implementación de la [**interfaz IOleControlSite.**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)

</dd> <dt>

<span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**propiedad de control**
</dt> <dd>

Propiedad en tiempo de ejecución que el propio control expone y administra. Por ejemplo, la fuente y el tamaño de texto utilizados por el control son propiedades de control.

</dd> <dt>

<span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controlar el objeto**
</dt> <dd>

Objeto dentro de un objeto agregado que controla qué interfaces dentro del objeto agregado se exponen y cuáles son privadas. La [**interfaz IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del objeto de control se denomina **IUnknown de control.** Las llamadas **a métodos IUnknown** de otros objetos del agregado deben pasarse al **IUnknown que controla**.

</dd> <dt>

<span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**sitio de control**
</dt> <dd>

Estructura implementada por un contenedor de controles para administrar la presentación y el almacenamiento de un control. Dentro de un contenedor determinado, cada control tiene un sitio de control correspondiente.

</dd> <dt>

<span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**objeto de transferencia de datos**
</dt> <dd>

Objeto que implementa la interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) y contiene los datos que se transferirán de un objeto a otro mediante el Portapapeles o las operaciones de arrastrar y colocar.

</dd> <dt>

<span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**controlador de objetos predeterminado**
</dt> <dd>

Un archivo DLL proporcionado con OLE que actúa como suplente en el espacio de procesamiento de la aplicación contenedora para el objeto real.

Con el controlador de objetos predeterminado, es posible ver los datos almacenados de un objeto sin activar realmente el objeto. El controlador de objetos predeterminado realiza otras tareas, como representar un objeto desde su estado almacenado en caché cuando el objeto se carga en la memoria.

</dd> <dt>

<span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**objeto dependiente**
</dt> <dd>

Un objeto COM inicializado normalmente por otro objeto (el objeto host). Aunque la duración del objeto dependiente solo puede tener sentido durante la vigencia del objeto host, el objeto host no funciona como [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de control para el objeto dependiente. En cambio, un objeto es un objeto agregado cuando el objeto de administración controla completamente su duración (por medio de su recuento de referencias).

</dd> <dt>

<span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**modo de acceso directo**
</dt> <dd>

Uno de los dos modos de acceso en los que se puede abrir un objeto de almacenamiento. En modo directo, todos los cambios se confirman inmediatamente en el objeto de almacenamiento raíz.

</dd> <dt>

<span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**objeto de documento**
</dt> <dd>

Un documento OLE que puede mostrar una o varias vistas activadas localmente de sus datos dentro de un marco nativo o externo, como un explorador, al tiempo que conserva el control total sobre su interfaz de usuario. Además de implementar el documento OLE habitual y las interfaces de activación en contexto, un objeto de documento debe implementar [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)y cada una de sus vistas (en forma de un objeto de vista de documento) debe implementar [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).

</dd> <dt>

<span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**contenedor de objetos de documento**
</dt> <dd>

Una aplicación contenedora capaz de mostrar una o varias vistas de uno o varios objetos de documento y de administrar todos los objetos de documento contenidos dentro de un archivo. Cada objeto de documento está asociado a un sitio de documento y cada sitio de documento contiene uno o varios sitios de vista de documento correspondientes a las vistas admitidas por el objeto de documento. Un contenedor de objetos de documento también incluye un marco de contenedor, que controla la negociación de menús y barras de herramientas y la enumeración de objetos contenidos.

</dd> <dt>

<span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**servidor de objetos de documento**
</dt> <dd>

Una aplicación de servidor capaz de proporcionar objetos de documento.

</dd> <dt>

<span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**sitio del documento**
</dt> <dd>

Un sitio cliente implementado por un contenedor de objetos de documento para administrar la presentación y el almacenamiento de un objeto de documento. Cada objeto de documento de un contenedor tiene un sitio de documento correspondiente.

</dd> <dt>

<span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**objeto de sitio de documento**
</dt> <dd>

Objeto COM que implementa la interfaz [**IOleDocumentSite,**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) además de las interfaces de sitio cliente habituales (como [**IOleClientSite).**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)

</dd> <dt>

<span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**vista de documento**
</dt> <dd>

Una presentación determinada de los datos de un documento. Un único objeto de documento puede tener una o varias vistas, pero una sola vista de documento puede pertenecer a uno y solo a un objeto de documento.

</dd> <dt>

<span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**objeto de vista de documento**
</dt> <dd>

Objeto COM que implementa la [**interfaz IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) y corresponde a una vista de documento determinada. Un objeto con varias vistas de documento agrega un objeto de vista de documento independiente para cada vista.

</dd> <dt>

<span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**sitio de vista de documentos**
</dt> <dd>

Objeto agregado por un objeto de sitio de documento para administrar el espacio de presentación de una vista determinada de un objeto de documento. Dentro de un sitio de documento determinado, cada vista de documento tiene un sitio de vista de documento correspondiente.

</dd> <dt>

<span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**objeto de sitio de vista de documento**
</dt> <dd>

Objeto COM que se agrega en un objeto de sitio de documento e implementa la interfaz [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) y, opcionalmente, la [**interfaz IContinueCallback.**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback)

</dd> <dt>

<span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**arrastrar y colocar**
</dt> <dd>

Una operación en la que el usuario final usa el mouse u otro dispositivo que apunta para mover datos a otra ubicación de la misma ventana u otra ventana.

</dd> <dt>

<span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Insertar**
</dt> <dd>

Para insertar un objeto en un documento compuesto de forma que se conserven los formatos de datos nativos de ese objeto y que se pueda editar desde dentro de su contenedor mediante herramientas expuestas por su servidor.

</dd> <dt>

<span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**objeto incrustado**
</dt> <dd>

Objeto cuyos datos se almacenan en un documento compuesto, pero el objeto se ejecuta en el espacio de proceso de su servidor. El controlador de objetos predeterminado proporciona un suplente en el espacio de procesamiento de la aplicación contenedora para el objeto real.

</dd> <dt>

<span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**propiedad extendida**
</dt> <dd>

Una propiedad en tiempo de ejecución, como la posición y el tamaño de un control, que un usuario asumiría que el control expone, pero que el contenedor expone y administra.

</dd> <dt>

<span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**moniker de archivo**
</dt> <dd>

Moniker basado en una ruta de acceso en el sistema de archivos. Los monikers de archivo se pueden usar para identificar los objetos que se guardan en sus propios archivos. Un moniker de archivo es un objeto COM que admite la implementación proporcionada por el sistema de la [**interfaz IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) para la clase de moniker de archivo.

</dd> <dt>

<span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**objeto font**
</dt> <dd>

Objeto COM que proporciona acceso a Interfaz de dispositivo gráfico (GDI) mediante la implementación de la [**interfaz IFont.**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)

</dd> <dt>

<span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**identificador de formato**
</dt> <dd>

GUID que identifica un conjunto de propiedades persistente. También se conoce como FMTID.

</dd> <dt>

<span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**Marco**
</dt> <dd>

Parte de una aplicación contenedora responsable de negociar menús, teclas de aceleración, barras de herramientas y otros elementos compartidos de la interfaz de usuario con un objeto COM incrustado o un objeto de documento.

</dd> <dt>

<span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**objeto frame**
</dt> <dd>

Objeto COM que implementa la interfaz [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) y, opcionalmente, la [**interfaz IOleCommandTarget.**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget)

</dd> <dt>

<span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**moniker compuesto genérico**
</dt> <dd>

Colección secuenciada de monikers, empezando por un moniker de archivo para proporcionar la ruta de acceso de nivel de documento y continuando con uno o varios monikers de elementos que, tomados como un todo, identifican de forma única un objeto.

</dd> <dt>

<span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**función auxiliar**
</dt> <dd>

Función que encapsula las llamadas a otras funciones y métodos de interfaz disponibles públicamente en el SDK de OLE. Las funciones auxiliares son una manera cómoda de llamar a secuencias usadas con frecuencia de llamadas a funciones y métodos que realiza tareas comunes.

</dd> <dt>

<span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**objeto host**
</dt> <dd>

Objeto COM que forma una relación jerárquica con uno o varios objetos COM, conocidos como objetos dependientes. Normalmente, el objeto host crea instancias de los objetos dependientes y su existencia solo tiene sentido durante la vigencia del objeto host. Sin embargo, el objeto host no actúa como [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de control para los objetos dependientes ni delega directamente en las implementaciones de interfaz de esos objetos.

</dd> <dt>

<span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**Hresult**
</dt> <dd>

Un identificador de resultado opaco definido como cero para una devolución correcta de una función y distinto de cero si se devuelve información de error o estado.

</dd> <dt>

<span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**objeto hyperlink**
</dt> <dd>

Objeto COM que implementa, como mínimo, la interfaz [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) y actúa como vínculo a un objeto en otra ubicación (el destino). Un hipervínculo se forma de cuatro partes: un moniker que identifica la ubicación del destino; una cadena para la ubicación dentro del destino; un nombre descriptivo o que se puede mostrar para el destino; y una cadena que puede contener parámetros adicionales.

</dd> <dt>

<span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**contexto de exploración de hipervínculo**
</dt> <dd>

Objeto COM que implementa la interfaz [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) y mantiene la pila de navegación del hipervínculo. El objeto de contexto de exploración administra la ventana del marco de hipervínculo y la ventana del objeto de destino de hipervínculo.

</dd> <dt>

<span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**contenedor de hipervínculos**
</dt> <dd>

Una aplicación contenedora que admite hipervínculos mediante la implementación de la interfaz [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) y, si los objetos del contenedor pueden ser destinos de otros hipervínculos, la [**interfaz IHlinkTarget.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85))

</dd> <dt>

<span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**objeto de marco de hipervínculo**
</dt> <dd>

Objeto COM que implementa la interfaz [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) y controla la navegación de nivel superior y la presentación de hipervínculos para el contenedor del marco y el servidor del destino del hipervínculo.

</dd> <dt>

<span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**objeto de sitio de hipervínculo**
</dt> <dd>

Objeto COM que implementa la interfaz [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) y proporciona el moniker o el identificador de interfaz de su contenedor de hipervínculos. Un sitio de hipervínculo puede atender varios hipervínculos.

</dd> <dt>

<span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**objeto de destino de hipervínculo**
</dt> <dd>

Objeto COM que implementa la interfaz [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) y proporciona su moniker, nombre descriptivo y otra información que otros objetos de hipervínculo usarán para navegar a él.

</dd> <dt>

<span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**en el parámetro**
</dt> <dd>

Parámetro que el autor de la llamada de una función o método de interfaz asigna, establece y libera. La función llamada no modifica un parámetro in.

</dd> <dt>

<span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**parámetro in/out**
</dt> <dd>

Parámetro asignado inicialmente por el autor de la llamada de una función o método de interfaz, y establecido, liberado y reasignado, si es necesario, por el proceso al que se llama.

</dd> <dt>

<span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**activación local**
</dt> <dd>

Edición de un objeto incrustado dentro de la ventana de su contenedor mediante las herramientas proporcionadas por el servidor. Los objetos vinculados no admiten la activación en contexto; siempre se editan en la ventana del servidor.

</dd> <dt>

<span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**servidor en proceso**
</dt> <dd>

Un servidor implementado como un archivo DLL que se ejecuta en el espacio de proceso del cliente.

</dd> <dt>

<span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**Ejemplo**
</dt> <dd>

Objeto para el que se asigna memoria o que es persistente.

</dd> <dt>

<span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**Interfaz**
</dt> <dd>

Grupo de funciones relacionadas semánticamente que proporcionan acceso a un objeto COM. Cada interfaz OLE define un contrato que permite que los objetos interactúen según el Modelo de objetos componentes (COM). Aunque OLE proporciona muchas implementaciones de interfaz, los desarrolladores que diseñan aplicaciones OLE también pueden implementar la mayoría de las interfaces.

</dd> <dt>

<span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**identificador de interfaz (IID)**
</dt> <dd>

Identificador único global (GUID) asociado a una interfaz. Algunas funciones toman IID como parámetros para permitir que el autor de la llamada especifique qué puntero de interfaz se debe devolver.

</dd> <dt>

<span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**moniker de elemento**
</dt> <dd>

Moniker basado en una cadena que identifica un objeto en un contenedor. Los monikers de elementos pueden identificar objetos más pequeños que un archivo, incluidos los objetos incrustados en un documento compuesto, o un pseudoelemento (como un intervalo de celdas en una hoja de cálculo).

</dd> <dt>

<span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**Licencias**
</dt> <dd>

Característica de COM que proporciona control sobre la creación de objetos. Los objetos con licencia solo los pueden crear los clientes que están autorizados para usarlos. Las licencias se implementan en COM mediante la [**interfaz IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) y la compatibilidad con una clave de licencia que se puede pasar en tiempo de ejecución.

</dd> <dt>

<span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**objeto de vínculo**
</dt> <dd>

Objeto COM que se crea cuando se crea o carga un objeto COM vinculado. OLE proporciona el objeto de vínculo e implementa la [**interfaz IOleLink.**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)

</dd> <dt>

<span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**objeto vinculado**
</dt> <dd>

Objeto COM cuyos datos de origen residen físicamente donde se crearon inicialmente. Solo un moniker que representa los datos de origen y los datos de presentación adecuados se mantienen con el documento compuesto. Los cambios realizados en el origen del vínculo se reflejan automáticamente en el objeto vinculado.

</dd> <dt>

<span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**origen del vínculo**
</dt> <dd>

Datos que son el origen de un objeto vinculado. Un origen de vínculo puede ser un archivo o una parte de un archivo, como un intervalo seleccionado de celdas dentro de un archivo (también denominado pseudo object).

</dd> <dt>

<span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**estado de carga**
</dt> <dd>

El estado de un objeto después de que sus estructuras de datos se hayan cargado en la memoria y sean accesibles para el proceso de cliente.

</dd> <dt>

<span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**servidor local**
</dt> <dd>

Un servidor fuera de proceso implementado como una aplicación .EXE que se ejecuta en el mismo equipo que su aplicación cliente.

</dd> <dt>

<span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**Cerradura**
</dt> <dd>

Puntero que se mantiene en y, posiblemente, un recuento de referencias incrementado en un objeto en ejecución. OLE define dos tipos de bloqueos que se pueden mantienen en un objeto: fuerte y débil. Para implementar un bloqueo seguro, un servidor debe mantener un puntero y un recuento de referencias, de modo que el objeto permanezca "bloqueado" en la memoria al menos hasta que el servidor llame a [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Para implementar un bloqueo débil, el servidor solo mantiene un puntero al objeto, de modo que otro proceso pueda destruir el objeto.

</dd> <dt>

<span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**Cálculo**
</dt> <dd>

Empaquetar y enviar llamadas a métodos de interfaz a través de los límites de subprocesos o procesos.

</dd> <dt>

<span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**tipo de medio**
</dt> <dd>

Extensión de MIME que permite la negociación de formato de datos entre un cliente y un objeto .

</dd> <dt>

<span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**Tipo de contenido MIME**
</dt> <dd>

Extensión de MIME que permite la negociación de formato de datos entre un cliente y un objeto .

</dd> <dt>

<span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Extensión multipropósito de Correo electrónico de Internet (MIME)**
</dt> <dd>

Un protocolo de Internet desarrollado originalmente para permitir el intercambio de mensajes de correo electrónico con contenido enriquecido a través de entornos heterogéneos de red, equipo y correo electrónico. En la práctica, MIME también se ha adoptado y ampliado por aplicaciones que no son de correo.

</dd> <dt>

<span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**Moniker**
</dt> <dd>

Objeto que implementa la interfaz [**IMoniker.**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) Un moniker actúa como un nombre que identifica de forma única un objeto COM. Del mismo modo que una ruta de acceso identifica un archivo en el sistema de archivos, un moniker identifica un objeto COM en el espacio de nombres de directorio.

</dd> <dt>

<span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker (clase)**
</dt> <dd>

Implementación de la [**interfaz IMoniker.**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) Las clases de moniker proporcionadas por el sistema incluyen monikers de archivo, monikers de elementos, monikers compuestos genéricos, anti monikers, monikers de puntero y monikers de url.

</dd> <dt>

<span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**Cliente de moniker**
</dt> <dd>

Una aplicación que usa monikers para adquirir punteros de interfaz a objetos administrados por otra aplicación.

</dd> <dt>

<span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**Proveedor de moniker**
</dt> <dd>

Una aplicación que pone a disposición monikers que identifican los objetos que administra, de modo que los objetos sean accesibles para otras aplicaciones.

</dd> <dt>

<span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**extensión de espacio de nombres**
</dt> <dd>

Objeto COM en proceso que implementa [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)e [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), que a veces se conocen como interfaces de extensión de espacio de nombres. Una extensión de espacio de nombres se usa para ampliar el espacio de nombres del shell o para crear un espacio de nombres independiente. Los usuarios primarios son los Windows explorer y los cuadros de diálogo comunes de archivos.

</dd> <dt>

<span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**datos nativos**
</dt> <dd>

Datos utilizados por una aplicación de servidor OLE al editar un objeto incrustado.

</dd> <dt>

<span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**Objeto**
</dt> <dd>

En OLE, una estructura de programación que encapsula los datos y la funcionalidad que se definen y asignan como una sola unidad y para la que el único acceso público es a través de las interfaces de la estructura de programación. Un objeto COM debe admitir, como mínimo, la interfaz [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) que mantiene la existencia del objeto mientras se usa y proporciona acceso a las otras interfaces del objeto.

</dd> <dt>

<span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**estado del objeto** 
</dt> <dd>

Relación entre un objeto de documento compuesto en su contenedor y la aplicación responsable de la creación del objeto: activa, pasiva, cargada o en ejecución. Los objetos pasivos se almacenan en el disco o en una base de datos, y el objeto no está seleccionado ni activo. En el estado cargado, las estructuras de datos del objeto se han cargado en la memoria, pero no están disponibles para operaciones como la edición. Los objetos en ejecución se cargan y están disponibles para todas las operaciones. Los objetos activos ejecutan objetos que tienen una interfaz de usuario visible.

</dd> <dt>

<span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**nombre del tipo de objeto**
</dt> <dd>

Cadena de identificación única que se almacena como parte de la información disponible para un objeto en la base de datos de registro.

</dd> <dt>

<span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**Ole**
</dt> <dd>

Tecnología basada en objetos de Microsoft para compartir información y servicios a través de los límites de procesos y equipos.

</dd> <dt>

<span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**servidor fuera de proceso**
</dt> <dd>

Un servidor, implementado como una aplicación .EXE, que se ejecuta fuera del proceso de su cliente, ya sea en el mismo equipo o en un equipo remoto.

</dd> <dt>

<span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out, parámetro**
</dt> <dd>

La función a la que se llama asigna un parámetro out y lo libera el autor de la llamada.

</dd> <dt>

<span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**estado pasivo**
</dt> <dd>

Estado de un objeto COM cuando se almacena (en disco o en una base de datos). El objeto no está seleccionado ni activo.

</dd> <dt>

<span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**propiedad persistente**
</dt> <dd>

Información que se puede almacenar de forma persistente como parte de un objeto de almacenamiento, como un archivo o directorio. Las propiedades persistentes se agrupan en conjuntos de propiedades, que se pueden mostrar y editar.

Una propiedad persistente es diferente de las propiedades en tiempo de ejecución de los objetos creados con tecnologías de automatización y controles OLE, que se pueden usar para afectar al comportamiento del sistema. La [**estructura PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) define todos los tipos válidos de propiedades persistentes, mientras que la estructura **VARIANT** define todos los tipos válidos de propiedades en tiempo de ejecución.

</dd> <dt>

<span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**almacenamiento persistente**
</dt> <dd>

Storage de un archivo u objeto en un medio, como un sistema de archivos o una base de datos, para que el objeto y sus datos se conserven cuando se cierre el archivo y, a continuación, se vuelvan a abrir más adelante.

</dd> <dt>

<span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**objeto picture**
</dt> <dd>

Objeto COM que proporciona acceso a imágenes GDI mediante la implementación de la [**interfaz IPicture.**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture)

</dd> <dt>

<span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**moniker de puntero**
</dt> <dd>

moniker que asigna un puntero de interfaz a un objeto en memoria. Mientras que la mayoría de los monikers identifican objetos que se pueden almacenar de forma persistente, los monikers de puntero identifican objetos que no pueden. Permiten que estos objetos participen en una operación de enlace de moniker.

</dd> <dt>

<span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**datos de presentación**
</dt> <dd>

Datos utilizados por un contenedor para mostrar objetos incrustados o vinculados.

</dd> <dt>

<span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**verbo principal**
</dt> <dd>

Acción asociada a la operación más común o preferida que realizan los usuarios en un objeto . El verbo principal siempre se define como verbo cero en la base de datos de registro del sistema. El verbo principal de un objeto se ejecuta haciendo doble clic en el objeto .

</dd> <dt>

<span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**Propiedad**
</dt> <dd>

Información asociada a un objeto . En OLE, las propiedades se divide en dos categorías: propiedades en tiempo de ejecución y propiedades persistentes. Las propiedades en tiempo de ejecución se suelen asociar a objetos de control o a sus contenedores. Por ejemplo, el color de fondo es una propiedad en tiempo de ejecución establecida por el contenedor de un control. Las propiedades persistentes están asociadas a objetos almacenados.

</dd> <dt>

<span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**marco de propiedades**
</dt> <dd>

Mecanismo de interfaz de usuario que muestra una o varias páginas de propiedades para un control . El sistema en tiempo de ejecución de controles OLE proporciona una implementación estándar de un marco de propiedades al que se puede acceder mediante la función auxiliar [**OleCreatePropertyFrame.**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe)

</dd> <dt>

<span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**identificador de propiedad**
</dt> <dd>

Entero con signo de cuatro bytes que identifica una propiedad persistente dentro de un conjunto de propiedades.

</dd> <dt>

<span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**página de propiedades**
</dt> <dd>

Un objeto COM con su propio CLSID que forma parte de una interfaz de usuario, implementado por un control , y permite ver y establecer las propiedades del control. Los objetos de página de propiedades implementan [**la interfaz IPropertyPage.**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage)

</dd> <dt>

<span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**sitio de la página de propiedades**
</dt> <dd>

Ubicación dentro de un marco de propiedades donde se muestra una página de propiedades. El marco de propiedades implementa la [**interfaz IPropertyPageSite,**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) que contiene métodos para administrar los sitios de cada una de las páginas de propiedades proporcionadas por un control .

</dd> <dt>

<span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**conjunto de propiedades**
</dt> <dd>

Un grupo de propiedades relacionados lógicamente que está asociado a un objeto almacenado de forma persistente. Para crear, abrir, eliminar o enumerar uno o varios conjuntos de propiedades, implemente la [**interfaz IPropertySetStorage.**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) Si usa archivos compuestos, puede usar la implementación de OLE de esta interfaz en lugar de implementar la suya propia.

</dd> <dt>

<span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**almacenamiento del conjunto de propiedades**
</dt> <dd>

Objeto de almacenamiento COM que contiene un conjunto de propiedades. Un almacenamiento de conjunto de propiedades es un objeto dependiente asociado a y administrado por un objeto de almacenamiento.

</dd> <dt>

<span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**hoja de propiedades**
</dt> <dd>

Conjunto de páginas de propiedades para uno o varios objetos.

</dd> <dt>

<span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**Proxy**
</dt> <dd>

Objeto específico de la interfaz que empaqueta parámetros para esa interfaz como preparación para una llamada de método remoto. Un proxy se ejecuta en el espacio de direcciones del remitente y se comunica con un código auxiliar correspondiente en el espacio de direcciones del receptor.

</dd> <dt>

<span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**administrador de proxy**
</dt> <dd>

En la serialización estándar, un proxy que administra todos los servidores proxy de interfaz para un solo objeto.

</dd> <dt>

<span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo object**
</dt> <dd>

Una parte de un documento o un objeto incrustado, como un intervalo de celdas de una hoja de cálculo, que puede ser el origen de un objeto COM.

</dd> <dt>

<span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**recuento de referencias**
</dt> <dd>

Mantener un recuento de cada puntero de interfaz mantenido en un objeto para asegurarse de que el objeto no se destruye antes de que se liberan todas las referencias a él.

</dd> <dt>

<span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**moniker relativo**
</dt> <dd>

moniker que especifica la ubicación de un objeto con respecto a la ubicación de otro objeto. Un moniker relativo es análogo a una ruta de acceso relativa, como . \\ backup \\ report.old.

</dd> <dt>

<span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**servidor remoto**
</dt> <dd>

Una aplicación de servidor, implementada como exe, que se ejecuta en un equipo diferente de la aplicación cliente que la usa.

</dd> <dt>

<span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**Revertir**
</dt> <dd>

Para descartar los cambios realizados en un objeto desde la última vez que se confirman o se abre el almacenamiento del objeto.

</dd> <dt>

<span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**objeto de almacenamiento raíz**
</dt> <dd>

Objeto de almacenamiento más externo de un documento. Un objeto de almacenamiento raíz puede contener otros objetos de flujo y almacenamiento anidados. Por ejemplo, un documento compuesto se guarda en el disco como una serie de objetos de almacenamiento y flujo dentro de un objeto de almacenamiento raíz.

</dd> <dt>

<span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**estado de ejecución**
</dt> <dd>

El estado de un objeto COM cuando se ejecuta su aplicación de servidor y es posible acceder a sus interfaces y recibir notificaciones de cambios.

</dd> <dt>

<span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**tabla de objetos en ejecución (ROT)**
</dt> <dd>

Tabla accesible globalmente en cada equipo que realiza un seguimiento de todos los objetos COM en estado en ejecución que se pueden identificar mediante un moniker. Los proveedores de moniker registran un objeto en la tabla, lo que incrementa el recuento de referencias del objeto. Para poder destruir el objeto, su moniker debe liberarse de la tabla.

</dd> <dt>

<span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**propiedad en tiempo de ejecución**
</dt> <dd>

Información de estado discreta asociada a un objeto de control o a su contenedor. Hay tres tipos de propiedades en tiempo de ejecución: propiedades ambientales, propiedades de control y propiedades extendidas.

</dd> <dt>

<span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**registro propio**
</dt> <dd>

Proceso por el que un servidor puede realizar sus propias operaciones del Registro.

</dd> <dt>

<span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**aplicación de servidor**
</dt> <dd>

Una aplicación que puede crear objetos COM. A continuación, las aplicaciones de contenedor pueden insertar o vincular a estos objetos.

</dd> <dt>

<span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**objeto estático**
</dt> <dd>

Objeto que contiene solo una presentación, sin datos nativos. Un contenedor puede tratar un objeto estático como si fuera un objeto vinculado o incrustado, salvo que no es posible editar un objeto estático.

Un objeto estático puede producir, por ejemplo, la separación de un vínculo en un objeto vinculado, es decir, que la aplicación de servidor no está disponible o que el usuario ya no quiere que el objeto vinculado se actualice.

</dd> <dt>

<span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**objeto de almacenamiento**
</dt> <dd>

Objeto COM que implementa la [**interfaz IStorage.**](/windows/desktop/api/objidl/nn-objidl-istorage) Un objeto de almacenamiento contiene objetos de almacenamiento anidados o objetos de secuencia, lo que da como resultado el equivalente de una estructura de directorios o archivos dentro de un único archivo.

</dd> <dt>

<span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**objeto stream**
</dt> <dd>

Objeto COM que implementa la [**interfaz IStream.**](/windows/desktop/api/objidl/nn-objidl-istream) Un objeto de secuencia es análogo a un archivo en un sistema de directorios o archivos.

</dd> <dt>

<span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Estructurada Storage**
</dt> <dd>

Tecnología de OLE para almacenar archivos compuestos en sistemas de archivos nativos.

</dd> <dt>

<span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**Trozo**
</dt> <dd>

Cuando los parámetros de una función o del método de interfaz se serializan a través de un límite de proceso, el código auxiliar es un objeto específico de la interfaz que desempaquete los parámetros serializados y llama al método necesario. El código auxiliar se ejecuta en el espacio de direcciones del receptor y se comunica con un proxy correspondiente en el espacio de direcciones del remitente.

</dd> <dt>

<span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**administrador de código auxiliar**
</dt> <dd>

Administra todos los códigos auxiliares de interfaz para un solo objeto.

</dd> <dt>

<span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**llamada sincrónica**
</dt> <dd>

Una llamada de función que no permite que se ejecuten más instrucciones en el proceso de llamada hasta que se devuelva la función.

</dd> <dt>

<span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**registro del sistema**
</dt> <dd>

Un repositorio de información de todo el sistema compatible con Windows, que contiene información sobre el sistema y sus aplicaciones, incluidos los servidores y clientes OLE.

</dd> <dt>

<span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**modo de acceso con transacciones**
</dt> <dd>

Uno de los dos modos de acceso en los que se puede abrir un objeto de almacenamiento. Cuando se abren en modo de transacción, los cambios se almacenan en búferes hasta que el objeto de almacenamiento raíz confirma sus cambios.

</dd> <dt>

<span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**información de tipo**
</dt> <dd>

Información sobre la clase de un objeto proporcionada por una biblioteca de tipos. Para proporcionar información de tipo, un objeto COM implementa la [**interfaz IProvideClassInfo.**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo)

</dd> <dt>

<span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**transferencia uniforme de datos**
</dt> <dd>

Modelo para transferir datos a través del Portapapeles, arrastrar y colocar o Automation. Los objetos que se ajustan a este modelo implementan [**la interfaz IDataObject.**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) Este modelo reemplaza a DDE (intercambio dinámico de datos).

</dd> <dt>

<span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**desmarque**
</dt> <dd>

Desempaquetar los parámetros que se han enviado a un proxy a través de los límites del proceso.

</dd> <dt>

<span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**localizador de recursos universal (URL)**
</dt> <dd>

Identificador utilizado por el World Wide Web para los nombres y ubicaciones de objetos en Internet. OLE proporciona una clase de moniker, moniker de dirección URL, cuya implementación se puede usar para enlazar un cliente a objetos identificados por una dirección URL.

</dd> <dt>

<span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**Moniker de dirección URL**
</dt> <dd>

Un moniker basado en un localizador de recursos universal (URL). Un cliente puede usar monikers de dirección URL para enlazar a objetos que residen en Internet. La clase moniker URL proporcionada por el sistema admite el enlace sincrónico y asincrónico.

</dd> </dl>

 

 