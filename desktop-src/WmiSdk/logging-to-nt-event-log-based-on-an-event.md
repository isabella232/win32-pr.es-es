---
description: La clase NTEventLogEventConsumer escribe un mensaje en el registro de eventos de Windows cuando se produce un evento especificado. Esta clase es un consumidor de eventos estándar que proporciona WMI.
ms.assetid: ca998a91-d9f7-44ff-bb83-5ba92d68f31e
ms.tgt_platform: multiple
title: Registro en el registro de eventos de NT basado en un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69bf24c0d64c95a012b8681b88bde34dc28fa179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911490"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a><span data-ttu-id="acdb7-104">Registro en el registro de eventos de NT basado en un evento</span><span class="sxs-lookup"><span data-stu-id="acdb7-104">Logging to NT Event Log Based on an Event</span></span>

<span data-ttu-id="acdb7-105">La clase [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) escribe un mensaje en el registro de eventos de Windows cuando se produce un evento especificado.</span><span class="sxs-lookup"><span data-stu-id="acdb7-105">The [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class writes a message to the Windows Event log when a specified event occurs.</span></span> <span data-ttu-id="acdb7-106">Esta clase es un consumidor de eventos estándar que proporciona WMI.</span><span class="sxs-lookup"><span data-stu-id="acdb7-106">This class is a standard event consumer that WMI provides.</span></span>

> [!Note]  
> <span data-ttu-id="acdb7-107">De forma predeterminada, los usuarios autenticados no pueden registrar los eventos en el registro de aplicaciones de un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="acdb7-107">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="acdb7-108">Como resultado, se producirá un error en el ejemplo que se describe en este tema si usa la propiedad **UNCServerName** de la clase [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) y especifica un equipo remoto como su valor.</span><span class="sxs-lookup"><span data-stu-id="acdb7-108">As a result, the example described in this topic will fail if you use the **UNCServerName** property of the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class and specify a remote computer as its value.</span></span> <span data-ttu-id="acdb7-109">Para obtener información sobre cómo cambiar la seguridad del registro de eventos, consulte este [artículo de Knowledge Base](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="acdb7-109">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

 

<span data-ttu-id="acdb7-110">El procedimiento básico para usar un consumidor estándar se describe en [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="acdb7-110">The basic procedure for using a standard consumer is described in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="acdb7-111">A continuación se indican otros pasos adicionales que se requieren al usar la clase [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="acdb7-111">The following are additional steps beyond the basic procedure, required when using the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class.</span></span> <span data-ttu-id="acdb7-112">En los pasos se describe cómo crear un consumidor de eventos que escribe en el registro de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="acdb7-112">The steps describe how to create an event consumer that writes to the Application event log.</span></span>

<span data-ttu-id="acdb7-113">En el procedimiento siguiente se describe cómo crear un consumidor de eventos que escribe en el registro de eventos de NT.</span><span class="sxs-lookup"><span data-stu-id="acdb7-113">The following procedure describes how to create an event consumer that writes to the NT Event Log.</span></span>

<span data-ttu-id="acdb7-114">**Para crear un consumidor de eventos que escribe en el registro de eventos de Windows**</span><span class="sxs-lookup"><span data-stu-id="acdb7-114">**To create an event consumer that writes to the Windows Event Log**</span></span>

1.  <span data-ttu-id="acdb7-115">En un archivo Managed Object Format (MOF), cree una instancia de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) para recibir los eventos que solicita en la consulta.</span><span class="sxs-lookup"><span data-stu-id="acdb7-115">In a Managed Object Format (MOF) file, create an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="acdb7-116">Para obtener más información sobre cómo escribir código MOF, vea [diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="acdb7-116">For more information about writing MOF code, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="acdb7-117">Cree una instancia de [**\_ \_ EventFilter**](--eventfilter.md)y asígnele el nombre y, a continuación, cree una consulta para especificar el tipo de evento que desencadena la escritura en el registro de eventos de NT.</span><span class="sxs-lookup"><span data-stu-id="acdb7-117">Create, and name, an instance of [**\_\_EventFilter**](--eventfilter.md), and then create a query to specify the type of event which triggers writing to the NT Event Log.</span></span>

    <span data-ttu-id="acdb7-118">Para obtener más información, vea [consultas con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="acdb7-118">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

3.  <span data-ttu-id="acdb7-119">Cree una instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para asociar el filtro a la instancia de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="acdb7-119">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span>
4.  <span data-ttu-id="acdb7-120">Compile el archivo MOF mediante [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="acdb7-120">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="acdb7-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="acdb7-121">Example</span></span>

<span data-ttu-id="acdb7-122">El ejemplo de esta sección está en código MOF, pero puede crear las instancias mediante programación con la API de [scripting para WMI](scripting-api-for-wmi.md) o la [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="acdb7-122">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="acdb7-123">En el ejemplo se muestra cómo crear un consumidor para escribir en el registro de eventos de aplicación mediante [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="acdb7-123">The example shows how to create a consumer to write to the Application event log by using [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="acdb7-124">El MOF crea una nueva clase denominada "NTLogCons \_ example", un filtro de eventos para consultar las operaciones, como la creación, en una instancia de esta nueva clase y un enlace entre el filtro y el consumidor.</span><span class="sxs-lookup"><span data-stu-id="acdb7-124">The MOF creates a new class named "NTLogCons\_Example", an event filter to query for operations, such as creation, on an instance of this new class, and a binding between filter and consumer.</span></span> <span data-ttu-id="acdb7-125">Dado que la última acción del MOF es crear una instancia de NTLogCons \_ ejemplo, puede ver inmediatamente el evento en el registro de eventos de aplicación ejecutando Eventvwr.exe.</span><span class="sxs-lookup"><span data-stu-id="acdb7-125">Because the last action in the MOF is to create an instance of NTLogCons\_Example, you can immediately see the event in the Application event log by running Eventvwr.exe.</span></span>

<span data-ttu-id="acdb7-126">`EventID=0x0A for SourceName="WinMgmt"`Identifica un mensaje con el siguiente texto.</span><span class="sxs-lookup"><span data-stu-id="acdb7-126">The `EventID=0x0A for SourceName="WinMgmt"` identifies a message with the following text.</span></span> <span data-ttu-id="acdb7-127">"%1", "%2", "%3" son marcadores de posición para las cadenas correspondientes especificadas en la matriz InsertionStringTemplates.</span><span class="sxs-lookup"><span data-stu-id="acdb7-127">The "%1", "%2", "%3" are placeholders for corresponding strings specified in InsertionStringTemplates array.</span></span>

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

<span data-ttu-id="acdb7-128">En el procedimiento siguiente se describe cómo utilizar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="acdb7-128">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="acdb7-129">**Para usar el ejemplo**</span><span class="sxs-lookup"><span data-stu-id="acdb7-129">**To use the example**</span></span>

1.  <span data-ttu-id="acdb7-130">Copie la siguiente lista de MOF en un archivo de texto y guárdelo con una extensión. mof.</span><span class="sxs-lookup"><span data-stu-id="acdb7-130">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="acdb7-131">En un ventana Comandos, compile el archivo MOF con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="acdb7-131">In a Command window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="acdb7-132">Nombre de archivo de **MOFCOMP** \*\* \* *. mof*\*</span><span class="sxs-lookup"><span data-stu-id="acdb7-132">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="acdb7-133">Ejecute Eventvwr.exe.</span><span class="sxs-lookup"><span data-stu-id="acdb7-133">Run Eventvwr.exe.</span></span> <span data-ttu-id="acdb7-134">Examine el registro de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="acdb7-134">Look at the Application event log.</span></span> <span data-ttu-id="acdb7-135">Debería ver un evento con ID = 10 ( **EventID**), source = "WMI" y Type = error.</span><span class="sxs-lookup"><span data-stu-id="acdb7-135">You should see an event with ID = 10 (the **EventID**), Source = "WMI", and Type = Error.</span></span>
4.  <span data-ttu-id="acdb7-136">Haga doble clic en el mensaje de **tipo de información** de WMI con 10 en la columna **evento** .</span><span class="sxs-lookup"><span data-stu-id="acdb7-136">Double-click the **Information type** message from WMI with 10 in the **Event** column.</span></span> <span data-ttu-id="acdb7-137">Se mostrará la descripción siguiente para el evento.</span><span class="sxs-lookup"><span data-stu-id="acdb7-137">The following description will be displayed for the event.</span></span>

    ``` syntax
    Event filter with query "STRING2" could not be [re]activated in 
    namespace "STRING1" because of error STRING3. Events cannot be 
    delivered through this filter until the problem is corrected.
    ```

``` syntax
// Set the namespace as root\subscription.
// The NTEventLogEventConsumer is already
// compiled in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")
class NTLogCons_Example
{
 [key] string name;
 string InsertionString;
};

// Create an instance of the NT Event log consumer
// and give it the alias $CONSUMER

instance of NTEventLogEventConsumer as $CONSUMER
{
    // Unique instance name
    Name = "NTConsumerTest"; 
    // System component that generates the event
    SourceName = "WinMgmt";
    // Event message WBEM_MC_CANNOT_ACTIVATE_FILTER
    EventID = 0xC000000A;
    // EVENTLOG_ERROR_TYPE
    EventType = 1;
    // WMI event messages do not have multiple categories
    Category = 0;
    // Number of strings in InsertionStringTemplates property
    NumberOfInsertionStrings = 3;

    InsertionStringTemplates =
       {"%TargetInstance.Name%",
        "%TargetInstance.InsertionString%",
        "STRING3"};
};

// Create an instance of the event filter
// and give it the alias $FILTER
// The filter queries for any instance operation event
// for instances of the NTLogCons_Example class

instance of __EventFilter as $FILTER
{
    // Unique instance name
    Name = "NTLogConsFilter";
    Query = "SELECT * from __InstanceOperationEvent"
            " WHERE TargetInstance ISA \"NTLogCons_Example\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER;
    Filter = $FILTER;
};

// Create an instance of this class right now. 

instance of NTLogCons_Example
{
   Name = "STRING1";
   InsertionString = "STRING2";
};
```

## <a name="related-topics"></a><span data-ttu-id="acdb7-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acdb7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acdb7-139">Supervisión y respuesta a eventos con consumidores estándar</span><span class="sxs-lookup"><span data-stu-id="acdb7-139">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



