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
# <a name="com-glossary"></a><span data-ttu-id="9a6a3-103">Glosario de COM+</span><span class="sxs-lookup"><span data-stu-id="9a6a3-103">COM+ Glossary</span></span>

<dl> <dt>

<span data-ttu-id="9a6a3-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**token de acceso**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**access token**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-105">Objeto que describe el contexto de seguridad de un proceso o subproceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-105">An object that describes the security context of a process or thread.</span></span> <span data-ttu-id="9a6a3-106">La información de un token incluye la identidad y los privilegios de la cuenta de usuario asociada con el proceso o subproceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-106">The information in a token includes the identity and privileges of the user account associated with the process or thread.</span></span> <span data-ttu-id="9a6a3-107">Cuando un usuario inicia sesión, el sistema comprueba la contraseña del usuario comparándola con la información almacenada en una base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-107">When a user logs on, the system verifies the user's password by comparing it with information stored in a security database.</span></span> <span data-ttu-id="9a6a3-108">Si la contraseña se autentica, el sistema genera un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-108">If the password is authenticated, the system produces an access token.</span></span> <span data-ttu-id="9a6a3-109">Cada proceso ejecutado en nombre de este usuario tiene una copia de este token de acceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-109">Every process executed on behalf of this user has a copy of this access token.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**Propiedades ACID**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID properties**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-111">Acrónimo acuñó de los pioneros en el procesamiento de transacciones para atomicidad, coherencia, aislamiento y durabilidad.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-111">Acronym coined by transaction processing pioneers for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="9a6a3-112">Estas propiedades garantizan un comportamiento predecible, lo que refuerza el rol de las transacciones como proposiciones All-or-None diseñadas para proporcionar resultados coherentes y predecibles en un entorno distribuido cuando se pueden producir errores independientes.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-112">These properties ensure predictable behavior, reinforcing the role of transactions as all-or-none propositions designed to provide consistent and predictable results in a distributed environment when independent failures can occur.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**activación**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-114">Cadena de eventos que tiene como resultado la creación de un objeto COM y la devolución de un puntero válido a una interfaz en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-114">The chain of events that results in the creation of a COM object and the return of a valid pointer to an interface on that object.</span></span> <span data-ttu-id="9a6a3-115">En COM+, un objeto se activa en su propio contexto o en el de su creador (un objeto que ha solicitado el objeto que se está activando).</span><span class="sxs-lookup"><span data-stu-id="9a6a3-115">In COM+, an object gets activated either in its own context or in that of its creator (an object that has requested the object being activated).</span></span> <span data-ttu-id="9a6a3-116">Los servicios COM+ dependen de la activación adecuada de un objeto en función de la configuración del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-116">COM+ services rely on appropriate activation of an object based on the object's configuration.</span></span> <span data-ttu-id="9a6a3-117">En el transcurso de la activación, el sistema determina el contexto en el que se ejecuta el objeto, inicializa las propiedades de contexto, comprueba los permisos de acceso y establece una identidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-117">In the course of activation, the system determines the context in which the object runs, initializes the context properties, checks access permissions, and establishes a security identity.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**seguridad de activación**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**activation security**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-119">Forma de protección de seguridad que determina quién puede iniciar un servidor.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-119">A form of security protection that determines who can launch a server.</span></span> <span data-ttu-id="9a6a3-120">El administrador de control de servicios (SCM) de un equipo determinado aplica automáticamente la seguridad de activación.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-120">Activation security is automatically applied by the Service Control Manager (SCM) of a particular computer.</span></span> <span data-ttu-id="9a6a3-121">Tras recibir una solicitud de un cliente para activar un objeto, el SCM comprueba la solicitud con la información de seguridad de activación almacenada en el registro.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-121">Upon receipt of a request from a client to activate an object, the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="9a6a3-122">También se comprueba la seguridad de activación para las activaciones del mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-122">Activation security is also checked for same-computer activations.</span></span> <span data-ttu-id="9a6a3-123">También se denomina *seguridad de inicio*.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-123">Also called *launch security*.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**tipo de activación**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**activation type**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-125">Categoría de activación para una aplicación COM+ que indica si la aplicación se ejecuta dentro o fuera del espacio de proceso de su cliente (en función de si se trata de una aplicación de biblioteca o servidor, respectivamente) y de si la aplicación se ejecuta como un servicio.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-125">Activation category for a COM+ application that indicates whether the application runs in or out of its client's process space (depending on whether it's a library or server application, respectively) as well as whether the application runs as a service.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**proceso**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**activity**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-127">En COM+, subproceso lógico que consta de una o varias transacciones y que contiene una colección de componentes que se agrupan en una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-127">In COM+, a logical thread comprising one or more transactions and containing a collection of components that are grouped into a COM+ application.</span></span> <span data-ttu-id="9a6a3-128">Cada objeto COM pertenece a una actividad.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-128">Every COM object belongs to one activity.</span></span> <span data-ttu-id="9a6a3-129">No se puede cambiar la asociación entre un objeto y una actividad.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-129">The association between an object and an activity cannot be changed.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**proceso del modelo de apartamento**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**apartment model process**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-131">Proceso que tiene dos o más apartamentos de un solo subproceso y sin apartamentos multiproceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-131">A process that has two or more single-threaded apartments and no multithreaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**proxy de aplicación**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**application proxy**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-133">Conjunto de archivos que contiene información de registro que permite a un cliente tener acceso remoto a una aplicación de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-133">A set of files containing registration information that allows a client to remotely access a COM+ server application.</span></span> <span data-ttu-id="9a6a3-134">Cuando se instala en un equipo cliente, un archivo de proxy de aplicación escribe información acerca de la aplicación de servidor en el equipo cliente. después, el cliente puede tener acceso de forma remota a la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-134">When installed on a client computer, an application proxy file writes information about the server application to the client computer; the client can then remotely access the server application.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**autenticación**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**authentication**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-136">El proceso de seguridad para determinar que un llamador de una aplicación es realmente quien dice ser: comprobar la autenticidad de una solicitud de identidad.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-136">The security process of determining that a caller of an application is actually who it says it is—verifying the authenticity of an identity claim.</span></span> <span data-ttu-id="9a6a3-137">En el caso de las aplicaciones COM+, la autenticación se puede activar y configurar de forma administrativa, después de que funciona de forma transparente en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-137">For COM+ applications, authentication can be turned on and configured administratively, after which it works transparently to the application.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**on**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**authorization**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-139">El proceso de seguridad que determina si un llamador de una aplicación está autorizado para hacer lo que se le pide.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-139">The security process of determining whether a caller of an application is authorized to do what it is asking to do.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**almacenamiento en caché de Resource Manager**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**caching resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-141">Un administrador de recursos que actúa como front-end a otro administrador de recursos y que almacena en caché la información de forma local, lo que reduce el costo de acceso al recurso subyacente.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-141">A resource manager that acts as a front-end to another resource manager and that caches information locally, reducing the cost of accessing the underlying resource.</span></span> <span data-ttu-id="9a6a3-142">A diferencia de un administrador de recursos convencional, un administrador de recursos de almacenamiento en caché no participa en la recuperación porque nunca almacena permanentemente los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-142">Unlike a conventional resource manager, a caching resource manager does not participate in recovery because it never permanently stores the underlying data.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**seguridad de llamadas**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**call security**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-144">Forma de protección de seguridad que ayuda a controlar el acceso a los métodos de un objeto de servidor después de que se haya iniciado un servidor.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-144">A form of security protection that helps control access to a server object's methods after a server has been launched.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**(clase) (COM)**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**class (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-146">Una implementación concreta y con nombre de una o más interfaces.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-146">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="9a6a3-147">Una clase COM se identifica mediante un CLSID y, a veces, un ProgID.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-147">A COM class is identified by a CLSID and, sometimes, a ProgID.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**esconder**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-149">La capacidad de un servidor de enmascarar su propia identidad al realizar llamadas en el nombre de un cliente.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-149">A server's ability to mask its own identity when making calls on a client's behalf.</span></span> <span data-ttu-id="9a6a3-150">Cuando está habilitada la ocultación, las llamadas realizadas por el servidor que suplanta al cliente pueden realizarse en la identidad del cliente.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-150">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="9a6a3-151">Cuando se deshabilita la ocultación, las llamadas realizadas por el servidor se realizarán en la identidad del servidor.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-151">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Aplicación COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**COM+ application**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-153">La unidad principal de administración y seguridad de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-153">The primary unit of administration and security for Component Services.</span></span> <span data-ttu-id="9a6a3-154">Una aplicación COM+ es un grupo de componentes COM que, por lo general, realizan funciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-154">A COM+ application is a group of COM components that, generally, perform related functions.</span></span> <span data-ttu-id="9a6a3-155">Estos componentes se componen además de interfaces y métodos COM.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-155">These components further consist of COM interfaces and methods.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Agrupación de aplicaciones COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**COM+ Application Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-157">Característica de servicios de componentes que permite escalar los procesos de un solo subproceso y también puede ayudarle a recuperarse de los errores en procesos únicos proporcionando otros procesos en ejecución capaces de controlar las activaciones.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-157">A Component Services feature that allows single-threaded processes to scale and can also help you recover from failures in single processes by providing other running processes able to handle activations.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Reciclaje de aplicaciones COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**COM+ Application Recycling**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-159">Característica de servicios de componentes que aumenta significativamente la estabilidad general de las aplicaciones, ya que permite cerrar correctamente un proceso asociado a una aplicación y reiniciarlo.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-159">A Component Services feature that significantly increases the overall stability of your applications by allowing you to gracefully shut down a process associated with an application and restart it.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Catálogo de COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**COM+ catalog**</span></span> 
</dt> <dd>

<span data-ttu-id="9a6a3-161">Almacén de datos que contiene los datos de configuración de COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-161">The data store that holds COM+ configuration data.</span></span> <span data-ttu-id="9a6a3-162">El rendimiento de las tareas de administración de COM+ requiere leer y escribir datos almacenados en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-162">Performance of COM+ administration tasks requires reading and writing data stored in the catalog.</span></span> <span data-ttu-id="9a6a3-163">Solo se puede tener acceso al catálogo a través de la herramienta administrativa Servicios de componentes o a través de la biblioteca COMAdmin.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-163">The catalog can be accessed only through the Component Services administrative tool or through the COMAdmin library.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Eventos COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**COM+ Events**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-165">Los eventos COM+ coinciden y conectan a publicadores y suscriptores a través de un sistema de eventos de acoplamiento flexible.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-165">COM+ Events matches and connects publishers and subscribers through a loosely coupled events system.</span></span> <span data-ttu-id="9a6a3-166">Un publicador realiza la llamada al método para iniciar un evento y un suscriptor recibe estas llamadas a través del sistema de eventos en lugar de hacerlo directamente desde el publicador.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-166">A publisher makes the method call to initiate an event, and a subscriber receives these calls through the event system rather than directly from the publisher.</span></span> <span data-ttu-id="9a6a3-167">El servicio de eventos COM+ mantiene la lista de suscriptores interesados que reciben las llamadas y dirige esas llamadas sin necesidad de conocer el publicador.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-167">The COM+ Events service maintains the list of interested subscribers who receive the calls and directs those calls without requiring the knowledge of the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Aplicación de biblioteca COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**COM+ library application**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-169">Aplicación COM+ que se ejecuta en el proceso del cliente que la crea.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-169">A COM+ application that runs in the process of the client that creates it.</span></span> <span data-ttu-id="9a6a3-170">Las aplicaciones de biblioteca pueden utilizar la seguridad basada en roles pero no admiten el acceso remoto o los componentes en cola.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-170">Library applications can use role-based security but do not support remote access or queued components.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Agrupación de objetos COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**COM+ Object Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-172">Servicio automático proporcionado por COM+ que le permite configurar un componente para que las instancias de se mantengan activas en un grupo, listas para ser utilizadas por cualquier cliente que solicite el componente.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-172">An automatic service provided by COM+ that enables you to configure a component to have instances of itself kept active in a pool, ready to be used by any client that requests the component.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Particiones COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**COM+ Partitions**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-174">Servicio COM+ que habilita, en un solo equipo, la creación de espacios de ejecución independientes para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-174">A COM+ service that enables, on a single computer, the creation of separate execution spaces for applications.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Conjuntos de particiones COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**COM+ partition sets**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-176">Grupo de particiones de COM+ que se asigna a un identificador de usuario determinado en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-176">A group of COM+ partitions that is mapped to a particular user ID in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Componentes en cola de COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**COM+ Queued Components**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-178">Un servicio COM+, basado en Microsoft Message Queuing, que proporciona una manera sencilla de invocar y ejecutar componentes de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-178">A COM+ service, based on Microsoft Message Queuing, that provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="9a6a3-179">El procesamiento de mensajes puede producirse sin tener en cuenta la disponibilidad o la accesibilidad del remitente o del receptor.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-179">Message processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**Aplicación de servidor COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM+ server application**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-181">Aplicación COM+ que se ejecuta en su propio proceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-181">A COM+ application that runs in its own process.</span></span> <span data-ttu-id="9a6a3-182">Las aplicaciones de servidor pueden admitir todos los servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-182">Server applications can support all COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**SOAP DE COM+**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM+ SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-184">Característica de servicios de componentes que permite exponer una aplicación COM+ como un servicio Web XML.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-184">A Component Services feature that allows you to expose a COM+ application as an XML web service.</span></span> <span data-ttu-id="9a6a3-185">El protocolo SOAP de COM+ también le permite utilizar un servicio Web XML como componente COM.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-185">COM+ SOAP also enables you to use an XML web service as a COM component.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**Componente COM**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM component**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-187">Unidad binaria de código que incluye el código de empaquetado y de registro y que crea objetos COM.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-187">A binary unit of code that includes packaging and registration code and that creates COM objects.</span></span> <span data-ttu-id="9a6a3-188">Todas las aplicaciones COM+ constan de uno o varios componentes COM.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-188">All COM+ applications consist of one or more COM components.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**árbol de confirmación**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**commit tree**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-190">En un sistema de transacciones distribuidas, representación conceptual de una transacción según las relaciones jerárquicas entre los administradores de transacciones individuales que participan en una transacción distribuida.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-190">In a distributed transaction system, the conceptual representation of a transaction as based on the hierarchical relationships between individual transaction managers participating in a distributed transaction.</span></span> <span data-ttu-id="9a6a3-191">En esa jerarquía se incluyen los administradores de recursos inscritos asociados a los administradores de transacciones.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-191">Included in that hierarchy are the enlisted resource managers associated with the transaction managers.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**Objeto COM**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-193">En el modelo de programación COM, una estructura de programación que encapsula los datos y la funcionalidad, que se definen y asignan como una sola unidad y para los que el único acceso público se realiza a través de las interfaces de la estructura de programación.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-193">In the COM programming model, a programming structure encapsulating both data and functionality, which are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="9a6a3-194">Un objeto COM debe admitir, como mínimo, la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , que mantiene la existencia del objeto mientras se usa y proporciona acceso a las demás interfaces del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-194">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Administrador de recursos de compensaciones (CRM)**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Compensating Resource Manager (CRM)**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-196">Característica de COM+ que permite a los recursos no transaccionales participar en una transacción de confirmación en dos fases con Microsoft Coordinador de transacciones distribuidas (DTC).</span><span class="sxs-lookup"><span data-stu-id="9a6a3-196">A COM+ feature that enables non-transactional resources to participate in a two-phase commit transaction with the Microsoft Distributed Transaction Coordinator (DTC).</span></span> <span data-ttu-id="9a6a3-197">Normalmente, los CRMs no proporcionan las capacidades de aislamiento de los administradores de recursos completos, pero proporcionan atomicidad y durabilidad transaccional escribiendo en un registro.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-197">Typically, CRMs do not provide the isolation capabilities of full resource managers, but they do provide transactional atomicity and durability by writing to a log.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Herramienta administrativa Servicios de componentes**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Component Services administrative tool**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-199">Complemento de interfaz de usuario a través del cual los administradores y programadores pueden crear, configurar y mantener aplicaciones COM+, así como administrar las transacciones distribuidas y las bases de datos residentes en memoria.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-199">A user-interface snap-in through which administrators and developers can create, configure, and maintain COM+ applications, as well as administer distributed transactions and memory-resident databases.</span></span> <span data-ttu-id="9a6a3-200">La herramienta administrativa Servicios de componentes también se puede usar para ver eventos del sistema y administrar servicios del sistema locales en el equipo en el que está instalada la herramienta.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-200">The Component Services administrative tool can also be used to view system events and manage system services local to the computer on which the tool is installed.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**modelo conceptual**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**conceptual model**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-202">El primer paso de la fase de diseño de la aplicación COM+, donde el desarrollador define los problemas empresariales que se van a resolver y decide qué componentes y servicios son necesarios.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-202">The first step in the COM+ application design phase, where the developer defines the business problems to be solved and decides what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**simultaneidad**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**concurrency**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-204">La capacidad de más de una transacción o proceso para tener acceso a los mismos datos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-204">The ability of more than one transaction or process to access the same data at the same time.</span></span> <span data-ttu-id="9a6a3-205">COM+ normalmente administra la simultaneidad a través de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-205">COM+ generally manages concurrency through synchronization.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**componente configurado**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**configured component**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-207">Componente COM que se ha instalado en una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-207">A COM component that has been installed into a COM+ application.</span></span> <span data-ttu-id="9a6a3-208">Una vez instalado, el componente se configura en el catálogo de COM+ para que use los servicios COM+ disponibles.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-208">After it is installed, the component is configured within the COM+ catalog to make use of the available COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**contexto**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-210">Conjunto de propiedades de tiempo de ejecución asociadas a uno o varios objetos COM que se usan para proporcionar servicios para esos objetos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-210">A set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span> <span data-ttu-id="9a6a3-211">Cada objeto COM se ejecuta en un contexto único desde la activación hasta la desactivación (siempre dentro del mismo apartamento).</span><span class="sxs-lookup"><span data-stu-id="9a6a3-211">Every COM object runs in a single context from activation to deactivation (always within the same apartment).</span></span> <span data-ttu-id="9a6a3-212">Se inicializa cuando se activa un objeto, las propiedades de contexto, como las propiedades de contexto de seguridad, representan las necesidades de tiempo de ejecución de un objeto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-212">Initialized when an object is activated, context properties, such as security context properties, represent the run-time needs of an object.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**capa de datos**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**data tier**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-214">En el modelo de arquitectura de tres niveles para aplicaciones empresariales, la capa de acceso de DBMS, a la que se puede tener acceso a través del nivel intermedio o el nivel de servicios empresariales, y en ocasiones a través del nivel de presentación o el nivel de servicios de usuario.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-214">In the three-tier architecture model for business applications, the DBMS access layer, which can be accessed through the middle tier, or business services layer, and on occasion through the presentation tier, or user services layer.</span></span> <span data-ttu-id="9a6a3-215">La capa de datos consta de componentes de acceso a datos (en lugar de conexiones DBMS sin formato) para ayudar en el uso compartido de recursos y para permitir que los clientes se configuren sin necesidad de instalar las bibliotecas DBMS y los controladores ODBC en cada cliente.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-215">The data tier consists of data access components (rather than raw DBMS connections) to aid in resource sharing and to allow clients to be configured without installing the DBMS libraries and ODBC drivers on each client.</span></span> <span data-ttu-id="9a6a3-216">También se denomina *capa de servicios de datos*.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-216">Also called *data services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**quedó**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**deadlock**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-218">En aplicaciones multiproceso, problema de subprocesos que se produce cuando cada miembro de un conjunto de subprocesos está esperando a otro miembro del conjunto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-218">In multithreaded applications, a threading problem that occurs when each member of a set of threads is waiting for another member of the set.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**Delegado**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**delegation**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-220">Forma de suplantación que autoriza a un servidor a actuar en nombre de un cliente, lo que permite al servidor suplantar a los clientes a través de la red.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-220">A form of impersonation that authorizes a server to act on a client's behalf, giving the server the ability to impersonate clients over the network.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**transacción distribuida**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**distributed transaction**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-222">Una transacción que implica varios administradores de recursos, que puede estar en el mismo equipo o en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-222">A transaction that involves multiple resource managers, which can be on the same or different computers.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Coordinador de transacciones distribuidas (DTC)**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-224">Servicio del sistema que administra las transacciones y las comunicaciones relacionadas con las transacciones que se distribuyen entre dos o más administradores de recursos en uno o varios sistemas para garantizar las transacciones ACID correctas.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-224">A system service that manages transactions and transaction-related communications that are distributed across two or more resource managers on one or more systems to ensure correct ACID transactions.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**Cloaking dinámico**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**dynamic cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-226">Forma de Cloaking en la que se detecta la identidad del cliente original como el token de acceso del subproceso del servidor en cada llamada al método en el servidor que sigue en la cadena.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-226">A form of cloaking where the original client identity is discovered as the server thread access token on each method call to the downstream server.</span></span> <span data-ttu-id="9a6a3-227">Aunque la identidad que se presenta se puede determinar de forma dinámica, la sobrecarga necesaria para ello puede ser considerablemente más costosa.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-227">Although the identity that is presented can be determined dynamically, the overhead required to do this can be considerably more expensive.</span></span> <span data-ttu-id="9a6a3-228">En el caso de las aplicaciones COM+, la configuración predeterminada es para la funcionalidad de ocultación dinámica, ya que proporciona la flexibilidad que suele ser necesaria en las circunstancias que requieren el uso de la suplantación en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-228">For COM+ applications, the default configuration is for dynamic cloaking capability because it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**objeto Enumerator**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**enumerator object**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-230">Permite la enumeración de elementos en una colección.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-230">Enables enumeration of items in a collection.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**ceso**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**event**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-232">Acción reconocida por un objeto, como hacer clic con el mouse o presionar una tecla, y para la que puede escribir código para responder.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-232">An action recognized by an object, such as clicking the mouse or pressing a key, and for which you can write code to respond.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**objeto de clase de evento**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**event class object**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-234">Componente configurado que proporciona un registro persistente en el sistema de eventos COM+ para describir los publicadores y las interfaces de activación asociadas a esos publicadores.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-234">A configured component that provides a persistent record in the COM+ event system to describe the publishers and the firing interfaces associated with those publishers.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**Event (método)**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**event method**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-236">Método en una interfaz de COM+ que identifica un evento de COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-236">A method in a COM+ interface that identifies a COM+ event.</span></span> <span data-ttu-id="9a6a3-237">Los métodos de evento deben tener un nombre único y solo pueden contener parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-237">Event methods must be uniquely named and can contain only input parameters.</span></span> <span data-ttu-id="9a6a3-238">El valor devuelto debe ser **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-238">The return value must be an **HRESULT**.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**objeto de evento**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**event object**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-240">Objeto COM que puede señalar uno o más subprocesos que se ha producido un evento.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-240">A COM object that can signal one or more threads that an event has occurred.</span></span> <span data-ttu-id="9a6a3-241">Cualquier subproceso de un proceso puede crear un objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-241">Any thread within a process can create an event object.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**excepcional**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**exception**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-243">Una condición anómala o un error que se produce durante la ejecución de un programa y que requiere la ejecución de software fuera del flujo de control normal.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-243">An abnormal condition or error that occurs during the execution of a program and that requires the execution of software outside the normal flow of control.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**muta**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**failover**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-245">En un sistema de red de clústeres, proceso de reubicación de un recurso sobrecargado o con errores, como un servidor, una unidad de disco o una red, a su componente de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-245">In a cluster network system, the process of relocating an overloaded or failed resource—such as a server, a disk drive, or a network—to its backup component.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**proceso de subprocesamiento libre**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**free-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-247">Proceso que tiene un apartamento multiproceso y sin apartamentos de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-247">A process that has a multithreaded apartment and no single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**Coordinador de confirmaciones globales**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**global commit coordinator**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-249">En un sistema de transacciones distribuidas basado en Microsoft Windows, el administrador de transacciones raíz del árbol de confirmación.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-249">On a Microsoft Windows–based distributed transaction system, the root transaction manager of the commit tree.</span></span> <span data-ttu-id="9a6a3-250">Este Coordinador toma la decisión de confirmar o anular una transacción determinada y nunca está en duda.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-250">This coordinator makes the decision to either commit or abort a given transaction and is never in doubt.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**suplantación**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-252">La capacidad de un subproceso de ejecutarse en un contexto de seguridad diferente del proceso que posee el subproceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-252">The ability of a thread to execute in a security context different from that of the process owning the thread.</span></span> <span data-ttu-id="9a6a3-253">El subproceso de servidor utiliza un token de acceso que representa las credenciales del cliente y, con esto, puede tener acceso a los recursos a los que el cliente puede tener acceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-253">The server thread uses an access token representing the client's credentials, and with this, it can access resources that the client can access.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**nivel de suplantación**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**impersonation level**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-255">La configuración utilizada por el cliente para conceder al servidor un nivel de autoridad determinado para llevar a cabo acciones en el nombre del cliente.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-255">The setting used by the client to grant the server a particular level of authority to carry out actions on the client's behalf.</span></span> <span data-ttu-id="9a6a3-256">En COM+, solo se puede establecer para aplicaciones de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-256">In COM+, this can be set only for COM+ server applications.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**intercepción**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**interception**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-258">Para un objeto activado en un contexto determinado, el proceso de control de las llamadas a ese objeto a través del límite del contexto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-258">For an object activated in a given context, the process of handling calls to that object from across the context boundary.</span></span> <span data-ttu-id="9a6a3-259">Las llamadas en contexto se controlan con servidores proxy de interfaz ligera que controlarán cualquier mediación necesaria para ajustar el entorno en tiempo de ejecución desde uno que admita al llamador a uno que admita el destinatario.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-259">Calls across context are handled with lightweight interface proxies that will handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interfaz**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-261">En la programación basada en COM, colección de funciones públicas relacionadas que proporcionan acceso a un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-261">In COM-based programming, a collection of related public functions that provide access to a COM object.</span></span> <span data-ttu-id="9a6a3-262">El conjunto de interfaces de un objeto COM se compone de un contrato que especifica cómo los programas y otros objetos pueden interactuar con el objeto COM.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-262">The set of interfaces on a COM object composes a contract that specifies how programs and other objects can interact with the COM object.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**proxy de interfaz**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**interface proxy**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-264">Objeto específico de la interfaz que empaqueta (calcula las referencias) de los parámetros de esa interfaz como preparación para una llamada de método remoto y desempaqueta (no calcula las referencias) de los valores devueltos desde el código auxiliar de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-264">An interface-specific object that packages (marshals) parameters for that interface in preparation for a remote method call and unpackages (unmarshals) the return values from the interface stub.</span></span> <span data-ttu-id="9a6a3-265">Un proxy se ejecuta en el espacio de direcciones del remitente y se comunica con el código auxiliar correspondiente en el espacio de direcciones del receptor.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-265">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**código auxiliar de la interfaz**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**interface stub**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-267">Objeto específico de la interfaz que desempaqueta los parámetros de cálculo de referencias, llama al método necesario y los paquetes (serialización) devuelven valores del método llamado.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-267">An interface-specific object that unpackages marshaled parameters, calls the required method, and packages (marshals) return values from the called method.</span></span> <span data-ttu-id="9a6a3-268">El código auxiliar se ejecuta en el espacio de direcciones del receptor y se comunica con el proxy de interfaz correspondiente en el espacio de direcciones del remitente.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-268">The stub runs in the receiver's address space and communicates with a corresponding interface proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**interior (objeto)**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**interior object**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-270">En una jerarquía transaccional, cualquier objeto bajo el objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-270">In a transactional hierarchy, any object under the root object.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**activación Just-in-Time (JIT)**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**just-in-time (JIT) activation**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-272">Servicio automático proporcionado por COM+ que permite usar de forma más productiva los recursos del servidor inactivos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-272">An automatic service provided by COM+ that allows idle server resources to be used more productively.</span></span> <span data-ttu-id="9a6a3-273">Cuando un componente se configura como activado JIT, COM+ puede desactivar una instancia de él mientras un cliente todavía mantiene una referencia activa al objeto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-273">When a component is configured as JIT activated, COM+ can deactivate an instance of it while a client still holds an active reference to the object.</span></span> <span data-ttu-id="9a6a3-274">La próxima vez que el cliente llame a un método en el objeto, COM+ volverá a activar el objeto de forma transparente para el cliente, justo a tiempo.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-274">The next time the client calls a method on the object, COM+ will reactivate the object transparently to the client, just in time.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**componente heredado**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**legacy component**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-276">Componente no configurado que se ha instalado en una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-276">An unconfigured component that has been installed into a COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**Escucha**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**listener**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-278">Un elemento arquitectónico del servicio de componentes en cola de COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-278">An architectural element of the COM+ Queued Components service.</span></span> <span data-ttu-id="9a6a3-279">El agente de escucha es un objeto COM que abre la cola de mensajes asociada a su aplicación host y espera a que lleguen los mensajes.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-279">The listener is a COM object that opens the message queue associated with its host application and waits for messages to arrive.</span></span> <span data-ttu-id="9a6a3-280">A medida que llegan los mensajes, el agente de escucha envía los subprocesos que procesan los mensajes.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-280">As messages arrive, the listener dispatches threads that process messages.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**modelo lógico**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**logical model**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-282">El segundo paso de un proceso de diseño de la aplicación COM+, donde el modelo conceptual se divide en los niveles lógicos de la arquitectura de tres niveles, como se indica a continuación: el nivel de presentación o los servicios de usuario; el nivel intermedio o servicios empresariales; y el nivel de datos o Data Services.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-282">The second step in a COM+ application design process, where the conceptual model is broken out into the logical tiers of the three-tier architecture, as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**evento de acoplamiento flexible**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**loosely coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-284">Evento cuyo remitente (publicador) y receptor (suscriptor) no están estrechamente enlazados.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-284">An event whose sender (publisher) and receiver (subscriber) are not closely bound.</span></span> <span data-ttu-id="9a6a3-285">En un sistema de eventos de acoplamiento flexible, como los eventos COM+, la información de eventos de distintos publicadores se conserva en un almacén de eventos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-285">In a loosely coupled event system, such as COM+ Events, event information from different publishers is persisted in an event store.</span></span> <span data-ttu-id="9a6a3-286">Los suscriptores consultan este almacén y seleccionan los eventos que desean recibir.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-286">Subscribers query this store and select the events that they want to receive.</span></span> <span data-ttu-id="9a6a3-287">La selección de información de eventos del almacén de eventos crea una suscripción.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-287">Selecting event information from the event store creates a subscription.</span></span> <span data-ttu-id="9a6a3-288">Cuando se produce un evento, el sistema de eventos busca en esta base de datos y busca los suscriptores interesados, crea un nuevo objeto de cada clase interesada y llama a un método en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-288">When an event occurs, the event system looks in this database and finds the interested subscribers, creates a new object of each interested class, and calls a method on that object.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**serialización**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-290">Proceso de empaquetar y desempaquetar los parámetros de método de interfaz en los límites de subprocesos o procesos para que pueda tener lugar una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-290">The process of packaging and unpackaging interface method parameters across thread or process boundaries so that a remote procedure call can take place.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**Movedor de mensajes**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**message mover**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-292">El elemento arquitectónico del servicio de componentes en cola de COM+ que mueve los mensajes con errores a su cola de entrada para que se puedan volver a intentar.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-292">The architectural element of the COM+ Queued Components service that moves failed messages back to their input queue so that they can be retried.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**evento meta**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-event**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-294">Tipo de evento utilizado por el sistema de eventos COM+ para notificar a los suscriptores interesados cada vez que se crean, modifican o quitan suscripciones o objetos de clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-294">A type of event used by the COM+ Events system to notify interested subscribers whenever event class objects or subscriptions are created, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**forma**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**method**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-296">En la programación basada en COM, proceso que realiza un objeto COM cuando recibe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-296">In COM-based programming, a process performed by a COM object when it receives a message.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**nivel intermedio**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**middle tier**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-298">En el modelo de arquitectura de tres niveles para aplicaciones empresariales, la capa que comprende las reglas de lógica de negocios y de datos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-298">In the three-tier architecture model for business applications, the layer comprising the business logic and data rules.</span></span> <span data-ttu-id="9a6a3-299">Los componentes que componen el nivel intermedio se pueden usar para aplicar reglas de negocios, como algoritmos de negocio, normativas legales o gubernamentales y reglas de datos, que están diseñadas para mantener la coherencia de las estructuras de datos en bases de datos específicas o varias.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-299">The components that make up the middle tier can be used to enforce business rules, such as business algorithms, legal or governmental regulations, and data rules, which are designed to keep the data structures consistent within either specific or multiple databases.</span></span> <span data-ttu-id="9a6a3-300">Dado que estos componentes de nivel intermedio no están asociados a un cliente específico, pueden ser utilizados por todas las aplicaciones y pueden moverse a ubicaciones diferentes, ya que el tiempo de respuesta y otras reglas requieren.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-300">Because these middle-tier components are not tied to a specific client, they can be used by all applications and can be moved to different locations as response time and other rules require.</span></span> <span data-ttu-id="9a6a3-301">También se denomina *capa de servicios empresariales* o *nivel de lógica de negocios*.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-301">Also called *business services layer* or *business logic tier*.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**proceso de modelo mixto**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**mixed model process**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-303">Proceso que tiene un apartamento multiproceso y uno o más apartamentos de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-303">A process that has a multithreaded apartment and one or more single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**Nike**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-305">Nombre que identifica de forma única un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-305">A name that uniquely identifies a COM object.</span></span> <span data-ttu-id="9a6a3-306">Del mismo modo que una ruta de acceso identifica un archivo en el sistema de archivos, un moniker identifica un objeto COM en el espacio de nombres de directorio.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-306">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**archivo. msi**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi file**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-308">Archivo creado por la herramienta administrativa Servicios de componentes cuando se exporta una aplicación COM+ o un proxy de aplicación para su instalación en otro equipo.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-308">A file created by the Component Services administrative tool when you export a COM+ application or application proxy for installation on another computer.</span></span> <span data-ttu-id="9a6a3-309">El archivo. msi se puede instalar en cualquier cliente basado en Windows mediante Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-309">The .msi file can be installed on any Windows-based client using Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**modelo de Apartamento multiproceso**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**multithreaded apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-311">Modelo de apartamento en el que todos los subprocesos del proceso que se han inicializado como subproceso libre se encuentran en un único apartamento.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-311">An apartment model in which all the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span> <span data-ttu-id="9a6a3-312">Por lo tanto, no hay necesidad de calcular las referencias entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-312">Therefore, there is no need to marshal between threads.</span></span> <span data-ttu-id="9a6a3-313">Los subprocesos no necesitan recuperar y enviar mensajes porque COM no utiliza los mensajes de ventana de este modelo.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-313">The threads need not retrieve and dispatch messages because COM does not use window messages in this model.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**transacción anidada**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**nested transaction**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-315">Una transacción secundaria iniciada desde dentro de un límite de transacción principal o primario existente.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-315">A secondary transaction initiated from within an existing primary or parent transaction boundary.</span></span> <span data-ttu-id="9a6a3-316">La transacción principal no se confirma hasta que se confirman todas las transacciones subordinadas, o anidadas.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-316">The primary transaction does not commit until all of its subordinate, or nested, transactions commit.</span></span> <span data-ttu-id="9a6a3-317">COM+ no admite transacciones anidadas.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-317">COM+ does not support nested transactions.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**modelo de Apartamento neutro**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**neutral apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-319">Modelo de subprocesos en el que los objetos siguen las instrucciones para apartamentos multiproceso pero se pueden ejecutar en cualquier tipo de subproceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-319">A threading model in which objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="9a6a3-320">El modelo de Apartamento neutro es el modelo de subprocesos recomendado para los componentes COM y las aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-320">The neutral apartment model is the recommended threading model for COM components and COM+ applications.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**objeto persistente**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**persistent object**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-322">Objeto COM que puede guardar su estado interno cuando lo pide un cliente y que se ajusta a los estándares definidos por COM a través de los cuales los clientes pueden solicitar que los objetos se inicialicen, carguen y guarden en un almacén de datos (por ejemplo, archivo sin formato, almacenamiento estructurado o memoria).</span><span class="sxs-lookup"><span data-stu-id="9a6a3-322">A COM object that can save its internal state when asked to do so by a client and that conforms to COM-defined standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="9a6a3-323">Es responsabilidad del cliente administrar la ubicación donde se almacenan los datos persistentes del objeto, pero no el formato de los datos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-323">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**interfaz de objeto persistente**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**persistent object interface**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-325">Una interfaz COM implementada por un objeto persistente.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-325">A COM interface implemented by a persistent object.</span></span> <span data-ttu-id="9a6a3-326">Los clientes usan interfaces de objeto persistentes para indicar a esos objetos persistentes Cuándo y dónde almacenar su estado.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-326">Clients use persistent object interfaces to tell those persistent objects when and where to store their state.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**interfaz de notificación de fase cero**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**phase zero notification interface**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-328">Interfaz COM+ que permite a las aplicaciones detectar cuándo está preparada una transacción para continuar con un protocolo de confirmación en dos fases, de modo que pueda realizar las operaciones de notificación necesarias y comunicarse con el administrador de transacciones cuando se hayan completado las operaciones.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-328">COM+ interface that allows applications to detect when a transaction is ready to proceed with a two-phase commit protocol so that it can perform the necessary notification operations and communicate to the transaction manager when the operations have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**modelo físico**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**physical model**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-330">El tercer y último paso del proceso de diseño de la aplicación COM+, donde el desarrollador determina dónde residen los componentes físicamente y cómo se van a codificar.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-330">The third and final step in the COM+ application design process, where the developer determines where the components reside physically and how they are to be coded.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**encargado**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**player**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-332">El elemento arquitectónico del servicio de componentes en cola COM+ que recupera el mensaje de una cola y, a continuación, carga el objeto de servidor y los códigos auxiliares de la interfaz estándar para quitar las referencias de los datos e invocar métodos de servidor.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-332">The architectural element of the COM+ Queued Components service that retrieves the message from a queue and then loads the server object and the standard interface stubs to unmarshal data and invoke server methods.</span></span> <span data-ttu-id="9a6a3-333">El reproductor Anula la serialización del contexto de seguridad del cliente en el lado del servidor y, a continuación, invoca el componente del servidor y realiza las mismas llamadas al método.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-333">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="9a6a3-334">El reproductor no reproduce las llamadas al método hasta que el componente de cliente finaliza y la transacción que registra el método llama a las confirmaciones.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-334">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**nivel de presentación**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**presentation tier**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-336">En el modelo de arquitectura de tres niveles para aplicaciones empresariales, la capa que presenta los datos al usuario y, opcionalmente, permite la manipulación de datos y la entrada de datos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-336">In the three-tier architecture model for business applications, the layer that presents data to the user and optionally permits data manipulation and data entry.</span></span> <span data-ttu-id="9a6a3-337">Los dos tipos principales de interfaz de usuario para el nivel de presentación son la aplicación tradicional y la aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-337">The two main types of user interface for the presentation tier are the traditional application and the Web-based application.</span></span> <span data-ttu-id="9a6a3-338">También se denomina *nivel de servicios de usuario*.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-338">Also called *user services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**token de acceso principal**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**primary access token**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-340">Describe el contexto de seguridad de la cuenta de usuario asociada a un proceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-340">Describes the security context of the user account associated with a process.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**Administrador de proxy**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-342">En el cálculo de referencias estándar, componente que administra todos los proxies de interfaz para un solo objeto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-342">In standard marshaling, a component that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo-objeto**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo-object**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-344">Un tipo de objeto contenido, como una selección de usuario en un documento, un rango de celdas de una hoja de cálculo o un intervalo de caracteres en un documento de texto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-344">A type of contained object, such as a user selection in a document, a range of cells in a spreadsheet, or a range of characters in a text document.</span></span> <span data-ttu-id="9a6a3-345">Este tipo de objeto se denomina pseudo objeto porque no se trata como un objeto distinto hasta que un usuario marca la selección.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-345">This type of object is called a pseudo-object because it isn't treated as a distinct object until a user marks the selection.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**publicador**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**publisher**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-347">Remitente de un evento.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-347">The sender of an event.</span></span> <span data-ttu-id="9a6a3-348">En la arquitectura de eventos COM+, el publicador hace que la llamada al método inicie un evento.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-348">In the COM+ Events architecture, the publisher makes the method call to initiate an event.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**moniker de cola**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**queue moniker**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-350">Moniker utilizado para activar un componente en cola.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-350">The moniker used to activate a queued component.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**condición de carrera**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**race condition**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-352">En una aplicación multiproceso, condición que se produce cuando varios subprocesos tienen acceso a un elemento de datos sin coordinación, posiblemente produciendo resultados incoherentes, dependiendo del subproceso que llegue primero al elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-352">In a multithreaded application, a condition that occurs when multiple threads access a data item without coordination, possibly causing inconsistent results, depending on which thread reaches the data item first.</span></span> <span data-ttu-id="9a6a3-353">COM proporciona algunas funciones diseñadas específicamente para ayudar a evitar condiciones de carrera en servidores fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-353">COM supplies some functions specifically designed to help avoid race conditions in out-of-process servers.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**reproductor**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**recorder**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-355">El elemento arquitectónico del servicio de componentes en cola COM+ que calcula las referencias del contexto de seguridad del cliente en un mensaje y registra todas las llamadas de método para un objeto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-355">The architectural element of the COM+ Queued Components service that marshals the client's security context into a message and records all of the method calls for an object.</span></span> <span data-ttu-id="9a6a3-356">La grabadora es un administrador proxy proporcionado por el sistema que selecciona interfaces de las interfaces queuable en el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-356">The recorder is a system-provided proxy manager that selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**dispensador de recursos**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**resource dispenser**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-358">En el modelo de programación COM+, componente que administra el estado compartido no duradero en nombre de los componentes de la aplicación dentro de un proceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-358">In the COM+ programming model, a component that manages nondurable shared state on behalf of the application components within a process.</span></span> <span data-ttu-id="9a6a3-359">Los distribuidores de recursos son similares a los administradores de recursos, pero sin la garantía de durabilidad.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-359">Resource dispensers are similar to resource managers but without the guarantee of durability.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Administrador de recursos**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-361">Servicio que administra datos persistentes o duraderos en bases de datos, colas de mensajes duraderas o sistemas de archivos transaccionales.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-361">A service that manages persistent or durable data in databases, durable message queues, or transactional file systems.</span></span> <span data-ttu-id="9a6a3-362">Es el administrador de recursos que sabe cómo almacenar datos y realizar la recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-362">It is the resource manager that knows how to store data and perform disaster recovery.</span></span> <span data-ttu-id="9a6a3-363">Las aplicaciones de servidor COM+ usan administradores de recursos para mantener el estado duradero de una aplicación, como el registro de inventario a mano, los pedidos pendientes y las cuentas por cobrar.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-363">COM+ server applications use resource managers to maintain the durable state of an application, such as the record of inventory on hand, pending orders, and accounts receivable.</span></span> <span data-ttu-id="9a6a3-364">Los administradores de recursos trabajan en cooperación con Microsoft Coordinador de transacciones distribuidas (DTC) para garantizar la atomicidad y el aislamiento de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-364">Resource managers work in cooperation with the Microsoft Distributed Transaction Coordinator (DTC) to guarantee atomicity and isolation to an application.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**seguridad basada en roles**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**role-based security**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-366">Servicio de seguridad COM+ proporcionado para aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-366">A COM+ security service provided for COM+ applications.</span></span> <span data-ttu-id="9a6a3-367">Un rol representa una categoría de usuarios definidos para una aplicación COM+ con el fin de determinar los permisos de acceso a los recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-367">A role represents a category of users defined for a COM+ application for the purpose of determining access permissions to the application's resources.</span></span> <span data-ttu-id="9a6a3-368">Los roles los asigna un programador a los componentes, interfaces y métodos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-368">Roles are assigned by a developer to components, interfaces, and methods.</span></span> <span data-ttu-id="9a6a3-369">Los usuarios son asignados por un administrador a los roles adecuados, lo que permite a un usuario dentro de un rol determinado tener acceso a los recursos a los que está asignado ese rol.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-369">Users are assigned by an administrator to appropriate roles, enabling a user within a given role to access any resources to which that role is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**objeto raíz**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**root object**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-371">El primer objeto de una transacción, denominado raíz de la transacción, y siempre se coloca en un nuevo límite transaccional.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-371">The first object of a transaction, called the root of the transaction, and always placed in a new transactional boundary.</span></span> <span data-ttu-id="9a6a3-372">Solo puede haber un objeto raíz en una transacción.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-372">There can be only one root object in a transaction.</span></span> <span data-ttu-id="9a6a3-373">Todos los demás objetos de la jerarquía transaccional bajo el objeto raíz se denominan objetos interiores.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-373">All other objects in the transactional hierarchy under the root object are called interior objects.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**Administrador de transacciones raíz**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**root transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-375">Administrador de transacciones en el sistema que inicia una transacción.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-375">The transaction manager on the system that initiates a transaction.</span></span> <span data-ttu-id="9a6a3-376">La transacción no se finaliza hasta que el administrador de transacciones raíz determina el estado de la transacción (confirmada o anulada).</span><span class="sxs-lookup"><span data-stu-id="9a6a3-376">The transaction is not finalized until the root transaction manager determines the transaction's status (either committed or aborted).</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**semáforo**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**semaphore**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-378">Objeto de kernel que se usa para arbitrar el acceso a un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-378">A kernel object used to arbitrate access to a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Administrador de control de servicios (SCM)**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**service control manager (SCM)**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-380">Proceso de Microsoft Windows Server que administra todos los servicios del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-380">A Microsoft Windows server process that manages all the services in the Windows registry.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**Administrador de propiedades compartidas (SPM)**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**shared property manager (SPM)**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-382">En com+, un dispensador de recursos que puede usar para compartir el estado no persistente entre varios objetos dentro de un proceso de servidor.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-382">In Com+, a resource dispenser that you can use to share nonpersistent state among multiple objects within a server process.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**proceso de un solo subproceso**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**single-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-384">Proceso que consta de un solo apartamento de un solo subproceso, que a su vez consta de exactamente un subproceso.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-384">A process that consists of just one single-threaded apartment, which in turn consists of exactly one thread.</span></span> <span data-ttu-id="9a6a3-385">Todos los objetos COM que residen en un contenedor uniproceso pueden recibir llamadas a métodos solo de un subproceso que pertenezca a ese apartamento.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-385">All COM objects that live in a single-threaded apartment can receive method calls from only the one thread that belongs to that apartment.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**JABÓN**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-387">Protocolo simple basado en XML para intercambiar información estructurada y de tipos en la Web.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-387">A simple, XML-based protocol for exchanging structured and type information on the Web.</span></span> <span data-ttu-id="9a6a3-388">El Protocolo no contiene semántica de aplicación o de transporte, lo que hace que sea muy modular y extensible.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-388">The protocol contains no application or transport semantics, which makes it highly modular and extensible.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**dividir registro**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**split registration**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-390">En el caso de los componentes que ya tienen componentes COM existentes y que se usan en el entorno de servicios COM+, la disposición de registro en la que se almacena el aspecto COM básico del registro en el registro de Windows y los nuevos servicios y atributos de COM+ (por ejemplo, los componentes en cola) se almacenan en la base de datos de registro de COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-390">For components that are already existing COM components and are used in the COM+ services environment, the registration arrangement in which the basic COM aspect of the registration is stored in the Windows registry and new COM+ services and attributes (for example, Queued Components) are stored in the COM+ Registration Database.</span></span> <span data-ttu-id="9a6a3-391">Cada atributo de componente se almacena en el registro de Windows o en la base de datos de registro de COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-391">Each component attribute is stored in either the Windows registry or the COM+ Registration Database.</span></span> <span data-ttu-id="9a6a3-392">Los nuevos componentes COM se registran exclusivamente en la base de datos de registro de COM+, con algunas duplicaciones en el registro de Windows para que las herramientas existentes puedan utilizarlos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-392">New COM components are registered exclusively in the COM+ Registration Database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**con estado**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**stateful**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-394">De o perteneciente a un sistema o proceso que supervisa todos los detalles del estado de una actividad en la que participa.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-394">Of or pertaining to a system or process that monitors all details of the state of an activity in which it participates.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**sin estado**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**stateless**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-396">De o perteneciente a un sistema o proceso que participa en la actividad sin supervisar todos los detalles de su estado.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-396">Of or pertaining to a system or process that participates in activity without monitoring all details of its state.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**Cloaking estático**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**static cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-398">Forma de esconder dónde se puede presentar la identidad del cliente original una vez en un servidor de nivel inferior, estableciendo la identidad del cliente original una vez en el proxy.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-398">A form of cloaking where the original client identity can be presented once to a downstream server, setting the original client identity once on the proxy.</span></span> <span data-ttu-id="9a6a3-399">Esta identidad del cliente se presenta como un token de subproceso de servidor que se usará en las llamadas de método posteriores.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-399">This client identity is presented as a server thread token that will be used on subsequent method calls.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**suscriptor**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**subscriber**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-401">Receptor de un evento.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-401">The receiver of an event.</span></span> <span data-ttu-id="9a6a3-402">En la arquitectura de eventos COM+, el suscriptor recibe las llamadas realizadas por el publicador.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-402">In the COM+ Events architecture, the subscriber receives the calls made by the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**objeto de suscripción**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**subscription object**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-404">En el sistema de eventos COM+, objeto creado por un suscriptor para solicitar y administrar la entrega de eventos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-404">In the COM+ Events system, an object created by a subscriber to request and manage the delivery of events.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**sincronización**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**synchronization**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-406">En COM+, servicio que fluye del componente al componente y prohíbe que más de un llamador escriba el componente en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-406">In COM+, a service that flows from component to component and prohibits more than one caller from entering the component at any given time.</span></span> <span data-ttu-id="9a6a3-407">La sincronización determina si los subprocesos pueden enviar llamadas a un objeto.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-407">Synchronization determines when threads can dispatch calls to an object.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**modelo arquitectónico de tres niveles**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**three-tier architectural model**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-409">El marco fundamental para el modelo de diseño lógico, divide los componentes de una aplicación en tres niveles de servicio de la siguiente manera: el nivel de presentación o los servicios de usuario; el nivel intermedio o servicios empresariales; y el nivel de datos o Data Services.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-409">The fundamental framework for the logical design model, segments an application's components into three tiers of services as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span> <span data-ttu-id="9a6a3-410">Estos niveles no corresponden necesariamente a ubicaciones físicas en varios equipos de una red, sino a capas lógicas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-410">These tiers do not necessarily correspond to physical locations on various computers on a network, but rather to logical layers of the application.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**evento estrechamente acoplado**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**tightly coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-412">Evento cuyo remitente (publicador) y receptor (suscriptor) están estrechamente enlazados.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-412">An event whose sender (publisher) and receiver (subscriber) are closely bound.</span></span> <span data-ttu-id="9a6a3-413">En un sistema de eventos estrechamente acoplado, se proporciona al publicador una interfaz en la que llamar a un método cuando se produce un cambio.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-413">In a tightly coupled event system, the publisher is provided with an interface on which to call a method when a change occurs.</span></span> <span data-ttu-id="9a6a3-414">El Suscriptor sabe a qué publicador debe solicitar la notificación y las interfaces que se exponen.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-414">The subscriber knows which publisher to request notification from and the interfaces that are exposed.</span></span> <span data-ttu-id="9a6a3-415">Un sistema de eventos estrechamente acoplado requiere que tanto el publicador como el suscriptor se ejecuten en todo momento.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-415">A tightly coupled event system requires that both the publisher and the subscriber are running at all times.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**registro de seguimiento**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**trace log**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-417">Un archivo de registro generado automáticamente por Microsoft Coordinador de transacciones distribuidas que muestra los datos relacionados con una o varias transacciones distribuidas.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-417">A log file automatically generated by the Microsoft Distributed Transaction Coordinator that shows data related to one or more distributed transactions.</span></span> <span data-ttu-id="9a6a3-418">Ejemplos de datos en un registro de seguimiento son el identificador de la transacción, el tiempo de la transacción y los mensajes que indican el resultado de la transacción.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-418">Examples of data in a trace log are transaction ID, transaction time, and messages indicating the transaction outcome.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**transacción**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**transaction**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-420">Unidad de trabajo en la que se produce una serie de operaciones relacionadas durante un proceso de aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-420">A unit of work in which a series of related operations occur during an application process.</span></span> <span data-ttu-id="9a6a3-421">Una transacción se ejecuta exactamente una vez y es atómica, o bien se realiza todo el trabajo o ninguno de ellos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-421">A transaction executes exactly once and is atomic—either all of the work is done or none of it is.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Protocolo de transacciones de Internet (TIP)**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Transaction Internet Protocol (TIP)**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-423">El protocolo de Internet de transacciones es un protocolo estándar de confirmación en dos fases que permite a los administradores de transacciones heterogéneos coordinar las transacciones distribuidas, especialmente a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-423">Transaction Internet Protocol is a standard two-phase commit protocol that enables heterogeneous transaction managers to coordinate distributed transactions, especially over the Internet.</span></span> <span data-ttu-id="9a6a3-424">El protocolo TIP de confirmación en dos fases es fácil de implementar y es independiente del Protocolo de comunicaciones de aplicación a aplicación, de modo que se pueda usar con cualquier protocolo de aplicación, pero especialmente con HTTP.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-424">The TIP two-phase commit protocol is simple to implement and is independent of the application-to-application communications protocol, such that it may be used with any application protocol but especially HTTP.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**Administrador de transacciones**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-426">La parte de Microsoft Coordinador de transacciones distribuidas (DTC) que se ejecuta en cada equipo que participa en una transacción distribuida y administra las actividades relacionadas con la confirmación o anulación de esa parte de la transacción.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-426">The part of the Microsoft Distributed Transaction Coordinator (DTC) that executes on each computer participating in a distributed transaction and manages the activities related to committing or aborting that part of the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**aplicación de procesamiento de transacciones**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**transaction processing application**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-428">Colección de operaciones de transacción que automatizan una tarea empresarial determinada.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-428">A collection of transaction operations that automate a given business task.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**sistema de procesamiento de transacciones**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**transaction processing system**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-430">Un sistema completo, que incluye el hardware y el software del equipo, que hospeda una aplicación de procesamiento de transacciones para realizar las transacciones rutinarias necesarias para llevar a cabo la actividad empresarial.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-430">A complete system, comprising both computer hardware and software, that hosts a transaction processing application to perform routine transactions necessary to conduct business.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**Protocolo de confirmación en dos fases**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**two-phase commit protocol**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-432">Un protocolo utilizado únicamente en las transacciones distribuidas garantiza que el resultado de una transacción es coherente en todos los administradores de transacciones que participan en la transacción.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-432">A protocol used only in distributed transactions, ensures that the outcome of a transaction is consistent across all transaction managers participating in the transaction.</span></span> <span data-ttu-id="9a6a3-433">El protocolo opera en dos fases distintas para confirmar o anular una transacción en última instancia: la fase uno evalúa la condición de cada administrador de recursos y la fase dos completa la transacción.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-433">The protocol operates in two distinct phases to ultimately commit or abort a transaction: phase one evaluates the condition of each resource manager, and phase two completes the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**componente no configurado**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**unconfigured component**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-435">Componente COM que no se ha configurado en el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-435">A COM component that has not been configured within the COM+ catalog.</span></span> <span data-ttu-id="9a6a3-436">Los componentes no configurados no pueden hacer uso de servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-436">Unconfigured components cannot make use of COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**situación**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**whereabouts**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-438">Para las transacciones DTC, una estructura de datos opaca que representa la dirección del administrador de transacciones del administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-438">For DTC transactions, an opaque data structure that represents the address of the resource manager's transaction manager.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**Interfaces XA**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA interfaces**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-440">Conjunto estándar de interfaces de programación que permiten a los desarrolladores de aplicaciones COM+ tener acceso a las bases de datos compatibles con XA y crear administradores de recursos que operan con bases de datos relacionales, Message Queue Server, archivos transaccionales y bases de datos orientadas a objetos.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-440">A standard set of programming interfaces that allow COM+ application developers to access XA-compliant databases and create resource managers that operate with relational databases, message queuing, transactional files, and object-oriented databases.</span></span> <span data-ttu-id="9a6a3-441">Aunque Microsoft no admite directamente el protocolo XA, Microsoft admite las funciones de traducción entre las transacciones OLE y XA.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-441">Although Microsoft does not directly support the XA protocol, Microsoft does support translation facilities between OLE transactions and XA.</span></span>

</dd> <dt>

<span data-ttu-id="9a6a3-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**Servicios Web XML**</span><span class="sxs-lookup"><span data-stu-id="9a6a3-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML web services**</span></span>
</dt> <dd>

<span data-ttu-id="9a6a3-443">Unidades de lógica de aplicación que proporcionan datos y servicios a otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-443">Units of application logic providing data and services to other applications.</span></span> <span data-ttu-id="9a6a3-444">Las aplicaciones obtienen acceso a los servicios Web XML a través de protocolos web estándar, como SOAP.</span><span class="sxs-lookup"><span data-stu-id="9a6a3-444">Applications access XML web services through standard Web protocols, such as SOAP.</span></span>

</dd> </dl>

 

 
