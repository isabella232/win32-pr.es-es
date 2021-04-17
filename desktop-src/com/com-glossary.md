---
title: Glosario de COM
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c12f3c021988f0349d9eaf6a2bdbd9505ca8a6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705044"
---
# <a name="com-glossary"></a>Glosario de COM

<dl> <dt>

<span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**activación**
</dt> <dd>

Proceso de carga de un objeto en la memoria, que lo pone en el estado de ejecución.

</dd> <dt>

<span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**estado activo**
</dt> <dd>

Un objeto COM que se encuentra en estado de ejecución y tiene una interfaz de usuario visible.

</dd> <dt>

<span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**moniker absoluto**
</dt> <dd>

Moniker que especifica la ubicación absoluta de un objeto. Un moniker absoluto es análogo a una ruta de acceso completa.

</dd> <dt>

<span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**titular de asesoría**
</dt> <dd>

Objeto COM que almacena en caché, administra y envía notificaciones de cambios en los receptores de consulta de aplicaciones de contenedor.

</dd> <dt>

<span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**receptor de consulta**
</dt> <dd>

Objeto COM que puede recibir notificaciones de cambios en un objeto incrustado o vinculado porque implementa la interfaz [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) o [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) . Los contenedores a los que se debe notificar los cambios en los objetos de implementan un receptor de consulta. Las notificaciones se originan en el servidor, que utiliza un objeto de titular de consulta para almacenar en memoria caché y administrar las notificaciones de los contenedores.

</dd> <dt>

<span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**Aggregate (objeto)**
</dt> <dd>

Objeto COM que se compone de uno o varios objetos COM. Un objeto del agregado se designa como objeto de control, que controla qué interfaces del agregado se exponen y cuáles son privadas. Este objeto de control tiene una implementación especial de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) denominada **IUnknown** de control. Todos los objetos del agregado deben pasar llamadas a métodos **IUnknown** a través del **IUnknown** de control.

</dd> <dt>

<span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**concentrado**
</dt> <dd>

Técnica de composición para implementar objetos COM. Permite crear un nuevo objeto mediante la reutilización de una o más implementaciones de interfaz de objetos existentes. El objeto agregado elige las interfaces que se van a exponer a los clientes, y las interfaces se exponen como si fueran implementadas por el objeto agregado. Los clientes del objeto agregado solo se comunican con el objeto agregado.

</dd> <dt>

<span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**propiedad Ambient**
</dt> <dd>

Propiedad en tiempo de ejecución administrada y expuesta por el contenedor. Normalmente, una propiedad de ambiente representa una característica de un formulario, como el color de fondo, que debe comunicarse con un control para que el control pueda asumir la apariencia y el funcionamiento de su entorno circundante.

</dd> <dt>

<span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**
</dt> <dd>

El inverso de un moniker de archivo, elemento o puntero. Se agrega un anti-moniker al final de un archivo, elemento o moniker de puntero para anularlo. Los anti-monikers se usan en la construcción de monikers relativos.

</dd> <dt>

<span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**recuento de referencias artificiales**
</dt> <dd>

Técnica que se usa para ayudar a proteger un objeto antes de llamar a una función o un método que podría destruirlo prematuramente. Un programa llama a **IUnknown:: AddRef** para incrementar el recuento de referencias del objeto antes de realizar la llamada que podría liberar el objeto. Una vez que la función devuelve, el programa llama a **IUnknown:: Release** para reducir el recuento.

</dd> <dt>

<span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**enlace asincrónico**
</dt> <dd>

Tipo de enlace en el que es necesario que el proceso se produzca de forma asincrónica para evitar la degradación del rendimiento del usuario final. Normalmente, el enlace asincrónico se usa en entornos distribuidos como el World Wide Web. OLE admite clases de moniker asincrónico y mecanismos de devolución de llamada que permiten que se produzca el proceso de búsqueda e inicialización de un objeto en un entorno distribuido mientras se llevan a cabo otras operaciones.

</dd> <dt>

<span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**llamada asincrónica**
</dt> <dd>

Una llamada a una función que se ejecuta por separado para que el llamador pueda seguir procesando instrucciones sin esperar a que la función devuelva.

</dd> <dt>

<span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**moniker asincrónico**
</dt> <dd>

Moniker que admite el enlace asincrónico. Por ejemplo, las instancias de la clase de moniker de dirección URL proporcionada por el sistema son monikers asincrónicos.

</dd> <dt>

<span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**automatiza**
</dt> <dd>

Una manera de manipular los objetos de una aplicación desde fuera de la aplicación. La automatización se usa normalmente para crear aplicaciones que exponen objetos a herramientas de programación y lenguajes de macros, crear y manipular objetos de una aplicación desde otras aplicaciones o crear herramientas para tener acceso a los objetos y manipularlos.

</dd> <dt>

<span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**contexto de enlace**
</dt> <dd>

Objeto COM que implementa la interfaz [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) . Los contextos de enlace se utilizan en las operaciones de moniker para conservar las referencias a los objetos activados cuando se enlaza un moniker. El contexto de enlace contiene parámetros que se aplican a todas las operaciones durante el enlace de un moniker compuesto genérico y proporciona la implementación de moniker con acceso a información sobre su entorno.

</dd> <dt>

<span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**enlace**
</dt> <dd>

Asociar un nombre a su correspondiente. En concreto, para localizar el objeto denominado por un moniker, ponerlo en su estado de ejecución, si aún no lo está, y devolver un puntero de interfaz a él. Los objetos se pueden enlazar en tiempo de ejecución (también denominado enlace tardío o enlace dinámico) o en tiempo de compilación (también denominado enlace estático).

</dd> <dt>

<span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**almacenar**
</dt> <dd>

Un almacén local (normalmente temporal) de información. En OLE, una memoria caché contiene información que define la presentación de un objeto vinculado o incrustado cuando se abre el contenedor.

</dd> <dt>

<span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**inicialización de caché**
</dt> <dd>

Rellenar la caché de un objeto vinculado o incrustado con datos de presentación. La interfaz [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) proporciona métodos a los que puede llamar un contenedor para controlar los datos que se almacenan en caché para objetos vinculados o incrustados.

</dd> <dt>

<span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**las**
</dt> <dd>

Definición de un objeto en el código. En C++, la clase de un objeto se define como un tipo de datos, pero este no es el caso en otros lenguajes. Dado que OLE se puede codificar en cualquier lenguaje, la clase se utiliza para hacer referencia a la definición de objeto general.

</dd> <dt>

<span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**generador de clases**
</dt> <dd>

Objeto COM que implementa la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) y que crea una o varias instancias de un objeto identificado por un identificador de clase (CLSID) determinado.

</dd> <dt>

<span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**identificador de clase (CLSID)**
</dt> <dd>

Identificador único global (GUID) asociado a un objeto de clase OLE. Si un objeto de clase se va a utilizar para crear más de una instancia de un objeto, la aplicación de servidor asociada debe registrar su CLSID en el registro del sistema para que los clientes puedan buscar y cargar el código ejecutable asociado a los objetos. Cada servidor o contenedor OLE que permite vincular a sus objetos incrustados debe registrar un CLSID para cada definición de objeto compatible.

</dd> <dt>

<span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**objeto de clase**
</dt> <dd>

En la programación orientada a objetos, objeto cuyo estado comparten todos los objetos de una clase y cuyo comportamiento actúa en los datos de estado classwide. En COM, los objetos de clase se denominan generadores de clase y, por lo general, no tienen ningún comportamiento excepto para crear nuevas instancias de la clase.

</dd> <dt>

<span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**Nº**
</dt> <dd>

Objeto COM que solicita servicios de otro objeto.

</dd> <dt>

<span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**sitio de cliente**
</dt> <dd>

El sitio de presentación de un objeto incrustado o vinculado dentro de un documento compuesto. El sitio del cliente es el medio principal por el que un objeto solicita servicios de su contenedor.

</dd> <dt>

<span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**
</dt> <dd>

Identificador único global (GUID) asociado a un objeto de clase OLE. Si un objeto de clase se va a utilizar para crear más de una instancia de un objeto, la aplicación de servidor asociada debe registrar su CLSID en el registro del sistema para que los clientes puedan buscar y cargar el código ejecutable asociado a los objetos. Cada servidor o contenedor OLE que permite vincular a sus objetos incrustados debe registrar un CLSID para cada definición de objeto compatible.

</dd> <dt>

<span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**promete**
</dt> <dd>

Para guardar de forma persistente cualquier cambio realizado en un objeto de almacenamiento o de flujo desde que se abrió o se guardaron los cambios por última vez.

</dd> <dt>

<span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**pone**
</dt> <dd>

Objeto que encapsula los datos y el código, y proporciona un conjunto bien especificado de servicios disponibles públicamente.

</dd> <dt>

<span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Modelo de objetos componentes (COM)**
</dt> <dd>

Modelo de programación orientado a objetos OLE que define cómo interactúan los objetos dentro de un proceso único o entre procesos. En COM, los clientes tienen acceso a un objeto a través de las interfaces implementadas en el objeto.

</dd> <dt>

<span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**barra de menús compuesta**
</dt> <dd>

Barra de menús compartida formada por grupos de menús de una aplicación contenedora y una aplicación de servidor activa en contexto.

</dd> <dt>

<span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**moniker compuesto**
</dt> <dd>

Moniker que se compone de dos o más monikers que se tratan como una unidad. Un moniker compuesto puede ser no genérico, lo que significa que sus monikers de componente tienen un conocimiento especial entre sí, o genérico, lo que significa que sus monikers de componente no saben nada sobre sí, salvo que son monikers.

</dd> <dt>

<span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**documento compuesto**
</dt> <dd>

Documento que incluye objetos vinculados o incrustados, así como sus propios datos nativos.

</dd> <dt>

<span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**archivo compuesto**
</dt> <dd>

Una implementación de almacenamiento estructurado proporcionada por OLE.

</dd> <dt>

<span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**Objeto COM**
</dt> <dd>

Objeto que se ajusta al modelo de objetos componentes (COM) de OLE. Un objeto COM es una instancia de una definición de objeto, que especifica los datos del objeto y una o varias implementaciones de interfaces en el objeto. Los clientes interactúan con un objeto COM solo a través de sus interfaces.

</dd> <dt>

<span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**objeto conectable**
</dt> <dd>

Objeto COM que implementa, como mínimo, la interfaz [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) para la administración de objetos de punto de conexión. Los objetos conectables admiten la comunicación desde el servidor al cliente. Un objeto conectable crea y administra uno o varios subobjetos de punto de conexión, que reciben eventos de interfaces implementadas en otros objetos y los envían al cliente.

</dd> <dt>

<span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**objeto de punto de conexión**
</dt> <dd>

Objeto COM que se administra mediante un objeto conectable y que implementa la interfaz [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) . Uno o varios objetos de punto de conexión se pueden crear y administrar mediante un objeto conectable. Cada objeto de punto de conexión administra los eventos entrantes de una interfaz específica en otro objeto y envía los eventos al cliente.

</dd> <dt>

<span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**aplicación contenedora**
</dt> <dd>

Aplicación que admite documentos compuestos. La aplicación contenedora proporciona almacenamiento para un objeto incrustado o vinculado, un sitio para su presentación, acceso al sitio para mostrar y un receptor de consulta para recibir notificaciones de cambios en el objeto.

</dd> <dt>

<span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**contención**
</dt> <dd>

Técnica de composición para implementar objetos COM. Permite que un objeto reutilice algunas o todas las implementaciones de interfaz de uno o más objetos. El objeto externo actúa como cliente de los demás objetos, delegando la implementación cuando desea utilizar los servicios de uno de los objetos contenidos.

</dd> <dt>

<span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**contexto**
</dt> <dd>

En COM+, conjunto de propiedades de tiempo de ejecución asociadas a uno o varios objetos COM que se usan para proporcionar servicios para esos objetos.

</dd> <dt>

<span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**control**
</dt> <dd>

Objeto COM que se puede incrustar y reutilizar que admite, como mínimo, la interfaz [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) . Normalmente, los controles se asocian a la interfaz de usuario. También admiten la comunicación con un contenedor y pueden ser reutilizados por varios clientes, según los criterios de licencia.

</dd> <dt>

<span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**contenedor de control**
</dt> <dd>

Aplicación que admite la inserción de controles mediante la implementación de la interfaz [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) .

</dd> <dt>

<span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**propiedad de control**
</dt> <dd>

Propiedad en tiempo de ejecución que el propio control expone y administra. Por ejemplo, la fuente y el tamaño del texto utilizados por el control son propiedades del control.

</dd> <dt>

<span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controlar objeto**
</dt> <dd>

Objeto dentro de un objeto agregado que controla qué interfaces del objeto agregado se exponen y cuáles son privadas. La interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del objeto de control se denomina **IUnknown** de control. Las llamadas a los métodos **IUnknown** de otros objetos del agregado se deben pasar al objeto **IUnknown** de control.

</dd> <dt>

<span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**sitio de control**
</dt> <dd>

Estructura implementada por un contenedor de controles para administrar la presentación y el almacenamiento de un control. Dentro de un contenedor determinado, cada control tiene un sitio de control correspondiente.

</dd> <dt>

<span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**objeto de transferencia de datos**
</dt> <dd>

Objeto que implementa la interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) y que contiene los datos que se van a transferir de un objeto a otro a través del portapapeles o las operaciones de arrastrar y colocar.

</dd> <dt>

<span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**controlador de objetos predeterminado**
</dt> <dd>

Un archivo DLL proporcionado con OLE que actúa como suplente en el espacio de procesamiento de la aplicación contenedora para el objeto real.

Con el controlador de objetos predeterminado, es posible ver los datos almacenados de un objeto sin activar realmente el objeto. El controlador de objetos predeterminado realiza otras tareas, como la representación de un objeto a partir de su estado almacenado en memoria caché cuando el objeto se carga en la memoria.

</dd> <dt>

<span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**objeto dependiente**
</dt> <dd>

Objeto COM que normalmente inicializa otro objeto (el objeto host). Aunque la duración del objeto dependiente solo puede tener sentido durante la duración del objeto host, el objeto host no funciona como [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de control para el objeto dependiente. En cambio, un objeto es un objeto agregado cuando su duración (por medio de su recuento de referencias) está completamente controlada por el objeto de administración.

</dd> <dt>

<span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**modo de acceso directo**
</dt> <dd>

Uno de los dos modos de acceso en los que se puede abrir un objeto de almacenamiento. En el modo directo, todos los cambios se confirman inmediatamente en el objeto de almacenamiento raíz.

</dd> <dt>

<span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**objeto de documento**
</dt> <dd>

Documento OLE que puede mostrar una o varias vistas activadas en contexto de sus datos dentro de un marco nativo o externo, como un explorador, conservando el control total sobre su interfaz de usuario. Además de implementar el documento OLE habitual y las interfaces de activación en contexto, un objeto de documento debe implementar [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)y cada una de sus vistas (en forma de objeto de vista de documento) debe implementar [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).

</dd> <dt>

<span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**contenedor de objetos de documento**
</dt> <dd>

Aplicación contenedora capaz de mostrar una o más vistas de uno o más objetos de documento y de administrar todos los objetos de documento contenidos dentro de un archivo. Cada objeto de documento está asociado a un sitio de documento y cada sitio de documento contiene uno o más sitios de vista de documento correspondientes a las vistas admitidas por el objeto de documento. Un contenedor de objetos de documento también incluye un marco de contenedor, que controla la negociación de menús y barras de herramientas y la enumeración de objetos contenidos.

</dd> <dt>

<span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**servidor de objetos de documento**
</dt> <dd>

Aplicación de servidor capaz de proporcionar objetos de documento.

</dd> <dt>

<span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**sitio de documento**
</dt> <dd>

Sitio cliente implementado por un contenedor de objetos de documento para administrar la presentación y el almacenamiento de un objeto de documento. Cada objeto de documento de un contenedor tiene un sitio de documento correspondiente.

</dd> <dt>

<span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**objeto de sitio de documento**
</dt> <dd>

Objeto COM que implementa la interfaz [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) , además de las interfaces de sitio de cliente habituales (como [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).

</dd> <dt>

<span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**vista de documento**
</dt> <dd>

Una presentación determinada de los datos de un documento. Un único objeto de documento puede tener una o más vistas, pero una sola vista de documento puede pertenecer a un solo objeto de documento.

</dd> <dt>

<span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**objeto de vista de documento**
</dt> <dd>

Objeto COM que implementa la interfaz [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) y corresponde a una vista de documento determinada. Un objeto con varias vistas de documento agrega un objeto de vista de documento independiente para cada vista.

</dd> <dt>

<span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**sitio de vista de documento**
</dt> <dd>

Objeto agregado por un objeto de sitio de documento para administrar el espacio de presentación para una vista determinada de un objeto de documento. Dentro de un sitio de documento determinado, cada vista de documento tiene un sitio de vista de documento correspondiente.

</dd> <dt>

<span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**objeto de sitio de vista de documento**
</dt> <dd>

Objeto COM que se agrega en un objeto de sitio de documento e implementa la interfaz [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) y, opcionalmente, la interfaz [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) .

</dd> <dt>

<span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**arrastrar y colocar**
</dt> <dd>

Operación en la que el usuario final usa el mouse u otro dispositivo señalador para trasladar los datos a otra ubicación en la misma ventana o en otra ventana.

</dd> <dt>

<span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Insertar**
</dt> <dd>

Para insertar un objeto en un documento compuesto de manera que se conserven los formatos de datos nativos de ese objeto y para permitir que se edite desde dentro de su contenedor mediante las herramientas expuestas por su servidor.

</dd> <dt>

<span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**objeto incrustado**
</dt> <dd>

Objeto cuyos datos se almacenan en un documento compuesto, pero el objeto se ejecuta en el espacio de proceso de su servidor. El controlador de objetos predeterminado proporciona un suplente en el espacio de procesamiento de la aplicación contenedora para el objeto real.

</dd> <dt>

<span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**propiedad extendida**
</dt> <dd>

Propiedad en tiempo de ejecución, como la posición y el tamaño de un control, que un usuario consideraría expuesto por el control pero que el contenedor expone y administra.

</dd> <dt>

<span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**moniker de archivo**
</dt> <dd>

Moniker basado en una ruta de acceso en el sistema de archivos. Los monikers de archivo se pueden usar para identificar los objetos que se guardan en sus propios archivos. Un moniker de archivo es un objeto COM que admite la implementación proporcionada por el sistema de la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) para la clase de moniker de archivo.

</dd> <dt>

<span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**objeto Font**
</dt> <dd>

Objeto COM que proporciona acceso a las fuentes de Interfaz de dispositivo gráfico (GDI) implementando la interfaz [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .

</dd> <dt>

<span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**identificador de formato**
</dt> <dd>

GUID que identifica un conjunto de propiedades persistentes. También se conoce como FMTID.

</dd> <dt>

<span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**grama**
</dt> <dd>

Parte de una aplicación contenedora responsable de negociar menús, teclas de aceleración, barras de herramientas y otros elementos compartidos de la interfaz de usuario con un objeto COM incrustado o un objeto de documento.

</dd> <dt>

<span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**objeto Frame**
</dt> <dd>

Objeto COM que implementa la interfaz [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) y, opcionalmente, la interfaz [**IOLECommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) .

</dd> <dt>

<span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**moniker compuesto genérico**
</dt> <dd>

Colección secuenciada de monikers, que comienza con un moniker de archivo para proporcionar la ruta de acceso de nivel de documento y continuar con uno o más monikers de elemento que, tomadas en conjunto, identifica de forma única un objeto.

</dd> <dt>

<span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**función auxiliar**
</dt> <dd>

Función que encapsula llamadas a otras funciones y métodos de interfaz públicamente disponibles en el SDK de OLE. Las funciones auxiliares son una manera cómoda de llamar a secuencias de funciones y llamadas a métodos de uso frecuente que realizan tareas comunes.

</dd> <dt>

<span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**objeto host**
</dt> <dd>

Objeto COM que forma una relación jerárquica con uno o varios objetos COM, denominados objetos dependientes. Normalmente, el objeto host crea instancias de los objetos dependientes y su existencia solo tiene sentido dentro de la duración del objeto host. Sin embargo, el objeto host no actúa como el [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de control de los objetos dependientes, ni se delega directamente a las implementaciones de interfaz de esos objetos.

</dd> <dt>

<span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**VALOR**
</dt> <dd>

Un identificador de resultado opaco definido como cero para una devolución correcta de una función y un valor distinto de cero si se devuelve información de error o de estado.

</dd> <dt>

<span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**HYPERLINK (objeto)**
</dt> <dd>

Objeto COM que implementa, como mínimo, la interfaz [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) y actúa como un vínculo a un objeto en otra ubicación (el destino). Un hipervínculo se compone de cuatro partes: un moniker que identifica la ubicación del destino; una cadena para la ubicación dentro del destino; un nombre descriptivo, o que se pueda mostrar, para el destino; y una cadena que puede contener parámetros adicionales.

</dd> <dt>

<span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**contexto de exploración de hipervínculo**
</dt> <dd>

Objeto COM que implementa la interfaz [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) y mantiene la pila de navegación del hipervínculo. El objeto de contexto de exploración administra la ventana de marco de hipervínculo y la ventana del objeto de destino de hipervínculo.

</dd> <dt>

<span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**contenedor de hipervínculo**
</dt> <dd>

Una aplicación contenedora que admita hipervínculos implementando la interfaz [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) y, si los objetos del contenedor pueden ser destinos de otros hipervínculos, la interfaz [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) .

</dd> <dt>

<span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**HYPERLINK (objeto de marco)**
</dt> <dd>

Objeto COM que implementa la interfaz [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) y controla la navegación de nivel superior y la presentación de hipervínculos para el contenedor del marco y el servidor del destino del hipervínculo.

</dd> <dt>

<span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**objeto de sitio de hipervínculo**
</dt> <dd>

Objeto COM que implementa la interfaz [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) y proporciona el moniker o el identificador de interfaz de su contenedor de hipervínculos. Un sitio de hipervínculo puede servir varios hipervínculos.

</dd> <dt>

<span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**objeto de destino de hipervínculo**
</dt> <dd>

Objeto COM que implementa la interfaz [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) y proporciona el moniker, el nombre descriptivo y otra información que otros objetos de hipervínculo usarán para navegar hasta él.

</dd> <dt>

<span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in (parámetro)**
</dt> <dd>

Parámetro que el llamador de una función o un método de interfaz ha asignado, establecido y liberado. La función llamada no modifica un parámetro in.

</dd> <dt>

<span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**parámetro in/out**
</dt> <dd>

Un parámetro asignado inicialmente por el llamador de una función o un método de interfaz, y establecer, liberar y reasignar, si es necesario, por el proceso al que se llama.

</dd> <dt>

<span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**activación en contexto**
</dt> <dd>

Editar un objeto incrustado en la ventana de su contenedor mediante las herramientas proporcionadas por el servidor. Los objetos vinculados no admiten la activación en contexto; siempre se editan en la ventana del servidor.

</dd> <dt>

<span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**servidor en proceso**
</dt> <dd>

Servidor implementado como un archivo DLL que se ejecuta en el espacio de proceso del cliente.

</dd> <dt>

<span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**repetición**
</dt> <dd>

Objeto para el que se asigna memoria o que es persistente.

</dd> <dt>

<span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interfaz**
</dt> <dd>

Grupo de funciones relacionadas semánticamente que proporcionan acceso a un objeto COM. Cada interfaz OLE define un contrato que permite a los objetos interactuar según el modelo de objetos componentes (COM). Aunque OLE proporciona muchas implementaciones de interfaz, la mayoría de las interfaces también pueden ser implementadas por desarrolladores que diseñan aplicaciones OLE.

</dd> <dt>

<span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**identificador de interfaz (IID)**
</dt> <dd>

Identificador único global (GUID) asociado a una interfaz. Algunas funciones toman IID como parámetros para permitir que el llamador especifique el puntero de interfaz que se debe devolver.

</dd> <dt>

<span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**moniker de elemento**
</dt> <dd>

Moniker basado en una cadena que identifica un objeto en un contenedor. Los monikers de elemento pueden identificar objetos más pequeños que un archivo, incluidos los objetos incrustados en un documento compuesto o un pseudo objeto (como un rango de celdas de una hoja de cálculo).

</dd> <dt>

<span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licencias**
</dt> <dd>

Característica de COM que proporciona control sobre la creación de objetos. Los objetos con licencia solo los pueden crear los clientes que tienen autorización para usarlos. Las licencias se implementan en COM a través de la interfaz [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) y admiten una clave de licencia que se puede pasar en tiempo de ejecución.

</dd> <dt>

<span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**Link (objeto)**
</dt> <dd>

Objeto COM que se crea cuando se crea o se carga un objeto COM vinculado. OLE proporciona el objeto de vínculo e implementa la interfaz [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) .

</dd> <dt>

<span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**objeto vinculado**
</dt> <dd>

Objeto COM cuyos datos de origen residen físicamente donde se crearon inicialmente. Solo se mantiene en el documento compuesto un moniker que representa los datos de origen y los datos de presentación adecuados. Los cambios realizados en el origen del vínculo se reflejan automáticamente en el objeto vinculado.

</dd> <dt>

<span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**origen del vínculo**
</dt> <dd>

Los datos que son el origen de un objeto vinculado. Un origen de vínculo puede ser un archivo o una parte de un archivo, como un intervalo de celdas seleccionado dentro de un archivo (también denominado pseudo objeto).

</dd> <dt>

<span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**estado cargado**
</dt> <dd>

El estado de un objeto después de sus estructuras de datos se ha cargado en la memoria y es accesible para el proceso del cliente.

</dd> <dt>

<span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**servidor local**
</dt> <dd>

Un servidor fuera de proceso implementado como un. Aplicación EXE que se ejecuta en el mismo equipo que su aplicación cliente.

</dd> <dt>

<span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**bloquea**
</dt> <dd>

Un puntero se mantiene en y, posiblemente, un recuento de referencias incrementado en un objeto en ejecución. OLE define dos tipos de bloqueos que se pueden mantener en un objeto: strong y débil. Para implementar un bloqueo fuerte, un servidor debe mantener un puntero y un recuento de referencias, de modo que el objeto permanezca "bloqueado" en la memoria al menos hasta que el servidor llame a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Para implementar un bloqueo débil, el servidor mantiene solo un puntero al objeto, de modo que otro proceso pueda destruir el objeto.

</dd> <dt>

<span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**serialización**
</dt> <dd>

Empaquetado y envío de llamadas a métodos de interfaz a través de los límites de subprocesos o procesos.

</dd> <dt>

<span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**tipo de medio**
</dt> <dd>

Extensión de MIME que permite la negociación de formato de datos entre un cliente y un objeto.

</dd> <dt>

<span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**Tipo de contenido MIME**
</dt> <dd>

Extensión de MIME que permite la negociación de formato de datos entre un cliente y un objeto.

</dd> <dt>

<span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Extensión multipropósito de correo Internet (MIME)**
</dt> <dd>

Un protocolo de Internet desarrollado originalmente para permitir el intercambio de mensajes de correo electrónico con contenido enriquecido en entornos de red, equipos y correo electrónico heterogéneos. En la práctica, MIME también se ha adoptado y ampliado por aplicaciones que no son de correo.

</dd> <dt>

<span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**Nike**
</dt> <dd>

Objeto que implementa la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) . Un moniker actúa como un nombre que identifica de forma única un objeto COM. Del mismo modo que una ruta de acceso identifica un archivo en el sistema de archivos, un moniker identifica un objeto COM en el espacio de nombres de directorio.

</dd> <dt>

<span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker (clase)**
</dt> <dd>

Implementación de la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) . Entre las clases de moniker suministradas por el sistema se incluyen monikers de archivos, monikers, monikers compuestos genéricos, anti-monikers, monikers de puntero y monikers de dirección URL.

</dd> <dt>

<span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**cliente de moniker**
</dt> <dd>

Aplicación que usa monikers para adquirir punteros de interfaz a objetos administrados por otra aplicación.

</dd> <dt>

<span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**proveedor de moniker**
</dt> <dd>

Aplicación que pone a los monikers disponibles que identifican los objetos que administra, de modo que las demás aplicaciones puedan tener acceso a los objetos.

</dd> <dt>

<span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**extensión de espacio de nombres**
</dt> <dd>

Objeto COM en proceso que implementa [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)y [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), a veces denominados interfaces de extensión de espacio de nombres. Una extensión de espacio de nombres se utiliza para extender el espacio de nombres del shell o para crear un espacio de nombres independiente. Los usuarios primarios son el explorador de Windows y los cuadros de diálogo de archivos comunes.

</dd> <dt>

<span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**datos nativos**
</dt> <dd>

Datos utilizados por una aplicación de servidor OLE al editar un objeto incrustado.

</dd> <dt>

<span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**objeto**
</dt> <dd>

En OLE, estructura de programación que encapsula los datos y la funcionalidad definidos y asignados como una sola unidad y para los que el único acceso público se realiza a través de las interfaces de la estructura de programación. Un objeto COM debe admitir, como mínimo, la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , que mantiene la existencia del objeto mientras se usa y proporciona acceso a las demás interfaces del objeto.

</dd> <dt>

<span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**Estado del objeto** 
</dt> <dd>

La relación entre un objeto de documento compuesto en su contenedor y la aplicación responsable de la creación del objeto: activo, pasivo, cargado o en ejecución. Los objetos pasivos se almacenan en el disco o en una base de datos, y el objeto no está seleccionado o activo. En el estado Loaded, las estructuras de datos del objeto se han cargado en la memoria, pero no están disponibles para operaciones como la edición. Los objetos en ejecución se cargan y están disponibles para todas las operaciones. Los objetos activos ejecutan objetos que tienen una interfaz de usuario visible.

</dd> <dt>

<span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**nombre del tipo de objeto**
</dt> <dd>

Cadena de identificación única que se almacena como parte de la información disponible para un objeto en la base de datos de registro.

</dd> <dt>

<span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OLE**
</dt> <dd>

Tecnología basada en objetos de Microsoft para compartir información y servicios a través de límites de equipos y procesos.

</dd> <dt>

<span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**servidor fuera de proceso**
</dt> <dd>

Un servidor de, implementado como un. Aplicación EXE, que se ejecuta fuera del proceso de su cliente, ya sea en el mismo equipo o en un equipo remoto.

</dd> <dt>

<span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out (parámetro)**
</dt> <dd>

Un parámetro out se asigna mediante la función a la que se llama y se libera por el autor de la llamada.

</dd> <dt>

<span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**estado pasivo**
</dt> <dd>

El estado de un objeto COM cuando se almacena (en disco o en una base de datos). El objeto no está seleccionado o activo.

</dd> <dt>

<span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**propiedad Persistent**
</dt> <dd>

Información que se puede almacenar de forma persistente como parte de un objeto de almacenamiento, como un archivo o un directorio. Las propiedades persistentes se agrupan en conjuntos de propiedades, que se pueden mostrar y editar.

Una propiedad persistente es diferente de las propiedades en tiempo de ejecución de los objetos creados con controles OLE y tecnologías de automatización, que se pueden usar para afectar al comportamiento del sistema. La estructura [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) define todos los tipos válidos de propiedades persistentes, mientras que la estructura **Variant** define todos los tipos válidos de propiedades en tiempo de ejecución.

</dd> <dt>

<span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**almacenamiento persistente**
</dt> <dd>

Almacenamiento de un archivo o un objeto en un medio, como un sistema de archivos o una base de datos, para que el objeto y sus datos se conserven cuando el archivo se cierre y se vuelva a abrir en otro momento.

</dd> <dt>

<span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**objeto de imagen**
</dt> <dd>

Objeto COM que proporciona acceso a las imágenes de GDI implementando la interfaz [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .

</dd> <dt>

<span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**moniker de puntero**
</dt> <dd>

Moniker que asigna un puntero de interfaz a un objeto en memoria. Mientras que la mayoría de los monikers identifican objetos que se pueden almacenar de forma persistente, los monikers de puntero identifican los objetos que no pueden. Permiten que estos objetos participen en una operación de enlace de moniker.

</dd> <dt>

<span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**datos de presentación**
</dt> <dd>

Los datos que usa un contenedor para mostrar objetos incrustados o vinculados.

</dd> <dt>

<span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**verbo principal**
</dt> <dd>

Acción asociada a la operación más común o preferida que realizan los usuarios en un objeto. El verbo principal siempre se define como verbo cero en la base de datos de registro del sistema. El verbo principal de un objeto se ejecuta haciendo doble clic en el objeto.

</dd> <dt>

<span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**propiedad**
</dt> <dd>

Información asociada a un objeto. En OLE, las propiedades se dividen en dos categorías: propiedades de tiempo de ejecución y propiedades persistentes. Las propiedades de tiempo de ejecución están asociadas normalmente a objetos de control o a sus contenedores. Por ejemplo, el color de fondo es una propiedad en tiempo de ejecución establecida por el contenedor de un control. Las propiedades persistentes están asociadas a objetos almacenados.

</dd> <dt>

<span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**marco de propiedades**
</dt> <dd>

Mecanismo de la interfaz de usuario que muestra una o varias páginas de propiedades de un control. El sistema en tiempo de ejecución de controles OLE proporciona una implementación estándar de un marco de propiedades al que se puede tener acceso mediante la función auxiliar [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) .

</dd> <dt>

<span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**identificador de propiedad**
</dt> <dd>

Entero con signo de cuatro bytes que identifica una propiedad persistente dentro de un conjunto de propiedades.

</dd> <dt>

<span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**Página de propiedades**
</dt> <dd>

Objeto COM con su propio CLSID que forma parte de una interfaz de usuario, implementada por un control, y permite ver y establecer las propiedades del control. Los objetos de la página de propiedades implementan la interfaz [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) .

</dd> <dt>

<span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**sitio de la página de propiedades**
</dt> <dd>

Ubicación dentro de un marco de propiedades donde se muestra una página de propiedades. El marco de propiedades implementa la interfaz [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) , que contiene métodos para administrar los sitios de cada una de las páginas de propiedades proporcionadas por un control.

</dd> <dt>

<span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**conjunto de propiedades**
</dt> <dd>

Un grupo de propiedades relacionadas lógicamente que está asociado a un objeto almacenado de forma persistente. Para crear, abrir, eliminar o enumerar uno o más conjuntos de propiedades, implemente la interfaz [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) . Si usa archivos compuestos, puede usar la implementación de OLE de esta interfaz en lugar de implementar la suya propia.

</dd> <dt>

<span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**almacenamiento del conjunto de propiedades**
</dt> <dd>

Objeto de almacenamiento COM que contiene un conjunto de propiedades. Un almacenamiento de conjunto de propiedades es un objeto dependiente asociado y administrado por un objeto de almacenamiento.

</dd> <dt>

<span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**hoja de propiedades**
</dt> <dd>

Un conjunto de páginas de propiedades para uno o más objetos.

</dd> <dt>

<span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**proxi**
</dt> <dd>

Objeto específico de la interfaz que empaqueta los parámetros de esa interfaz como preparación para una llamada de método remoto. Un proxy se ejecuta en el espacio de direcciones del remitente y se comunica con el código auxiliar correspondiente en el espacio de direcciones del receptor.

</dd> <dt>

<span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**Administrador de proxy**
</dt> <dd>

En el cálculo de referencias estándar, proxy que administra todos los proxies de interfaz para un solo objeto.

</dd> <dt>

<span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo (objeto)**
</dt> <dd>

Parte de un documento o un objeto incrustado, como un rango de celdas de una hoja de cálculo, que puede ser el origen de un objeto COM.

</dd> <dt>

<span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**recuento de referencias**
</dt> <dd>

Mantener un recuento de cada puntero de interfaz mantenido en un objeto para asegurarse de que no se destruye el objeto antes de que se liberen todas las referencias a él.

</dd> <dt>

<span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**moniker relativo**
</dt> <dd>

Moniker que especifica la ubicación de un objeto en relación con la ubicación de otro objeto. Un moniker relativo es análogo a una ruta de acceso relativa, como. \\ Informe de copia de seguridad \\ . old.

</dd> <dt>

<span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**servidor remoto**
</dt> <dd>

Aplicación de servidor, implementada como un archivo EXE, que se ejecuta en un equipo diferente de la aplicación cliente que la utiliza.

</dd> <dt>

<span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**revertir**
</dt> <dd>

Para descartar los cambios realizados en un objeto desde la última vez que se confirmaron los cambios o se abrió el almacenamiento del objeto.

</dd> <dt>

<span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**objeto de almacenamiento raíz**
</dt> <dd>

Objeto de almacenamiento más externo de un documento. Un objeto de almacenamiento raíz puede contener otros objetos de flujo y almacenamiento anidado. Por ejemplo, un documento compuesto se guarda en el disco como una serie de objetos de almacenamiento y de secuencia dentro de un objeto de almacenamiento raíz.

</dd> <dt>

<span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**Estado de ejecución**
</dt> <dd>

El estado de un objeto COM cuando su aplicación de servidor se está ejecutando y es posible tener acceso a sus interfaces y recibir notificaciones de cambios.

</dd> <dt>

<span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**tabla de objetos en ejecución (ROT)**
</dt> <dd>

Una tabla accesible globalmente en cada equipo que realiza un seguimiento de todos los objetos COM en el estado de ejecución que pueden identificarse mediante un moniker. Los proveedores de moniker registran un objeto en la tabla, lo que incrementa el recuento de referencias del objeto. Antes de que se pueda destruir el objeto, su moniker debe liberarse de la tabla.

</dd> <dt>

<span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**propiedad en tiempo de ejecución**
</dt> <dd>

Información de estado discreto asociada a un objeto de control o a su contenedor. Hay tres tipos de propiedades de tiempo de ejecución: propiedades de ambiente, propiedades de control y propiedades extendidas.

</dd> <dt>

<span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**registro automático**
</dt> <dd>

Proceso por el que un servidor puede realizar sus propias operaciones del registro.

</dd> <dt>

<span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**aplicación de servidor**
</dt> <dd>

Aplicación que puede crear objetos COM. Después, las aplicaciones contenedoras pueden incrustar o vincular estos objetos.

</dd> <dt>

<span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**Static (objeto)**
</dt> <dd>

Objeto que contiene solo una presentación, sin datos nativos. Un contenedor puede tratar un objeto estático como si fuera un objeto vinculado o incrustado, con la excepción de que no es posible editar un objeto estático.

Un objeto estático puede producir, por ejemplo, una interrupción de un vínculo en un objeto vinculado; es decir, la aplicación de servidor no está disponible o el usuario no desea que el objeto vinculado se actualice ya.

</dd> <dt>

<span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**objeto de almacenamiento**
</dt> <dd>

Objeto COM que implementa la interfaz [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) . Un objeto de almacenamiento contiene objetos de almacenamiento anidados u objetos de secuencia, lo que da lugar al equivalente de una estructura de directorio/archivo dentro de un único archivo.

</dd> <dt>

<span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**Stream (objeto)**
</dt> <dd>

Objeto COM que implementa la interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) . Un objeto de secuencia es análogo a un archivo en un sistema de archivos o directorios.

</dd> <dt>

<span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Almacenamiento estructurado**
</dt> <dd>

Tecnología de OLE para almacenar archivos compuestos en sistemas de archivos nativos.

</dd> <dt>

<span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**agrupa**
</dt> <dd>

Cuando se calculan las referencias de los parámetros de un método de interfaz o de una función a través de un límite de proceso, el código auxiliar es un objeto específico de la interfaz que desempaqueta los parámetros de cálculo de referencias y llama al método requerido. El código auxiliar se ejecuta en el espacio de direcciones del receptor y se comunica con el proxy correspondiente en el espacio de direcciones del remitente.

</dd> <dt>

<span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**Administrador de código auxiliar**
</dt> <dd>

Administra todos los códigos auxiliares de interfaz para un solo objeto.

</dd> <dt>

<span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**llamada sincrónica**
</dt> <dd>

Una llamada de función que no permite ejecutar más instrucciones en el proceso de llamada hasta que la función devuelve.

</dd> <dt>

<span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**registro del sistema**
</dt> <dd>

Repositorio de información de todo el sistema compatible con Windows que contiene información sobre el sistema y sus aplicaciones, incluidos los clientes y servidores OLE.

</dd> <dt>

<span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**modo de acceso de transacción**
</dt> <dd>

Uno de los dos modos de acceso en los que se puede abrir un objeto de almacenamiento. Cuando se abre en modo de transacción, los cambios se almacenan en búferes hasta que el objeto de almacenamiento raíz confirma los cambios.

</dd> <dt>

<span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**información de tipo**
</dt> <dd>

Información sobre la clase de un objeto que proporciona una biblioteca de tipos. Para proporcionar información de tipo, un objeto COM implementa la interfaz [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .

</dd> <dt>

<span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**transferencia de datos uniforme**
</dt> <dd>

Modelo para transferir datos a través del portapapeles, arrastrar y colocar, o automatización. Los objetos que se ajustan a este modelo implementan la interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . Este modelo reemplaza a DDE (intercambio dinámico de datos).

</dd> <dt>

<span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**resolución**
</dt> <dd>

Desempaquetar los parámetros que se han enviado a un proxy a través de los límites del proceso.

</dd> <dt>

<span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**Localizador de recursos universal (URL)**
</dt> <dd>

El identificador utilizado por el World Wide Web para los nombres y las ubicaciones de los objetos en Internet. OLE proporciona una clase moniker, moniker de dirección URL, cuya implementación se puede usar para enlazar un cliente a objetos identificados por una dirección URL.

</dd> <dt>

<span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**Moniker de dirección URL**
</dt> <dd>

Moniker basado en un localizador de recursos universal (URL). Un cliente puede usar monikers de dirección URL para enlazar a objetos que residen en Internet. La clase de moniker de dirección URL proporcionada por el sistema admite enlaces sincrónicos y asincrónicos.

</dd> </dl>

 

 