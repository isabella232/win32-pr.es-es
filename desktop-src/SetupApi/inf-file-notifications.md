---
description: Las siguientes notificaciones se usan con las funciones SetupInstallFile, SetupInstallFileEx y SetupInstallFromInfSection. Para obtener más información sobre el formato y el uso de las notificaciones, vea notificaciones.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: Notificaciones de archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f58863d48c1af809c0cbbcdc2d625214a6e90a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002073"
---
# <a name="inf-file-notifications"></a><span data-ttu-id="4ec37-104">Notificaciones de archivo INF</span><span class="sxs-lookup"><span data-stu-id="4ec37-104">INF File Notifications</span></span>

<span data-ttu-id="4ec37-105">Las siguientes notificaciones se usan con las funciones [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)y [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) .</span><span class="sxs-lookup"><span data-stu-id="4ec37-105">The following notifications are used with the [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) functions.</span></span> <span data-ttu-id="4ec37-106">Para obtener más información sobre el formato y el uso de las notificaciones, vea [notificaciones](notifications.md).</span><span class="sxs-lookup"><span data-stu-id="4ec37-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="4ec37-107">notificación</span><span class="sxs-lookup"><span data-stu-id="4ec37-107">Notification</span></span>                                                      | <span data-ttu-id="4ec37-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ec37-108">Description</span></span>                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ec37-109">**SPFILENOTIFY \_ FILEOPDELAYED**</span><span class="sxs-lookup"><span data-stu-id="4ec37-109">**SPFILENOTIFY\_FILEOPDELAYED**</span></span>](spfilenotify-fileopdelayed.md) | <span data-ttu-id="4ec37-110">El archivo está en uso y la operación actual se retrasa hasta que se reinicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="4ec37-110">The file is in use, and the current operation is delayed until the system is rebooted.</span></span> |
| [<span data-ttu-id="4ec37-111">**SPFILENOTIFY \_ LANGMISMATCH**</span><span class="sxs-lookup"><span data-stu-id="4ec37-111">**SPFILENOTIFY\_LANGMISMATCH**</span></span>](spfilenotify-langmismatch.md)   | <span data-ttu-id="4ec37-112">El idioma del archivo actual no coincide con el idioma del sistema.</span><span class="sxs-lookup"><span data-stu-id="4ec37-112">The language of the current file does not match the system language.</span></span>                   |
| [<span data-ttu-id="4ec37-113">**SPFILENOTIFY \_ TARGETEXISTS**</span><span class="sxs-lookup"><span data-stu-id="4ec37-113">**SPFILENOTIFY\_TARGETEXISTS**</span></span>](spfilenotify-targetexists.md)   | <span data-ttu-id="4ec37-114">Ya existe una copia del archivo especificado en el destino.</span><span class="sxs-lookup"><span data-stu-id="4ec37-114">A copy of the specified file already exists on the target.</span></span>                             |
| [<span data-ttu-id="4ec37-115">**SPFILENOTIFY \_ TARGETNEWER**</span><span class="sxs-lookup"><span data-stu-id="4ec37-115">**SPFILENOTIFY\_TARGETNEWER**</span></span>](spfilenotify-targetnewer.md)     | <span data-ttu-id="4ec37-116">Existe una versión más reciente del archivo especificado en el destino.</span><span class="sxs-lookup"><span data-stu-id="4ec37-116">A newer version of the specified file exists on the target.</span></span>                            |



 

> [!Note]  
> <span data-ttu-id="4ec37-117">Dado que [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) crea y confirma una cola de archivos interna, también usa las [notificaciones de cola de archivos](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="4ec37-117">Because [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) creates and commits an internal file queue, it also uses the [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 

 



