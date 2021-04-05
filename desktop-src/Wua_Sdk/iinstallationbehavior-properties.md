---
description: La interfaz IInstallationBehavior define las siguientes propiedades.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Propiedades de IInstallationBehavior
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001199"
---
# <a name="iinstallationbehavior-properties"></a><span data-ttu-id="b314b-103">Propiedades de IInstallationBehavior</span><span class="sxs-lookup"><span data-stu-id="b314b-103">IInstallationBehavior Properties</span></span>

<span data-ttu-id="b314b-104">La interfaz [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="b314b-104">The [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) interface defines the following properties.</span></span>



| <span data-ttu-id="b314b-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b314b-105">Property</span></span>                                                                                 | <span data-ttu-id="b314b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b314b-106">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b314b-107">**CanRequestUserInput**</span><span class="sxs-lookup"><span data-stu-id="b314b-107">**CanRequestUserInput**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | <span data-ttu-id="b314b-108">Obtiene un valor booleano thast indica si la instalación o desinstalación de una actualización puede solicitar la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="b314b-108">Gets a Boolean value thast indicates whether the installation or uninstallation of an update can prompt for user input.</span></span>                                                        |
| [<span data-ttu-id="b314b-109">**Impacto**</span><span class="sxs-lookup"><span data-stu-id="b314b-109">**Impact**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | <span data-ttu-id="b314b-110">Obtiene una enumeración [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) que indica cómo afecta la instalación o desinstalación de la actualización al equipo.</span><span class="sxs-lookup"><span data-stu-id="b314b-110">Gets an [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) enumeration that indicates how the installation or uninstallation of the update affects the computer.</span></span>                 |
| [<span data-ttu-id="b314b-111">**RebootBehavior**</span><span class="sxs-lookup"><span data-stu-id="b314b-111">**RebootBehavior**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | <span data-ttu-id="b314b-112">Obtiene una enumeración [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) que especifica el comportamiento de reinicio que se produce al instalar o desinstalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="b314b-112">Gets an [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) enumeration that specifies the restart behavior that occurs when you install or uninstall the update.</span></span> |
| [<span data-ttu-id="b314b-113">**RequiresNetworkConnectivity**</span><span class="sxs-lookup"><span data-stu-id="b314b-113">**RequiresNetworkConnectivity**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | <span data-ttu-id="b314b-114">Obtiene un valor booleano que indica si la instalación o desinstalación de una actualización requiere conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="b314b-114">Gets a Boolean value that indicates whether the installation or uninstallation of an update requires network connectivity.</span></span>                                                     |



 

 

 



