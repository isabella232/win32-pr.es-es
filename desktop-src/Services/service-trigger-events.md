---
description: Un servicio puede registrarse para iniciarse o detenerse cuando se produce un evento desencadenador.
ms.assetid: ca02a3ae-b16a-4427-b6db-b935c9cf23b3
title: Eventos de desencadenador de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67b6c219f91668af3372cf6c50b005d544a2544232d83e2e215d50a194db95b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967268"
---
# <a name="service-trigger-events"></a>Eventos de desencadenador de servicio

Un servicio puede registrarse para iniciarse o detenerse cuando se produce un evento desencadenador. Esto elimina la necesidad de que los servicios se inicien cuando se inicie el sistema o de que los servicios sondean o esperan activamente un evento; un servicio puede iniciarse cuando es necesario, en lugar de iniciarse automáticamente tanto si hay trabajo que hacer como si no. Algunos ejemplos de eventos de desencadenador predefinidos son la llegada de un dispositivo de una clase de interfaz de dispositivo especificada o la disponibilidad de un puerto de firewall determinado. Un servicio también puede registrarse para un evento de desencadenador personalizado generado por un proveedor [de seguimiento](../etw/event-tracing-portal.md) de eventos Windows (ETW).

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Los eventos de desencadenador de servicio no se admiten hasta Windows Server 2008 R2 y Windows 7.

Un desencadenador consta de un tipo de evento de desencadenador, un subtipo de evento de desencadenador, la acción que se va a realizar en respuesta al evento de desencadenador y (para determinados tipos de eventos de desencadenador) uno o varios elementos de datos específicos del desencadenador. El subtipo y los elementos de datos específicos del desencadenador juntos especifican las condiciones para notificar al servicio del evento. El formato de un elemento de datos depende del tipo de evento de desencadenador; un elemento de datos puede ser datos binarios, una cadena o una cadena múltiple. Las cadenas deben ser Unicode; No se admiten cadenas ANSI.

Para registrarse para eventos de desencadenador, el servicio llama a [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) con **SERVICE CONFIG TRIGGER \_ \_ \_ INFO** y proporciona una [**estructura SERVICE TRIGGER \_ \_ INFO.**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info) La **estructura SERVICE TRIGGER \_ \_ INFO** apunta a una matriz de [**estructuras SERVICE \_ TRIGGER,**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger) cada una de las que especifica un desencadenador.

La acción de desencadenador especificada se toma si la condición del desencadenador es true cuando se inicia el sistema o si la condición del desencadenador se convierte en true mientras el sistema se está ejecutando. Por ejemplo, si un servicio se registra para iniciarse cuando un dispositivo determinado está disponible, el servicio se inicia cuando el sistema se inicia si el dispositivo ya está conectado al equipo; el servicio se inicia cuando llega el dispositivo si el usuario lo conecta mientras se ejecuta el sistema.

Si un desencadenador tiene elementos de datos específicos del desencadenador, la acción del desencadenador solo se lleva a la acción si el elemento de datos que acompaña al evento de desencadenador coincide con uno de los elementos de datos que el servicio especificó con el desencadenador. La coincidencia de datos binarios se realiza mediante la comparación bit a bit. La coincidencia de cadenas no tiene en cuenta mayúsculas de minúsculas. Si el elemento de datos es una cadena múltiple, todas las cadenas de la cadena múltiple deben coincidir.

Cuando se inicia un servicio en respuesta a un evento de desencadenador, el servicio recibe **SERVICE \_ TRIGGER STARTED \_ \_ ARGUMENT** como *argv* 1 en su función de devolución de llamada \[ \] [*ServiceMain.*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) *Argv* \[ 0 \] siempre es el nombre corto del servicio.

Un servicio que se registra para iniciarse en respuesta a un evento de desencadenador podría detenerse después de un tiempo de espera de inactividad cuando el servicio no tiene trabajo que hacer. Un servicio que se detenga debe estar preparado para controlar las solicitudes de control **\_ \_ TRIGGEREVENT** de SERVICE CONTROL que llegan mientras el servicio se detiene a sí mismo. El SCM envía una solicitud de control **SERVICE \_ CONTROL \_ TRIGGEREVENT** cada vez que se produce un nuevo evento de desencadenador mientras el servicio está en estado de ejecución. Para evitar la pérdida de eventos de desencadenador, el servicio debe devolver **ERROR \_ SHUTDOWN IN \_ \_ PROGRESS** para cualquier solicitud de control **\_ \_ TRIGGEREVENT** de CONTROL DE SERVICIO que llegue mientras el servicio pasa de ejecutarse a detenido. Esto indica al SCM que poner en cola los eventos de desencadenador y esperar a que el servicio entre en el estado detenido. A continuación, el SCM realiza la acción asociada al evento de desencadenador en cola, como iniciar el servicio.

Cuando el servicio está listo para controlar de nuevo los eventos de desencadenador, establece **SERVICE \_ ACCEPT \_ TRIGGEREVENT** en su máscara aceptada por controles en una llamada a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus). Esto suele hacerse cuando el servicio llama a **SetServiceStatus** con **SERVICE \_ RUNNING**. A continuación, el SCM emite una **solicitud SERVICE \_ CONTROL \_ TRIGGEREVENT** para cada evento de desencadenador en cola hasta que la cola esté vacía.

Un servicio que tiene servicios dependientes en ejecución no se puede detener en respuesta a un evento de desencadenador.

Las solicitudes trigger-start y trigger-stop no se garantizan en condiciones de memoria baja.

Use la [**función QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) para recuperar la configuración de eventos de desencadenador de un servicio.

La herramienta SC (sc.exe) se puede usar para configurar o consultar los eventos de desencadenador de un servicio en el símbolo del sistema. Use la **opción triggerinfo** para configurar un servicio para iniciar o detener en respuesta a un evento de desencadenador. Use la **opción qtriggerinfo** para consultar la configuración del desencadenador de un servicio.

En el ejemplo siguiente se consulta la configuración del desencadenador del servicio W32time, que se configura para iniciarse cuando el equipo se une a un dominio y detenerse cuando el equipo abandona el dominio.

``` syntax
C:\>sc qtriggerinfo w32time
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: w32time

        START SERVICE
          DOMAIN JOINED STATUS         : 1ce20aba-9851-4421-9430-1ddeb766e809 [DOMAIN JOINED]
        STOP SERVICE
          DOMAIN JOINED STATUS         : ddaf516e-58c2-4866-9574-c3b615d42ea1 [NOT DOMAIN JOINED]
```

En el ejemplo siguiente se consulta la configuración del desencadenador del servicio de entrada de tabletas, que se configura para iniciarse cuando llega un dispositivo HID con el **GUID** {4d1e55b2-f16f-11cf-88cb-001111000030} y cualquiera de los identificadores de dispositivos HID especificados.

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

 

 
