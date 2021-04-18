---
description: Inicio y recuperación de COM+ CRM
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Inicio y recuperación de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714889"
---
# <a name="com-crm-startup-and-recovery"></a><span data-ttu-id="fd3c5-103">Inicio y recuperación de COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="fd3c5-103">COM+ CRM Startup and Recovery</span></span>

<span data-ttu-id="fd3c5-104">Si una aplicación de servidor tiene activada la casilla **Habilitar administradores de compensación de recursos** (mediante la herramienta administrativa Servicios de componentes, en la pestaña **Opciones avanzadas** de la página de propiedades de la aplicación com+), la primera vez que se inicia crea un archivo de registro de CRM para que lo usen todos los CRMs en el proceso de la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-104">If a server application has the **Enable compensating resource managers** checkbox selected (using the Component Services administrative tool, on the **Advanced** tab of the COM+ application's property page), the first time it starts up it creates a CRM log file to be used by all CRMs in that server application process.</span></span> <span data-ttu-id="fd3c5-105">(Para obtener instrucciones detalladas acerca de cómo configurar el CRM, consulte [configuración de componentes com+ CRM](configuring-com--crm-components.md)).</span><span class="sxs-lookup"><span data-stu-id="fd3c5-105">(For detailed instructions about configuring the CRM, see [Configuring COM+ CRM Components](configuring-com--crm-components.md).)</span></span>

<span data-ttu-id="fd3c5-106">El nombre del archivo de registro de CRM creado para la aplicación de servidor se basa en el AppId (GUID) de la aplicación de servidor y el archivo de registro de CRM se coloca en el mismo directorio que el archivo de registro de DTC (normalmente el directorio% SystemRoot% \\ WinNT \\ system32 \\ DtcLog).</span><span class="sxs-lookup"><span data-stu-id="fd3c5-106">The name of the CRM log file created for the server application is based on the AppId (a GUID) of the server application, and the CRM log file is placed in the same directory as the DTC log file (normally your %SystemRoot%\\winnt\\system32\\DtcLog directory).</span></span> <span data-ttu-id="fd3c5-107">Los archivos de registro de CRM tienen la extensión. crmlog.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-107">CRM log files have the extension .crmlog.</span></span>

> [!Note]  
> <span data-ttu-id="fd3c5-108">Puede que sea necesario cambiar la ubicación predeterminada de un archivo de registro de CRM por motivos de rendimiento (para que el archivo de registro de DTC esté en un disco diferente al del archivo de registro de CRM) o quizás debido al uso de CRM en un entorno de clúster.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-108">It may be necessary to change the default location of a CRM log file due to performance reasons (to have the DTC log file on a different disk than the CRM log file) or perhaps due to use of the CRM in a cluster environment.</span></span> <span data-ttu-id="fd3c5-109">La ubicación de los archivos de registro de CRM se puede cambiar mediante el SDK de administración de COM+.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-109">The location of the CRM log files can be changed using the COM+ administration SDK.</span></span> <span data-ttu-id="fd3c5-110">El nombre de la propiedad es CRMLogFile y existe en el objeto de colección de [**aplicaciones**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="fd3c5-110">The property name is CRMLogFile, and it exists on the [**Applications**](applications.md) collection object.</span></span>

 

<span data-ttu-id="fd3c5-111">Cuando una aplicación de servidor (habilitada para CRM) se inicia y detecta que ya existe un archivo de registro de CRM para esa aplicación de servidor, realiza la recuperación en ese archivo de registro de CRM.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-111">When a server application (that is CRM-enabled) starts up and finds that a CRM log file already exists for that server application, it performs recovery on that CRM log file.</span></span> <span data-ttu-id="fd3c5-112">La *recuperación* es el proceso de completar cualquier transacción interrumpida por un error e implica que la infraestructura de CRM Lea el archivo de registro de CRM para las transacciones que no se completaron completamente.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-112">*Recovery* is the process of completing any transactions that were interrupted by a failure and involves the CRM infrastructure reading the CRM log file for any transactions that were not fully completed.</span></span> <span data-ttu-id="fd3c5-113">Si encuentra alguno, se pone en contacto con el DTC para determinar el resultado de la transacción.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-113">If it finds any, it contacts the DTC to determine the transaction outcome.</span></span> <span data-ttu-id="fd3c5-114">A continuación, crea el compensador de CRM y pasa las notificaciones commit o Abort según sea necesario, junto con las entradas de registro asociadas.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-114">It then creates the CRM Compensator and passes on the commit or abort notifications as required, together with the associated log records.</span></span>

<span data-ttu-id="fd3c5-115">El compensador de CRM no recibe las notificaciones de preparación durante la recuperación.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-115">Prepare notifications are not received by the CRM Compensator during recovery.</span></span> <span data-ttu-id="fd3c5-116">El compensador de CRM tiene una marca para distinguir si se llama durante el funcionamiento normal o durante la recuperación.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-116">The CRM Compensator has a flag to distinguish whether it is being called during normal operation or during recovery.</span></span>

<span data-ttu-id="fd3c5-117">Normalmente, la recuperación solo encontrará transacciones incompletas si la aplicación de servidor se ha cerrado de forma anómala, debido a un bloqueo del proceso de la aplicación de servidor o a un bloqueo del equipo.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-117">Recovery will normally find uncompleted transactions only if the server application has been shutdown abnormally, due to either a server application process crash or a computer crash.</span></span> <span data-ttu-id="fd3c5-118">Si se permite que la aplicación de servidor se apague normalmente, debido al tiempo de espera de inactividad o al cierre manual a través de la herramienta administrativa Servicios de componentes, el archivo de registro estará limpio.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-118">If the server application is allowed to shut down normally, due either to the idle time-out or to manual shutdown via the Component Services administrative tool, the log file will be clean.</span></span>

<span data-ttu-id="fd3c5-119">El inicio de una aplicación de servidor CRM para la recuperación no se inicia automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-119">Starting of a CRM server application for recovery is not automatically initiated.</span></span> <span data-ttu-id="fd3c5-120">Se debe realizar alguna acción externa para iniciar la aplicación de servidor CRM donde se requiere recuperación.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-120">Some external action must be taken to start the CRM server application where recovery is required.</span></span> <span data-ttu-id="fd3c5-121">Normalmente, esto sería crear un componente en esa aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="fd3c5-121">Typically this would be creating a component in that server application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd3c5-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd3c5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd3c5-123">Conceptos de Administrador de recursos de compensación de COM+</span><span class="sxs-lookup"><span data-stu-id="fd3c5-123">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[<span data-ttu-id="fd3c5-124">Proceso operativo COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="fd3c5-124">COM+ CRM Operating Process</span></span>](com--crm-operating-process.md)
</dt> </dl>

 

 



