---
description: Se trata de una directiva del sistema por equipo que se puede usar cuando el administrador solo desea tener instaladas las aplicaciones por máquina.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ee8275567c62fc383c0488d6ad3ef8dfc928f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153883"
---
# <a name="disableuserinstalls"></a><span data-ttu-id="97e61-103">DisableUserInstalls</span><span class="sxs-lookup"><span data-stu-id="97e61-103">DisableUserInstalls</span></span>

<span data-ttu-id="97e61-104">Se trata de una [Directiva del sistema](system-policy.md) por equipo que se puede usar cuando el administrador solo desea tener instaladas las aplicaciones por máquina.</span><span class="sxs-lookup"><span data-stu-id="97e61-104">This is a per-machine [system policy](system-policy.md) that can be used when the administrator only wants per-machine applications installed.</span></span>

<span data-ttu-id="97e61-105">Si no se establece esta Directiva, el instalador busca en el registro las aplicaciones en el siguiente orden: las aplicaciones administradas registradas como aplicaciones por usuario y no administradas registradas como por usuario y, por último, las aplicaciones registradas como por equipo.</span><span class="sxs-lookup"><span data-stu-id="97e61-105">If this policy is not set, the installer searches the registry for applications in the following order: managed applications registered as per-user, unmanaged applications registered as per-user, and finally applications registered as per-machine.</span></span>

<span data-ttu-id="97e61-106">Si esta Directiva se establece en 1, el instalador omite todas las aplicaciones registradas como por usuario y solo busca las aplicaciones registradas como por equipo.</span><span class="sxs-lookup"><span data-stu-id="97e61-106">If this policy is set to 1, the installer ignores all applications registered as per-user and only searches for applications registered as per-machine.</span></span> <span data-ttu-id="97e61-107">Las llamadas a la interfaz de programación de aplicaciones de Windows Installer o el sistema omiten las aplicaciones por usuario.</span><span class="sxs-lookup"><span data-stu-id="97e61-107">Calls to the Windows Installer application programming interface or system ignore per-user applications.</span></span> <span data-ttu-id="97e61-108">Un intento de realizar una instalación en el [contexto de instalación](installation-context.md) por usuario hace que el instalador muestre un mensaje de error y detenga la instalación.</span><span class="sxs-lookup"><span data-stu-id="97e61-108">An attempt to perform an installation in the per-user [installation context](installation-context.md) causes the installer to display an error message and stops the installation.</span></span> <span data-ttu-id="97e61-109">En este caso, el Windows Installer también evita las instalaciones por usuario de un servidor de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="97e61-109">In this case, the Windows Installer also prevents per-user installations from a terminal server.</span></span>

## <a name="registry-key"></a><span data-ttu-id="97e61-110">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="97e61-110">Registry Key</span></span>

<span data-ttu-id="97e61-111">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="97e61-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="97e61-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="97e61-112">Data Type</span></span>

<span data-ttu-id="97e61-113">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="97e61-113">**REG\_DWORD**</span></span>

 

 



