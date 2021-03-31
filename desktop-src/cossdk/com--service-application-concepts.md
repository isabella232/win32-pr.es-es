---
description: Conceptos de la aplicación de servicio COM+
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Conceptos de la aplicación de servicio COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496054"
---
# <a name="com-service-application-concepts"></a><span data-ttu-id="84def-103">Conceptos de la aplicación de servicio COM+</span><span class="sxs-lookup"><span data-stu-id="84def-103">COM+ Service Application Concepts</span></span>

<span data-ttu-id="84def-104">Puede usar la herramienta administrativa Servicios de componentes para configurar una aplicación de servidor COM+ como una aplicación de servicio.</span><span class="sxs-lookup"><span data-stu-id="84def-104">You can use the Component Services administrative tool to configure a COM+ server application as a service application.</span></span> <span data-ttu-id="84def-105">La ejecución de una aplicación de servidor COM+ como servicio ofrece las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="84def-105">Running a COM+ server application as a service offers the following advantages:</span></span>

-   <span data-ttu-id="84def-106">Si la aplicación siempre debe estar en ejecución, los servicios de componentes pueden tener opcionalmente que el servidor se inicie automáticamente y también puede reiniciar el servidor si se agota el tiempo de espera. Por ejemplo, si se reinicia un equipo que ejecuta componentes del agente de escucha de componentes en cola, los agentes de escucha de los componentes en cola se pueden iniciar automáticamente si están configurados como un servicio.</span><span class="sxs-lookup"><span data-stu-id="84def-106">If your application always needs to be running, Component Services can optionally have the server started automatically and can also restart the server if it times out. For example, if a computer running Queued Components listener components is rebooted, the Queued Components listeners can be started automatically if they are configured as a service.</span></span>
-   <span data-ttu-id="84def-107">Si la aplicación necesita realizar operaciones con privilegios, la aplicación se puede ejecutar como la cuenta del sistema local.</span><span class="sxs-lookup"><span data-stu-id="84def-107">If your application needs to perform privileged operations, the application can run as the local system account.</span></span> <span data-ttu-id="84def-108">Solo se permite que los servicios NT se ejecuten con este nivel de seguridad.</span><span class="sxs-lookup"><span data-stu-id="84def-108">Only NT services are allowed to run with this level of security.</span></span> <span data-ttu-id="84def-109">La aplicación será compatible con la Servicio de clúster de Windows, que administra los servicios durante la conmutación por error del sistema.</span><span class="sxs-lookup"><span data-stu-id="84def-109">The application will be compatible with the Windows Cluster service, which manages services during system failover.</span></span>
-   <span data-ttu-id="84def-110">Si otros servicios deben marcarse como dependientes, servicios de componentes proporciona esa opción.</span><span class="sxs-lookup"><span data-stu-id="84def-110">If other services need to be marked as dependent, Component Services provides that option.</span></span> <span data-ttu-id="84def-111">Por ejemplo, si la aplicación hace uso de la funcionalidad proporcionada por otro servicio, el servicio marcado como dependiente se iniciará antes de que se inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="84def-111">For example, if your application makes use of functionality provided by another service, the service marked as dependent will be started before your application starts.</span></span>

## <a name="starting-an-application-automatically"></a><span data-ttu-id="84def-112">Inicio automático de una aplicación</span><span class="sxs-lookup"><span data-stu-id="84def-112">Starting an Application Automatically</span></span>

<span data-ttu-id="84def-113">Cuando la aplicación de servidor COM+ se inicia automáticamente, actúa como un servicio, lo que requiere que el desarrollador administre el servidor mediante la herramienta administrativa servicios.</span><span class="sxs-lookup"><span data-stu-id="84def-113">When the COM+ server application is started automatically, it acts like a service, requiring the developer to manage the server using the Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="84def-114">Se puede tener acceso a la herramienta administrativa Servicios iniciando la herramienta administrativa Servicios de componentes y haciendo clic en **servicios (local)**.</span><span class="sxs-lookup"><span data-stu-id="84def-114">The Services administrative tool can be accessed by launching the Component Services administrative tool and then clicking **Services (Local)**.</span></span>

 

## <a name="starting-an-application-manually"></a><span data-ttu-id="84def-115">Inicio manual de una aplicación</span><span class="sxs-lookup"><span data-stu-id="84def-115">Starting an Application Manually</span></span>

<span data-ttu-id="84def-116">Cuando la aplicación de servidor COM+ se inicia manualmente, actúa como un host de DLL con la configuración de seguridad de un servicio.</span><span class="sxs-lookup"><span data-stu-id="84def-116">When the COM+ server application is started manually, it acts like a DLL host with the security settings of a service.</span></span> <span data-ttu-id="84def-117">El servicio se iniciará manualmente cuando se active y se apagará automáticamente cuando se agote el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="84def-117">The service will be started up manually when activated and shut down automatically when it times out.</span></span>

## <a name="service-configurations"></a><span data-ttu-id="84def-118">Configuraciones de servicio</span><span class="sxs-lookup"><span data-stu-id="84def-118">Service Configurations</span></span>

<span data-ttu-id="84def-119">Independientemente del tipo de inicio, la aplicación puede configurarse para ejecutarse como una cuenta de sistema local o asignarse a una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="84def-119">Regardless of the startup type, the application can be configured to run as a local system account or assigned to a user account.</span></span> <span data-ttu-id="84def-120">El sistema local y la cuenta de usuario se pueden configurar en el momento de crear el servicio.</span><span class="sxs-lookup"><span data-stu-id="84def-120">The local system and user account can be configured at the time of creating the service.</span></span> <span data-ttu-id="84def-121">Para configurar las opciones de seguridad, se debe usar la herramienta administrativa servicios.</span><span class="sxs-lookup"><span data-stu-id="84def-121">To configure the security settings, the Services administrative tool will have to be used.</span></span> <span data-ttu-id="84def-122">También se pueden establecer dependencias para el servicio.</span><span class="sxs-lookup"><span data-stu-id="84def-122">Dependencies can also be set for the service.</span></span>

<span data-ttu-id="84def-123">La aplicación también puede iniciarse en cualquier orden determinado seleccionando dependencias de una lista de otros servicios del sistema.</span><span class="sxs-lookup"><span data-stu-id="84def-123">The application can also be started in any particular order by selecting dependencies from a list of other system services.</span></span> <span data-ttu-id="84def-124">Por ejemplo, los servicios del sistema se pueden marcar como dependientes y no iniciarán la aplicación hasta que se hayan iniciado los servicios del sistema en el orden especificado.</span><span class="sxs-lookup"><span data-stu-id="84def-124">For example, the system services can be marked as dependent and will not start the application until the system services have been started in the specified order.</span></span> <span data-ttu-id="84def-125">Esto inicializará correctamente la aplicación de servicio antes de que se use.</span><span class="sxs-lookup"><span data-stu-id="84def-125">This will properly initialize the service application before it is used.</span></span>

<span data-ttu-id="84def-126">Para obtener instrucciones paso a paso sobre cómo configurar una aplicación COM+ para que se ejecute como un servicio, vea [configurar una aplicación de servidor com+ como aplicación de servicio](configuring-a-com--server-application-as-a-service-application.md).</span><span class="sxs-lookup"><span data-stu-id="84def-126">For a step-by-step instruction on how to configure a COM+ application to run as a service, see [Configuring a COM+ Server Application as a Service Application](configuring-a-com--server-application-as-a-service-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84def-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84def-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84def-128">Tareas de aplicación de servicio COM+</span><span class="sxs-lookup"><span data-stu-id="84def-128">COM+ Service Application Tasks</span></span>](com--service-application-tasks.md)
</dt> </dl>

 

 



