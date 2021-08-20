---
description: Cada servicio tiene un controlador de control, la función Handler, invocado por el distribuidor de controles cuando el proceso de servicio recibe una solicitud de control de un programa de control de servicio.
ms.assetid: 437334ed-05fa-4ab6-aab3-dc2739113e19
title: Función de controlador de control de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85fec3baaebe31eb4c44857be0eca3a64e1c2bf754875368d8bf8abf41d857e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967689"
---
# <a name="service-control-handler-function"></a>Función de controlador de control de servicio

Cada servicio tiene un controlador de control, la función [**Handler,**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) invocado por el distribuidor de controles cuando el proceso de servicio recibe una solicitud de control de un programa de control de servicio. Por lo tanto, esta función se ejecuta en el contexto del distribuidor de controles. Para obtener un ejemplo, vea [Escribir una función de controlador de control](writing-a-control-handler-function.md).

Un servicio llama a la [**función RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) [**o RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) para registrar su función de controlador de control de servicio.

Cuando se invoca el controlador de control de servicio, el servicio debe llamar a la función [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para notificar su estado al SCM solo si el control del código de control hace que el estado del servicio cambie. Si el control del código de control no hace que el estado del servicio cambie, no es necesario llamar a **SetServiceStatus**.

Un programa de control de servicio puede enviar solicitudes de control mediante la [**función ControlService.**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) Todos los servicios deben aceptar y procesar el código de control **SERVICE \_ CONTROL \_ INTERROGATE.** Puede habilitar o deshabilitar la aceptación de los otros códigos de control llamando a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus). Para recibir el código de control **\_ SERVICE CONTROL \_ DEVICEEVENT,** debe llamar a la [**función RegisterDeviceNotification.**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) Los servicios también pueden controlar códigos de control adicionales definidos por el usuario.

Si un servicio acepta el código de **control SERVICE \_ CONTROL \_ STOP,** debe detenerse tras la recepción, pasando al estado **SERVICE STOP \_ \_ PENDING** o **SERVICE \_ STOPPED.** Después de que el SCM envíe este código de control, no enviará otros códigos de control.

**Windows XP:** Si el servicio devuelve **NO \_ ERROR** y continúa en ejecución, sigue recibiendo códigos de control. Este comportamiento cambió a partir de Windows Server 2003 y Windows XP con Service Pack 2 (SP2).

El controlador de control debe devolver en un plazo de 30 segundos o el SCM devuelve un error. Si un servicio debe realizar un procesamiento largo cuando el servicio ejecuta el controlador de control, debe crear un subproceso secundario para realizar el procesamiento largo y, a continuación, devolver desde el controlador de control. Esto evita que el servicio acote el distribuidor de control. Por ejemplo, al controlar la solicitud de detenerse para un servicio que tarda mucho tiempo, cree otro subproceso para controlar el proceso de detenerse. El controlador de control simplemente debe llamar [**a SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con el mensaje **SERVICE STOP \_ \_ PENDING** y devolver.

Cuando el usuario cierra el sistema, todos los controladores de control que han llamado a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con el código de control **SERVICE ACCEPT \_ \_ PRESHUTDOWN** reciben el código de **control SERVICE CONTROL \_ \_ PRESHUTDOWN.** El administrador de control de servicios espera hasta que el servicio se detenga o expire el valor de tiempo de espera de apagado previo especificado (este valor se puede establecer con la [**función ChangeServiceConfig2).**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) Este código de control solo debe usarse en circunstancias especiales, ya que un servicio que controla esta notificación bloquea el apagado del sistema hasta que el servicio se detiene o expira el intervalo de tiempo de espera previo al apagado.

Una vez completadas las notificaciones previas al apagado, todos los controladores de control que han llamado [**a SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con el código de control **SERVICE ACCEPT \_ \_ SHUTDOWN** reciben el código **de control SERVICE CONTROL \_ \_ SHUTDOWN.** Se les notifica en el orden en que aparecen en la base de datos de los servicios instalados. De forma predeterminada, un servicio tiene aproximadamente 20 segundos para realizar tareas de limpieza antes de que se cierre el sistema. Una vez transcurrido este tiempo, el apagado del sistema continúa independientemente de si se ha completado el apagado del servicio. Tenga en cuenta que si el sistema se deja en estado de apagado (no reiniciado ni apagado), el servicio continúa en ejecución.

Si el servicio requiere más tiempo para la limpieza, envía mensajes de estado **STOP \_ PENDING,** junto con una sugerencia de espera, para que el controlador de servicio sepa cuánto tiempo se debe esperar antes de notificar al sistema que se ha completado el apagado del servicio. Sin embargo, para evitar que un servicio detenga el apagado, hay un límite en cuanto al tiempo que espera el controlador de servicio. Si el servicio se está cerrando a través del complemento Servicios, el límite es de 125 segundos o 125 000 milisegundos. Si el sistema operativo se está reiniciando, el límite de tiempo se especifica en el valor **WaitToKillServiceTimeout** (en milisegundos) de la siguiente clave del Registro:

**HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ (Control)**

> [!IMPORTANT]
> Un servicio no debe intentar aumentar el límite de tiempo modificando este valor. Si necesita establecer **WaitToKillServiceTimeout** a mano, el valor debe estar en milisegundos.

Los clientes requieren un apagado rápido del sistema operativo. Por ejemplo, si un equipo que se ejecuta en la alimentación ups no puede completar el apagado antes de que el UPS se queda sin energía, se pueden perder datos. Por lo tanto, los servicios deben completar sus tareas de limpieza lo antes posible. Es un procedimiento recomendado minimizar los datos no guardados guardando los datos de forma periódica, realizar un seguimiento de los datos que se guardan en el disco y guardar solo los datos no guardados al apagar. Dado que el equipo se está apagando, no dedle tiempo a liberar memoria asignada u otros recursos del sistema. Si necesita notificar a un servidor que está saliendo, minimice el tiempo dedicado a esperar una respuesta, ya que los problemas de red podrían retrasar el cierre del servicio.

Tenga en cuenta que, durante el cierre del servicio, de forma predeterminada, el SCM no tiene en cuenta las dependencias. El SCM enumera la lista de servicios en ejecución y envía el comando **SERVICE \_ CONTROL \_ SHUTDOWN.** Por lo tanto, un servicio puede producir un error porque otro servicio del que depende ya se ha detenido.

Para establecer manualmente el orden de apagado de los servicios, cree un valor del Registro de varias cadenas que contenga los nombres de servicio en el orden en que se deben apagar y asígnelo al valor **PreshutdownOrder** de la clave de control, como se muestra a continuación:

**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ PreshutdownOrder="Shutdown Order"**

Para establecer el orden de apagado de los servicios dependientes de la aplicación, use la [**función SetProcessShutdownParameters.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) El SCM usa esta función para proporcionar a su controlador 0x1E0 prioridad. El SCM envía **notificaciones SERVICE \_ CONTROL \_ SHUTDOWN** cuando se llama a su controlador de control y espera a que los servicios se cierren antes de volver de su controlador de control.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir una función de controlador de control](writing-a-control-handler-function.md)
</dt> </dl>

 

 
