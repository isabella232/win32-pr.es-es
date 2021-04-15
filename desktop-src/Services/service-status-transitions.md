---
description: Un servicio es responsable de notificar los cambios en su estado al administrador de control de servicios (SCM).
ms.assetid: 74a85730-6667-46fe-ae12-26561ccedb73
title: Transiciones de estado del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df7684b1ebc04aa1116b09a3ae4321f2552d7b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568767"
---
# <a name="service-state-transitions"></a>Transiciones de estado del servicio

Un servicio es responsable de notificar los cambios en su estado al administrador de control de servicios (SCM). Los programas de control de servicios y el sistema pueden averiguar el estado de un servicio únicamente desde el SCM, por lo que es importante que un servicio notifique su estado correctamente. Un servicio informa de su estado mediante una llamada a la función [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con un puntero a una estructura de [**\_ Estado de servicio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) completamente inicializada. El miembro **dwCurrentState** de la estructura contiene el estado del servicio que se va a informar.

El estado inicial de un servicio es \_ detenido. Cuando el SCM inicia el servicio, establece el estado del servicio en Inicio de servicio \_ \_ pendiente y llama a la función [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) del servicio. Después, el servicio completa su inicialización mediante una de las técnicas descritas en la [función ServiceMain de servicio](service-servicemain-function.md). Una vez que el servicio completa su inicialización y está listo para empezar a recibir solicitudes de control, el servicio llama a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para informar del servicio en \_ ejecución y especifica las solicitudes de control que el servicio está preparado para aceptar. La transición desde \_ el inicio del servicio \_ pendiente al servicio en \_ ejecución indica al SCM y a las herramientas de supervisión de servicios que el servicio se ha iniciado correctamente. Si el servicio informa de un Estado distinto del servicio \_ que se está ejecutando, el SCM o las herramientas de supervisión de servicios podrían marcar el servicio como no se pudo iniciar.

El SCM envía solo las solicitudes de control especificadas al servicio (excepto para la \_ solicitud de interrogación de control de servicio \_ , que siempre se envía). Para obtener una lista de las solicitudes de control que puede aceptar un servicio, consulte el miembro **dwControlsAccepted** de la estructura de [**\_ Estado del servicio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) . Para obtener información sobre el registro para recibir eventos de dispositivo, consulte la función [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) .

Normalmente, el estado del servicio cambia como resultado de controlar una solicitud de control. Las solicitudes de control que provocan el cambio del estado del servicio incluyen la \_ detención del control \_ de servicio, la pausa del control de servicio y el \_ \_ control de servicio \_ \_ . Si el servicio debe realizar un procesamiento prolongado para controlar cualquiera de estas solicitudes, debe crear un subproceso secundario para realizar el procesamiento largo y notificar el estado pendiente correspondiente al SCM. (Para obtener el mejor rendimiento en Windows Vista y versiones posteriores de Windows, el servicio debe usar un subproceso de trabajo de un [grupo de subprocesos](/windows/desktop/ProcThread/thread-pools) para este propósito). Después, el servicio debe notificar la transición de estado completado cuando finalice el procesamiento prolongado. Para obtener más información sobre cómo controlar las solicitudes de control, vea [función de controlador de control de servicio](service-control-handler-function.md).

Solo algunas transiciones de estado del servicio son válidas. En el diagrama siguiente se muestran las transiciones válidas.

![transiciones de estado de servicio válidas](images/service-status-transitions.png)

El estado de servicio comunicado al SCM determina cómo interactúa el SCM con el servicio. Por ejemplo, si un servicio de notificaciones de servicio está \_ \_ pendiente, el SCM no transmite más solicitudes de control al servicio porque este estado indica que el servicio se está cerrando. El siguiente estado indicado por el servicio debe ser \_ detenido porque es el único estado válido después de que el servicio se \_ detenga \_ . Sin embargo, si un servicio informa de una transición que no es válida, el SCM no producirá un error en la llamada.

En el diagrama siguiente se muestran las transiciones de estado del servicio con más detalle, incluidas las solicitudes de control iniciadas por un programa de control de servicios (el cliente del servicio) y las llamadas [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) que un servicio realiza para informar de los cambios de estado en el SCM. Como se mencionó anteriormente, el SCM envía solo las solicitudes de control que el servicio ha especificado y acepta, por lo que es posible que un servicio no reciba todas las solicitudes que se muestran en el diagrama.

![transiciones de estado de servicio en detalle ](images/service-status-flow-diagram.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)
</dt> <dt>

[**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)
</dt> <dt>

[**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)
</dt> </dl>

 

 
