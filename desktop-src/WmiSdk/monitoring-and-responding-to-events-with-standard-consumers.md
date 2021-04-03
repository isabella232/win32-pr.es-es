---
description: Puede usar las clases de consumidor estándar instaladas para realizar acciones basadas en eventos de un sistema operativo.
ms.assetid: 1979dc55-a440-4c31-832b-36fa84def4c9
ms.tgt_platform: multiple
title: Supervisión y respuesta a eventos con consumidores estándar
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5bd1d329cd861fa45c99851707177322d0b9d12f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "103914838"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a><span data-ttu-id="22e61-103">Supervisión y respuesta a eventos con consumidores estándar</span><span class="sxs-lookup"><span data-stu-id="22e61-103">Monitoring and Responding to Events with Standard Consumers</span></span>

<span data-ttu-id="22e61-104">Puede usar las clases de [consumidor estándar](standard-consumer-classes.md) instaladas para realizar acciones basadas en eventos de un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="22e61-104">You can use the installed [standard consumer classes](standard-consumer-classes.md) to perform actions based on events in an operating system.</span></span> <span data-ttu-id="22e61-105">Los consumidores estándar son clases simples que ya están registradas y definen clases de consumidor permanentes.</span><span class="sxs-lookup"><span data-stu-id="22e61-105">Standard consumers are simple classes that are already registered, and they define permanent consumer classes.</span></span> <span data-ttu-id="22e61-106">Cada consumidor estándar toma una acción específica después de recibir una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="22e61-106">Each standard consumer takes a specific action after it receives an event notification.</span></span> <span data-ttu-id="22e61-107">Por ejemplo, puede definir una instancia de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para ejecutar un script cuando el espacio libre en disco de un equipo es diferente de un tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="22e61-107">For example, you can define an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to execute a script when free disk space on a computer is different from a specified size.</span></span>

<span data-ttu-id="22e61-108">WMI compila los consumidores estándar en espacios de nombres predeterminados que dependen del sistema operativo, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="22e61-108">WMI compiles the standard consumers into default namespaces that depend on the operating system, for example:</span></span>

-   <span data-ttu-id="22e61-109">En Windows Server 2003, todos los consumidores estándar se compilan de forma predeterminada en el \\ espacio de nombres "suscripción raíz".</span><span class="sxs-lookup"><span data-stu-id="22e61-109">In Windows Server 2003, all of the standard consumers are compiled by default into the "Root\\Subscription" namespace.</span></span>

> [!Note]  
> <span data-ttu-id="22e61-110">Para los espacios de nombres y los sistemas operativos predeterminados que son específicos de cada clase WMI, vea las secciones comentarios y requisitos de cada tema de la clase.</span><span class="sxs-lookup"><span data-stu-id="22e61-110">For the default namespaces and operating systems that are specific for each WMI class, see the Remarks and Requirements sections of each class topic.</span></span>

 

<span data-ttu-id="22e61-111">En la tabla siguiente se enumeran y describen los consumidores estándar de WMI.</span><span class="sxs-lookup"><span data-stu-id="22e61-111">The following table lists and describes the WMI standard consumers.</span></span>



| <span data-ttu-id="22e61-112">Consumidor estándar</span><span class="sxs-lookup"><span data-stu-id="22e61-112">Standard consumer</span></span>                                              | <span data-ttu-id="22e61-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="22e61-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22e61-114">**ActiveScriptEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="22e61-114">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md) | <span data-ttu-id="22e61-115">Ejecuta un script cuando recibe una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="22e61-115">Executes a script when it receives an event notification.</span></span> <span data-ttu-id="22e61-116">Para obtener más información, vea [ejecutar un script basado en un evento](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="22e61-116">For more information, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="22e61-117">**LogFileEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="22e61-117">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)           | <span data-ttu-id="22e61-118">Escribe cadenas personalizadas en un archivo de registro de texto cuando recibe una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="22e61-118">Writes customized strings to a text log file when it receives an event notification.</span></span> <span data-ttu-id="22e61-119">Para obtener más información, consulte [escribir en un archivo de registro basado en un evento](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="22e61-119">For more information, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="22e61-120">**NTEventLogEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="22e61-120">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)     | <span data-ttu-id="22e61-121">Registra un mensaje específico en el registro de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="22e61-121">Logs a specific message to the Application event log.</span></span> <span data-ttu-id="22e61-122">Para obtener más información, vea [registrar un registro de eventos de NT basado en un evento](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="22e61-122">For more information, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="22e61-123">**SMTPEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="22e61-123">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                 | <span data-ttu-id="22e61-124">Envía un mensaje de correo electrónico mediante SMTP cada vez que se le entrega un evento.</span><span class="sxs-lookup"><span data-stu-id="22e61-124">Sends an email message by using SMTP each time an event is delivered to it.</span></span> <span data-ttu-id="22e61-125">Para obtener más información, consulte [envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="22e61-125">For more information, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="22e61-126">**CommandLineEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="22e61-126">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)   | <span data-ttu-id="22e61-127">Inicia un proceso cuando se entrega un evento a un sistema local.</span><span class="sxs-lookup"><span data-stu-id="22e61-127">Launches a process when an event is delivered to a local system.</span></span> <span data-ttu-id="22e61-128">El archivo ejecutable debe estar en una ubicación segura o estar protegido con una lista de control de acceso (ACL) segura para evitar que un usuario no autorizado Reemplace el archivo ejecutable por otro ejecutable diferente.</span><span class="sxs-lookup"><span data-stu-id="22e61-128">The executable file must be in a secure location, or secured with a strong access control list (ACL) to prevent an unauthorized user from replacing your executable with a different executable.</span></span> <span data-ttu-id="22e61-129">Para obtener más información, vea [ejecutar un programa desde la línea de comandos en función de un evento](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="22e61-129">For more information, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span> |



 

<span data-ttu-id="22e61-130">En el procedimiento siguiente se describe cómo supervisar y responder a eventos mediante un consumidor estándar.</span><span class="sxs-lookup"><span data-stu-id="22e61-130">The following procedure describes how to monitor and respond to events by using a standard consumer.</span></span> <span data-ttu-id="22e61-131">Tenga en cuenta que el procedimiento es el mismo para un archivo, un script o una aplicación de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="22e61-131">Note that the procedure is the same for a Managed Object Format (MOF) file, script, or application.</span></span>

<span data-ttu-id="22e61-132">**Para supervisar y responder a eventos con un consumidor estándar**</span><span class="sxs-lookup"><span data-stu-id="22e61-132">**To monitor and respond to events with a standard consumer**</span></span>

1.  <span data-ttu-id="22e61-133">Especifique el espacio de nombres en un archivo MOF mediante el uso del espacio de [ \# nombres pragma](pragma-namespace.md)de comandos del preprocesador MOF.</span><span class="sxs-lookup"><span data-stu-id="22e61-133">Specify the namespace in a MOF file by using the MOF preprocessor command [\#pragma namespace](pragma-namespace.md).</span></span> <span data-ttu-id="22e61-134">En un script o una aplicación, especifique el espacio de nombres en el código que se conecta a WMI.</span><span class="sxs-lookup"><span data-stu-id="22e61-134">In a script or application, specify the namespace in the code that connects to WMI.</span></span>

    <span data-ttu-id="22e61-135">En el siguiente ejemplo de código MOF se muestra cómo especificar el espacio de nombres de la \\ suscripción raíz.</span><span class="sxs-lookup"><span data-stu-id="22e61-135">The following MOF code example shows how to specify the root\\subscription namespace.</span></span>

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    <span data-ttu-id="22e61-136">La mayoría de [*los eventos intrínsecos*](gloss-i.md) están asociados a cambios en instancias de clase en el \\ espacio de nombres root cimv2.</span><span class="sxs-lookup"><span data-stu-id="22e61-136">Most [*intrinsic events*](gloss-i.md) are associated with changes to class instances in the root\\cimv2 namespace.</span></span> <span data-ttu-id="22e61-137">Sin embargo, [](/previous-versions/windows/desktop/regprov/registrykeychangeevent) \\ el [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider)desencadena los eventos del registro como RegistryKeyChangeEvent en el espacio de nombres predeterminado raíz.</span><span class="sxs-lookup"><span data-stu-id="22e61-137">However, registry events such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) are fired in the root\\default namespace by the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider).</span></span>

    <span data-ttu-id="22e61-138">Un consumidor puede incluir clases de eventos ubicadas en otros espacios de nombres especificando el espacio de nombres en la propiedad **EventNamespace** de la consulta [**\_ \_ EventFilter**](--eventfilter.md) para los eventos.</span><span class="sxs-lookup"><span data-stu-id="22e61-138">A consumer can include event classes located in other namespaces by specifying the namespace in the **EventNamespace** property in the [**\_\_EventFilter**](--eventfilter.md) query for events.</span></span> <span data-ttu-id="22e61-139">Las clases de [*eventos intrínsecos*](gloss-i.md) , como [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , están disponibles en todos los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="22e61-139">The [*intrinsic events*](gloss-i.md) classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

2.  <span data-ttu-id="22e61-140">Cree y rellene una instancia de una clase de consumidor estándar.</span><span class="sxs-lookup"><span data-stu-id="22e61-140">Create and populate an instance of a standard consumer class.</span></span>

    <span data-ttu-id="22e61-141">Esta instancia puede tener un valor único en la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="22e61-141">This instance may have a unique value in the **Name** property.</span></span> <span data-ttu-id="22e61-142">Puede actualizar un consumidor existente si reutiliza el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="22e61-142">You can update an existing consumer by reusing the same name.</span></span>

    <span data-ttu-id="22e61-143">**InsertionStringTemplates** contiene el texto que se va a insertar en un evento que se especifique en **EventType**.</span><span class="sxs-lookup"><span data-stu-id="22e61-143">**InsertionStringTemplates** contains the text to insert in an event that you specify in **EventType**.</span></span> <span data-ttu-id="22e61-144">Puede usar cadenas literales o hacer referencia directamente a una propiedad.</span><span class="sxs-lookup"><span data-stu-id="22e61-144">You can use literal strings or refer directly to a property.</span></span> <span data-ttu-id="22e61-145">Para obtener más información, vea [usar las plantillas de cadena estándar](using-standard-string-templates.md) y [la instrucción SELECT para las consultas de eventos](select-statement-for-event-queries.md).</span><span class="sxs-lookup"><span data-stu-id="22e61-145">For more information, see [Using Standard String Templates](using-standard-string-templates.md) and [SELECT Statement for Event Queries](select-statement-for-event-queries.md).</span></span>

    <span data-ttu-id="22e61-146">Use un origen existente para el registro de eventos que admita una cadena de inserción sin texto asociado.</span><span class="sxs-lookup"><span data-stu-id="22e61-146">Use an existing source for the event log that supports an insertion string without associated text.</span></span>

    <span data-ttu-id="22e61-147">En el siguiente ejemplo de código MOF se muestra cómo utilizar un origen existente de WSH y un valor **EventID** de 8.</span><span class="sxs-lookup"><span data-stu-id="22e61-147">The following MOF code example shows how to use an existing source of WSH and an **EventID** value of 8.</span></span>

    ```syntax
    instance of NTEventLogEventConsumer as $Consumer
    {
        Name = "RunKeyEventlogConsumer";
        SourceName = "WSH";               
        EventID = 8;
        // Warning                              
        EventType = 2;
        // One string supplies the entire message          
        NumberOfInsertionStrings = 1;             
        // the %Hive% and %KeyPath% are properties of
        // the RegistryKeyChangeEvent instance 
        InsertionStringTemplates = 
            {"The key %Hive%\\%RootPath% has been modified."
            "Check if the change is intentional"};
    };
    ```

3.  <span data-ttu-id="22e61-148">Cree una instancia de [**\_ \_ EventFilter**](--eventfilter.md) y defina una consulta para los eventos.</span><span class="sxs-lookup"><span data-stu-id="22e61-148">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query for events.</span></span>

    <span data-ttu-id="22e61-149">En el ejemplo siguiente, el filtro supervisa la clave del registro donde se registran los programas de inicio.</span><span class="sxs-lookup"><span data-stu-id="22e61-149">In the following example, the filter monitors the registry key where startup programs are registered.</span></span> <span data-ttu-id="22e61-150">La supervisión de esta clave del registro puede ser importante porque un programa no autorizado puede registrarse en la clave, lo que hace que se inicie cuando se inicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="22e61-150">Monitoring this registry key may be important because an unauthorized program can register itself under the key, which causes it to be launched when the computer boots.</span></span>

    ```syntax
    instance of __EventFilter as $Filter
    {
    Name = "RunKeyFilter";
    QueryLanguage = "WQL"; 
    Query = "Select * from RegistryTreeChangeEvent"
        " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
        "RootPath = \"Software\\\\Microsoft\\\\Windows"
        "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire in root\default namespace
    EventNamespace = "root\\default";                       
    };
    ```

4.  <span data-ttu-id="22e61-151">Identifique un evento para supervisar y crear una consulta de evento.</span><span class="sxs-lookup"><span data-stu-id="22e61-151">Identify an event to monitor and create an event query.</span></span>

    <span data-ttu-id="22e61-152">Puede comprobar si hay un evento intrínseco o extrínseco que use.</span><span class="sxs-lookup"><span data-stu-id="22e61-152">You can check to see if there is an intrinsic or extrinsic event that use.</span></span> <span data-ttu-id="22e61-153">Por ejemplo, utilice la clase [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) del proveedor del registro para supervisar los cambios en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="22e61-153">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="22e61-154">Si una clase no existe y describe un evento que debe supervisar, debe crear su propio proveedor de eventos y definir nuevas clases de eventos extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="22e61-154">If a class does not exist that describes an event you need to monitor, you must create your own event provider, and define new extrinsic event classes.</span></span> <span data-ttu-id="22e61-155">Para obtener más información, consulte [escribir un proveedor de eventos](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="22e61-155">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

    <span data-ttu-id="22e61-156">En un archivo MOF, puede definir un [*alias*](gloss-a.md) para el filtro y el consumidor, lo que proporciona una manera fácil de describir las rutas de acceso de instancia.</span><span class="sxs-lookup"><span data-stu-id="22e61-156">In a MOF file, you can define an [*alias*](gloss-a.md) for the filter and consumer, which provides an easy way to describe the instance paths.</span></span>

    <span data-ttu-id="22e61-157">En el ejemplo siguiente se muestra cómo definir un [*alias*](gloss-a.md) para el filtro y el consumidor.</span><span class="sxs-lookup"><span data-stu-id="22e61-157">The following example shows how to define an [*alias*](gloss-a.md) for the filter and consumer.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  <span data-ttu-id="22e61-158">Cree una instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para asociar el filtro y las clases de consumidor.</span><span class="sxs-lookup"><span data-stu-id="22e61-158">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer classes.</span></span> <span data-ttu-id="22e61-159">Esta instancia determina que cuando se produce un evento que coincide con el filtro especificado, se debe producir la acción especificada por el consumidor.</span><span class="sxs-lookup"><span data-stu-id="22e61-159">This instance determines that when an event occurs that matches the specified filter, the action specified by the consumer must occur.</span></span> <span data-ttu-id="22e61-160">[**\_ \_ EventFilter**](--eventfilter.md), [**\_ \_ EventConsumer**](--eventconsumer.md)y **\_ \_ FilterToConsumerBinding** deben tener el mismo identificador de seguridad (SID) individual en la propiedad **CreatorSID** .</span><span class="sxs-lookup"><span data-stu-id="22e61-160">[**\_\_EventFilter**](--eventfilter.md), [**\_\_EventConsumer**](--eventconsumer.md), and **\_\_FilterToConsumerBinding** must have the same individual security identifier (SID) in the **CreatorSID** property.</span></span> <span data-ttu-id="22e61-161">Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="22e61-161">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

    <span data-ttu-id="22e61-162">En el ejemplo siguiente se muestra cómo identificar una instancia por la ruta de acceso del objeto o utilizar un alias como una expresión abreviada para la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="22e61-162">The following example shows how to identify an instance by the object path, or use an alias as a shorthand expression for the object path.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    <span data-ttu-id="22e61-163">En el siguiente ejemplo se enlaza el filtro al consumidor mediante el uso de alias.</span><span class="sxs-lookup"><span data-stu-id="22e61-163">The following example binds the filter to the consumer by using aliases.</span></span>

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    <span data-ttu-id="22e61-164">Puede enlazar un filtro a varios consumidores, lo que indica que cuando se producen eventos coincidentes, se deben realizar varias acciones; o bien, puede enlazar un consumidor a varios filtros, lo que indica que la acción se debe realizar cuando se producen eventos que coinciden con uno de los filtros.</span><span class="sxs-lookup"><span data-stu-id="22e61-164">You can bind one filter to several consumers, which indicates that when matching events occur, several actions must be taken; or you can bind one consumer to several filters, which indicates that the action must be taken when events that match one of the filters occur.</span></span>

    <span data-ttu-id="22e61-165">Las siguientes acciones se realizan en función de la condición de los consumidores y eventos:</span><span class="sxs-lookup"><span data-stu-id="22e61-165">The following actions are taken based on the condition of consumers and events:</span></span>

    -   <span data-ttu-id="22e61-166">Si se produce un error en uno de los consumidores permanentes, otros consumidores que soliciten la notificación de recepción de eventos.</span><span class="sxs-lookup"><span data-stu-id="22e61-166">If one of the permanent consumers fails, other consumers that request the event receive notification.</span></span>
    -   <span data-ttu-id="22e61-167">Si se quita un evento, WMI desencadena [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="22e61-167">If an event is dropped, WMI fires [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>
    -   <span data-ttu-id="22e61-168">Si se suscribe a este evento, devuelve el evento que se quita y una referencia a [**\_ \_ EventConsumer**](--eventconsumer.md) representa el consumidor con error.</span><span class="sxs-lookup"><span data-stu-id="22e61-168">If you subscribe to this event, it returns the event that is dropped, and a reference to the [**\_\_EventConsumer**](--eventconsumer.md) represents the failed consumer.</span></span>
    -   <span data-ttu-id="22e61-169">Si se produce un error en un consumidor, WMI activa [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md), que puede contener más información en las propiedades **ErrorCode**, **ErrorDescription** y **ErrorObject** .</span><span class="sxs-lookup"><span data-stu-id="22e61-169">If a consumer fails, WMI fires [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md), which may contain more information in the **ErrorCode**, **ErrorDescription** and **ErrorObject** properties.</span></span>

    <span data-ttu-id="22e61-170">Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="22e61-170">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

## <a name="example"></a><span data-ttu-id="22e61-171">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="22e61-171">Example</span></span>

<span data-ttu-id="22e61-172">En el ejemplo siguiente se muestra el MOF para una instancia de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="22e61-172">The following example shows the MOF for an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="22e61-173">Después de compilar este MOF, cualquier intento de crear, eliminar o modificar un valor en la ruta de acceso del registro **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run** registra una entrada en el registro de eventos de la aplicación, en el origen "WSH".</span><span class="sxs-lookup"><span data-stu-id="22e61-173">After you compile this MOF, any attempt to create, delete, or modify a value in the Registry path **HKEY\_LOCAL\_MACHINE\\ Software\\Microsoft\\Windows\\CurrentVersion\\Run** logs an entry in the Application eventlog, under the source "WSH".</span></span>


```mof
#pragma namespace ("\\\\.\\root\\subscription")
 
instance of __EventFilter as $Filter
{
    Name = "RunKeyFilter";
    QueryLanguage = "WQL";
    Query = "Select * from RegistryTreeChangeEvent"
            " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
            "KeyPath = \"Software\\\\Microsoft\\\\Windows"
            "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire
    // in root\default namespace
    EventNamespace = "root\\default";   
};
 
instance of NTEventLogEventConsumer as $Consumer
{
    Name = "RunKeyEventlogConsumer";
    SourceName = "WSH";               
    EventID = 8;
    EventType = 2;                            // Warning
    Category = 0;
    NumberOfInsertionStrings = 1;

    // the %Hive% and %KeyPath% are properties
    // of the RegistryKeyChangeEvent instance 
    InsertionStringTemplates = {"The key %Hive%\\%RootPath% "
        "has been modified. Check if the change is intentional"};
};
 

// Bind the filter to the consumer
instance of __FilterToConsumerBinding
{
    Filter = $Filter;
    Consumer = $Consumer;
};
```



## <a name="related-topics"></a><span data-ttu-id="22e61-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22e61-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22e61-175">Recepción segura de eventos</span><span class="sxs-lookup"><span data-stu-id="22e61-175">Receiving Events Securely</span></span>](receiving-events-securely.md)
</dt> </dl>

 

 
