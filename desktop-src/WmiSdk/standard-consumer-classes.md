---
description: En la tabla siguiente se enumeran las clases de los consumidores permanentes preinstalados por WMI.
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: Clases de consumidor estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a5033077f3dabf90d3e935b2dfec9fad892f630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279293"
---
# <a name="standard-consumer-classes"></a><span data-ttu-id="ddf0b-103">Clases de consumidor estándar</span><span class="sxs-lookup"><span data-stu-id="ddf0b-103">Standard Consumer Classes</span></span>

<span data-ttu-id="ddf0b-104">En la tabla siguiente se enumeran las clases de los consumidores permanentes preinstalados por WMI.</span><span class="sxs-lookup"><span data-stu-id="ddf0b-104">The following table lists the classes for WMI preinstalled permanent consumers.</span></span> <span data-ttu-id="ddf0b-105">Puede crear instancias de estas clases para proporcionar a la clase de consumidor permanente el consumidor lógico que responde cuando lo desencadenan los eventos especificados en el filtro.</span><span class="sxs-lookup"><span data-stu-id="ddf0b-105">You can create instances of these classes to provide the permanent consumer class to supply the logical consumer that responds when triggered by the events specified in the filter.</span></span> <span data-ttu-id="ddf0b-106">Por ejemplo, utilice la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para definir el script que se ejecuta cuando se produce un evento especificado.</span><span class="sxs-lookup"><span data-stu-id="ddf0b-106">For example, use the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to define the script that executes when a specified event occurs.</span></span>

<span data-ttu-id="ddf0b-107">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md) y [eventos de supervisión](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="ddf0b-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md) and [Monitoring Events](monitoring-events.md).</span></span>



| <span data-ttu-id="ddf0b-108">Clase</span><span class="sxs-lookup"><span data-stu-id="ddf0b-108">Class</span></span>                                                                        | <span data-ttu-id="ddf0b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddf0b-109">Description</span></span>                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddf0b-110">**ActiveScriptEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="ddf0b-110">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md)               | <span data-ttu-id="ddf0b-111">Ejecuta un script predefinido en un lenguaje de scripting arbitrario cuando se le entrega un evento.</span><span class="sxs-lookup"><span data-stu-id="ddf0b-111">Executes a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span><br/> <span data-ttu-id="ddf0b-112">Ejemplo: [ejecutar un script basado en un evento](running-a-script-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="ddf0b-112">Example: [Running a Script Based on an Event](running-a-script-based-on-an-event.md)</span></span><br/>                                         |
| [<span data-ttu-id="ddf0b-113">**CommandLineEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="ddf0b-113">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)                 | <span data-ttu-id="ddf0b-114">Inicia un proceso arbitrario en el contexto del sistema local cuando se le entrega un evento.</span><span class="sxs-lookup"><span data-stu-id="ddf0b-114">Launches an arbitrary process in the local system context when an event is delivered to it.</span></span><br/> <span data-ttu-id="ddf0b-115">Ejemplo: [ejecutar un programa desde la línea de comandos en función de un evento](running-a-program-from-the-command-line-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="ddf0b-115">Example: [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md)</span></span><br/> |
| [<span data-ttu-id="ddf0b-116">**LogFileEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="ddf0b-116">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)                         | <span data-ttu-id="ddf0b-117">Escribe cadenas personalizadas en un archivo de registro de texto cuando se le entregan eventos.</span><span class="sxs-lookup"><span data-stu-id="ddf0b-117">Writes customized strings to a text log file when events are delivered to it.</span></span><br/> <span data-ttu-id="ddf0b-118">Ejemplo: [escribir en un archivo de registro basado en un evento](writing-to-a-log-file-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="ddf0b-118">Example: [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md)</span></span><br/>                                                   |
| [<span data-ttu-id="ddf0b-119">**NTEventLogEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="ddf0b-119">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)                   | <span data-ttu-id="ddf0b-120">Registra un mensaje específico en el registro de eventos de Windows cuando se le entrega un evento.</span><span class="sxs-lookup"><span data-stu-id="ddf0b-120">Logs a specific message to the Windows event log when an event is delivered to it.</span></span><br/> <span data-ttu-id="ddf0b-121">Ejemplo: [registro en un registro de eventos de NT basado en un evento](logging-to-nt-event-log-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="ddf0b-121">Example: [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md)</span></span><br/>                                          |
| [<span data-ttu-id="ddf0b-122">**ScriptingStandardConsumerSetting**</span><span class="sxs-lookup"><span data-stu-id="ddf0b-122">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md) | <span data-ttu-id="ddf0b-123">Proporciona datos de registro comunes a todas las instancias de la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="ddf0b-123">Provides registration data common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="ddf0b-124">**SMTPEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="ddf0b-124">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                               | <span data-ttu-id="ddf0b-125">Envía un mensaje de correo electrónico mediante SMTP cada vez que se le entrega un evento.</span><span class="sxs-lookup"><span data-stu-id="ddf0b-125">Sends an email message using SMTP each time an event is delivered to it.</span></span><br/> <span data-ttu-id="ddf0b-126">Ejemplo: [envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="ddf0b-126">Example: [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md)</span></span><br/>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="ddf0b-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ddf0b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddf0b-128">Supervisión de eventos</span><span class="sxs-lookup"><span data-stu-id="ddf0b-128">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="ddf0b-129">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="ddf0b-129">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="ddf0b-130">Ejecutar un script basado en un evento</span><span class="sxs-lookup"><span data-stu-id="ddf0b-130">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="ddf0b-131">Envío de correo electrónico basado en un evento</span><span class="sxs-lookup"><span data-stu-id="ddf0b-131">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




