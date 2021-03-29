---
description: Puede usar cualquiera de los métodos siguientes para depurar el servicio.
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: Depuración de un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809248"
---
# <a name="debugging-a-service"></a>Depuración de un servicio

Puede usar cualquiera de los métodos siguientes para depurar el servicio.

-   Use el depurador para depurar el servicio mientras se está ejecutando. En primer lugar, obtenga el identificador de proceso (PID) del proceso de servicio. Una vez obtenido el PID, adjunte al proceso en ejecución. Para obtener información sobre la sintaxis, vea la documentación que se incluye con el depurador.
-   Llame a la función [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) para invocar el depurador Just-in-Time.
-   Especifique el depurador que se va a utilizar al iniciar un programa. Para ello, cree una clave denominada **Image File Execution Options** en la siguiente ubicación del registro:

    **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**

    Cree una subclave con el mismo nombre que el servicio (por ejemplo, MYSERV.EXE). Para esta subclave, agregue un valor de tipo **reg \_ SZ**, denominado **Debugger**. Use la ruta de acceso completa al depurador como el valor de cadena. En el applet servicios del panel de control, seleccione el servicio, haga clic en **Inicio** y Active **permitir que el servicio interactúe con el escritorio**. El servicio debe ser un servicio interactivo o, de lo contrario, el depurador no se puede ejecutar en el escritorio predeterminado. Tenga en cuenta que esta técnica ya no es compatible con Windows Vista porque todos los servicios se ejecutan en una sesión que está reservada exclusivamente para servicios y no admite la visualización de una interfaz de usuario.

-   Use el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) para registrar información.

Para depurar el código de inicialización de un servicio de inicio automático, tendrá que instalar y ejecutar temporalmente el servicio como un servicio de inicio de petición.

En ocasiones, puede ser necesario ejecutar un servicio como una aplicación de consola para la depuración. En este escenario, la función [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) devolverá **error error \_ al \_ \_ \_ conectar el controlador de servicio**. Por lo tanto, asegúrese de estructurar el código para que no se llame al código específico del servicio cuando se devuelva este error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depurar una aplicación de servicio](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[Herramientas de depuración para Windows](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
