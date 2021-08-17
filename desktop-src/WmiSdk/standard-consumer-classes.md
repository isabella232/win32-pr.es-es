---
description: En la tabla siguiente se enumeran las clases para los consumidores permanentes preinstalados de WMI.
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: Clases de consumidor estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f89463a459adb3dd800f77564002366c7500a2abbaa6010444ba7890802d5a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315282"
---
# <a name="standard-consumer-classes"></a>Clases de consumidor estándar

En la tabla siguiente se enumeran las clases para los consumidores permanentes preinstalados de WMI. Puede crear instancias de estas clases para proporcionar la clase de consumidor permanente para proporcionar el consumidor lógico que responde cuando lo desencadenan los eventos especificados en el filtro. Por ejemplo, use la [**clase ActiveScriptEventConsumer**](activescripteventconsumer.md) para definir el script que se ejecuta cuando se produce un evento especificado.

Para obtener más información, vea [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md) and Monitoring [Events](monitoring-events.md).



| Clase                                                                        | Descripción                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md)               | Ejecuta un script predefinido en un lenguaje de scripting arbitrario cuando se le entrega un evento.<br/> Ejemplo: [Ejecución de un script basado en un evento](running-a-script-based-on-an-event.md)<br/>                                         |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)                 | Inicia un proceso arbitrario en el contexto del sistema local cuando se le entrega un evento.<br/> Ejemplo: [Ejecución de un programa desde la línea de comandos en función de un evento](running-a-program-from-the-command-line-based-on-an-event.md)<br/> |
| [**LogFileEventConsumer**](logfileeventconsumer.md)                         | Escribe cadenas personalizadas en un archivo de registro de texto cuando se le entregan eventos.<br/> Ejemplo: [Escribir en un archivo de registro basado en un evento](writing-to-a-log-file-based-on-an-event.md)<br/>                                                   |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)                   | Registra un mensaje específico en el Windows de eventos cuando se le entrega un evento.<br/> Ejemplo: [Registro en el registro de eventos NT basado en un evento](logging-to-nt-event-log-based-on-an-event.md)<br/>                                          |
| [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md) | Proporciona datos de registro comunes a todas las instancias de la [**clase ActiveScriptEventConsumer.**](activescripteventconsumer.md)<br/>                                                                                                            |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                               | Envía un mensaje de correo electrónico mediante SMTP cada vez que se le entrega un evento.<br/> Ejemplo: [Envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md)<br/>                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión de eventos](monitoring-events.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[Ejecución de un script basado en un evento](running-a-script-based-on-an-event.md)
</dt> <dt>

[Envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




