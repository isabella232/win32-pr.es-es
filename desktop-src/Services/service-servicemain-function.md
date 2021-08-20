---
description: Cuando un programa de control de servicio solicita que se ejecute un nuevo servicio, el Administrador de control de servicios (SCM) inicia el servicio y envía una solicitud de inicio al distribuidor de control.
ms.assetid: e55e056f-7628-4e3d-9aea-b55c371b4287
title: Service ServiceMain (Función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bc264bd657f1458a3310f504443ed62abba495c5f56cd08f26b0f41e1da075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967288"
---
# <a name="service-servicemain-function"></a>Service ServiceMain (Función)

Cuando un programa de control de servicio solicita que se ejecute un nuevo servicio, el Administrador de control de servicios (SCM) inicia el servicio y envía una solicitud de inicio al distribuidor de control. El distribuidor de controles crea un nuevo subproceso para ejecutar la [**función ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) para el servicio. Para obtener un ejemplo, vea [Escribir una función ServiceMain](writing-a-servicemain-function.md).

La [**función ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) debe realizar las siguientes tareas:

1.  Inicialice todas las variables globales.
2.  Llame inmediatamente [**a la función RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) para registrar una [**función Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) para controlar las solicitudes de control para el servicio. El valor devuelto de **RegisterServiceCtrlHandler es** un identificador de estado de servicio que se usará en las llamadas para notificar al SCM el estado del servicio. 
3.  Realice la inicialización. Si se espera que el tiempo de ejecución del código de inicialización sea muy corto (menos de un segundo), la inicialización se puede realizar directamente [**en ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona).

    Si se espera que el tiempo de inicialización sea superior a un segundo, el servicio debe usar una de las siguientes técnicas de inicialización:

    -   Llame a la [**función SetServiceStatus para**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) notificar SERVICE RUNNING, pero \_ no acepte ningún control hasta que finalice la inicialización. Para ello, el servicio llama a **SetServiceStatus** con **dwCurrentState** establecido en SERVICE RUNNING y \_ **dwControlsAccepted** establecido en 0 en la [**estructura SERVICE \_ STATUS.**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Esto garantiza que el SCM no enviará ninguna solicitud de control al servicio antes de que esté listo y libera al SCM para administrar otros servicios. Este enfoque de inicialización se recomienda para el rendimiento, especialmente para los servicios de inicio automático.
    -   Report SERVICE \_ START \_ PENDING, no acepte ningún control y especifique una sugerencia de espera. Si el código de inicialización del servicio realiza tareas que se espera que tardan más tiempo que el valor inicial de la sugerencia de espera, el código debe llamar periódicamente a la función [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) (posiblemente con una sugerencia de espera revisada) para indicar que se está avanzando. Asegúrese de llamar a **SetServiceStatus solo** si la inicialización está progresando. De lo contrario, el SCM puede esperar a que el servicio escriba el estado SERVICE RUNNING suponiendo que el servicio está progresando y bloquear el inicio \_ de otros servicios. No llame a **SetServiceStatus desde un** subproceso independiente a menos que esté seguro de que el subproceso que realiza la inicialización está progresando realmente.

        Un servicio que usa este enfoque también puede especificar un valor de punto de comprobación e incrementar el valor periódicamente durante una inicialización larga. El programa que inició el servicio puede llamar a [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) o [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) para obtener el valor de punto de comprobación más reciente del SCM y usar el valor para notificar el progreso incremental al usuario.

4.  Una vez completada la inicialización, llame a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para establecer el estado del servicio en SERVICE RUNNING y especifique los controles que el servicio \_ está preparado para aceptar. Para obtener una lista de controles, vea la [**estructura SERVICE \_ STATUS.**](/windows/desktop/api/Winsvc/ns-winsvc-service_status)
5.  Realice las tareas de servicio o, si no hay tareas pendientes, devuelva el control al autor de la llamada. Cualquier cambio en el estado del servicio garantiza una llamada a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para notificar información de estado nueva.
6.  Si se produce un error mientras el servicio se inicializa o se está ejecutando, el servicio debe llamar a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para establecer el estado del servicio en SERVICE STOP PENDING si la limpieza será \_ \_ larga. Una vez completada la limpieza, llame a **SetServiceStatus para** establecer el estado del servicio en SERVICE STOPPED desde el último subproceso que se \_ va a finalizar. Asegúrese de establecer los **miembros dwServiceSpecificExitCode** y **dwWin32ExitCode** de la estructura [**SERVICE \_ STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) para identificar el error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir una función ServiceMain](writing-a-servicemain-function.md)
</dt> </dl>

 

 
