---
description: Para iniciar un servicio o un servicio de controlador, el programa de control de servicios utiliza la función StartService.
ms.assetid: 7d2ee779-1554-436a-a65c-f0322745f46a
title: Inicio del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fcd9ee820357e75bf07649da8e6c5445d3f42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668464"
---
# <a name="service-startup"></a>Inicio del servicio

Para iniciar un servicio o un servicio de controlador, el programa de control de servicios utiliza la función [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) . Se produce un error en la función **StartService** si la base de datos está bloqueada. Si esto ocurre, el programa de control de servicios debe esperar unos segundos y volver a llamar a **StartService** . Puede comprobar el estado de bloqueo actual de la base de datos mediante una llamada a la función [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) .

Si el programa de control de servicios está iniciando un servicio, puede usar la función [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) para especificar una matriz de argumentos que se van a pasar a la función [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) del servicio. La función **StartService** devuelve después de crear un nuevo subproceso para ejecutar la función **ServiceMain** . El programa de control de servicios puede recuperar el estado del servicio recién iniciado en una estructura de [**\_ Estado de servicio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) llamando a la función [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) . Durante la inicialización, el miembro **dwCurrentState** debe ser un inicio de servicio \_ \_ pendiente. El miembro **dwWaitHint** es un intervalo de tiempo, en milisegundos, que indica cuánto tiempo debe esperar el programa de control de servicio antes de volver a llamar a **QueryServiceStatus** . Una vez completada la inicialización, el servicio cambia **dwCurrentState** al servicio en \_ ejecución.

El administrador de control de servicios no permite pasar variables de entorno personalizadas a un servicio en el inicio. Además, el administrador de control de servicios no detecta ni pasa los cambios en las variables de entorno cuando el servicio se está ejecutando. En lugar de que un servicio dependa de una variable de entorno, use valores del registro o argumentos de [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) .

A continuación se ofrece una introducción simplificada de lo que ocurre cuando el administrador de control de servicios inicia un servicio típico:

-   El SCM lee la ruta de acceso del servicio desde el registro y se prepara para iniciar el servicio. Esto incluye la adquisición del bloqueo de servicio. Cualquier intento de iniciar otro servicio mientras se mantiene el bloqueo del servicio se bloqueará hasta que se libere el bloqueo del servicio.
-   El SCM inicia el proceso y espera hasta que se cierra el proceso secundario (lo que indica un error) o informa del \_ Estado de ejecución del servicio.
-   La aplicación realiza su inicialización muy sencilla y llama a la función [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) .
-   [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) se conecta al administrador de control de servicios e inicia un segundo subproceso que llama a la función [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) para el servicio. **ServiceMain** debe notificar el servicio \_ en ejecución lo antes posible.
-   Cuando el administrador de control de servicios recibe una notificación de que el servicio se está ejecutando, libera el bloqueo del servicio.

Si el servicio no actualiza su estado en 80 segundos, más la sugerencia de última espera, el administrador de control de servicios determina que el servicio ha dejado de responder. El administrador de control de servicios registrará un evento y detendrá el servicio.

Si el programa está iniciando un servicio de controlador, [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) vuelve una vez que el controlador de dispositivo ha completado su inicialización.

Para obtener más información, consulte [Inicio de un servicio](starting-a-service.md).

 

 
