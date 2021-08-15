---
description: Para iniciar un servicio o servicio de controlador, el programa de control de servicio usa la función StartService.
ms.assetid: 7d2ee779-1554-436a-a65c-f0322745f46a
title: Inicio del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17901987581b6a2680e0a70cfe2e0ed80472d293cbe32932f768e9133b6a058d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888704"
---
# <a name="service-startup"></a>Inicio del servicio

Para iniciar un servicio o servicio de controlador, el programa de control de servicio usa la [**función StartService.**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) Se produce un error en la función **StartService** si la base de datos está bloqueada. Si esto ocurre, el programa de control de servicio debe esperar unos segundos y volver a llamar a **StartService.** Puede comprobar el estado de bloqueo actual de la base de datos llamando a la [**función QueryServiceLockStatus.**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa)

Si el programa de control de servicio inicia un servicio, puede usar la función [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) para especificar una matriz de argumentos que se pasarán a la función [**ServiceMain del**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) servicio. La **función StartService** devuelve después de crear un nuevo subproceso para ejecutar la **función ServiceMain.** El programa de control de servicio puede recuperar el estado del servicio recién iniciado en una estructura [**SERVICE \_ STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) llamando a la [**función QueryServiceStatus.**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) Durante la inicialización, el **miembro dwCurrentState** debe ser SERVICE \_ START \_ PENDING. El **miembro dwWaitHint** es un intervalo de tiempo, en milisegundos, que indica cuánto tiempo debe esperar el programa de control de servicio antes de volver a llamar a **QueryServiceStatus.** Una vez completada la inicialización, el servicio cambia **dwCurrentState** a SERVICE \_ RUNNING.

El administrador de control de servicios no admite el paso de variables de entorno personalizadas a un servicio durante el inicio. Además, el administrador de control de servicios no detecta ni pasa los cambios en las variables de entorno mientras se ejecuta el servicio. En lugar de hacer que un servicio dependa de una variable de entorno, use valores del Registro o [**argumentos de ServiceMain.**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)

A continuación se proporciona información general simplificada de lo que sucede cuando el administrador de control de servicios inicia un servicio típico:

-   El SCM lee la ruta de acceso del servicio del Registro y se prepara para iniciar el servicio. Esto incluye la adquisición del bloqueo de servicio. Cualquier intento de iniciar otro servicio mientras se mantiene el bloqueo del servicio se bloqueará hasta que se libera el bloqueo del servicio.
-   El SCM inicia el proceso y espera hasta que el proceso secundario se cierra (lo que indica un error) o notifica el estado DE \_ EJECUCIÓN DEL SERVICIO.
-   La aplicación realiza su inicialización muy sencilla y llama a la [**función StartServiceCtrlDispatcher.**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)
-   [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) se conecta al administrador de control de servicios e inicia un segundo subproceso que llama a la [**función ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) para el servicio. **ServiceMain debe notificar** service \_ running lo antes posible.
-   Cuando se notifica al administrador de control de servicios que el servicio se está ejecutando, libera el bloqueo del servicio.

Si el servicio no actualiza su estado en 80 segundos, más la última sugerencia de espera, el administrador de control de servicios determina que el servicio ha dejado de responder. El administrador de control de servicios registrará un evento y detendrá el servicio.

Si el programa inicia un servicio de controladores, [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) devuelve una vez que el controlador del dispositivo ha completado su inicialización.

Para obtener más información, vea [Starting a Service](starting-a-service.md).

 

 
