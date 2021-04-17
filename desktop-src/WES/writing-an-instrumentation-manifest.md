---
title: Escritura de un manifiesto de instrumentación
description: Las aplicaciones y los archivos dll utilizan un manifiesto de instrumentación para identificar sus proveedores de instrumentación y los eventos que escriben los proveedores.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420751"
---
# <a name="writing-an-instrumentation-manifest"></a><span data-ttu-id="e96ff-103">Escritura de un manifiesto de instrumentación</span><span class="sxs-lookup"><span data-stu-id="e96ff-103">Writing an Instrumentation Manifest</span></span>

<span data-ttu-id="e96ff-104">Las aplicaciones y los archivos dll utilizan un manifiesto de instrumentación para identificar sus proveedores de instrumentación y los eventos que escriben los proveedores.</span><span class="sxs-lookup"><span data-stu-id="e96ff-104">Applications and DLLs use an instrumentation manifest to identify their instrumentation providers and the events that the providers write.</span></span> <span data-ttu-id="e96ff-105">Un manifiesto es un archivo XML que contiene los elementos que identifican el proveedor.</span><span class="sxs-lookup"><span data-stu-id="e96ff-105">A manifest is an XML file that contains the elements that identify your provider.</span></span> <span data-ttu-id="e96ff-106">La Convención es usar. man como extensión del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="e96ff-106">The convention is to use .man as the extension for your manifest.</span></span> <span data-ttu-id="e96ff-107">El manifiesto debe cumplir el manifiesto del evento XSD.</span><span class="sxs-lookup"><span data-stu-id="e96ff-107">The manifest must conform to the event manifest XSD.</span></span> <span data-ttu-id="e96ff-108">Para más información sobre el esquema, consulte [esquema de EventManifest](eventmanifestschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="e96ff-108">For details on the schema, see [EventManifest Schema](eventmanifestschema-schema.md).</span></span>

<span data-ttu-id="e96ff-109">Un proveedor de instrumentación es cualquier aplicación o DLL que llama a las funciones [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)o [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) para escribir eventos en una sesión de seguimiento de [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) o en un canal de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="e96ff-109">An instrumentation provider is any application or DLL that calls the [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring), or [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) functions to write events to an [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) tracing session or an Event Log channel.</span></span> <span data-ttu-id="e96ff-110">Una aplicación puede definir un proveedor de instrumentación único que abarque todos los eventos que escribe o puede definir un proveedor para la aplicación y un proveedor para cada uno de sus dll.</span><span class="sxs-lookup"><span data-stu-id="e96ff-110">An application can define a single instrumentation provider that covers all events that it writes or it can define a provider for the application and a provider for each of its DLLs.</span></span> <span data-ttu-id="e96ff-111">El número de proveedores que define la aplicación en el manifiesto depende únicamente del modo en que la aplicación desea organizar los eventos que escribe.</span><span class="sxs-lookup"><span data-stu-id="e96ff-111">The number of providers that the application defines in the manifest depends solely on how the application wants to organize the events that it writes.</span></span>

<span data-ttu-id="e96ff-112">La ventaja de especificar un proveedor para cada DLL es que, a continuación, puede habilitar y deshabilitar los proveedores individuales y, por tanto, los eventos que generan.</span><span class="sxs-lookup"><span data-stu-id="e96ff-112">The advantage of specifying a provider for each DLL is that you can then enable and disable the individual providers and thus the events that they generate.</span></span> <span data-ttu-id="e96ff-113">Esta ventaja solo se aplica si el proveedor está habilitado por una sesión de seguimiento de ETW.</span><span class="sxs-lookup"><span data-stu-id="e96ff-113">This advantage applies only if the provider is enabled by an ETW tracing session.</span></span> <span data-ttu-id="e96ff-114">Cualquier evento que especifique un canal de registro de eventos siempre se escribe en ese canal.</span><span class="sxs-lookup"><span data-stu-id="e96ff-114">Any events that specify an event log channel are always written to that channel.</span></span>

<span data-ttu-id="e96ff-115">El manifiesto debe identificar el proveedor y los eventos que escribe, pero los demás metadatos, como los canales, los niveles y las palabras clave, son opcionales. la definición de los metadatos opcionales depende de quién vaya a consumir los eventos.</span><span class="sxs-lookup"><span data-stu-id="e96ff-115">The manifest must identify the provider and the events that it writes but the other metadata such as channels, levels, and keywords are optional; whether you define the optional metadata depends on who will be consuming the events.</span></span> <span data-ttu-id="e96ff-116">Por ejemplo, si los administradores o el personal de soporte técnico consumen los eventos con una herramienta como Windows Visor de eventos que lee los eventos de los canales del registro de eventos, debe definir los canales en los que se escriben los eventos.</span><span class="sxs-lookup"><span data-stu-id="e96ff-116">For example, if administrators or support personnel consume the events using a tool like the Windows Event Viewer that reads events from event log channels, then you must define the channels to which the events are written.</span></span> <span data-ttu-id="e96ff-117">Sin embargo, si el proveedor solo se va a habilitar mediante una sesión de seguimiento de ETW, no es necesario definir canales.</span><span class="sxs-lookup"><span data-stu-id="e96ff-117">However, if the provider will only be enabled by an ETW tracing session, then you do not need to define channels.</span></span>

<span data-ttu-id="e96ff-118">Aunque los metadatos de los niveles, las tareas, los códigos de operación y las palabras clave son opcionales, deben usarse para agrupar o depositar lógicamente los eventos.</span><span class="sxs-lookup"><span data-stu-id="e96ff-118">Although the levels, tasks, opcodes, and keywords metadata are optional, you should use them to logically group or bucket the events.</span></span> <span data-ttu-id="e96ff-119">La agrupación de eventos ayuda a los consumidores a consumir solo los eventos que le interesan.</span><span class="sxs-lookup"><span data-stu-id="e96ff-119">Grouping the events helps the consumers consume only those events that are of interest.</span></span> <span data-ttu-id="e96ff-120">Por ejemplo, el consumidor podría consultar todos los eventos en los que el nivel sea "crítico" y la palabra clave sea "escribir", o bien consultar todos los eventos escritos por una tarea específica.</span><span class="sxs-lookup"><span data-stu-id="e96ff-120">For example, the consumer could query for all events where level is "critical" and keyword is "write", or query for all events written by a specific task.</span></span>

<span data-ttu-id="e96ff-121">Además de los consumidores que usan el nivel y las palabras clave para consumir tipos de eventos específicos, una sesión de seguimiento de ETW puede usar los metadatos de nivel y de palabra clave para indicar a ETW que limite los eventos que se escriben en el registro de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="e96ff-121">In addition to consumers using level and keywords to consume specific types of events, an ETW tracing session can use the level and keyword metadata to tell ETW to limit the events that are written to the event tracing log.</span></span> <span data-ttu-id="e96ff-122">Por ejemplo, la sesión podría limitar los eventos a solo los eventos en los que el nivel sea "error" o "crítico" y la palabra clave sea "lectura".</span><span class="sxs-lookup"><span data-stu-id="e96ff-122">For example, the session could limit the events to only events where level is "error" or "critical" and keyword is "read".</span></span>

<span data-ttu-id="e96ff-123">Un proveedor puede definir los filtros que una sesión utiliza para filtrar los eventos en función de los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="e96ff-123">A provider can define filters that a session uses to filter the events based on event data.</span></span> <span data-ttu-id="e96ff-124">Con el nivel y las palabras clave, ETW determina si el evento se escribe en el registro, pero con filtros, el proveedor utiliza los criterios de datos de filtro para determinar si escribe el evento en esa sesión.</span><span class="sxs-lookup"><span data-stu-id="e96ff-124">With level and keywords, ETW determines whether the event is written to the log but with filters, the provider uses the filter data criteria to determine whether it writes the event to that session.</span></span> <span data-ttu-id="e96ff-125">Los filtros solo se aplican cuando una sesión de seguimiento de ETW habilita el proveedor.</span><span class="sxs-lookup"><span data-stu-id="e96ff-125">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="e96ff-126">En las secciones siguientes se muestra cómo definir los componentes del manifiesto:</span><span class="sxs-lookup"><span data-stu-id="e96ff-126">The following sections show how to define the components of the manifest:</span></span>

-   [<span data-ttu-id="e96ff-127">Identificación del proveedor</span><span class="sxs-lookup"><span data-stu-id="e96ff-127">Identifying the provider</span></span>](identifying-the-provider.md)
-   [<span data-ttu-id="e96ff-128">Definir los canales en los que se escriben los eventos</span><span class="sxs-lookup"><span data-stu-id="e96ff-128">Defining the channels to where the events are written</span></span>](defining-channels.md)
-   [<span data-ttu-id="e96ff-129">Definir los niveles de gravedad de los eventos que escribe el proveedor</span><span class="sxs-lookup"><span data-stu-id="e96ff-129">Defining the severity levels of events that the provider writes</span></span>](defining-severity-levels.md)
-   [<span data-ttu-id="e96ff-130">Definir las tareas y las operaciones que realiza el proveedor</span><span class="sxs-lookup"><span data-stu-id="e96ff-130">Defining the tasks and operations that your provider performs</span></span>](defining-tasks-and-opcodes.md)
-   [<span data-ttu-id="e96ff-131">Definir las palabras clave que clasifican los eventos que escribe el proveedor</span><span class="sxs-lookup"><span data-stu-id="e96ff-131">Defining the keywords that classify the events that the provider writes</span></span>](defining-keywords-used-to-classify-types-of-events.md)
-   [<span data-ttu-id="e96ff-132">Definir los filtros que utiliza el proveedor para filtrar los eventos que escribe</span><span class="sxs-lookup"><span data-stu-id="e96ff-132">Defining the filters that the provider uses to filter the events that it writes</span></span>](defining-filters.md)
-   [<span data-ttu-id="e96ff-133">Definir las asignaciones de nombre y valor a las que hacen referencia los datos de la plantilla</span><span class="sxs-lookup"><span data-stu-id="e96ff-133">Defining the name/value maps that your template data references</span></span>](defining-name-value-mappings.md)
-   [<span data-ttu-id="e96ff-134">Definir las plantillas que definen los datos específicos del evento</span><span class="sxs-lookup"><span data-stu-id="e96ff-134">Defining the templates that define the event-specific data</span></span>](defining-event-data-templates.md)
-   [<span data-ttu-id="e96ff-135">Definir los eventos que escribe el proveedor</span><span class="sxs-lookup"><span data-stu-id="e96ff-135">Defining the events that the provider writes</span></span>](defining-events.md)

<span data-ttu-id="e96ff-136">Aunque puede crear un manifiesto de instrumentación manualmente, debería considerar la posibilidad de usar la herramienta de ECManGen.exe que se incluye en la \\ carpeta bin de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e96ff-136">Although you can author an instrumentation manifest manually, you should consider using the ECManGen.exe tool that is included in the \\Bin folder of the Windows SDK.</span></span> <span data-ttu-id="e96ff-137">La herramienta ECManGen.exe usa una GUI que le guía a través de la creación de un manifiesto desde cero sin tener que usar etiquetas XML.</span><span class="sxs-lookup"><span data-stu-id="e96ff-137">The ECManGen.exe tool uses a GUI that guides you through creating a manifest from scratch without ever having to use XML tags.</span></span> <span data-ttu-id="e96ff-138">Conocer la información de esta sección y en la sección del [esquema EventManifest](eventmanifestschema-schema.md) le ayudará a usar la herramienta.</span><span class="sxs-lookup"><span data-stu-id="e96ff-138">Having knowledge of the information in this section and in the [EventManifest Schema](eventmanifestschema-schema.md) section will help when using the tool.</span></span>

<span data-ttu-id="e96ff-139">Si usa Visual Studio como editor XML, puede Agregar el esquema [EventManifest](eventmanifestschema-schema.md) al proyecto (vea el menú XML) para aprovechar las ventajas de IntelliSense, la validación de esquemas en línea y otras características para que la escritura del manifiesto sea fácil y precisa.</span><span class="sxs-lookup"><span data-stu-id="e96ff-139">If you use Visual Studio as your XML editor, you can add the [EventManifest](eventmanifestschema-schema.md) schema to the project (see the XML menu) to take advantage of Intellisense, inline schema validation, and other features to make writing the manifest easy and accurate.</span></span>

<span data-ttu-id="e96ff-140">Después de escribir el manifiesto, use el compilador de mensajes para validar el manifiesto y generar los archivos de recursos y de encabezado que se incluyen en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="e96ff-140">After writing your manifest, use the message compiler to validate the manifest and generate the resource and header files that you include in your provider.</span></span> <span data-ttu-id="e96ff-141">Para obtener más información, vea [compilar un manifiesto de instrumentación](compiling-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="e96ff-141">For more information, see [Compiling an Instrumentation Manifest](compiling-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="e96ff-142">En el ejemplo siguiente se muestra el esqueleto de un manifiesto de evento totalmente definido.</span><span class="sxs-lookup"><span data-stu-id="e96ff-142">The following example shows the skeleton of a fully defined event manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 