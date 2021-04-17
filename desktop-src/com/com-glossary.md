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
# <a name="com-glossary"></a><span data-ttu-id="21f9a-103">Glosario de COM</span><span class="sxs-lookup"><span data-stu-id="21f9a-103">COM Glossary</span></span>

<dl> <dt>

<span data-ttu-id="21f9a-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**activación**</span><span class="sxs-lookup"><span data-stu-id="21f9a-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-105">Proceso de carga de un objeto en la memoria, que lo pone en el estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="21f9a-105">The process of loading an object in memory, which puts it into the running state.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**estado activo**</span><span class="sxs-lookup"><span data-stu-id="21f9a-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**active state**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-107">Un objeto COM que se encuentra en estado de ejecución y tiene una interfaz de usuario visible.</span><span class="sxs-lookup"><span data-stu-id="21f9a-107">A COM object that is in the running state and has a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**moniker absoluto**</span><span class="sxs-lookup"><span data-stu-id="21f9a-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**absolute moniker**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-109">Moniker que especifica la ubicación absoluta de un objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-109">A moniker that specifies the absolute location of an object.</span></span> <span data-ttu-id="21f9a-110">Un moniker absoluto es análogo a una ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="21f9a-110">An absolute moniker is analogous to a full path.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**titular de asesoría**</span><span class="sxs-lookup"><span data-stu-id="21f9a-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**advisory holder**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-112">Objeto COM que almacena en caché, administra y envía notificaciones de cambios en los receptores de consulta de aplicaciones de contenedor.</span><span class="sxs-lookup"><span data-stu-id="21f9a-112">A COM object that caches, manages, and sends notifications of changes to container applications' advisory sinks.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**receptor de consulta**</span><span class="sxs-lookup"><span data-stu-id="21f9a-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**advisory sink**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-114">Objeto COM que puede recibir notificaciones de cambios en un objeto incrustado o vinculado porque implementa la interfaz [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) o [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-114">A COM object that can receive notifications of changes in an embedded object or linked object because it implements the [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) or [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) interface.</span></span> <span data-ttu-id="21f9a-115">Los contenedores a los que se debe notificar los cambios en los objetos de implementan un receptor de consulta.</span><span class="sxs-lookup"><span data-stu-id="21f9a-115">Containers that need to be notified of changes in objects implement an advisory sink.</span></span> <span data-ttu-id="21f9a-116">Las notificaciones se originan en el servidor, que utiliza un objeto de titular de consulta para almacenar en memoria caché y administrar las notificaciones de los contenedores.</span><span class="sxs-lookup"><span data-stu-id="21f9a-116">Notifications originate in the server, which uses an advisory holder object to cache and manage notifications to containers.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**Aggregate (objeto)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**aggregate object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-118">Objeto COM que se compone de uno o varios objetos COM.</span><span class="sxs-lookup"><span data-stu-id="21f9a-118">A COM object that is made up of one or more other COM objects.</span></span> <span data-ttu-id="21f9a-119">Un objeto del agregado se designa como objeto de control, que controla qué interfaces del agregado se exponen y cuáles son privadas.</span><span class="sxs-lookup"><span data-stu-id="21f9a-119">One object in the aggregate is designated the controlling object, which controls which interfaces in the aggregate are exposed and which are private.</span></span> <span data-ttu-id="21f9a-120">Este objeto de control tiene una implementación especial de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) denominada **IUnknown** de control.</span><span class="sxs-lookup"><span data-stu-id="21f9a-120">This controlling object has a special implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) called the controlling **IUnknown**.</span></span> <span data-ttu-id="21f9a-121">Todos los objetos del agregado deben pasar llamadas a métodos **IUnknown** a través del **IUnknown** de control.</span><span class="sxs-lookup"><span data-stu-id="21f9a-121">All objects in the aggregate must pass calls to **IUnknown** methods through the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**concentrado**</span><span class="sxs-lookup"><span data-stu-id="21f9a-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-123">Técnica de composición para implementar objetos COM.</span><span class="sxs-lookup"><span data-stu-id="21f9a-123">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="21f9a-124">Permite crear un nuevo objeto mediante la reutilización de una o más implementaciones de interfaz de objetos existentes.</span><span class="sxs-lookup"><span data-stu-id="21f9a-124">It allows you to build a new object by reusing one or more existing objects' interface implementations.</span></span> <span data-ttu-id="21f9a-125">El objeto agregado elige las interfaces que se van a exponer a los clientes, y las interfaces se exponen como si fueran implementadas por el objeto agregado.</span><span class="sxs-lookup"><span data-stu-id="21f9a-125">The aggregate object chooses which interfaces to expose to clients, and the interfaces are exposed as if they were implemented by the aggregate object.</span></span> <span data-ttu-id="21f9a-126">Los clientes del objeto agregado solo se comunican con el objeto agregado.</span><span class="sxs-lookup"><span data-stu-id="21f9a-126">Clients of the aggregate object communicate only with the aggregate object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**propiedad Ambient**</span><span class="sxs-lookup"><span data-stu-id="21f9a-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**ambient property**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-128">Propiedad en tiempo de ejecución administrada y expuesta por el contenedor.</span><span class="sxs-lookup"><span data-stu-id="21f9a-128">A run-time property that is managed and exposed by the container.</span></span> <span data-ttu-id="21f9a-129">Normalmente, una propiedad de ambiente representa una característica de un formulario, como el color de fondo, que debe comunicarse con un control para que el control pueda asumir la apariencia y el funcionamiento de su entorno circundante.</span><span class="sxs-lookup"><span data-stu-id="21f9a-129">Typically, an ambient property represents a characteristic of a form, such as background color, that needs to be communicated to a control so that the control can assume the look and feel of its surrounding environment.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**</span><span class="sxs-lookup"><span data-stu-id="21f9a-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-131">El inverso de un moniker de archivo, elemento o puntero.</span><span class="sxs-lookup"><span data-stu-id="21f9a-131">The inverse of a file, item, or pointer moniker.</span></span> <span data-ttu-id="21f9a-132">Se agrega un anti-moniker al final de un archivo, elemento o moniker de puntero para anularlo.</span><span class="sxs-lookup"><span data-stu-id="21f9a-132">An anti-moniker is added to the end of a file, item, or pointer moniker to nullify it.</span></span> <span data-ttu-id="21f9a-133">Los anti-monikers se usan en la construcción de monikers relativos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-133">Anti-monikers are used in the construction of relative monikers.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**recuento de referencias artificiales**</span><span class="sxs-lookup"><span data-stu-id="21f9a-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**artificial reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-135">Técnica que se usa para ayudar a proteger un objeto antes de llamar a una función o un método que podría destruirlo prematuramente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-135">A technique used to help protect an object before calling a function or method that could prematurely destroy it.</span></span> <span data-ttu-id="21f9a-136">Un programa llama a **IUnknown:: AddRef** para incrementar el recuento de referencias del objeto antes de realizar la llamada que podría liberar el objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-136">A program calls **IUnknown::AddRef** to increment the object's reference count before making the call that could free the object.</span></span> <span data-ttu-id="21f9a-137">Una vez que la función devuelve, el programa llama a **IUnknown:: Release** para reducir el recuento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-137">After the function returns, the program calls **IUnknown::Release** to decrement the count.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**enlace asincrónico**</span><span class="sxs-lookup"><span data-stu-id="21f9a-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**asynchronous binding**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-139">Tipo de enlace en el que es necesario que el proceso se produzca de forma asincrónica para evitar la degradación del rendimiento del usuario final.</span><span class="sxs-lookup"><span data-stu-id="21f9a-139">A type of binding in which it is necessary for the process to occur asynchronously to avoid performance degradation for the end user.</span></span> <span data-ttu-id="21f9a-140">Normalmente, el enlace asincrónico se usa en entornos distribuidos como el World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="21f9a-140">Typically, asynchronous binding is used in distributed environments such as the World Wide Web.</span></span> <span data-ttu-id="21f9a-141">OLE admite clases de moniker asincrónico y mecanismos de devolución de llamada que permiten que se produzca el proceso de búsqueda e inicialización de un objeto en un entorno distribuido mientras se llevan a cabo otras operaciones.</span><span class="sxs-lookup"><span data-stu-id="21f9a-141">OLE supports asynchronous moniker classes and callback mechanisms that allow the process of locating and initializing an object in a distributed environment to occur while other operations are being carried out.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**llamada asincrónica**</span><span class="sxs-lookup"><span data-stu-id="21f9a-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**asynchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-143">Una llamada a una función que se ejecuta por separado para que el llamador pueda seguir procesando instrucciones sin esperar a que la función devuelva.</span><span class="sxs-lookup"><span data-stu-id="21f9a-143">A call to a function that is executed separately so that the caller can continue processing instructions without waiting for the function to return.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**moniker asincrónico**</span><span class="sxs-lookup"><span data-stu-id="21f9a-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**asynchronous moniker**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-145">Moniker que admite el enlace asincrónico.</span><span class="sxs-lookup"><span data-stu-id="21f9a-145">A moniker that supports asynchronous binding.</span></span> <span data-ttu-id="21f9a-146">Por ejemplo, las instancias de la clase de moniker de dirección URL proporcionada por el sistema son monikers asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-146">For example, instances of the system-supplied URL moniker class are asynchronous monikers.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**automatiza**</span><span class="sxs-lookup"><span data-stu-id="21f9a-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**automation**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-148">Una manera de manipular los objetos de una aplicación desde fuera de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="21f9a-148">A way to manipulate an application's objects from outside the application.</span></span> <span data-ttu-id="21f9a-149">La automatización se usa normalmente para crear aplicaciones que exponen objetos a herramientas de programación y lenguajes de macros, crear y manipular objetos de una aplicación desde otras aplicaciones o crear herramientas para tener acceso a los objetos y manipularlos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-149">Automation is typically used to create applications that expose objects to programming tools and macro languages, create and manipulate one application's objects from another applications, or to create tools for accessing and manipulating objects.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**contexto de enlace**</span><span class="sxs-lookup"><span data-stu-id="21f9a-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**bind context**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-151">Objeto COM que implementa la interfaz [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-151">A COM object that implements the [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="21f9a-152">Los contextos de enlace se utilizan en las operaciones de moniker para conservar las referencias a los objetos activados cuando se enlaza un moniker.</span><span class="sxs-lookup"><span data-stu-id="21f9a-152">Bind contexts are used in moniker operations to hold references to the objects activated when a moniker is bound.</span></span> <span data-ttu-id="21f9a-153">El contexto de enlace contiene parámetros que se aplican a todas las operaciones durante el enlace de un moniker compuesto genérico y proporciona la implementación de moniker con acceso a información sobre su entorno.</span><span class="sxs-lookup"><span data-stu-id="21f9a-153">The bind context contains parameters that apply to all operations during the binding of a generic composite moniker and provides the moniker implementation with access to information about its environment.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**enlace**</span><span class="sxs-lookup"><span data-stu-id="21f9a-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-155">Asociar un nombre a su correspondiente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-155">Associating a name with its referent.</span></span> <span data-ttu-id="21f9a-156">En concreto, para localizar el objeto denominado por un moniker, ponerlo en su estado de ejecución, si aún no lo está, y devolver un puntero de interfaz a él.</span><span class="sxs-lookup"><span data-stu-id="21f9a-156">Specifically, locating the object named by a moniker, putting it into its running state if it isn't already, and returning an interface pointer to it.</span></span> <span data-ttu-id="21f9a-157">Los objetos se pueden enlazar en tiempo de ejecución (también denominado enlace tardío o enlace dinámico) o en tiempo de compilación (también denominado enlace estático).</span><span class="sxs-lookup"><span data-stu-id="21f9a-157">Objects can be bound at run time (also called late binding or dynamic binding) or at compile time (also called static binding).</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**almacenar**</span><span class="sxs-lookup"><span data-stu-id="21f9a-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**cache**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-159">Un almacén local (normalmente temporal) de información.</span><span class="sxs-lookup"><span data-stu-id="21f9a-159">A (usually temporary) local store of information.</span></span> <span data-ttu-id="21f9a-160">En OLE, una memoria caché contiene información que define la presentación de un objeto vinculado o incrustado cuando se abre el contenedor.</span><span class="sxs-lookup"><span data-stu-id="21f9a-160">In OLE, a cache contains information that defines the presentation of a linked or embedded object when the container is opened.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**inicialización de caché**</span><span class="sxs-lookup"><span data-stu-id="21f9a-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**cache initialization**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-162">Rellenar la caché de un objeto vinculado o incrustado con datos de presentación.</span><span class="sxs-lookup"><span data-stu-id="21f9a-162">Filling a linked or embedded object's cache with presentation data.</span></span> <span data-ttu-id="21f9a-163">La interfaz [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) proporciona métodos a los que puede llamar un contenedor para controlar los datos que se almacenan en caché para objetos vinculados o incrustados.</span><span class="sxs-lookup"><span data-stu-id="21f9a-163">The [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) interface provides methods that a container can call to control the data that gets cached for linked or embedded objects.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**las**</span><span class="sxs-lookup"><span data-stu-id="21f9a-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**class**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-165">Definición de un objeto en el código.</span><span class="sxs-lookup"><span data-stu-id="21f9a-165">The definition of an object in code.</span></span> <span data-ttu-id="21f9a-166">En C++, la clase de un objeto se define como un tipo de datos, pero este no es el caso en otros lenguajes.</span><span class="sxs-lookup"><span data-stu-id="21f9a-166">In C++, the class of an object is defined as a data type, but this is not the case in other languages.</span></span> <span data-ttu-id="21f9a-167">Dado que OLE se puede codificar en cualquier lenguaje, la clase se utiliza para hacer referencia a la definición de objeto general.</span><span class="sxs-lookup"><span data-stu-id="21f9a-167">Because OLE can be coded in any language, class is used to refer to the general object definition.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**generador de clases**</span><span class="sxs-lookup"><span data-stu-id="21f9a-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**class factory**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-169">Objeto COM que implementa la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) y que crea una o varias instancias de un objeto identificado por un identificador de clase (CLSID) determinado.</span><span class="sxs-lookup"><span data-stu-id="21f9a-169">A COM object that implements the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface and that creates one or more instances of an object identified by a given class identifier(CLSID).</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**identificador de clase (CLSID)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**class identifier (CLSID)**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-171">Identificador único global (GUID) asociado a un objeto de clase OLE.</span><span class="sxs-lookup"><span data-stu-id="21f9a-171">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="21f9a-172">Si un objeto de clase se va a utilizar para crear más de una instancia de un objeto, la aplicación de servidor asociada debe registrar su CLSID en el registro del sistema para que los clientes puedan buscar y cargar el código ejecutable asociado a los objetos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-172">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="21f9a-173">Cada servidor o contenedor OLE que permite vincular a sus objetos incrustados debe registrar un CLSID para cada definición de objeto compatible.</span><span class="sxs-lookup"><span data-stu-id="21f9a-173">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**objeto de clase**</span><span class="sxs-lookup"><span data-stu-id="21f9a-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**class object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-175">En la programación orientada a objetos, objeto cuyo estado comparten todos los objetos de una clase y cuyo comportamiento actúa en los datos de estado classwide.</span><span class="sxs-lookup"><span data-stu-id="21f9a-175">In object-oriented programming, an object whose state is shared by all the objects in a class and whose behavior acts on that classwide state data.</span></span> <span data-ttu-id="21f9a-176">En COM, los objetos de clase se denominan generadores de clase y, por lo general, no tienen ningún comportamiento excepto para crear nuevas instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="21f9a-176">In COM, class objects are called class factories, and typically have no behavior except to create new instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**Nº**</span><span class="sxs-lookup"><span data-stu-id="21f9a-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**client**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-178">Objeto COM que solicita servicios de otro objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-178">A COM object that requests services from another object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**sitio de cliente**</span><span class="sxs-lookup"><span data-stu-id="21f9a-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**client site**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-180">El sitio de presentación de un objeto incrustado o vinculado dentro de un documento compuesto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-180">The display site for an embedded or linked object within a compound document.</span></span> <span data-ttu-id="21f9a-181">El sitio del cliente es el medio principal por el que un objeto solicita servicios de su contenedor.</span><span class="sxs-lookup"><span data-stu-id="21f9a-181">The client site is the principal means by which an object requests services from its container.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**</span><span class="sxs-lookup"><span data-stu-id="21f9a-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-183">Identificador único global (GUID) asociado a un objeto de clase OLE.</span><span class="sxs-lookup"><span data-stu-id="21f9a-183">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="21f9a-184">Si un objeto de clase se va a utilizar para crear más de una instancia de un objeto, la aplicación de servidor asociada debe registrar su CLSID en el registro del sistema para que los clientes puedan buscar y cargar el código ejecutable asociado a los objetos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-184">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="21f9a-185">Cada servidor o contenedor OLE que permite vincular a sus objetos incrustados debe registrar un CLSID para cada definición de objeto compatible.</span><span class="sxs-lookup"><span data-stu-id="21f9a-185">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**promete**</span><span class="sxs-lookup"><span data-stu-id="21f9a-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-187">Para guardar de forma persistente cualquier cambio realizado en un objeto de almacenamiento o de flujo desde que se abrió o se guardaron los cambios por última vez.</span><span class="sxs-lookup"><span data-stu-id="21f9a-187">To persistently save any changes made to a storage or stream object since it was opened or changes were last saved.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**pone**</span><span class="sxs-lookup"><span data-stu-id="21f9a-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-189">Objeto que encapsula los datos y el código, y proporciona un conjunto bien especificado de servicios disponibles públicamente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-189">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Modelo de objetos componentes (COM)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-191">Modelo de programación orientado a objetos OLE que define cómo interactúan los objetos dentro de un proceso único o entre procesos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-191">The OLE object-oriented programming model that defines how objects interact within a single process or between processes.</span></span> <span data-ttu-id="21f9a-192">En COM, los clientes tienen acceso a un objeto a través de las interfaces implementadas en el objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-192">In COM, clients have access to an object through interfaces implemented on the object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**barra de menús compuesta**</span><span class="sxs-lookup"><span data-stu-id="21f9a-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**composite menu bar**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-194">Barra de menús compartida formada por grupos de menús de una aplicación contenedora y una aplicación de servidor activa en contexto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-194">A shared menu bar composed of menu groups from both a container application and an in-place-activated server application.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**moniker compuesto**</span><span class="sxs-lookup"><span data-stu-id="21f9a-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-196">Moniker que se compone de dos o más monikers que se tratan como una unidad.</span><span class="sxs-lookup"><span data-stu-id="21f9a-196">A moniker that consists of two or more monikers that are treated as a unit.</span></span> <span data-ttu-id="21f9a-197">Un moniker compuesto puede ser no genérico, lo que significa que sus monikers de componente tienen un conocimiento especial entre sí, o genérico, lo que significa que sus monikers de componente no saben nada sobre sí, salvo que son monikers.</span><span class="sxs-lookup"><span data-stu-id="21f9a-197">A composite moniker can be non-generic, meaning that its component monikers have special knowledge of each other, or generic, meaning that its component monikers know nothing about each other except that they are monikers</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**documento compuesto**</span><span class="sxs-lookup"><span data-stu-id="21f9a-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**compound document**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-199">Documento que incluye objetos vinculados o incrustados, así como sus propios datos nativos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-199">A document that includes linked or embedded objects, as well as its own native data.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**archivo compuesto**</span><span class="sxs-lookup"><span data-stu-id="21f9a-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**compound file**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-201">Una implementación de almacenamiento estructurado proporcionada por OLE.</span><span class="sxs-lookup"><span data-stu-id="21f9a-201">An OLE-provided Structured Storage implementation.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**Objeto COM**</span><span class="sxs-lookup"><span data-stu-id="21f9a-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-203">Objeto que se ajusta al modelo de objetos componentes (COM) de OLE.</span><span class="sxs-lookup"><span data-stu-id="21f9a-203">An object that conforms to the OLE Component Object Model (COM).</span></span> <span data-ttu-id="21f9a-204">Un objeto COM es una instancia de una definición de objeto, que especifica los datos del objeto y una o varias implementaciones de interfaces en el objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-204">A COM object is an instance of an object definition, which specifies the object's data and one or more implementations of interfaces on the object.</span></span> <span data-ttu-id="21f9a-205">Los clientes interactúan con un objeto COM solo a través de sus interfaces.</span><span class="sxs-lookup"><span data-stu-id="21f9a-205">Clients interact with a COM object only through its interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**objeto conectable**</span><span class="sxs-lookup"><span data-stu-id="21f9a-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**connectable object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-207">Objeto COM que implementa, como mínimo, la interfaz [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) para la administración de objetos de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="21f9a-207">A COM object that implements, at a minimum, the [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) interface, for the management of connection point objects.</span></span> <span data-ttu-id="21f9a-208">Los objetos conectables admiten la comunicación desde el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-208">Connectable objects support communication from the server to the client.</span></span> <span data-ttu-id="21f9a-209">Un objeto conectable crea y administra uno o varios subobjetos de punto de conexión, que reciben eventos de interfaces implementadas en otros objetos y los envían al cliente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-209">A connectable object creates and manages one or more connection point subobjects, which receive events from interfaces implemented on other objects and send them on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**objeto de punto de conexión**</span><span class="sxs-lookup"><span data-stu-id="21f9a-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**connection point object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-211">Objeto COM que se administra mediante un objeto conectable y que implementa la interfaz [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-211">A COM object that is managed by a connectable object and that implements the [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) interface.</span></span> <span data-ttu-id="21f9a-212">Uno o varios objetos de punto de conexión se pueden crear y administrar mediante un objeto conectable.</span><span class="sxs-lookup"><span data-stu-id="21f9a-212">One or more connection point objects can be created and managed by a connectable object.</span></span> <span data-ttu-id="21f9a-213">Cada objeto de punto de conexión administra los eventos entrantes de una interfaz específica en otro objeto y envía los eventos al cliente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-213">Each connection point object manages incoming events from a specific interface on another object and sends those events on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**aplicación contenedora**</span><span class="sxs-lookup"><span data-stu-id="21f9a-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**container application**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-215">Aplicación que admite documentos compuestos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-215">An application that supports compound documents.</span></span> <span data-ttu-id="21f9a-216">La aplicación contenedora proporciona almacenamiento para un objeto incrustado o vinculado, un sitio para su presentación, acceso al sitio para mostrar y un receptor de consulta para recibir notificaciones de cambios en el objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-216">The container application provides storage for an embedded or linked object, a site for its display, access to the display site, and an advisory sink for receiving notifications of changes in the object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**contención**</span><span class="sxs-lookup"><span data-stu-id="21f9a-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**containment**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-218">Técnica de composición para implementar objetos COM.</span><span class="sxs-lookup"><span data-stu-id="21f9a-218">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="21f9a-219">Permite que un objeto reutilice algunas o todas las implementaciones de interfaz de uno o más objetos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-219">It allows one object to reuse some or all of the interface implementations of one or more other objects.</span></span> <span data-ttu-id="21f9a-220">El objeto externo actúa como cliente de los demás objetos, delegando la implementación cuando desea utilizar los servicios de uno de los objetos contenidos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-220">The outer object acts as a client to the other objects, delegating implementation when it wishes to use the services of one of the contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**contexto**</span><span class="sxs-lookup"><span data-stu-id="21f9a-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-222">En COM+, conjunto de propiedades de tiempo de ejecución asociadas a uno o varios objetos COM que se usan para proporcionar servicios para esos objetos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-222">In COM+, a set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**control**</span><span class="sxs-lookup"><span data-stu-id="21f9a-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**control**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-224">Objeto COM que se puede incrustar y reutilizar que admite, como mínimo, la interfaz [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-224">An embeddable, reusable COM object that supports, at a minimum, the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) interface.</span></span> <span data-ttu-id="21f9a-225">Normalmente, los controles se asocian a la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="21f9a-225">Controls are typically associated with the user interface.</span></span> <span data-ttu-id="21f9a-226">También admiten la comunicación con un contenedor y pueden ser reutilizados por varios clientes, según los criterios de licencia.</span><span class="sxs-lookup"><span data-stu-id="21f9a-226">They also support communication with a container and can be reused by multiple clients, depending upon licensing criteria.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**contenedor de control**</span><span class="sxs-lookup"><span data-stu-id="21f9a-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**control container**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-228">Aplicación que admite la inserción de controles mediante la implementación de la interfaz [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-228">An application that supports embedding of controls by implementing the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**propiedad de control**</span><span class="sxs-lookup"><span data-stu-id="21f9a-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**control property**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-230">Propiedad en tiempo de ejecución que el propio control expone y administra.</span><span class="sxs-lookup"><span data-stu-id="21f9a-230">A run-time property that is exposed and managed by the control itself.</span></span> <span data-ttu-id="21f9a-231">Por ejemplo, la fuente y el tamaño del texto utilizados por el control son propiedades del control.</span><span class="sxs-lookup"><span data-stu-id="21f9a-231">For example, the font and text size used by the control are control properties.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controlar objeto**</span><span class="sxs-lookup"><span data-stu-id="21f9a-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controlling object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-233">Objeto dentro de un objeto agregado que controla qué interfaces del objeto agregado se exponen y cuáles son privadas.</span><span class="sxs-lookup"><span data-stu-id="21f9a-233">The object within an aggregate object that controls which interfaces within the aggregate object are exposed and which are private.</span></span> <span data-ttu-id="21f9a-234">La interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del objeto de control se denomina **IUnknown** de control.</span><span class="sxs-lookup"><span data-stu-id="21f9a-234">The [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the controlling object is called the controlling **IUnknown**.</span></span> <span data-ttu-id="21f9a-235">Las llamadas a los métodos **IUnknown** de otros objetos del agregado se deben pasar al objeto **IUnknown** de control.</span><span class="sxs-lookup"><span data-stu-id="21f9a-235">Calls to **IUnknown** methods of other objects in the aggregate must be passed to the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**sitio de control**</span><span class="sxs-lookup"><span data-stu-id="21f9a-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**control site**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-237">Estructura implementada por un contenedor de controles para administrar la presentación y el almacenamiento de un control.</span><span class="sxs-lookup"><span data-stu-id="21f9a-237">A structure implemented by a control container for managing the display and storage of a control.</span></span> <span data-ttu-id="21f9a-238">Dentro de un contenedor determinado, cada control tiene un sitio de control correspondiente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-238">Within a given container, each control has a corresponding control site.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**objeto de transferencia de datos**</span><span class="sxs-lookup"><span data-stu-id="21f9a-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**data transfer object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-240">Objeto que implementa la interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) y que contiene los datos que se van a transferir de un objeto a otro a través del portapapeles o las operaciones de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="21f9a-240">An object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface and contains data to be transferred from one object to another through either the Clipboard or drag-and-drop operations.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**controlador de objetos predeterminado**</span><span class="sxs-lookup"><span data-stu-id="21f9a-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**default object handler**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-242">Un archivo DLL proporcionado con OLE que actúa como suplente en el espacio de procesamiento de la aplicación contenedora para el objeto real.</span><span class="sxs-lookup"><span data-stu-id="21f9a-242">A DLL provided with OLE that acts as a surrogate in the processing space of the container application for the real object.</span></span>

<span data-ttu-id="21f9a-243">Con el controlador de objetos predeterminado, es posible ver los datos almacenados de un objeto sin activar realmente el objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-243">With the default object handler, it is possible to look at an object's stored data without actually activating the object.</span></span> <span data-ttu-id="21f9a-244">El controlador de objetos predeterminado realiza otras tareas, como la representación de un objeto a partir de su estado almacenado en memoria caché cuando el objeto se carga en la memoria.</span><span class="sxs-lookup"><span data-stu-id="21f9a-244">The default object handler performs other tasks, such as rendering an object from its cached state when the object is loaded into memory.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**objeto dependiente**</span><span class="sxs-lookup"><span data-stu-id="21f9a-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**dependent object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-246">Objeto COM que normalmente inicializa otro objeto (el objeto host).</span><span class="sxs-lookup"><span data-stu-id="21f9a-246">A COM object that is typically initialized by another object (the host object).</span></span> <span data-ttu-id="21f9a-247">Aunque la duración del objeto dependiente solo puede tener sentido durante la duración del objeto host, el objeto host no funciona como [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de control para el objeto dependiente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-247">Although the dependent object's lifetime may only make sense during the lifetime of the host object, the host object does not function as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent object.</span></span> <span data-ttu-id="21f9a-248">En cambio, un objeto es un objeto agregado cuando su duración (por medio de su recuento de referencias) está completamente controlada por el objeto de administración.</span><span class="sxs-lookup"><span data-stu-id="21f9a-248">In contrast, an object is an aggregated object when its lifetime (by means of its reference count) is completely controlled by the managing object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**modo de acceso directo**</span><span class="sxs-lookup"><span data-stu-id="21f9a-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**direct access mode**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-250">Uno de los dos modos de acceso en los que se puede abrir un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-250">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="21f9a-251">En el modo directo, todos los cambios se confirman inmediatamente en el objeto de almacenamiento raíz.</span><span class="sxs-lookup"><span data-stu-id="21f9a-251">In direct mode, all changes are immediately committed to the root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**objeto de documento**</span><span class="sxs-lookup"><span data-stu-id="21f9a-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**document object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-253">Documento OLE que puede mostrar una o varias vistas activadas en contexto de sus datos dentro de un marco nativo o externo, como un explorador, conservando el control total sobre su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="21f9a-253">An OLE document that can display one or more in-place activated views of its data within a native or foreign frame, such as a browser, while retaining full control over its user interface.</span></span> <span data-ttu-id="21f9a-254">Además de implementar el documento OLE habitual y las interfaces de activación en contexto, un objeto de documento debe implementar [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)y cada una de sus vistas (en forma de objeto de vista de documento) debe implementar [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).</span><span class="sxs-lookup"><span data-stu-id="21f9a-254">In addition to implementing the usual OLE document and in-place activation interfaces, a document object must implement [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument), and each of its views (in the form of a document view object) must implement [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**contenedor de objetos de documento**</span><span class="sxs-lookup"><span data-stu-id="21f9a-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**document object container**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-256">Aplicación contenedora capaz de mostrar una o más vistas de uno o más objetos de documento y de administrar todos los objetos de documento contenidos dentro de un archivo.</span><span class="sxs-lookup"><span data-stu-id="21f9a-256">A container application capable of displaying one or more views of one or more document objects and of managing all contained document objects within a file.</span></span> <span data-ttu-id="21f9a-257">Cada objeto de documento está asociado a un sitio de documento y cada sitio de documento contiene uno o más sitios de vista de documento correspondientes a las vistas admitidas por el objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-257">Each document object is associated with a document site, and each document site contains one or more document view sites corresponding to the views supported by the document object.</span></span> <span data-ttu-id="21f9a-258">Un contenedor de objetos de documento también incluye un marco de contenedor, que controla la negociación de menús y barras de herramientas y la enumeración de objetos contenidos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-258">A document object container also includes a container frame, which handles menu and toolbar negotiation and the enumeration of contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**servidor de objetos de documento**</span><span class="sxs-lookup"><span data-stu-id="21f9a-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**document object server**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-260">Aplicación de servidor capaz de proporcionar objetos de documento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-260">A server application capable of providing document objects.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**sitio de documento**</span><span class="sxs-lookup"><span data-stu-id="21f9a-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**document site**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-262">Sitio cliente implementado por un contenedor de objetos de documento para administrar la presentación y el almacenamiento de un objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-262">A client site implemented by a document object container for managing the display and storage of a document object.</span></span> <span data-ttu-id="21f9a-263">Cada objeto de documento de un contenedor tiene un sitio de documento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-263">Each document object in a container has a corresponding document site.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**objeto de sitio de documento**</span><span class="sxs-lookup"><span data-stu-id="21f9a-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**document site object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-265">Objeto COM que implementa la interfaz [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) , además de las interfaces de sitio de cliente habituales (como [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).</span><span class="sxs-lookup"><span data-stu-id="21f9a-265">A COM object that implements the [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) interface, in addition to the usual client-site interfaces (such as [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**vista de documento**</span><span class="sxs-lookup"><span data-stu-id="21f9a-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**document view**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-267">Una presentación determinada de los datos de un documento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-267">A particular presentation of a document's data.</span></span> <span data-ttu-id="21f9a-268">Un único objeto de documento puede tener una o más vistas, pero una sola vista de documento puede pertenecer a un solo objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-268">A single document object can have one or more views, but a single document view can belong to one and only one document object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**objeto de vista de documento**</span><span class="sxs-lookup"><span data-stu-id="21f9a-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**document view object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-270">Objeto COM que implementa la interfaz [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) y corresponde a una vista de documento determinada.</span><span class="sxs-lookup"><span data-stu-id="21f9a-270">A COM object that implements the [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) interface and corresponds to a particular document view.</span></span> <span data-ttu-id="21f9a-271">Un objeto con varias vistas de documento agrega un objeto de vista de documento independiente para cada vista.</span><span class="sxs-lookup"><span data-stu-id="21f9a-271">An object with multiple document views aggregates a separate document view object for each view.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**sitio de vista de documento**</span><span class="sxs-lookup"><span data-stu-id="21f9a-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**document view site**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-273">Objeto agregado por un objeto de sitio de documento para administrar el espacio de presentación para una vista determinada de un objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-273">An object aggregated by a document site object for managing the display space for a particular view of a document object.</span></span> <span data-ttu-id="21f9a-274">Dentro de un sitio de documento determinado, cada vista de documento tiene un sitio de vista de documento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-274">Within a given document site, each document view has a corresponding document view site.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**objeto de sitio de vista de documento**</span><span class="sxs-lookup"><span data-stu-id="21f9a-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**document view site object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-276">Objeto COM que se agrega en un objeto de sitio de documento e implementa la interfaz [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) y, opcionalmente, la interfaz [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-276">A COM object that is aggregated in a document site object and implements the [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) interface and, optionally, the [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) interface.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**arrastrar y colocar**</span><span class="sxs-lookup"><span data-stu-id="21f9a-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**drag and drop**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-278">Operación en la que el usuario final usa el mouse u otro dispositivo señalador para trasladar los datos a otra ubicación en la misma ventana o en otra ventana.</span><span class="sxs-lookup"><span data-stu-id="21f9a-278">An operation in which the end user uses the mouse or other pointing device to move data to another location in the same window or another window.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Insertar**</span><span class="sxs-lookup"><span data-stu-id="21f9a-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**embed**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-280">Para insertar un objeto en un documento compuesto de manera que se conserven los formatos de datos nativos de ese objeto y para permitir que se edite desde dentro de su contenedor mediante las herramientas expuestas por su servidor.</span><span class="sxs-lookup"><span data-stu-id="21f9a-280">To insert an object into a compound document in such a way as to preserve the data formats native to that object, and to enable it to be edited from within its container using tools exposed by its server.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**objeto incrustado**</span><span class="sxs-lookup"><span data-stu-id="21f9a-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**embedded object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-282">Objeto cuyos datos se almacenan en un documento compuesto, pero el objeto se ejecuta en el espacio de proceso de su servidor.</span><span class="sxs-lookup"><span data-stu-id="21f9a-282">An object whose data is stored in a compound document, but the object runs in the process space of its server.</span></span> <span data-ttu-id="21f9a-283">El controlador de objetos predeterminado proporciona un suplente en el espacio de procesamiento de la aplicación contenedora para el objeto real.</span><span class="sxs-lookup"><span data-stu-id="21f9a-283">The default object handler provides a surrogate in the processing space of the container application for the real object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**propiedad extendida**</span><span class="sxs-lookup"><span data-stu-id="21f9a-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**extended property**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-285">Propiedad en tiempo de ejecución, como la posición y el tamaño de un control, que un usuario consideraría expuesto por el control pero que el contenedor expone y administra.</span><span class="sxs-lookup"><span data-stu-id="21f9a-285">A run-time property, such as a control's position and size, that a user would assume to be exposed by the control but is exposed and managed by the container.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**moniker de archivo**</span><span class="sxs-lookup"><span data-stu-id="21f9a-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**file moniker**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-287">Moniker basado en una ruta de acceso en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-287">A moniker based on a path in the file system.</span></span> <span data-ttu-id="21f9a-288">Los monikers de archivo se pueden usar para identificar los objetos que se guardan en sus propios archivos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-288">File monikers can be used to identify objects that are saved in their own files.</span></span> <span data-ttu-id="21f9a-289">Un moniker de archivo es un objeto COM que admite la implementación proporcionada por el sistema de la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) para la clase de moniker de archivo.</span><span class="sxs-lookup"><span data-stu-id="21f9a-289">A file moniker is a COM object that supports the system-provided implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface for the file moniker class.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**objeto Font**</span><span class="sxs-lookup"><span data-stu-id="21f9a-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**font object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-291">Objeto COM que proporciona acceso a las fuentes de Interfaz de dispositivo gráfico (GDI) implementando la interfaz [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-291">A COM object that provides access to Graphics Device Interface (GDI) fonts by implementing the [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) interface.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**identificador de formato**</span><span class="sxs-lookup"><span data-stu-id="21f9a-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**format identifier**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-293">GUID que identifica un conjunto de propiedades persistentes.</span><span class="sxs-lookup"><span data-stu-id="21f9a-293">A GUID that identifies a persistent property set.</span></span> <span data-ttu-id="21f9a-294">También se conoce como FMTID.</span><span class="sxs-lookup"><span data-stu-id="21f9a-294">Also referred to as FMTID.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**grama**</span><span class="sxs-lookup"><span data-stu-id="21f9a-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-296">Parte de una aplicación contenedora responsable de negociar menús, teclas de aceleración, barras de herramientas y otros elementos compartidos de la interfaz de usuario con un objeto COM incrustado o un objeto de documento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-296">The part of a container application responsible for negotiating menus, accelerator keys, toolbars, and other shared user-interface elements with an embedded COM object or a document object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**objeto Frame**</span><span class="sxs-lookup"><span data-stu-id="21f9a-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**frame object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-298">Objeto COM que implementa la interfaz [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) y, opcionalmente, la interfaz [**IOLECommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-298">A COM object that implements the [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) interface and, optionally, the [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) interface.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**moniker compuesto genérico**</span><span class="sxs-lookup"><span data-stu-id="21f9a-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**generic composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-300">Colección secuenciada de monikers, que comienza con un moniker de archivo para proporcionar la ruta de acceso de nivel de documento y continuar con uno o más monikers de elemento que, tomadas en conjunto, identifica de forma única un objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-300">A sequenced collection of monikers, starting with a file moniker to provide the document-level path and continuing with one or more item monikers that, taken as a whole, uniquely identifies an object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**función auxiliar**</span><span class="sxs-lookup"><span data-stu-id="21f9a-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**helper function**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-302">Función que encapsula llamadas a otras funciones y métodos de interfaz públicamente disponibles en el SDK de OLE.</span><span class="sxs-lookup"><span data-stu-id="21f9a-302">A function that encapsulates calls to other functions and interface methods publicly available in the OLE SDK.</span></span> <span data-ttu-id="21f9a-303">Las funciones auxiliares son una manera cómoda de llamar a secuencias de funciones y llamadas a métodos de uso frecuente que realizan tareas comunes.</span><span class="sxs-lookup"><span data-stu-id="21f9a-303">Helper functions are a convenient way to call frequently used sequences of function and method calls that accomplish common tasks.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**objeto host**</span><span class="sxs-lookup"><span data-stu-id="21f9a-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**host object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-305">Objeto COM que forma una relación jerárquica con uno o varios objetos COM, denominados objetos dependientes.</span><span class="sxs-lookup"><span data-stu-id="21f9a-305">A COM object that forms a hierarchical relationship with one or more other COM objects, known as the dependent objects.</span></span> <span data-ttu-id="21f9a-306">Normalmente, el objeto host crea instancias de los objetos dependientes y su existencia solo tiene sentido dentro de la duración del objeto host.</span><span class="sxs-lookup"><span data-stu-id="21f9a-306">Typically, the host object instantiates the dependent objects, and their existence only makes sense within the lifetime of the host object.</span></span> <span data-ttu-id="21f9a-307">Sin embargo, el objeto host no actúa como el [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de control de los objetos dependientes, ni se delega directamente a las implementaciones de interfaz de esos objetos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-307">However, the host object does not act as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent objects, nor does it directly delegate to the interface implementations of those objects.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**VALOR**</span><span class="sxs-lookup"><span data-stu-id="21f9a-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**HRESULT**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-309">Un identificador de resultado opaco definido como cero para una devolución correcta de una función y un valor distinto de cero si se devuelve información de error o de estado.</span><span class="sxs-lookup"><span data-stu-id="21f9a-309">An opaque result handle defined to be zero for a successful return from a function and nonzero if error or status information is returned.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**HYPERLINK (objeto)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**hyperlink object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-311">Objeto COM que implementa, como mínimo, la interfaz [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) y actúa como un vínculo a un objeto en otra ubicación (el destino).</span><span class="sxs-lookup"><span data-stu-id="21f9a-311">A COM object that implements, at a minimum, the [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) interface and acts as a link to an object at another location (the target).</span></span> <span data-ttu-id="21f9a-312">Un hipervínculo se compone de cuatro partes: un moniker que identifica la ubicación del destino; una cadena para la ubicación dentro del destino; un nombre descriptivo, o que se pueda mostrar, para el destino; y una cadena que puede contener parámetros adicionales.</span><span class="sxs-lookup"><span data-stu-id="21f9a-312">A hyperlink is made up of four parts: a moniker that identifies the target's location; a string for the location within the target; a friendly, or displayable, name for the target; and a string that can contain additional parameters.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**contexto de exploración de hipervínculo**</span><span class="sxs-lookup"><span data-stu-id="21f9a-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**hyperlink browse context**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-314">Objeto COM que implementa la interfaz [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) y mantiene la pila de navegación del hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="21f9a-314">A COM object that implements the [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) interface and maintains the hyperlink navigation stack.</span></span> <span data-ttu-id="21f9a-315">El objeto de contexto de exploración administra la ventana de marco de hipervínculo y la ventana del objeto de destino de hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="21f9a-315">The browse context object manages the hyperlink frame window and hyperlink target object's window.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**contenedor de hipervínculo**</span><span class="sxs-lookup"><span data-stu-id="21f9a-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**hyperlink container**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-317">Una aplicación contenedora que admita hipervínculos implementando la interfaz [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) y, si los objetos del contenedor pueden ser destinos de otros hipervínculos, la interfaz [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-317">A container application that supports hyperlinks by implementing the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and, if the container's objects can be targets of other hyperlinks, the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**HYPERLINK (objeto de marco)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**hyperlink frame object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-319">Objeto COM que implementa la interfaz [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) y controla la navegación de nivel superior y la presentación de hipervínculos para el contenedor del marco y el servidor del destino del hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="21f9a-319">A COM object that implements the [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) interface and controls the top-level navigation and display of hyperlinks for the frame's container and the hyperlink target's server.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**objeto de sitio de hipervínculo**</span><span class="sxs-lookup"><span data-stu-id="21f9a-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**hyperlink site object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-321">Objeto COM que implementa la interfaz [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) y proporciona el moniker o el identificador de interfaz de su contenedor de hipervínculos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-321">A COM object that implements the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and supplies either the moniker or interface identifier of its hyperlink container.</span></span> <span data-ttu-id="21f9a-322">Un sitio de hipervínculo puede servir varios hipervínculos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-322">One hyperlink site can serve multiple hyperlinks.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**objeto de destino de hipervínculo**</span><span class="sxs-lookup"><span data-stu-id="21f9a-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**hyperlink target object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-324">Objeto COM que implementa la interfaz [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) y proporciona el moniker, el nombre descriptivo y otra información que otros objetos de hipervínculo usarán para navegar hasta él.</span><span class="sxs-lookup"><span data-stu-id="21f9a-324">A COM object that implements the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface and supplies its moniker, friendly name, and other information that other hyperlink objects will use to navigate to it.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in (parámetro)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in parameter**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-326">Parámetro que el llamador de una función o un método de interfaz ha asignado, establecido y liberado.</span><span class="sxs-lookup"><span data-stu-id="21f9a-326">A parameter that is allocated, set, and freed by the caller of a function or interface method.</span></span> <span data-ttu-id="21f9a-327">La función llamada no modifica un parámetro in.</span><span class="sxs-lookup"><span data-stu-id="21f9a-327">An in parameter is not modified by the called function.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**parámetro in/out**</span><span class="sxs-lookup"><span data-stu-id="21f9a-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**in/out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-329">Un parámetro asignado inicialmente por el llamador de una función o un método de interfaz, y establecer, liberar y reasignar, si es necesario, por el proceso al que se llama.</span><span class="sxs-lookup"><span data-stu-id="21f9a-329">A parameter that is initially allocated by the caller of a function or interface method, and set, freed, and reallocated, if necessary, by the process that is called.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**activación en contexto**</span><span class="sxs-lookup"><span data-stu-id="21f9a-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**in-place activation**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-331">Editar un objeto incrustado en la ventana de su contenedor mediante las herramientas proporcionadas por el servidor.</span><span class="sxs-lookup"><span data-stu-id="21f9a-331">Editing an embedded object within the window of its container, using tools provided by the server.</span></span> <span data-ttu-id="21f9a-332">Los objetos vinculados no admiten la activación en contexto; siempre se editan en la ventana del servidor.</span><span class="sxs-lookup"><span data-stu-id="21f9a-332">Linked objects do not support in-place activation; they are always edited in the window of the server.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**servidor en proceso**</span><span class="sxs-lookup"><span data-stu-id="21f9a-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**in-process server**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-334">Servidor implementado como un archivo DLL que se ejecuta en el espacio de proceso del cliente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-334">A server implemented as a DLL that runs in the process space of the client.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**repetición**</span><span class="sxs-lookup"><span data-stu-id="21f9a-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**instance**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-336">Objeto para el que se asigna memoria o que es persistente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-336">An object for which memory is allocated or which is persistent.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interfaz**</span><span class="sxs-lookup"><span data-stu-id="21f9a-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-338">Grupo de funciones relacionadas semánticamente que proporcionan acceso a un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="21f9a-338">A group of semantically related functions that provide access to a COM object.</span></span> <span data-ttu-id="21f9a-339">Cada interfaz OLE define un contrato que permite a los objetos interactuar según el modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="21f9a-339">Each OLE interface defines a contract that allows objects to interact according to the Component Object Model (COM).</span></span> <span data-ttu-id="21f9a-340">Aunque OLE proporciona muchas implementaciones de interfaz, la mayoría de las interfaces también pueden ser implementadas por desarrolladores que diseñan aplicaciones OLE.</span><span class="sxs-lookup"><span data-stu-id="21f9a-340">While OLE provides many interface implementations, most interfaces can also be implemented by developers designing OLE applications.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**identificador de interfaz (IID)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**interface identifier (IID)**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-342">Identificador único global (GUID) asociado a una interfaz.</span><span class="sxs-lookup"><span data-stu-id="21f9a-342">A globally unique identifier (GUID) associated with an interface.</span></span> <span data-ttu-id="21f9a-343">Algunas funciones toman IID como parámetros para permitir que el llamador especifique el puntero de interfaz que se debe devolver.</span><span class="sxs-lookup"><span data-stu-id="21f9a-343">Some functions take IIDs as parameters to allow the caller to specify which interface pointer should be returned.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**moniker de elemento**</span><span class="sxs-lookup"><span data-stu-id="21f9a-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**item moniker**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-345">Moniker basado en una cadena que identifica un objeto en un contenedor.</span><span class="sxs-lookup"><span data-stu-id="21f9a-345">A moniker based on a string that identifies an object in a container.</span></span> <span data-ttu-id="21f9a-346">Los monikers de elemento pueden identificar objetos más pequeños que un archivo, incluidos los objetos incrustados en un documento compuesto o un pseudo objeto (como un rango de celdas de una hoja de cálculo).</span><span class="sxs-lookup"><span data-stu-id="21f9a-346">Item monikers can identify objects smaller than a file, including embedded objects in a compound document, or a pseudo-object (like a range of cells in a spreadsheet).</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licencias**</span><span class="sxs-lookup"><span data-stu-id="21f9a-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licensing**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-348">Característica de COM que proporciona control sobre la creación de objetos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-348">A feature of COM that provides control over object creation.</span></span> <span data-ttu-id="21f9a-349">Los objetos con licencia solo los pueden crear los clientes que tienen autorización para usarlos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-349">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="21f9a-350">Las licencias se implementan en COM a través de la interfaz [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) y admiten una clave de licencia que se puede pasar en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="21f9a-350">Licensing is implemented in COM through the [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**Link (objeto)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**link object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-352">Objeto COM que se crea cuando se crea o se carga un objeto COM vinculado.</span><span class="sxs-lookup"><span data-stu-id="21f9a-352">A COM object that is created when a linked COM object is created or loaded.</span></span> <span data-ttu-id="21f9a-353">OLE proporciona el objeto de vínculo e implementa la interfaz [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-353">The link object is provided by OLE and implements the [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) interface.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**objeto vinculado**</span><span class="sxs-lookup"><span data-stu-id="21f9a-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**linked object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-355">Objeto COM cuyos datos de origen residen físicamente donde se crearon inicialmente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-355">A COM object whose source data physically resides where it was initially created.</span></span> <span data-ttu-id="21f9a-356">Solo se mantiene en el documento compuesto un moniker que representa los datos de origen y los datos de presentación adecuados.</span><span class="sxs-lookup"><span data-stu-id="21f9a-356">Only a moniker that represents the source data and the appropriate presentation data are kept with the compound document.</span></span> <span data-ttu-id="21f9a-357">Los cambios realizados en el origen del vínculo se reflejan automáticamente en el objeto vinculado.</span><span class="sxs-lookup"><span data-stu-id="21f9a-357">Changes made to the link source are automatically reflected in the linked object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**origen del vínculo**</span><span class="sxs-lookup"><span data-stu-id="21f9a-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**link source**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-359">Los datos que son el origen de un objeto vinculado.</span><span class="sxs-lookup"><span data-stu-id="21f9a-359">The data that is the source of a linked object.</span></span> <span data-ttu-id="21f9a-360">Un origen de vínculo puede ser un archivo o una parte de un archivo, como un intervalo de celdas seleccionado dentro de un archivo (también denominado pseudo objeto).</span><span class="sxs-lookup"><span data-stu-id="21f9a-360">A link source may be a file or a portion of a file, such as a selected range of cells within a file (also called a pseudo object).</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**estado cargado**</span><span class="sxs-lookup"><span data-stu-id="21f9a-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**loaded state**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-362">El estado de un objeto después de sus estructuras de datos se ha cargado en la memoria y es accesible para el proceso del cliente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-362">The state of an object after its data structures have been loaded into memory and are accessible to the client process.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**servidor local**</span><span class="sxs-lookup"><span data-stu-id="21f9a-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**local server**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-364">Un servidor fuera de proceso implementado como un. Aplicación EXE que se ejecuta en el mismo equipo que su aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-364">An out-of-process server implemented as an .EXE application running on the same computer as its client application.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**bloquea**</span><span class="sxs-lookup"><span data-stu-id="21f9a-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**lock**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-366">Un puntero se mantiene en y, posiblemente, un recuento de referencias incrementado en un objeto en ejecución.</span><span class="sxs-lookup"><span data-stu-id="21f9a-366">A pointer held to-and possibly, a reference count incremented on-a running object.</span></span> <span data-ttu-id="21f9a-367">OLE define dos tipos de bloqueos que se pueden mantener en un objeto: strong y débil.</span><span class="sxs-lookup"><span data-stu-id="21f9a-367">OLE defines two types of locks that can be held on an object: strong and weak.</span></span> <span data-ttu-id="21f9a-368">Para implementar un bloqueo fuerte, un servidor debe mantener un puntero y un recuento de referencias, de modo que el objeto permanezca "bloqueado" en la memoria al menos hasta que el servidor llame a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="21f9a-368">To implement a strong lock, a server must maintain both a pointer and a reference count, so that the object will remain "locked" in memory at least until the server calls [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="21f9a-369">Para implementar un bloqueo débil, el servidor mantiene solo un puntero al objeto, de modo que otro proceso pueda destruir el objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-369">To implement a weak lock, the server maintains only a pointer to the object, so that the object can be destroyed by another process.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**serialización**</span><span class="sxs-lookup"><span data-stu-id="21f9a-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-371">Empaquetado y envío de llamadas a métodos de interfaz a través de los límites de subprocesos o procesos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-371">Packaging and sending interface method calls across thread or process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**tipo de medio**</span><span class="sxs-lookup"><span data-stu-id="21f9a-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**media type**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-373">Extensión de MIME que permite la negociación de formato de datos entre un cliente y un objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-373">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**Tipo de contenido MIME**</span><span class="sxs-lookup"><span data-stu-id="21f9a-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**MIME content type**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-375">Extensión de MIME que permite la negociación de formato de datos entre un cliente y un objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-375">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Extensión multipropósito de correo Internet (MIME)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Multipurpose Internet Mail Extension (MIME)**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-377">Un protocolo de Internet desarrollado originalmente para permitir el intercambio de mensajes de correo electrónico con contenido enriquecido en entornos de red, equipos y correo electrónico heterogéneos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-377">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, computer, and email environments.</span></span> <span data-ttu-id="21f9a-378">En la práctica, MIME también se ha adoptado y ampliado por aplicaciones que no son de correo.</span><span class="sxs-lookup"><span data-stu-id="21f9a-378">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**Nike**</span><span class="sxs-lookup"><span data-stu-id="21f9a-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-380">Objeto que implementa la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-380">An object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="21f9a-381">Un moniker actúa como un nombre que identifica de forma única un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="21f9a-381">A moniker acts as a name that uniquely identifies a COM object.</span></span> <span data-ttu-id="21f9a-382">Del mismo modo que una ruta de acceso identifica un archivo en el sistema de archivos, un moniker identifica un objeto COM en el espacio de nombres de directorio.</span><span class="sxs-lookup"><span data-stu-id="21f9a-382">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker (clase)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker class**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-384">Implementación de la interfaz [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-384">An implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="21f9a-385">Entre las clases de moniker suministradas por el sistema se incluyen monikers de archivos, monikers, monikers compuestos genéricos, anti-monikers, monikers de puntero y monikers de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="21f9a-385">System-supplied moniker classes include file monikers, item monikers, generic composite monikers, anti-monikers, pointer monikers, and URL monikers.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**cliente de moniker**</span><span class="sxs-lookup"><span data-stu-id="21f9a-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**moniker client**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-387">Aplicación que usa monikers para adquirir punteros de interfaz a objetos administrados por otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="21f9a-387">An application that uses monikers to acquire interface pointers to objects managed by another application.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**proveedor de moniker**</span><span class="sxs-lookup"><span data-stu-id="21f9a-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**moniker provider**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-389">Aplicación que pone a los monikers disponibles que identifican los objetos que administra, de modo que las demás aplicaciones puedan tener acceso a los objetos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-389">An application that makes available monikers that identify the objects it manages, so that the objects are accessible to other applications.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**extensión de espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="21f9a-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-391">Objeto COM en proceso que implementa [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)y [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), a veces denominados interfaces de extensión de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="21f9a-391">An in-process COM object that implements [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), and [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), which are sometimes referred to as the namespace extension interfaces.</span></span> <span data-ttu-id="21f9a-392">Una extensión de espacio de nombres se utiliza para extender el espacio de nombres del shell o para crear un espacio de nombres independiente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-392">A namespace extension is used either to extend the shell's namespace or to create a separate namespace.</span></span> <span data-ttu-id="21f9a-393">Los usuarios primarios son el explorador de Windows y los cuadros de diálogo de archivos comunes.</span><span class="sxs-lookup"><span data-stu-id="21f9a-393">Primary users are the Windows Explorer and common file dialog boxes.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**datos nativos**</span><span class="sxs-lookup"><span data-stu-id="21f9a-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**native data**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-395">Datos utilizados por una aplicación de servidor OLE al editar un objeto incrustado.</span><span class="sxs-lookup"><span data-stu-id="21f9a-395">The data used by an OLE server application when editing an embedded object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**objeto**</span><span class="sxs-lookup"><span data-stu-id="21f9a-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-397">En OLE, estructura de programación que encapsula los datos y la funcionalidad definidos y asignados como una sola unidad y para los que el único acceso público se realiza a través de las interfaces de la estructura de programación.</span><span class="sxs-lookup"><span data-stu-id="21f9a-397">In OLE, a programming structure encapsulating both data and functionality that are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="21f9a-398">Un objeto COM debe admitir, como mínimo, la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , que mantiene la existencia del objeto mientras se usa y proporciona acceso a las demás interfaces del objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-398">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**Estado del objeto**</span><span class="sxs-lookup"><span data-stu-id="21f9a-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**object state**</span></span> 
</dt> <dd>

<span data-ttu-id="21f9a-400">La relación entre un objeto de documento compuesto en su contenedor y la aplicación responsable de la creación del objeto: activo, pasivo, cargado o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="21f9a-400">The relationship between a compound document object in its container and the application responsible for the object's creation: active, passive, loaded, or running.</span></span> <span data-ttu-id="21f9a-401">Los objetos pasivos se almacenan en el disco o en una base de datos, y el objeto no está seleccionado o activo.</span><span class="sxs-lookup"><span data-stu-id="21f9a-401">Passive objects are stored on disk or in a database, and the object is not selected or active.</span></span> <span data-ttu-id="21f9a-402">En el estado Loaded, las estructuras de datos del objeto se han cargado en la memoria, pero no están disponibles para operaciones como la edición.</span><span class="sxs-lookup"><span data-stu-id="21f9a-402">In the loaded state, the object's data structures have been loaded into memory, but they are not available for operations such as editing.</span></span> <span data-ttu-id="21f9a-403">Los objetos en ejecución se cargan y están disponibles para todas las operaciones.</span><span class="sxs-lookup"><span data-stu-id="21f9a-403">Running objects are both loaded and available for all operations.</span></span> <span data-ttu-id="21f9a-404">Los objetos activos ejecutan objetos que tienen una interfaz de usuario visible.</span><span class="sxs-lookup"><span data-stu-id="21f9a-404">Active objects are running objects that have a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**nombre del tipo de objeto**</span><span class="sxs-lookup"><span data-stu-id="21f9a-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**object type name**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-406">Cadena de identificación única que se almacena como parte de la información disponible para un objeto en la base de datos de registro.</span><span class="sxs-lookup"><span data-stu-id="21f9a-406">A unique identification string that is stored as part of the information available for an object in the registration database.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OLE**</span><span class="sxs-lookup"><span data-stu-id="21f9a-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OLE**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-408">Tecnología basada en objetos de Microsoft para compartir información y servicios a través de límites de equipos y procesos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-408">Microsoft's object-based technology for sharing information and services across process and computer boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**servidor fuera de proceso**</span><span class="sxs-lookup"><span data-stu-id="21f9a-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**out-of-process server**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-410">Un servidor de, implementado como un. Aplicación EXE, que se ejecuta fuera del proceso de su cliente, ya sea en el mismo equipo o en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-410">A server, implemented as an .EXE application, which runs outside the process of its client, either on the same computer or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out (parámetro)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-412">Un parámetro out se asigna mediante la función a la que se llama y se libera por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="21f9a-412">An out parameter is allocated by the function being called, and freed by caller.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**estado pasivo**</span><span class="sxs-lookup"><span data-stu-id="21f9a-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**passive state**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-414">El estado de un objeto COM cuando se almacena (en disco o en una base de datos).</span><span class="sxs-lookup"><span data-stu-id="21f9a-414">The state of a COM object when it is stored (on disk or in a database).</span></span> <span data-ttu-id="21f9a-415">El objeto no está seleccionado o activo.</span><span class="sxs-lookup"><span data-stu-id="21f9a-415">The object is not selected or active.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**propiedad Persistent**</span><span class="sxs-lookup"><span data-stu-id="21f9a-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**persistent property**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-417">Información que se puede almacenar de forma persistente como parte de un objeto de almacenamiento, como un archivo o un directorio.</span><span class="sxs-lookup"><span data-stu-id="21f9a-417">Information that can be stored persistently as part of a storage object such as a file or directory.</span></span> <span data-ttu-id="21f9a-418">Las propiedades persistentes se agrupan en conjuntos de propiedades, que se pueden mostrar y editar.</span><span class="sxs-lookup"><span data-stu-id="21f9a-418">Persistent properties are grouped into property sets, which can be displayed and edited.</span></span>

<span data-ttu-id="21f9a-419">Una propiedad persistente es diferente de las propiedades en tiempo de ejecución de los objetos creados con controles OLE y tecnologías de automatización, que se pueden usar para afectar al comportamiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="21f9a-419">A persistent property is different from the run-time properties of objects created with OLE Controls and Automation technologies, which can be used to affect system behavior.</span></span> <span data-ttu-id="21f9a-420">La estructura [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) define todos los tipos válidos de propiedades persistentes, mientras que la estructura **Variant** define todos los tipos válidos de propiedades en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="21f9a-420">The [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) structure defines all valid types of persistent properties, whereas the **VARIANT** structure defines all valid types of run-time properties.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**almacenamiento persistente**</span><span class="sxs-lookup"><span data-stu-id="21f9a-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-422">Almacenamiento de un archivo o un objeto en un medio, como un sistema de archivos o una base de datos, para que el objeto y sus datos se conserven cuando el archivo se cierre y se vuelva a abrir en otro momento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-422">Storage of a file or object in a medium such as a file system or database so that the object and its data persist when the file is closed and then re-opened at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**objeto de imagen**</span><span class="sxs-lookup"><span data-stu-id="21f9a-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**picture object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-424">Objeto COM que proporciona acceso a las imágenes de GDI implementando la interfaz [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-424">A COM object that provides access to GDI images by implementing the [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) interface.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**moniker de puntero**</span><span class="sxs-lookup"><span data-stu-id="21f9a-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**pointer moniker**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-426">Moniker que asigna un puntero de interfaz a un objeto en memoria.</span><span class="sxs-lookup"><span data-stu-id="21f9a-426">A moniker that maps an interface pointer to an object in memory.</span></span> <span data-ttu-id="21f9a-427">Mientras que la mayoría de los monikers identifican objetos que se pueden almacenar de forma persistente, los monikers de puntero identifican los objetos que no pueden.</span><span class="sxs-lookup"><span data-stu-id="21f9a-427">Whereas most monikers identify objects that can be persistently stored, pointer monikers identify objects that cannot.</span></span> <span data-ttu-id="21f9a-428">Permiten que estos objetos participen en una operación de enlace de moniker.</span><span class="sxs-lookup"><span data-stu-id="21f9a-428">They allow such objects to participate in a moniker binding operation.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**datos de presentación**</span><span class="sxs-lookup"><span data-stu-id="21f9a-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**presentation data**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-430">Los datos que usa un contenedor para mostrar objetos incrustados o vinculados.</span><span class="sxs-lookup"><span data-stu-id="21f9a-430">The data used by a container to display embedded or linked objects.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**verbo principal**</span><span class="sxs-lookup"><span data-stu-id="21f9a-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**primary verb**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-432">Acción asociada a la operación más común o preferida que realizan los usuarios en un objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-432">The action associated with the most common or preferred operation users perform on an object.</span></span> <span data-ttu-id="21f9a-433">El verbo principal siempre se define como verbo cero en la base de datos de registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="21f9a-433">The primary verb is always defined as verb zero in the system registration database.</span></span> <span data-ttu-id="21f9a-434">El verbo principal de un objeto se ejecuta haciendo doble clic en el objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-434">An object's primary verb is executed by double-clicking on the object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**propiedad**</span><span class="sxs-lookup"><span data-stu-id="21f9a-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-436">Información asociada a un objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-436">Information that is associated with an object.</span></span> <span data-ttu-id="21f9a-437">En OLE, las propiedades se dividen en dos categorías: propiedades de tiempo de ejecución y propiedades persistentes.</span><span class="sxs-lookup"><span data-stu-id="21f9a-437">In OLE, properties fall into two categories: run-time properties and persistent properties.</span></span> <span data-ttu-id="21f9a-438">Las propiedades de tiempo de ejecución están asociadas normalmente a objetos de control o a sus contenedores.</span><span class="sxs-lookup"><span data-stu-id="21f9a-438">Run-time properties are typically associated with control objects or their containers.</span></span> <span data-ttu-id="21f9a-439">Por ejemplo, el color de fondo es una propiedad en tiempo de ejecución establecida por el contenedor de un control.</span><span class="sxs-lookup"><span data-stu-id="21f9a-439">For example, background color is a run-time property set by a control's container.</span></span> <span data-ttu-id="21f9a-440">Las propiedades persistentes están asociadas a objetos almacenados.</span><span class="sxs-lookup"><span data-stu-id="21f9a-440">Persistent properties are associated with stored objects.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**marco de propiedades**</span><span class="sxs-lookup"><span data-stu-id="21f9a-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**property frame**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-442">Mecanismo de la interfaz de usuario que muestra una o varias páginas de propiedades de un control.</span><span class="sxs-lookup"><span data-stu-id="21f9a-442">The user interface mechanism that displays one or more property pages for a control.</span></span> <span data-ttu-id="21f9a-443">El sistema en tiempo de ejecución de controles OLE proporciona una implementación estándar de un marco de propiedades al que se puede tener acceso mediante la función auxiliar [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-443">The OLE Controls run-time system provides a standard implementation of a property frame that can be accessed by using the [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) helper function.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**identificador de propiedad**</span><span class="sxs-lookup"><span data-stu-id="21f9a-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**property identifier**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-445">Entero con signo de cuatro bytes que identifica una propiedad persistente dentro de un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="21f9a-445">A four-byte signed integer that identifies a persistent property within a property set.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**Página de propiedades**</span><span class="sxs-lookup"><span data-stu-id="21f9a-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**property page**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-447">Objeto COM con su propio CLSID que forma parte de una interfaz de usuario, implementada por un control, y permite ver y establecer las propiedades del control.</span><span class="sxs-lookup"><span data-stu-id="21f9a-447">A COM object with its own CLSID that is part of a user interface, implemented by a control, and allows the control's properties to be viewed and set.</span></span> <span data-ttu-id="21f9a-448">Los objetos de la página de propiedades implementan la interfaz [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-448">Property page objects implement the [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) interface.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**sitio de la página de propiedades**</span><span class="sxs-lookup"><span data-stu-id="21f9a-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**property page site**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-450">Ubicación dentro de un marco de propiedades donde se muestra una página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="21f9a-450">The location within a property frame where a property page is displayed.</span></span> <span data-ttu-id="21f9a-451">El marco de propiedades implementa la interfaz [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) , que contiene métodos para administrar los sitios de cada una de las páginas de propiedades proporcionadas por un control.</span><span class="sxs-lookup"><span data-stu-id="21f9a-451">The property frame implements the [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) interface, which contains methods to manage the sites of each of the property pages supplied by a control.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**conjunto de propiedades**</span><span class="sxs-lookup"><span data-stu-id="21f9a-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**property set**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-453">Un grupo de propiedades relacionadas lógicamente que está asociado a un objeto almacenado de forma persistente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-453">A logically related group of properties that is associated with a persistently stored object.</span></span> <span data-ttu-id="21f9a-454">Para crear, abrir, eliminar o enumerar uno o más conjuntos de propiedades, implemente la interfaz [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-454">To create, open, delete, or enumerate one or more property sets, implement the [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="21f9a-455">Si usa archivos compuestos, puede usar la implementación de OLE de esta interfaz en lugar de implementar la suya propia.</span><span class="sxs-lookup"><span data-stu-id="21f9a-455">If you are using compound files, you can use OLE's implementation of this interface rather than implementing your own.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**almacenamiento del conjunto de propiedades**</span><span class="sxs-lookup"><span data-stu-id="21f9a-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**property set storage**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-457">Objeto de almacenamiento COM que contiene un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="21f9a-457">A COM storage object that holds a property set.</span></span> <span data-ttu-id="21f9a-458">Un almacenamiento de conjunto de propiedades es un objeto dependiente asociado y administrado por un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-458">A property set storage is a dependent object associated with and managed by a storage object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**hoja de propiedades**</span><span class="sxs-lookup"><span data-stu-id="21f9a-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**property sheet**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-460">Un conjunto de páginas de propiedades para uno o más objetos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-460">A set of property pages for one or more objects.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**proxi**</span><span class="sxs-lookup"><span data-stu-id="21f9a-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**proxy**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-462">Objeto específico de la interfaz que empaqueta los parámetros de esa interfaz como preparación para una llamada de método remoto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-462">An interface-specific object that packages parameters for that interface in preparation for a remote method call.</span></span> <span data-ttu-id="21f9a-463">Un proxy se ejecuta en el espacio de direcciones del remitente y se comunica con el código auxiliar correspondiente en el espacio de direcciones del receptor.</span><span class="sxs-lookup"><span data-stu-id="21f9a-463">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**Administrador de proxy**</span><span class="sxs-lookup"><span data-stu-id="21f9a-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-465">En el cálculo de referencias estándar, proxy que administra todos los proxies de interfaz para un solo objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-465">In standard marshaling, a proxy that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo (objeto)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-467">Parte de un documento o un objeto incrustado, como un rango de celdas de una hoja de cálculo, que puede ser el origen de un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="21f9a-467">A portion of a document or embedded object, such as a range of cells in a spreadsheet, that can be the source for a COM object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**recuento de referencias**</span><span class="sxs-lookup"><span data-stu-id="21f9a-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-469">Mantener un recuento de cada puntero de interfaz mantenido en un objeto para asegurarse de que no se destruye el objeto antes de que se liberen todas las referencias a él.</span><span class="sxs-lookup"><span data-stu-id="21f9a-469">Keeping a count of each interface pointer held on an object to ensure that the object is not destroyed before all references to it are released.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**moniker relativo**</span><span class="sxs-lookup"><span data-stu-id="21f9a-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**relative moniker**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-471">Moniker que especifica la ubicación de un objeto en relación con la ubicación de otro objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-471">A moniker that specifies the location of an object relative to the location of another object.</span></span> <span data-ttu-id="21f9a-472">Un moniker relativo es análogo a una ruta de acceso relativa, como. \\ Informe de copia de seguridad \\ . old.</span><span class="sxs-lookup"><span data-stu-id="21f9a-472">A relative moniker is analogous to a relative path, such as ..\\backup\\report.old.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**servidor remoto**</span><span class="sxs-lookup"><span data-stu-id="21f9a-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**remote server**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-474">Aplicación de servidor, implementada como un archivo EXE, que se ejecuta en un equipo diferente de la aplicación cliente que la utiliza.</span><span class="sxs-lookup"><span data-stu-id="21f9a-474">A server application, implemented as an EXE, running on a different computer from the client application using it.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**revertir**</span><span class="sxs-lookup"><span data-stu-id="21f9a-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**revert**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-476">Para descartar los cambios realizados en un objeto desde la última vez que se confirmaron los cambios o se abrió el almacenamiento del objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-476">To discard any changes made to an object since the last time the changes were committed or the object's storage was opened.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**objeto de almacenamiento raíz**</span><span class="sxs-lookup"><span data-stu-id="21f9a-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**root storage object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-478">Objeto de almacenamiento más externo de un documento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-478">The outermost storage object in a document.</span></span> <span data-ttu-id="21f9a-479">Un objeto de almacenamiento raíz puede contener otros objetos de flujo y almacenamiento anidado.</span><span class="sxs-lookup"><span data-stu-id="21f9a-479">A root storage object can contain other nested storage and stream objects.</span></span> <span data-ttu-id="21f9a-480">Por ejemplo, un documento compuesto se guarda en el disco como una serie de objetos de almacenamiento y de secuencia dentro de un objeto de almacenamiento raíz.</span><span class="sxs-lookup"><span data-stu-id="21f9a-480">For example, a compound document is saved on disk as a series of storage and stream objects within a root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**Estado de ejecución**</span><span class="sxs-lookup"><span data-stu-id="21f9a-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**running state**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-482">El estado de un objeto COM cuando su aplicación de servidor se está ejecutando y es posible tener acceso a sus interfaces y recibir notificaciones de cambios.</span><span class="sxs-lookup"><span data-stu-id="21f9a-482">The state of a COM object when its server application is running and it is possible to access its interfaces and receive notification of changes.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**tabla de objetos en ejecución (ROT)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**running object table (ROT)**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-484">Una tabla accesible globalmente en cada equipo que realiza un seguimiento de todos los objetos COM en el estado de ejecución que pueden identificarse mediante un moniker.</span><span class="sxs-lookup"><span data-stu-id="21f9a-484">A globally accessible table on each computer that keeps track of all COM objects in the running state that can be identified by a moniker.</span></span> <span data-ttu-id="21f9a-485">Los proveedores de moniker registran un objeto en la tabla, lo que incrementa el recuento de referencias del objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-485">Moniker providers register an object in the table, which increments the object's reference count.</span></span> <span data-ttu-id="21f9a-486">Antes de que se pueda destruir el objeto, su moniker debe liberarse de la tabla.</span><span class="sxs-lookup"><span data-stu-id="21f9a-486">Before the object can be destroyed, its moniker must be released from the table.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**propiedad en tiempo de ejecución**</span><span class="sxs-lookup"><span data-stu-id="21f9a-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**run-time property**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-488">Información de estado discreto asociada a un objeto de control o a su contenedor.</span><span class="sxs-lookup"><span data-stu-id="21f9a-488">Discrete state information associated with a control object or its container.</span></span> <span data-ttu-id="21f9a-489">Hay tres tipos de propiedades de tiempo de ejecución: propiedades de ambiente, propiedades de control y propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="21f9a-489">There are three types of run-time properties: ambient properties, control properties, and extended properties.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**registro automático**</span><span class="sxs-lookup"><span data-stu-id="21f9a-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**self-registration**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-491">Proceso por el que un servidor puede realizar sus propias operaciones del registro.</span><span class="sxs-lookup"><span data-stu-id="21f9a-491">The process by which a server can perform its own registry operations.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**aplicación de servidor**</span><span class="sxs-lookup"><span data-stu-id="21f9a-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**server application**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-493">Aplicación que puede crear objetos COM.</span><span class="sxs-lookup"><span data-stu-id="21f9a-493">An application that can create COM objects.</span></span> <span data-ttu-id="21f9a-494">Después, las aplicaciones contenedoras pueden incrustar o vincular estos objetos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-494">Container applications can then embed or link to these objects.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**Static (objeto)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**static object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-496">Objeto que contiene solo una presentación, sin datos nativos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-496">An object that contains only a presentation, with no native data.</span></span> <span data-ttu-id="21f9a-497">Un contenedor puede tratar un objeto estático como si fuera un objeto vinculado o incrustado, con la excepción de que no es posible editar un objeto estático.</span><span class="sxs-lookup"><span data-stu-id="21f9a-497">A container can treat a static object as though it were a linked or embedded object, except that it is not possible to edit a static object.</span></span>

<span data-ttu-id="21f9a-498">Un objeto estático puede producir, por ejemplo, una interrupción de un vínculo en un objeto vinculado; es decir, la aplicación de servidor no está disponible o el usuario no desea que el objeto vinculado se actualice ya.</span><span class="sxs-lookup"><span data-stu-id="21f9a-498">A static object can result, for example, from the breaking of a link on a linked object-that is, the server application is unavailable, or the user doesn't want the linked object to be updated anymore.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**objeto de almacenamiento**</span><span class="sxs-lookup"><span data-stu-id="21f9a-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**storage object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-500">Objeto COM que implementa la interfaz [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-500">A COM object that implements the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="21f9a-501">Un objeto de almacenamiento contiene objetos de almacenamiento anidados u objetos de secuencia, lo que da lugar al equivalente de una estructura de directorio/archivo dentro de un único archivo.</span><span class="sxs-lookup"><span data-stu-id="21f9a-501">A storage object contains nested storage objects or stream objects, resulting in the equivalent of a directory/file structure within a single file.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**Stream (objeto)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**stream object**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-503">Objeto COM que implementa la interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-503">A COM object that implements the [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> <span data-ttu-id="21f9a-504">Un objeto de secuencia es análogo a un archivo en un sistema de archivos o directorios.</span><span class="sxs-lookup"><span data-stu-id="21f9a-504">A stream object is analogous to a file in a directory/file system.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Almacenamiento estructurado**</span><span class="sxs-lookup"><span data-stu-id="21f9a-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Structured Storage**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-506">Tecnología de OLE para almacenar archivos compuestos en sistemas de archivos nativos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-506">OLE's technology for storing compound files in native file systems.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**agrupa**</span><span class="sxs-lookup"><span data-stu-id="21f9a-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**stub**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-508">Cuando se calculan las referencias de los parámetros de un método de interfaz o de una función a través de un límite de proceso, el código auxiliar es un objeto específico de la interfaz que desempaqueta los parámetros de cálculo de referencias y llama al método requerido.</span><span class="sxs-lookup"><span data-stu-id="21f9a-508">When a function's or interface method's parameters are marshaled across a process boundary, the stub is an interface-specific object that unpackages the marshaled parameters and calls the required method.</span></span> <span data-ttu-id="21f9a-509">El código auxiliar se ejecuta en el espacio de direcciones del receptor y se comunica con el proxy correspondiente en el espacio de direcciones del remitente.</span><span class="sxs-lookup"><span data-stu-id="21f9a-509">The stub runs in the receiver's address space and communicates with a corresponding proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**Administrador de código auxiliar**</span><span class="sxs-lookup"><span data-stu-id="21f9a-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**stub manager**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-511">Administra todos los códigos auxiliares de interfaz para un solo objeto.</span><span class="sxs-lookup"><span data-stu-id="21f9a-511">Manages all of the interface stubs for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**llamada sincrónica**</span><span class="sxs-lookup"><span data-stu-id="21f9a-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**synchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-513">Una llamada de función que no permite ejecutar más instrucciones en el proceso de llamada hasta que la función devuelve.</span><span class="sxs-lookup"><span data-stu-id="21f9a-513">A function call that does not allow further instructions in the calling process to be executed until the function returns.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**registro del sistema**</span><span class="sxs-lookup"><span data-stu-id="21f9a-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**system registry**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-515">Repositorio de información de todo el sistema compatible con Windows que contiene información sobre el sistema y sus aplicaciones, incluidos los clientes y servidores OLE.</span><span class="sxs-lookup"><span data-stu-id="21f9a-515">A system-wide repository of information supported by Windows, which contains information about the system and its applications, including OLE clients and servers.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**modo de acceso de transacción**</span><span class="sxs-lookup"><span data-stu-id="21f9a-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**transacted access mode**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-517">Uno de los dos modos de acceso en los que se puede abrir un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="21f9a-517">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="21f9a-518">Cuando se abre en modo de transacción, los cambios se almacenan en búferes hasta que el objeto de almacenamiento raíz confirma los cambios.</span><span class="sxs-lookup"><span data-stu-id="21f9a-518">When opened in transacted mode, changes are stored in buffers until the root storage object commits its changes.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**información de tipo**</span><span class="sxs-lookup"><span data-stu-id="21f9a-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**type information**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-520">Información sobre la clase de un objeto que proporciona una biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-520">Information about an object's class provided by a type library.</span></span> <span data-ttu-id="21f9a-521">Para proporcionar información de tipo, un objeto COM implementa la interfaz [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-521">To provide type information, a COM object implements the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interface.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**transferencia de datos uniforme**</span><span class="sxs-lookup"><span data-stu-id="21f9a-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**uniform data transfer**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-523">Modelo para transferir datos a través del portapapeles, arrastrar y colocar, o automatización.</span><span class="sxs-lookup"><span data-stu-id="21f9a-523">A model for transferring data through the clipboard, drag and drop, or Automation.</span></span> <span data-ttu-id="21f9a-524">Los objetos que se ajustan a este modelo implementan la interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="21f9a-524">Objects conforming to this model implement the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="21f9a-525">Este modelo reemplaza a DDE (intercambio dinámico de datos).</span><span class="sxs-lookup"><span data-stu-id="21f9a-525">This model replaces DDE (dynamic data exchange).</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**resolución**</span><span class="sxs-lookup"><span data-stu-id="21f9a-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**unmarshaling**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-527">Desempaquetar los parámetros que se han enviado a un proxy a través de los límites del proceso.</span><span class="sxs-lookup"><span data-stu-id="21f9a-527">Unpacking parameters that have been sent to a proxy across process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**Localizador de recursos universal (URL)**</span><span class="sxs-lookup"><span data-stu-id="21f9a-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**universal resource locator (URL)**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-529">El identificador utilizado por el World Wide Web para los nombres y las ubicaciones de los objetos en Internet.</span><span class="sxs-lookup"><span data-stu-id="21f9a-529">The identifier used by the World Wide Web for the names and locations of objects on the Internet.</span></span> <span data-ttu-id="21f9a-530">OLE proporciona una clase moniker, moniker de dirección URL, cuya implementación se puede usar para enlazar un cliente a objetos identificados por una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="21f9a-530">OLE provides a moniker class, URL moniker, whose implementation can be used to bind a client to objects identified by a URL.</span></span>

</dd> <dt>

<span data-ttu-id="21f9a-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**Moniker de dirección URL**</span><span class="sxs-lookup"><span data-stu-id="21f9a-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**URL moniker**</span></span>
</dt> <dd>

<span data-ttu-id="21f9a-532">Moniker basado en un localizador de recursos universal (URL).</span><span class="sxs-lookup"><span data-stu-id="21f9a-532">A moniker based on a universal resource locator (URL).</span></span> <span data-ttu-id="21f9a-533">Un cliente puede usar monikers de dirección URL para enlazar a objetos que residen en Internet.</span><span class="sxs-lookup"><span data-stu-id="21f9a-533">A client can use URL monikers to bind to objects that reside on the Internet.</span></span> <span data-ttu-id="21f9a-534">La clase de moniker de dirección URL proporcionada por el sistema admite enlaces sincrónicos y asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="21f9a-534">The system-supplied URL moniker class supports both synchronous and asynchronous binding.</span></span>

</dd> </dl>

 

 