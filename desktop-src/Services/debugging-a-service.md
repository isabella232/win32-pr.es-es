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
# <a name="debugging-a-service"></a><span data-ttu-id="b774a-103">Depuración de un servicio</span><span class="sxs-lookup"><span data-stu-id="b774a-103">Debugging a Service</span></span>

<span data-ttu-id="b774a-104">Puede usar cualquiera de los métodos siguientes para depurar el servicio.</span><span class="sxs-lookup"><span data-stu-id="b774a-104">You can use any one of the following methods to debug your service.</span></span>

-   <span data-ttu-id="b774a-105">Use el depurador para depurar el servicio mientras se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="b774a-105">Use your debugger to debug the service while it is running.</span></span> <span data-ttu-id="b774a-106">En primer lugar, obtenga el identificador de proceso (PID) del proceso de servicio.</span><span class="sxs-lookup"><span data-stu-id="b774a-106">First, obtain the process identifier (PID) of the service process.</span></span> <span data-ttu-id="b774a-107">Una vez obtenido el PID, adjunte al proceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="b774a-107">After you have obtained the PID, attach to the running process.</span></span> <span data-ttu-id="b774a-108">Para obtener información sobre la sintaxis, vea la documentación que se incluye con el depurador.</span><span class="sxs-lookup"><span data-stu-id="b774a-108">For syntax information, see the documentation included with your debugger.</span></span>
-   <span data-ttu-id="b774a-109">Llame a la función [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) para invocar el depurador Just-in-Time.</span><span class="sxs-lookup"><span data-stu-id="b774a-109">Call the [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) function to invoke the debugger for just-in-time debugging.</span></span>
-   <span data-ttu-id="b774a-110">Especifique el depurador que se va a utilizar al iniciar un programa.</span><span class="sxs-lookup"><span data-stu-id="b774a-110">Specify a debugger to use when starting a program.</span></span> <span data-ttu-id="b774a-111">Para ello, cree una clave denominada **Image File Execution Options** en la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="b774a-111">To do so, create a key called **Image File Execution Options** in the following registry location:</span></span>

    <span data-ttu-id="b774a-112">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="b774a-112">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>

    <span data-ttu-id="b774a-113">Cree una subclave con el mismo nombre que el servicio (por ejemplo, MYSERV.EXE).</span><span class="sxs-lookup"><span data-stu-id="b774a-113">Create a subkey with the same name as your service (for example, MYSERV.EXE).</span></span> <span data-ttu-id="b774a-114">Para esta subclave, agregue un valor de tipo **reg \_ SZ**, denominado **Debugger**.</span><span class="sxs-lookup"><span data-stu-id="b774a-114">To this subkey, add a value of type **REG\_SZ**, named **Debugger**.</span></span> <span data-ttu-id="b774a-115">Use la ruta de acceso completa al depurador como el valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="b774a-115">Use the full path to the debugger as the string value.</span></span> <span data-ttu-id="b774a-116">En el applet servicios del panel de control, seleccione el servicio, haga clic en **Inicio** y Active **permitir que el servicio interactúe con el escritorio**.</span><span class="sxs-lookup"><span data-stu-id="b774a-116">In the Services control panel applet, select your service, click **Startup** and check **Allow Service to Interact with Desktop**.</span></span> <span data-ttu-id="b774a-117">El servicio debe ser un servicio interactivo o, de lo contrario, el depurador no se puede ejecutar en el escritorio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b774a-117">The service must be an interactive service, or else the debugger cannot run on the default desktop.</span></span> <span data-ttu-id="b774a-118">Tenga en cuenta que esta técnica ya no es compatible con Windows Vista porque todos los servicios se ejecutan en una sesión que está reservada exclusivamente para servicios y no admite la visualización de una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b774a-118">Note that this technique is no longer supported as of Windows Vista because all services are run in session that is reserved exclusively for services and does not support displaying a user interface.</span></span>

-   <span data-ttu-id="b774a-119">Use el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) para registrar información.</span><span class="sxs-lookup"><span data-stu-id="b774a-119">Use [Event Tracing](/windows/desktop/ETW/event-tracing-portal) to log information.</span></span>

<span data-ttu-id="b774a-120">Para depurar el código de inicialización de un servicio de inicio automático, tendrá que instalar y ejecutar temporalmente el servicio como un servicio de inicio de petición.</span><span class="sxs-lookup"><span data-stu-id="b774a-120">To debug the initialization code of an auto-start service, you will have to temporarily install and run the service as a demand-start service.</span></span>

<span data-ttu-id="b774a-121">En ocasiones, puede ser necesario ejecutar un servicio como una aplicación de consola para la depuración.</span><span class="sxs-lookup"><span data-stu-id="b774a-121">At times, it may be necessary to run a service as a console application for debugging purposes.</span></span> <span data-ttu-id="b774a-122">En este escenario, la función [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) devolverá **error error \_ al \_ \_ \_ conectar el controlador de servicio**.</span><span class="sxs-lookup"><span data-stu-id="b774a-122">In this scenario, the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function will return **ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**.</span></span> <span data-ttu-id="b774a-123">Por lo tanto, asegúrese de estructurar el código para que no se llame al código específico del servicio cuando se devuelva este error.</span><span class="sxs-lookup"><span data-stu-id="b774a-123">Therefore, be sure to structure your code such that service-specific code is not called when this error is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b774a-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b774a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b774a-125">Depurar una aplicación de servicio</span><span class="sxs-lookup"><span data-stu-id="b774a-125">Debugging a Service Application</span></span>](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[<span data-ttu-id="b774a-126">Herramientas de depuración para Windows</span><span class="sxs-lookup"><span data-stu-id="b774a-126">Debugging Tools for Windows</span></span>](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
