---
description: Durante el arranque del sistema, el SCM inicia todos los servicios de inicio automático y los servicios de los que dependen. Por ejemplo, si un servicio de inicio automático depende de un servicio de inicio de petición, el servicio de inicio de petición también se inicia automáticamente.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Inicio automático de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666349"
---
# <a name="automatically-starting-services"></a><span data-ttu-id="5ecd8-104">Inicio automático de servicios</span><span class="sxs-lookup"><span data-stu-id="5ecd8-104">Automatically Starting Services</span></span>

<span data-ttu-id="5ecd8-105">Durante el arranque del sistema, el SCM inicia todos los servicios de inicio automático y los servicios de los que dependen.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-105">During system boot, the SCM starts all auto-start services and the services on which they depend.</span></span> <span data-ttu-id="5ecd8-106">Por ejemplo, si un servicio de inicio automático depende de un servicio de inicio de petición, el servicio de inicio de petición también se inicia automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-106">For example, if an auto-start service depends on a demand-start service, the demand-start service is also started automatically.</span></span>

<span data-ttu-id="5ecd8-107">El orden de carga está determinado por lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5ecd8-107">The load order is determined by the following:</span></span>

1.  <span data-ttu-id="5ecd8-108">El orden de los grupos en la lista de grupos de orden de carga.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-108">The order of groups in the load ordering group list.</span></span> <span data-ttu-id="5ecd8-109">Esta información se almacena en el valor **ServiceGroupOrder** en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="5ecd8-109">This information is stored in the **ServiceGroupOrder** value in the following registry key:</span></span>

    <span data-ttu-id="5ecd8-110">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control**</span><span class="sxs-lookup"><span data-stu-id="5ecd8-110">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

    <span data-ttu-id="5ecd8-111">Para especificar el grupo de pedidos de carga para un servicio, use el parámetro *lpLoadOrderGroup* de la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) o [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="5ecd8-111">To specify the load ordering group for a service, use the *lpLoadOrderGroup* parameter of the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) or [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) function.</span></span>

2.  <span data-ttu-id="5ecd8-112">El orden de los servicios dentro de un grupo especificado en el vector de orden de las etiquetas.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-112">The order of services within a group specified in the tags order vector.</span></span> <span data-ttu-id="5ecd8-113">Esta información se almacena en el valor **GroupOrderList** en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="5ecd8-113">This information is stored in the **GroupOrderList** value in the following registry key:</span></span>

    <span data-ttu-id="5ecd8-114">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control**</span><span class="sxs-lookup"><span data-stu-id="5ecd8-114">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

3.  <span data-ttu-id="5ecd8-115">Las dependencias enumeradas para cada servicio.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-115">The dependencies listed for each service.</span></span>

<span data-ttu-id="5ecd8-116">Una vez completado el arranque, el sistema ejecuta el programa de comprobación de arranque especificado por el valor **BootVerificationProgram** de la siguiente clave del registro: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control**.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-116">When the boot is complete, the system executes the boot verification program specified by the **BootVerificationProgram** value of the following registry key: **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control**.</span></span>

<span data-ttu-id="5ecd8-117">De manera predeterminada, este valor no está establecido.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-117">By default, this value is not set.</span></span> <span data-ttu-id="5ecd8-118">El sistema simplemente informa de que el arranque se realizó correctamente después de que el primer usuario haya iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-118">The system simply reports that the boot was successful after the first user has logged on.</span></span> <span data-ttu-id="5ecd8-119">Puede proporcionar un programa de comprobación de arranque que compruebe si hay problemas en el sistema e informa del estado de arranque al SCM mediante la función [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .</span><span class="sxs-lookup"><span data-stu-id="5ecd8-119">You can supply a boot verification program that checks the system for problems and reports the boot status to the SCM using the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>

<span data-ttu-id="5ecd8-120">Después de un arranque correcto, el sistema guarda un clon de la base de datos en la última configuración buena conocida (válida conocida).</span><span class="sxs-lookup"><span data-stu-id="5ecd8-120">After a successful boot, the system saves a clone of the database in the last-known-good (LKG) configuration.</span></span> <span data-ttu-id="5ecd8-121">El sistema puede restaurar esta copia de la base de datos si los cambios realizados en la base de datos activa provocan un error en el reinicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-121">The system can restore this copy of the database if changes made to the active database cause the system reboot to fail.</span></span> <span data-ttu-id="5ecd8-122">A continuación se encuentra la clave del registro para esta base de datos:</span><span class="sxs-lookup"><span data-stu-id="5ecd8-122">The following is the registry key for this database:</span></span>

<span data-ttu-id="5ecd8-123">**HKEY \_ local \_ Machine \\ System \\ ControlSet *XXX* \\ Services**</span><span class="sxs-lookup"><span data-stu-id="5ecd8-123">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\ControlSet *XXX*\\Services**</span></span>

<span data-ttu-id="5ecd8-124">donde *XXX* es el valor que se guarda en el siguiente valor del registro: **HKEY \_ local \_ Machine \\ System \\ SELECT \\ LastKnownGood**.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-124">where *XXX* is the value saved in the following registry value: **HKEY\_LOCAL\_MACHINE\\System\\Select\\LastKnownGood**.</span></span>

<span data-ttu-id="5ecd8-125">Si no se puede iniciar un servicio de inicio automático con un error de servicio \_ \_ crítico nivel de control de errores, el SCM reinicia el equipo con la configuración de válida conocida.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-125">If an auto-start service with a SERVICE\_ERROR\_CRITICAL error control level fails to start, the SCM reboots the computer using the LKG configuration.</span></span> <span data-ttu-id="5ecd8-126">Si ya se usa la configuración válida conocida, se produce un error en el arranque.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-126">If the LKG configuration is already being used, the boot fails.</span></span>

<span data-ttu-id="5ecd8-127">Un servicio de inicio automático se puede configurar como un servicio de inicio automático retrasado mediante una llamada a la función [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) con la \_ información de \_ Inicio automático retrasada de la configuración del servicio \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5ecd8-127">An auto-start service can be configured as a delayed auto-start service by calling the [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function with SERVICE\_CONFIG\_DELAYED\_AUTO\_START\_INFO.</span></span> <span data-ttu-id="5ecd8-128">Este cambio surte efecto después del siguiente arranque del sistema.</span><span class="sxs-lookup"><span data-stu-id="5ecd8-128">This change takes effect after the next system boot.</span></span> <span data-ttu-id="5ecd8-129">Para obtener más información, [**vea \_ \_ información de \_ Inicio \_ automático retrasado del servicio**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span><span class="sxs-lookup"><span data-stu-id="5ecd8-129">For more information, see [**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span></span>

 

 



