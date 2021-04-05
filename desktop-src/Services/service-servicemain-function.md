---
description: Cuando un programa de control de servicios solicita que se ejecute un nuevo servicio, el administrador de control de servicios (SCM) inicia el servicio y envía una solicitud de inicio al distribuidor del control.
ms.assetid: e55e056f-7628-4e3d-9aea-b55c371b4287
title: Función ServiceMain del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed50f0f378f348415e56827a09fcf17eea7fc330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002845"
---
# <a name="service-servicemain-function"></a>Función ServiceMain del servicio

Cuando un programa de control de servicios solicita que se ejecute un nuevo servicio, el administrador de control de servicios (SCM) inicia el servicio y envía una solicitud de inicio al distribuidor del control. El distribuidor de control crea un nuevo subproceso para ejecutar la función [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) para el servicio. Para obtener un ejemplo, vea [escribir una función ServiceMain](writing-a-servicemain-function.md).

La función [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) debe realizar las siguientes tareas:

1.  Inicialice todas las variables globales.
2.  Llame a la función [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) inmediatamente para registrar una función de [**controlador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) para controlar las solicitudes de control del servicio. El valor devuelto de **RegisterServiceCtrlHandler** es un *identificador de estado de servicio* que se usará en las llamadas para notificar al SCM el estado del servicio.
3.  Realizar la inicialización. Si se espera que el tiempo de ejecución del código de inicialización sea muy breve (menos de un segundo), la inicialización se puede realizar directamente en [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona).

    Si se espera que el tiempo de inicialización sea superior a un segundo, el servicio debe usar una de las siguientes técnicas de inicialización:

    -   Llame a la función [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para que el servicio de informes \_ se ejecute, pero no acepte ningún control hasta que finalice la inicialización. Para ello, el servicio llama a **SetServiceStatus** con **DWCURRENTSTATE** establecido en Service \_ Running y **dwControlsAccepted** establecido en 0 en la estructura de [**\_ Estado del servicio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) . Esto garantiza que el SCM no enviará ninguna solicitud de control al servicio antes de que esté listo y liberará el SCM para administrar otros servicios. Se recomienda usar este enfoque para la inicialización en el rendimiento, especialmente en el caso de los servicios de inicio automático.
    -   Inicio del servicio de informes \_ \_ pendiente, no aceptar controles y especificar una sugerencia de espera. Si el código de inicialización del servicio realiza tareas que se espera que tarden más tiempo que el valor de la sugerencia de espera inicial, el código debe llamar a la función [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) periódicamente (posiblemente con una sugerencia de espera revisada) para indicar que se está realizando el progreso. Asegúrese de llamar a **SetServiceStatus** solo si la inicialización está realizando el progreso. En caso contrario, el SCM puede esperar a que el servicio entre en el estado de ejecución del servicio \_ suponiendo que el servicio progresa y bloquee el inicio de otros servicios. No llame a **SetServiceStatus** desde un subproceso independiente a menos que esté seguro de que el subproceso que realiza la inicialización está progresando realmente.

        Un servicio que usa este enfoque también puede especificar un valor de punto de comprobación e incrementar el valor periódicamente durante una inicialización prolongada. El programa que inició el servicio puede llamar a [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) o [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) para obtener el valor de punto de comprobación más reciente del SCM y usar el valor para informar del progreso incremental al usuario.

4.  Una vez completada la inicialización, llame a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para establecer el estado del servicio en servicio en \_ ejecución y especifique los controles que el servicio está preparado para aceptar. Para obtener una lista de controles, consulte la estructura de [**\_ Estado del servicio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) .
5.  Realice las tareas de servicio o, si no hay tareas pendientes, devuelva el control al autor de la llamada. Cualquier cambio en el estado del servicio garantiza una llamada a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para notificar la nueva información de estado.
6.  Si se produce un error mientras el servicio se está inicializando o se está ejecutando, el servicio debe llamar a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para establecer el estado del servicio en \_ detención \_ pendiente si la limpieza va a ser larga. Una vez completada la limpieza, llame a **SetServiceStatus** para establecer el estado del servicio en servicio \_ detenido desde el último subproceso para finalizar. Asegúrese de establecer los miembros **dwServiceSpecificExitCode** y **dwWin32ExitCode** de la estructura [**de \_ Estado del servicio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) para identificar el error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir una función ServiceMain](writing-a-servicemain-function.md)
</dt> </dl>

 

 
