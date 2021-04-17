---
description: Windows Installer se integra con la Directiva de restricción de software en Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Installer y Directiva de restricción de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678066"
---
# <a name="windows-installer-and-software-restriction-policy"></a><span data-ttu-id="b2588-103">Windows Installer y Directiva de restricción de software</span><span class="sxs-lookup"><span data-stu-id="b2588-103">Windows Installer and Software Restriction Policy</span></span>

<span data-ttu-id="b2588-104">Windows Installer se integra con la Directiva de restricción de software en Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2588-104">Windows Installer is integrated with Software Restriction Policy in Microsoft Windows XP.</span></span> <span data-ttu-id="b2588-105">La Directiva de restricción de software se puede configurar mediante la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="b2588-105">Software Restriction Policy is configurable through group policy.</span></span> <span data-ttu-id="b2588-106">La Directiva de restricción de software permite a un administrador restringir a los administradores y a los no administradores la ejecución de archivos basados en los criterios de ruta de acceso, zona URL, hash o publicador.</span><span class="sxs-lookup"><span data-stu-id="b2588-106">Software Restriction Policy allows an administrator to restrict both administrators and nonadministrators from running files based upon the path, URL zone, hash, or publisher criteria.</span></span> <span data-ttu-id="b2588-107">La Directiva de restricción de software tiene dos niveles: no restringido y no permitido.</span><span class="sxs-lookup"><span data-stu-id="b2588-107">Software Restriction Policy has two levels: unrestricted and disallowed.</span></span> <span data-ttu-id="b2588-108">La Windows Installer solo instala los paquetes que se pueden ejecutar en el nivel sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="b2588-108">The Windows Installer only installs packages allowed to run at the unrestricted level.</span></span>

<span data-ttu-id="b2588-109">También se debe permitir que las revisiones o transformaciones se ejecuten en el nivel sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="b2588-109">Patches or transforms must also be allowed to run at the unrestricted level.</span></span> <span data-ttu-id="b2588-110">Si un paquete, revisión o transformación está configurado para ejecutarse en un nivel diferente de Unrestricted, el Windows Installer muestra un mensaje de error y registra una entrada en el registro de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2588-110">If a package, patch, or transform is configured to run at a level different from unrestricted, the Windows Installer displays an error message and logs an entry in the application event log.</span></span> <span data-ttu-id="b2588-111">La Directiva de restricción de software se evalúa la primera vez que se instala una aplicación, cuando se aplica una nueva revisión y cuando se vuelve a almacenar en caché el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="b2588-111">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="b2588-112">Si un paquete, revisión o transformación está restringido, en el Windows Installer se muestra un mensaje de error y se escribe una entrada de [registro de eventos](event-logging.md) en el registro de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2588-112">If a package, patch, or transform is restricted, the Windows Installer displays an error message and writes an [Event Logging](event-logging.md) entry in the application event log.</span></span> <span data-ttu-id="b2588-113">La Directiva de restricción de software se evalúa la primera vez que se instala una aplicación, cuando se aplica una nueva revisión y cuando se vuelve a almacenar en caché el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="b2588-113">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="b2588-114">Para obtener más información sobre la Directiva de restricción de software, consulte la documentación del producto y [Busque en el sitio de TechNet](https://www.microsoft.com/technet/sitemap.mspx).</span><span class="sxs-lookup"><span data-stu-id="b2588-114">For more information on software restriction policy, consult the product documentation and [search the TechNet Site](https://www.microsoft.com/technet/sitemap.mspx).</span></span>

 

 



