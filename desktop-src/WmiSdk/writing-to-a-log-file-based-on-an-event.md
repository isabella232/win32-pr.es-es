---
description: La clase LogFileEventConsumer puede escribir texto predefinido en un archivo de registro cuando se produce un evento especificado. Esta clase es un consumidor de eventos estándar que proporciona WMI.
ms.assetid: c337e9f7-f40c-4d7d-a180-c053e24c882b
ms.tgt_platform: multiple
title: Escribir en un archivo de registro basado en un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33cc82925b6afc1690f2cd87607f21e9ea02fdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276243"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a><span data-ttu-id="0309e-104">Escribir en un archivo de registro basado en un evento</span><span class="sxs-lookup"><span data-stu-id="0309e-104">Writing to a Log File Based on an Event</span></span>

<span data-ttu-id="0309e-105">La clase [**LogFileEventConsumer**](logfileeventconsumer.md) puede escribir texto predefinido en un archivo de registro cuando se produce un evento especificado.</span><span class="sxs-lookup"><span data-stu-id="0309e-105">The [**LogFileEventConsumer**](logfileeventconsumer.md) class can write predefined text to a log file when a specified event occurs.</span></span> <span data-ttu-id="0309e-106">Esta clase es un consumidor de eventos estándar que proporciona WMI.</span><span class="sxs-lookup"><span data-stu-id="0309e-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="0309e-107">El procedimiento básico para usar consumidores estándar siempre es el mismo y se encuentra en [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="0309e-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="0309e-108">El siguiente procedimiento se agrega al procedimiento básico, es específico de la clase [**LogFileEventConsumer**](logfileeventconsumer.md) y describe cómo crear un consumidor de eventos que ejecute un programa.</span><span class="sxs-lookup"><span data-stu-id="0309e-108">The following procedure adds to the basic procedure, is specific to the [**LogFileEventConsumer**](logfileeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

<span data-ttu-id="0309e-109">**Para crear un consumidor de eventos que escribe en un archivo de registro**</span><span class="sxs-lookup"><span data-stu-id="0309e-109">**To create an event consumer that writes to a log file**</span></span>

1.  <span data-ttu-id="0309e-110">En el archivo Managed Object Format (MOF), cree una instancia de [**LogFileEventConsumer**](logfileeventconsumer.md) para recibir los eventos solicitados en la consulta, asigne un nombre a la instancia en la propiedad **nombre** y, a continuación, coloque la ruta de acceso al archivo de registro en **la propiedad nombre de archivo.**</span><span class="sxs-lookup"><span data-stu-id="0309e-110">In the Managed Object Format (MOF) file, create an instance of [**LogFileEventConsumer**](logfileeventconsumer.md) to receive the events you request in the query, name the instance in the **Name** property, and then place the path to the log file in the **Filename** property.</span></span>

    <span data-ttu-id="0309e-111">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="0309e-111">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="0309e-112">Proporcione la plantilla de texto para escribir en el archivo de registro en la propiedad Text.</span><span class="sxs-lookup"><span data-stu-id="0309e-112">Provide the text template to write to the log file in the Text property.</span></span>

    <span data-ttu-id="0309e-113">Para obtener más información, consulte [uso de plantillas de cadena estándar](using-standard-string-templates.md).</span><span class="sxs-lookup"><span data-stu-id="0309e-113">For more information, see [Using Standard String Templates](using-standard-string-templates.md).</span></span>

3.  <span data-ttu-id="0309e-114">Cree una instancia de [**\_ \_ EventFilter**](--eventfilter.md) y defina una consulta para especificar los eventos que activarán al consumidor.</span><span class="sxs-lookup"><span data-stu-id="0309e-114">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query to specify the events that will activate the consumer.</span></span>

    <span data-ttu-id="0309e-115">Para obtener más información, vea [consultas con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="0309e-115">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="0309e-116">Cree una instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para asociar el filtro a la instancia de [**LogFileEventConsumer**](logfileeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="0309e-116">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**LogFileEventConsumer**](logfileeventconsumer.md).</span></span>
5.  <span data-ttu-id="0309e-117">Para controlar quién lee o escribe en el archivo de registro, establezca la seguridad en el directorio donde se encuentra el registro en el nivel requerido.</span><span class="sxs-lookup"><span data-stu-id="0309e-117">To control who reads or writes to your log file, set the security on the directory where the log is located to the required level.</span></span>
6.  <span data-ttu-id="0309e-118">Compile el archivo MOF mediante [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="0309e-118">Compile your MOF file using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="0309e-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0309e-119">Example</span></span>

<span data-ttu-id="0309e-120">El ejemplo de esta sección está en código MOF, pero puede crear las instancias mediante programación con la API de [scripting para WMI](scripting-api-for-wmi.md) o la [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0309e-120">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="0309e-121">En el ejemplo se usa el LogFileEventConsumer estándar para crear una clase de consumidor denominada LogFileEvent que escribe una línea en el archivo c: \\ logfile. log cuando se crea una instancia de la clase LogFileEvent.</span><span class="sxs-lookup"><span data-stu-id="0309e-121">The example uses the standard LogFileEventConsumer to create a consumer class named LogFileEvent that writes a line to the file c:\\Logfile.log when an instance of the class LogFileEvent is created.</span></span>

<span data-ttu-id="0309e-122">En el procedimiento siguiente se describe cómo utilizar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0309e-122">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="0309e-123">**Para usar el ejemplo**</span><span class="sxs-lookup"><span data-stu-id="0309e-123">**To use the example**</span></span>

1.  <span data-ttu-id="0309e-124">Copie la siguiente lista de MOF en un archivo de texto y guárdelo con una extensión. mof.</span><span class="sxs-lookup"><span data-stu-id="0309e-124">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="0309e-125">En una ventana de comandos, compile el archivo MOF con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="0309e-125">In a command window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="0309e-126">Nombre de archivo de **MOFCOMP** \*\* \* *. mof*\*</span><span class="sxs-lookup"><span data-stu-id="0309e-126">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="0309e-127">Abra logfile. log para ver la línea especificada por LogFileEvent.Name: "logfile Event Consumer Event".</span><span class="sxs-lookup"><span data-stu-id="0309e-127">Open Logfile.log to see the line specified by LogFileEvent.Name: "Logfile Event Consumer event".</span></span>

``` syntax
// Set the namespace as root\subscription.
// The LogFileEventConsumer is already compiled 
//     in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")

class LogFileEvent
{
    [key]string Name;
};

// Create an instance of the standard log
// file consumer and give it the alias $CONSUMER

instance of LogFileEventConsumer as $CONSUMER
{
    // If the file does not already exist, it is created.
    Filename = "c:\\Logfile.log";  
    IsUnicode = FALSE;
    // Name of this instance of LogFileEventConsumer
    Name = "LogfileEventConsumer_Example";  
    // See "Using Standard String Templates"; 
    Text = "%TargetInstance.Name%"; 
    // TargetInstance is the instance of LogFileEvent 
    //    requested in the filter        
                                         
};

// Create an instance of the event filter 
// and give it the alias $FILTER
// Query for any instance operation type,
// such as instance creation, for LogFileEvent class

instance of __EventFilter as $FILTER
{
    Name = "LogFileFilter";
    Query = "SELECT * FROM __InstanceOperationEvent "
        "WHERE TargetInstance.__class = \"LogFileEvent\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding.

instance of __FilterToConsumerBinding
{
    Consumer=$CONSUMER;
    Filter=$FILTER;
 DeliverSynchronously=FALSE;
};

// Create an instance of this class right now
// Look at the file c:\Logfile.log to see
// that a line has been written.

instance of LogFileEvent
{
 Name = "Logfile Event Consumer event";  
};
```

## <a name="related-topics"></a><span data-ttu-id="0309e-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0309e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0309e-129">Supervisión y respuesta a eventos con consumidores estándar</span><span class="sxs-lookup"><span data-stu-id="0309e-129">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



