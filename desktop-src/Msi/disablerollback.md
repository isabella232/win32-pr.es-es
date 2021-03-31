---
description: Si esta Directiva del sistema está establecida en 1, el instalador no almacena los archivos de reversión durante la instalación y deshabilita la reversión de la instalación.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001295"
---
# <a name="disablerollback"></a><span data-ttu-id="747d9-103">DisableRollback</span><span class="sxs-lookup"><span data-stu-id="747d9-103">DisableRollback</span></span>

<span data-ttu-id="747d9-104">Si esta [Directiva del sistema](system-policy.md) está establecida en 1, el instalador no almacena los archivos de reversión durante la instalación y deshabilita la reversión de la instalación.</span><span class="sxs-lookup"><span data-stu-id="747d9-104">If this [system policy](system-policy.md) is set to 1, the installer does not store rollback files during installation and disables installation rollback.</span></span> <span data-ttu-id="747d9-105">De forma predeterminada, la reversión está habilitada.</span><span class="sxs-lookup"><span data-stu-id="747d9-105">By default, rollback is enabled.</span></span> <span data-ttu-id="747d9-106">Es aconsejable que los administradores no utilicen esta directiva a menos que sea absolutamente imprescindible.</span><span class="sxs-lookup"><span data-stu-id="747d9-106">Administrators are advised to not use this policy unless it is absolutely essential.</span></span> <span data-ttu-id="747d9-107">Para obtener más información, consulte [reversión de instalación](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="747d9-107">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="747d9-108">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="747d9-108">Registry Key</span></span>

<span data-ttu-id="747d9-109">Para deshabilitar la reversión de las instalaciones por usuario, establezca **DisableRollback** en 1 en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="747d9-109">To disable rollback for per-user installations, set **DisableRollback** to 1 under the following registry key:</span></span>

<span data-ttu-id="747d9-110">**HKEY \_ \_** Directivas de software de usuario actual \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="747d9-110">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="747d9-111">Para deshabilitar la reversión en instalaciones por equipo, establezca **DisableRollback** en 1 en la siguiente clave del registro.</span><span class="sxs-lookup"><span data-stu-id="747d9-111">To disable rollback for per-computer installations, set **DisableRollback** to 1 under the following registry key.</span></span>

<span data-ttu-id="747d9-112">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="747d9-112">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="747d9-113">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="747d9-113">Data Type</span></span>

<span data-ttu-id="747d9-114">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="747d9-114">**REG\_DWORD**</span></span>

 

 



