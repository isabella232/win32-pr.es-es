---
title: Directrices para aplicaciones y servicios
description: Para reducir el número de reinicios del sistema al instalar y dar servicio a las aplicaciones en Windows Vista o Windows Server 2008, debe seguir estas directrices para permitir que la aplicación o el servicio se cierren correctamente y se reinicien.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651292"
---
# <a name="guidelines-for-applications-and-services"></a><span data-ttu-id="2eaa9-103">Directrices para aplicaciones y servicios</span><span class="sxs-lookup"><span data-stu-id="2eaa9-103">Guidelines for Applications and Services</span></span>

<span data-ttu-id="2eaa9-104">Para reducir el número de reinicios del sistema al instalar y dar servicio a las aplicaciones en Windows Vista o Windows Server 2008, debe seguir estas directrices para permitir que la aplicación o el servicio se cierren correctamente y se reinicien.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-104">To reduce the number of system restarts when installing and servicing applications on Windows Vista or Windows Server 2008, you should observe the following guidelines to enable your application or service to be shut down cleanly and restarted.</span></span>

-   <span data-ttu-id="2eaa9-105">Las aplicaciones y los servicios deben estar preparados para que el sistema los cierre y lo reinicie cuando sea necesario para instalar una actualización.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-105">Your applications and services should be prepared to be shut down and restarted by the system when this is necessary to install an update.</span></span> <span data-ttu-id="2eaa9-106">Normalmente, cuando se instala una actualización, una aplicación o servicio debe cerrarse porque actualmente contiene un archivo afectado en uso.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-106">Typically, when an update is installed, an application or service needs to be shut down because it currently holds an affected file in use.</span></span> <span data-ttu-id="2eaa9-107">Todas las aplicaciones o servicios que pueden contener un archivo en uso durante una actualización deben estar preparados para cerrarse sin problemas.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-107">All applications or services that can hold a file in use during an update should be prepared to shut down cleanly.</span></span>
-   <span data-ttu-id="2eaa9-108">Las aplicaciones deben guardar los datos de usuario y la información de estado que se necesitan después de un reinicio y deben cumplir las directrices descritas en la sección [directrices para aplicaciones](guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="2eaa9-108">Your applications should save user data and state information that are needed after a restart and should adhere to the guidelines that are described in the section [Guidelines for Applications](guidelines-for-applications.md).</span></span>
-   <span data-ttu-id="2eaa9-109">Los servicios deben cumplir las directrices descritas en la sección [directrices para servicios](guidelines-for-services.md).</span><span class="sxs-lookup"><span data-stu-id="2eaa9-109">Your services should adhere to the guidelines that are described in the section [Guidelines for Services](guidelines-for-services.md).</span></span>
-   <span data-ttu-id="2eaa9-110">El administrador de reinicio no cierra los [servicios críticos del sistema](critical-system-services.md); por lo tanto, estos servicios deben limitar el número de archivos dll de los que dependen.</span><span class="sxs-lookup"><span data-stu-id="2eaa9-110">Restart Manager does not shut down [critical system services](critical-system-services.md); therefore, these services should limit the number of DLLs they depend on.</span></span>

 

 




