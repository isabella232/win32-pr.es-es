---
description: La interfaz IAutomaticUpdatesSettings define las siguientes propiedades.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Propiedades de IAutomaticUpdatesSettings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001206"
---
# <a name="iautomaticupdatessettings-properties"></a><span data-ttu-id="00818-103">Propiedades de IAutomaticUpdatesSettings</span><span class="sxs-lookup"><span data-stu-id="00818-103">IAutomaticUpdatesSettings Properties</span></span>

<span data-ttu-id="00818-104">La interfaz [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="00818-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following properties.</span></span>



| <span data-ttu-id="00818-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="00818-105">Property</span></span>                                                                                 | <span data-ttu-id="00818-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="00818-106">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00818-107">**NotificationLevel**</span><span class="sxs-lookup"><span data-stu-id="00818-107">**NotificationLevel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | <span data-ttu-id="00818-108">Obtiene y establece cómo se notifica a los usuarios acerca de los eventos de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="00818-108">Gets and sets how users are notified about Automatic Update events.</span></span>                              |
| [<span data-ttu-id="00818-109">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="00818-109">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | <span data-ttu-id="00818-110">Obtiene un valor booleano que indica si la configuración de actualización automática es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="00818-110">Gets a Boolean value that indicates whether the Automatic Update settings are read-only.</span></span>         |
| [<span data-ttu-id="00818-111">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="00818-111">**Required**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | <span data-ttu-id="00818-112">Obtiene un valor booleano que indica si directiva de grupo requiere el servicio Actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="00818-112">Gets a Boolean value that indicates whether Group Policy requires the Automatic Updates service.</span></span> |
| [<span data-ttu-id="00818-113">**ScheduledInstallationDay**</span><span class="sxs-lookup"><span data-stu-id="00818-113">**ScheduledInstallationDay**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | <span data-ttu-id="00818-114">Obtiene y establece los días de la semana en los que Actualizaciones automáticas instala o desinstala las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="00818-114">Gets and sets the days of the week on which Automatic Updates installs or uninstalls updates.</span></span>    |
| [<span data-ttu-id="00818-115">**ScheduledInstallationTime**</span><span class="sxs-lookup"><span data-stu-id="00818-115">**ScheduledInstallationTime**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | <span data-ttu-id="00818-116">Obtiene y establece la hora a la que Actualizaciones automáticas instala o desinstala las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="00818-116">Gets and sets the time at which Automatic Updates installs or uninstalls updates.</span></span>                |



 

> [!Note]  
> <span data-ttu-id="00818-117">Windows 8, Windows 8.1, Windows Server 2012 y Windows Server 2012 R2 proporcionan solo compatibilidad limitada para [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) y [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span><span class="sxs-lookup"><span data-stu-id="00818-117">Windows 8, Windows 8.1, Windows Server 2012, and Windows Server 2012 R2 provide only limited support for [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) and [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="00818-118">Si el equipo se ha configurado a través de directiva de grupo para utilizar un día y una hora de instalación programada, las propiedades **ScheduledInstallationDay** y **ScheduledInstallationTime** devuelven este día y hora programados.</span><span class="sxs-lookup"><span data-stu-id="00818-118">If the computer has been configured through Group Policy to use a scheduled installation day and time, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return this scheduled day and time.</span></span> <span data-ttu-id="00818-119">Si el equipo no se ha configurado a través de directiva de grupo de esta manera, las propiedades **ScheduledInstallationDay** y **ScheduledInstallationTime** devuelven valores predeterminados y no confiables.</span><span class="sxs-lookup"><span data-stu-id="00818-119">If the computer hasn't been configured through Group Policy in this way, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return default and unreliable values.</span></span> <span data-ttu-id="00818-120">Si intenta modificar el día y la hora de instalación programada en estos sistemas operativos, **ScheduledInstallationDay** y **ScheduledInstallationTime** parecen correctos, pero no tienen ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="00818-120">If you try to modify the scheduled installation day and time on these operating systems, **ScheduledInstallationDay** and **ScheduledInstallationTime** appear to succeed but have no effect.</span></span>

 

 

 



