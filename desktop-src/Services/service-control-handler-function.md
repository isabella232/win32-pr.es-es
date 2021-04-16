---
description: Cada servicio tiene un controlador de control, la función de controlador, que invoca el distribuidor del control cuando el proceso de servicio recibe una solicitud de control de un programa de control de servicios.
ms.assetid: 437334ed-05fa-4ab6-aab3-dc2739113e19
title: Función de controlador de control de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1303bff45421ee7206d02be9ee30066324648823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666448"
---
# <a name="service-control-handler-function"></a>Función de controlador de control de servicio

Cada servicio tiene un controlador de control, la función de [**controlador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) , que invoca el distribuidor del control cuando el proceso de servicio recibe una solicitud de control de un programa de control de servicios. Por lo tanto, esta función se ejecuta en el contexto del distribuidor del control. Para obtener un ejemplo, vea [escribir una función de controlador de control](writing-a-control-handler-function.md).

Un servicio llama a la función [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) o [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) para registrar su función de controlador de control de servicio.

Cuando se invoca el controlador de control de servicio, el servicio debe llamar a la función [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para notificar su estado al SCM solo si el control del código de control hace que el estado del servicio cambie. Si el control del código de control no hace que cambie el estado del servicio, no es necesario llamar a **SetServiceStatus**.

Un programa de control de servicios puede enviar solicitudes de control mediante la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . Todos los servicios deben aceptar y procesar el código de control de **\_ \_ interrogación de control de servicio** . Puede habilitar o deshabilitar la aceptación de los otros códigos de control llamando a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus). Para recibir el código de control **\_ \_ DEVICEEVENT de control de servicio** , debe llamar a la función [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) . Los servicios también pueden controlar códigos de control adicionales definidos por el usuario.

Si un servicio acepta el código de control de **\_ \_ detención del control de servicio** , debe detenerse tras la recepción, pasando al estado de servicio **\_ \_ pendiente o detención** del servicio. **\_** Una vez que el SCM envía este código de control, no enviará otros códigos de control.

**Windows XP:** Si el servicio **no devuelve ningún \_ error** y continúa ejecutándose, sigue recibiendo códigos de control. Este comportamiento ha cambiado a partir de Windows Server 2003 y Windows XP con Service Pack 2 (SP2).

El controlador de control debe volver en un plazo de 30 segundos o el SCM devuelve un error. Si un servicio debe realizar un procesamiento largo cuando el servicio está ejecutando el controlador de control, debe crear un subproceso secundario para realizar el procesamiento prolongado y, a continuación, volver del controlador de control. Esto evita que el servicio entre en el distribuidor de control. Por ejemplo, al controlar la solicitud de detención de un servicio que tarda mucho tiempo, cree otro subproceso para controlar el proceso de detención. El controlador de control solo debe llamar a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con el mensaje **\_ Stop \_ Pending** Message y devolverlo.

Cuando el usuario cierra el sistema, todos los controladores de control que han llamado a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con el servicio aceptan el código de control de **\_ \_ preapagado** reciben el código de control de **\_ \_ cierre del control de servicio** . El administrador de control de servicios espera hasta que el servicio se detenga o expire el valor de tiempo de espera de preapagado especificado (este valor se puede establecer con la función [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) ). Este código de control solo debe usarse en circunstancias especiales, ya que un servicio que administra esta notificación bloquea el cierre del sistema hasta que el servicio se detiene o hasta que expira el intervalo de tiempo de espera de cierre.

Una vez completadas las notificaciones de cierre, todos los controladores de control que han llamado [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con el servicio aceptan el código de control de **\_ \_ cierre** reciben el código de control de **\_ \_ cierre del control de servicio** . Se notifican en el orden en que aparecen en la base de datos de servicios instalados. De forma predeterminada, un servicio tiene aproximadamente 20 segundos para realizar tareas de limpieza antes de que se cierre el sistema. Después de que expire este tiempo, el cierre del sistema se reanuda independientemente de si se ha completado el cierre del servicio. Tenga en cuenta que si el sistema se queda en el estado de apagado (no reiniciado o apagado), el servicio continúa ejecutándose.

Si el servicio requiere más tiempo para la limpieza, envía mensajes de estado de **detención \_ pendiente** , junto con una sugerencia de espera, por lo que el controlador de servicio sabe cuánto tiempo hay que esperar antes de informar al sistema de que se ha completado el cierre del servicio. Sin embargo, para evitar que un servicio detenga el apagado, existe un límite en cuanto al tiempo que espera el controlador de servicio. Si el servicio se está cerrando a través del complemento Servicios, el límite es de 125 segundos o 125.000 milisegundos. Si el sistema operativo se está reiniciando, el límite de tiempo se especifica en el valor **WaitToKillServiceTimeout** (en milisegundos) de la siguiente clave del registro:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control**

> [!IMPORTANT]
> Un servicio no debe intentar aumentar el límite de tiempo mediante la modificación de este valor. Si necesita establecer **WaitToKillServiceTimeout** manualmente, el valor debe estar en milisegundos.

Los clientes requieren un apagado rápido del sistema operativo. Por ejemplo, si un equipo que ejecuta la alimentación de UPS no puede completar el apagado antes de que el SAI quede sin alimentación, se pueden perder datos. Por lo tanto, los servicios deben completar las tareas de limpieza lo más rápido posible. Es recomendable minimizar los datos no guardados guardando los datos periódicamente, realizando un seguimiento de los datos que se guardan en el disco y guardando los datos no guardados en el apagado. Dado que el equipo se está apagando, no dedique tiempo a liberar memoria asignada u otros recursos del sistema. Si necesita notificar a un servidor que está saliendo, minimice el tiempo invertido en esperar una respuesta, ya que los problemas de red pueden retrasar el cierre del servicio.

Tenga en cuenta que durante el cierre del servicio, de forma predeterminada, el SCM no tiene en cuenta las dependencias. El SCM enumera la lista de servicios en ejecución y envía el comando de **\_ \_ cierre del control de servicio** . Por lo tanto, se puede producir un error en un servicio porque ya se ha detenido otro servicio del que depende.

Para establecer manualmente el orden de cierre de los servicios, cree un valor del registro de multicadena que contenga los nombres de servicio en el orden en que deben cerrarse y asígnelo al valor **PreshutdownOrder** de la clave de control, como se indica a continuación:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ PreshutdownOrder = "orden de cierre"**

Para establecer el orden de cierre de los servicios dependientes de la aplicación, utilice la función [**SetProcessShutdownParameters**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) . El SCM usa esta función para proporcionar a su controlador prioridad 0x1E0. El SCM envía notificaciones de **\_ \_ cierre del control de servicio** cuando se llama a su controlador de control y espera a que los servicios salgan antes de volver de su controlador de control.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir una función de controlador de control](writing-a-control-handler-function.md)
</dt> </dl>

 

 
