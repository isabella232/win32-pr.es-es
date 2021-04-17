---
description: 'Para anunciar una aplicación según la instalación de cada usuario cuando la aplicación requiere privilegios elevados (es decir, sistema) para la instalación, siga las instrucciones de la lista siguiente:'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Anunciar una aplicación Per-User que se va a instalar con privilegios elevados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d9888714f28282e060b3a1e7eea0291b4e0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667048"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a><span data-ttu-id="d363a-103">Anunciar una aplicación Per-User que se va a instalar con privilegios elevados</span><span class="sxs-lookup"><span data-stu-id="d363a-103">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>

<span data-ttu-id="d363a-104">Para anunciar una aplicación según la instalación de cada usuario cuando la aplicación requiere privilegios elevados (es decir, sistema) para la instalación, siga las instrucciones de la lista siguiente:</span><span class="sxs-lookup"><span data-stu-id="d363a-104">To advertise an application on a per-user installation basis when the application requires elevated (that is, system) privileges for installation, use the guidelines in the following list:</span></span>

-   <span data-ttu-id="d363a-105">El proceso debe ser un servicio que se ejecute con la cuenta de sistema LocalSystem en Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="d363a-105">Your process must be a service that runs under the LocalSystem system account on Windows XP or later.</span></span>
-   <span data-ttu-id="d363a-106">Genere un script de anuncio mediante una llamada a [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) o [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).</span><span class="sxs-lookup"><span data-stu-id="d363a-106">Generate an advertise script by calling [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) or [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).</span></span>
-   <span data-ttu-id="d363a-107">El proceso debe suplantar al usuario que es el destino del anuncio.</span><span class="sxs-lookup"><span data-stu-id="d363a-107">Your process must impersonate the user that is the target for the advertisement.</span></span>
-   <span data-ttu-id="d363a-108">Llame a [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)y use los \_ \| \_ \_ \| \_ \_ \| \_ métodos abreviados de marcas SCRIPTFLAGS CACHEINFO SCRIPTFLAGS REGDATA APPINFO SCRIPTFLAGS REGDATA CNFGINFO SCRIPTFLAGS.</span><span class="sxs-lookup"><span data-stu-id="d363a-108">Call [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta), and use the flags SCRIPTFLAGS\_CACHEINFO \| SCRIPTFLAGS\_REGDATA\_APPINFO \| SCRIPTFLAGS\_REGDATA\_CNFGINFO \| SCRIPTFLAGS\_SHORTCUTS.</span></span>

<span data-ttu-id="d363a-109">Al seguir las instrucciones, se anuncia una aplicación a un usuario especificado y, cuando el usuario elige instalar, la aplicación se instala con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="d363a-109">When you follow the guidelines, you advertise an application to a specified user, and when the user chooses to install, the application is installed with elevated privileges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d363a-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d363a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d363a-111">Aplicación de revisiones para aplicaciones administradas por usuario</span><span class="sxs-lookup"><span data-stu-id="d363a-111">Patching Per-User Managed Applications</span></span>](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



