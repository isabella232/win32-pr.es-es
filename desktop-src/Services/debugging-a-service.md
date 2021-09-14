---
description: Puede usar cualquiera de los métodos siguientes para depurar el servicio.
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: Depuración de un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265068"
---
# <a name="debugging-a-service"></a>Depuración de un servicio

Puede usar cualquiera de los métodos siguientes para depurar el servicio.

-   Use el depurador para depurar el servicio mientras se está ejecutando. En primer lugar, obtenga el identificador de proceso (PID) del proceso de servicio. Una vez que haya obtenido el PID, adjunte al proceso en ejecución. Para obtener información sobre la sintaxis, consulte la documentación incluida con el depurador.
-   Llame a [**la función DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) para invocar el depurador para la depuración Just-In-Time.
-   Especifique un depurador que se usará al iniciar un programa. Para ello, cree una clave denominada Opciones de **ejecución de archivos de imagen** en la siguiente ubicación del Registro:

    **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion**

    Cree una subclave con el mismo nombre que el servicio (por ejemplo, MYSERV.EXE). A esta subclave, agregue un valor de tipo **REG \_ SZ**, denominado **Debugger**. Use la ruta de acceso completa al depurador como valor de cadena. En el applet del panel de control Servicios, seleccione el servicio, haga clic en **Inicio** y active Permitir que **el servicio interactúe con el escritorio.** El servicio debe ser un servicio interactivo o, de lo contrario, el depurador no se puede ejecutar en el escritorio predeterminado. Tenga en cuenta que esta técnica ya no se admite desde Windows Vista porque todos los servicios se ejecutan en una sesión reservada exclusivamente para los servicios y no admite la visualización de una interfaz de usuario.

-   Use [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) para registrar información.

Para depurar el código de inicialización de un servicio de inicio automático, tendrá que instalar y ejecutar temporalmente el servicio como servicio de inicio a petición.

En ocasiones, puede ser necesario ejecutar un servicio como una aplicación de consola con fines de depuración. En este escenario, la [**función StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) devolverá **ERROR FAILED SERVICE CONTROLLER \_ \_ \_ \_ CONNECT**. Por lo tanto, asegúrese de estructurar el código para que no se llame al código específico del servicio cuando se devuelva este error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depuración de una aplicación de servicio](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[Herramientas de depuración para Windows](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
