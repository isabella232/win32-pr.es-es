---
description: Un servicio se puede registrar para iniciarse o detenerse cuando se produce un evento de desencadenador.
ms.assetid: ca02a3ae-b16a-4427-b6db-b935c9cf23b3
title: Eventos de desencadenador de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdefd94b7896936f7ab4fc014647b08470611573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668461"
---
# <a name="service-trigger-events"></a>Eventos de desencadenador de servicio

Un servicio se puede registrar para iniciarse o detenerse cuando se produce un evento de desencadenador. Esto elimina la necesidad de que los servicios se inicien cuando se inicia el sistema, o para que los servicios sondeen o esperen activamente un evento; un servicio puede iniciarse cuando sea necesario, en lugar de iniciarse automáticamente tanto si hay trabajo que hacer como si no. Algunos ejemplos de eventos de desencadenador predefinidos son la llegada de un dispositivo de una clase de interfaz de dispositivo especificada o la disponibilidad de un puerto de Firewall determinado. Un servicio también se puede registrar para un evento de desencadenador personalizado generado por un proveedor [de seguimiento de eventos para Windows](../etw/event-tracing-portal.md) (ETW).

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Los eventos de desencadenador de servicio no se admiten hasta Windows Server 2008 R2 y Windows 7.

Un desencadenador está formado por un tipo de evento de desencadenador, un subtipo de evento de desencadenador, la acción que se va a realizar en respuesta al evento de desencadenador y (para determinados tipos de evento de desencadenador) uno o más elementos de datos específicos del desencadenador. El subtipo y los elementos de datos específicos del desencadenador juntos especifican las condiciones para notificar el servicio del evento. El formato de un elemento de datos depende del tipo de evento de desencadenador; un elemento de datos puede ser datos binarios, una cadena o una cadena multistring. Las cadenas deben ser Unicode; No se admiten cadenas ANSI.

Para registrar eventos de desencadenador, el servicio llama a [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) con la **\_ \_ \_ información del desencadenador de configuración de servicio** y proporciona una estructura de [**\_ \_ información de desencadenador de servicio**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info) . La estructura de **\_ \_ información del desencadenador de servicio** apunta a una matriz de estructuras de [**\_ desencadenador de servicio**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger) , cada una de las cuales especifica un desencadenador.

La acción del desencadenador especificado se realiza si la condición del desencadenador es true cuando se inicia el sistema, o si la condición del desencadenador se vuelve verdadera mientras el sistema se está ejecutando. Por ejemplo, si un servicio se registra para que se inicie cuando un dispositivo determinado está disponible, el servicio se inicia cuando se inicia el sistema si el dispositivo ya está conectado al equipo; el servicio se inicia cuando el dispositivo llega si el usuario se conecta al dispositivo mientras el sistema se está ejecutando.

Si un desencadenador tiene elementos de datos específicos del desencadenador, la acción del desencadenador solo se realiza si el elemento de datos que acompaña al evento de desencadenador coincide con uno de los elementos de datos especificados por el servicio con el desencadenador. La coincidencia de datos binarios se realiza mediante una comparación bit a bit. La coincidencia de cadenas no distingue entre mayúsculas y minúsculas. Si el elemento de datos es una cadena multistring, todas las cadenas de la cadena deben coincidir.

Cuando un servicio se inicia en respuesta a un evento de desencadenador, el servicio recibe el **\_ argumento de desencadenador de servicio \_ \_ iniciado** como *argv* \[ 1 \] en su función de devolución de llamada de [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) . *Argv* \[ 0 \] siempre es el nombre corto del servicio.

Un servicio que se registra para que se inicie en respuesta a un evento de desencadenador podría detenerse a sí mismo después de un tiempo de espera de inactividad cuando el servicio no tiene ningún trabajo que hacer. Un servicio que se detiene debe estar preparado para controlar las solicitudes de control de **\_ \_ TRIGGEREVENT de control de servicio** que llegan mientras el servicio se detiene. El SCM envía una solicitud de control de **\_ \_ TRIGGEREVENT de control de servicio** cada vez que se produce un nuevo evento de desencadenador mientras el servicio se encuentra en estado de ejecución. Para evitar la pérdida de eventos de desencadenador, el servicio debe devolver un **error \_ \_ de apagado en \_ curso** para cualquier solicitud de control de **TRIGGEREVENT de \_ control \_ de servicio** que llegue mientras el servicio está pasando de ejecutarse a detenido. Esto indica al SCM que debe poner en cola los eventos del desencadenador y esperar a que el servicio entre en el estado detenido. A continuación, el SCM toma la acción asociada con el evento de desencadenador en cola, como iniciar el servicio.

Cuando el servicio está listo para controlar de nuevo los eventos de desencadenador, establece el **servicio \_ Accept \_ TRIGGEREVENT** en su máscara de controles aceptados en una llamada a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus). Normalmente, esto se hace cuando el servicio llama a **SetServiceStatus** con el **servicio en \_ ejecución**. A continuación, el SCM emite una solicitud **\_ \_ TRIGGEREVENT de control de servicio** para cada evento de desencadenador en cola hasta que la cola esté vacía.

Un servicio que tiene servicios dependientes en ejecución no puede detenerse en respuesta a un evento de desencadenador.

Las solicitudes desencadenador-Inicio y detener desencadenador no se garantizan en condiciones de memoria insuficiente.

Utilice la función [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) para recuperar la configuración de eventos del desencadenador de un servicio.

La herramienta SC (sc.exe) se puede usar para configurar o consultar los eventos de desencadenador de un servicio en el símbolo del sistema. Use la opción **triggerinfo** para configurar un servicio para iniciarse o detenerse en respuesta a un evento de desencadenador. Use la opción **qtriggerinfo** para consultar la configuración del desencadenador de un servicio.

En el ejemplo siguiente se consulta la configuración del desencadenador del servicio W32time, que está configurado para iniciarse cuando el equipo se une a un dominio y se detiene cuando el equipo sale del dominio.

``` syntax
C:\>sc qtriggerinfo w32time
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: w32time

        START SERVICE
          DOMAIN JOINED STATUS         : 1ce20aba-9851-4421-9430-1ddeb766e809 [DOMAIN JOINED]
        STOP SERVICE
          DOMAIN JOINED STATUS         : ddaf516e-58c2-4866-9574-c3b615d42ea1 [NOT DOMAIN JOINED]
```

En el ejemplo siguiente se consulta la configuración del desencadenador del servicio de entrada de Tablet PC, que está configurado para iniciarse cuando un dispositivo HID con el **GUID** {4d1e55b2-f16f-11cf-88cb-001111000030} y cualquiera de los identificadores de dispositivo HID especificados llega.

``` syntax
C:\>sc qtriggerinfo tabletinputservice
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: tabletinputservice

        START SERVICE
          DEVICE INTERFACE ARRIVAL     : 4d1e55b2-f16f-11cf-88cb-001111000030 [INTERFACE CLASS GUID]
            DATA                       : HID_DEVICE_UP:000D_U:0001
            DATA                       : HID_DEVICE_UP:000D_U:0002
            DATA                       : HID_DEVICE_UP:000D_U:0003
            DATA                       : HID_DEVICE_UP:000D_U:0004
```

 

 
