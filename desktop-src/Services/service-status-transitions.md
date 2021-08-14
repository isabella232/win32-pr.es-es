---
description: Un servicio es responsable de notificar los cambios en su estado al administrador de control de servicios (SCM).
ms.assetid: 74a85730-6667-46fe-ae12-26561ccedb73
title: Transiciones de estado de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7039caf68ee7d9da93e86e1760e49df87667da8c16eb5ca6693cfdc7db7def2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967327"
---
# <a name="service-state-transitions"></a>Transiciones de estado de servicio

Un servicio es responsable de notificar los cambios en su estado al administrador de control de servicios (SCM). Los programas de control de servicio y el sistema pueden averiguar el estado de un servicio solo desde el SCM, por lo que es importante que un servicio informe de su estado correctamente. Un servicio notifica su estado llamando a la [**función SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con un puntero a una estructura [**SERVICE STATUS \_ totalmente**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) inicializada. El **miembro dwCurrentState** de la estructura contiene el estado del servicio que se va a notifica.

El estado inicial de un servicio es SERVICE \_ STOPPED. Cuando el SCM inicia el servicio, establece el estado del servicio en SERVICE START PENDING y llama a la \_ \_ función [*ServiceMain del*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) servicio. A continuación, el servicio completa su inicialización mediante una de las técnicas descritas en [Service ServiceMain Function](service-servicemain-function.md). Una vez que el servicio completa su inicialización y está listo para empezar a recibir solicitudes de control, el servicio llama a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para notificar SERVICE RUNNING y especificar las solicitudes de control que el servicio está preparado \_ para aceptar. La transición de SERVICE START PENDING a SERVICE RUNNING indica a SCM y a las herramientas de supervisión del servicio que el servicio \_ \_ se ha iniciado \_ correctamente. Si el servicio informa de un estado distinto de SERVICE RUNNING, las herramientas SCM o de supervisión de servicios podrían marcar el servicio como no se pudo \_ iniciar.

El SCM envía solo las solicitudes de control especificadas al servicio (excepto la solicitud SERVICE \_ CONTROL \_ INTERROGATE, que siempre se envía). Para obtener una lista de las solicitudes de control que un servicio puede aceptar, vea el **miembro dwControlsAccepted** de la [**estructura SERVICE \_ STATUS.**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Para obtener información sobre cómo registrarse para recibir eventos de dispositivo, vea [**la función RegisterDeviceNotification.**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)

El estado del servicio normalmente cambia como resultado de controlar una solicitud de control. Las solicitudes de control que hacen que el estado del servicio cambie incluyen SERVICE \_ CONTROL \_ STOP, SERVICE \_ CONTROL PAUSE y SERVICE CONTROL \_ \_ \_ CONTINUE. Si el servicio debe realizar un procesamiento largo para controlar cualquiera de estas solicitudes, debe crear un subproceso secundario para realizar el procesamiento largo e informar del estado pendiente correspondiente al SCM. (Para obtener el mejor rendimiento en Windows Vista y versiones posteriores de Windows, el servicio debe usar un subproceso de trabajo de un grupo de subprocesos [para](/windows/desktop/ProcThread/thread-pools) este propósito). A continuación, el servicio debe notificar la transición de estado completada cuando finalice el procesamiento largo. Para obtener más información sobre cómo controlar las solicitudes de control, vea [Función del controlador de control de servicio](service-control-handler-function.md).

Solo ciertas transiciones de estado de servicio son válidas. En el diagrama siguiente se muestran las transiciones válidas.

![transiciones de estado de servicio válidas](images/service-status-transitions.png)

El estado del servicio notificado al SCM determina cómo interactúa el SCM con el servicio. Por ejemplo, si un servicio notifica SERVICE STOP PENDING, el SCM no transmite más solicitudes de control al servicio porque este estado indica que el servicio \_ \_ se está cerrando. El siguiente estado notificado por el servicio debe ser SERVICE STOPPED porque es el único estado válido después \_ de SERVICE \_ STOP \_ PENDING. Sin embargo, si un servicio informa de una transición que no es válida, el SCM no producirá un error en la llamada.

En el diagrama siguiente se muestran las transiciones de estado del servicio con más detalle, incluidas las solicitudes de control iniciadas por un programa de control de servicio (el cliente de servicio) y las llamadas [**setServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) que realiza un servicio para notificar los cambios de estado en el SCM. Como se mencionó anteriormente, el SCM envía solo las solicitudes de control que el servicio ha especificado que aceptará, por lo que es posible que un servicio no reciba todas las solicitudes que se muestran en el diagrama.

![transiciones de estado de servicio en detalle ](images/service-status-flow-diagram.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)
</dt> <dt>

[**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)
</dt> <dt>

[**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)
</dt> </dl>

 

 
