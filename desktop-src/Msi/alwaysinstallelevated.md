---
description: Instale un paquete de Windows Installer con privilegios elevados (sistema).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545195"
---
# <a name="alwaysinstallelevated"></a><span data-ttu-id="1d37c-103">AlwaysInstallElevated</span><span class="sxs-lookup"><span data-stu-id="1d37c-103">AlwaysInstallElevated</span></span>

<span data-ttu-id="1d37c-104">Puede usar la Directiva AlwaysInstallElevated para instalar un paquete de Windows Installer con privilegios elevados (sistema).</span><span class="sxs-lookup"><span data-stu-id="1d37c-104">You can use the AlwaysInstallElevated policy to install a Windows Installer package with elevated (system) privileges.</span></span>

<span data-ttu-id="1d37c-105">\* \* ADVERTENCIA: \* \*</span><span class="sxs-lookup"><span data-stu-id="1d37c-105">\*\*Warning:  \*\*</span></span>

<span data-ttu-id="1d37c-106">Esta opción es equivalente a conceder derechos administrativos completos, lo que puede suponer un riesgo de seguridad masivo.</span><span class="sxs-lookup"><span data-stu-id="1d37c-106">This option is equivalent to granting full administrative rights, which can pose a massive security risk.</span></span> <span data-ttu-id="1d37c-107">Microsoft no recomienda encarecidamente el uso de esta opción.</span><span class="sxs-lookup"><span data-stu-id="1d37c-107">Microsoft strongly discourages the use of this setting.</span></span>

<span data-ttu-id="1d37c-108">Para instalar un paquete con privilegios elevados (sistema), establezca el valor de AlwaysInstallElevated en "1" en las dos claves del registro siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d37c-108">To install a package with elevated (system) privileges, set the AlwaysInstallElevated value to "1" under both of the following registry keys:</span></span>

<span data-ttu-id="1d37c-109">**HKEY \_ \_** Directivas de software de usuario actual \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="1d37c-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="1d37c-110">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="1d37c-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="1d37c-111">Si el valor AlwaysInstallElevated no se establece en "1" en las dos claves del registro anteriores, el instalador usa privilegios elevados para instalar las aplicaciones administradas y usa el nivel de privilegios del usuario actual para las aplicaciones no administradas.</span><span class="sxs-lookup"><span data-stu-id="1d37c-111">If the AlwaysInstallElevated value is not set to "1" under both of the preceding registry keys, the installer uses elevated privileges to install managed applications and uses the current user's privilege level for unmanaged applications.</span></span>

<span data-ttu-id="1d37c-112">Dado que esta directiva permite a los usuarios instalar aplicaciones que requieren acceso a directorios y claves del registro para los que es posible que el usuario no tenga permiso para ver o cambiar, debe considerar si proporciona a los usuarios un nivel de seguridad adecuado.</span><span class="sxs-lookup"><span data-stu-id="1d37c-112">Because this policy permits users to install applications that require access to directories and registry keys for which the user may not have permission to view or change, you should consider whether it provides your users with an appropriate level of security.</span></span> <span data-ttu-id="1d37c-113">La configuración de esta directiva indica a Windows Installer que use permisos del sistema cuando instale la aplicación en el sistema.</span><span class="sxs-lookup"><span data-stu-id="1d37c-113">Setting this policy directs Windows Installer to use system permissions when it installs the application on the system.</span></span> <span data-ttu-id="1d37c-114">Si no se establece esta Directiva, las aplicaciones que el administrador no distribuya se instalarán con los privilegios del usuario y solo las aplicaciones administradas obtendrán privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="1d37c-114">If this policy is not set, applications not distributed by the administrator are installed using the user's privileges and only managed applications get elevated privileges.</span></span>

<span data-ttu-id="1d37c-115">Tenga en cuenta que una vez habilitada la Directiva por equipo para AlwaysInstallElevated, cualquier usuario puede establecer su configuración por usuario.</span><span class="sxs-lookup"><span data-stu-id="1d37c-115">Note that once the per-machine policy for AlwaysInstallElevated is enabled, any user can set their per-user setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d37c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d37c-116">Remarks</span></span>

<span data-ttu-id="1d37c-117">Para obtener información sobre la interacción de esta directiva con los orígenes de instalación, consulte [Administración de orígenes de instalación](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="1d37c-117">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="1d37c-118">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1d37c-118">Data Type</span></span>

<span data-ttu-id="1d37c-119">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="1d37c-119">**REG\_DWORD**</span></span>

 

 



