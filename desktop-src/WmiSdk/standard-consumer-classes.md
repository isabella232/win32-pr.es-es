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
# <a name="standard-consumer-classes"></a>Clases de consumidor estándar

En la tabla siguiente se enumeran las clases de los consumidores permanentes preinstalados por WMI. Puede crear instancias de estas clases para proporcionar a la clase de consumidor permanente el consumidor lógico que responde cuando lo desencadenan los eventos especificados en el filtro. Por ejemplo, utilice la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para definir el script que se ejecuta cuando se produce un evento especificado.

Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md) y [eventos de supervisión](monitoring-events.md).



| Clase                                                                        | Descripción                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md)               | Ejecuta un script predefinido en un lenguaje de scripting arbitrario cuando se le entrega un evento.<br/> Ejemplo: [ejecutar un script basado en un evento](running-a-script-based-on-an-event.md)<br/>                                         |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)                 | Inicia un proceso arbitrario en el contexto del sistema local cuando se le entrega un evento.<br/> Ejemplo: [ejecutar un programa desde la línea de comandos en función de un evento](running-a-program-from-the-command-line-based-on-an-event.md)<br/> |
| [**LogFileEventConsumer**](logfileeventconsumer.md)                         | Escribe cadenas personalizadas en un archivo de registro de texto cuando se le entregan eventos.<br/> Ejemplo: [escribir en un archivo de registro basado en un evento](writing-to-a-log-file-based-on-an-event.md)<br/>                                                   |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)                   | Registra un mensaje específico en el registro de eventos de Windows cuando se le entrega un evento.<br/> Ejemplo: [registro en un registro de eventos de NT basado en un evento](logging-to-nt-event-log-based-on-an-event.md)<br/>                                          |
| [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md) | Proporciona datos de registro comunes a todas las instancias de la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) .<br/>                                                                                                            |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                               | Envía un mensaje de correo electrónico mediante SMTP cada vez que se le entrega un evento.<br/> Ejemplo: [envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md)<br/>                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión de eventos](monitoring-events.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[Ejecutar un script basado en un evento](running-a-script-based-on-an-event.md)
</dt> <dt>

[Envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




