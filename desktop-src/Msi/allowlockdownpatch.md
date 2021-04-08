---
description: Si no se establece esta Directiva del sistema por equipo, solo los administradores pueden aplicar revisiones a los productos existentes que se instalaron con privilegios elevados.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001754"
---
# <a name="allowlockdownpatch"></a><span data-ttu-id="380be-103">AllowLockdownPatch</span><span class="sxs-lookup"><span data-stu-id="380be-103">AllowLockdownPatch</span></span>

<span data-ttu-id="380be-104">Si no se establece esta [Directiva del sistema](system-policy.md) por equipo, solo los administradores pueden aplicar revisiones a los productos existentes que se instalaron con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="380be-104">If this per-machine [system policy](system-policy.md) is not set, only administrators can patch existing products that were installed using elevated privileges.</span></span> <span data-ttu-id="380be-105">Si AllowLockdownPatch se establece en "1", los usuarios no administrativos pueden, en algunos casos, aplicar revisiones a los productos mientras se ejecuta una instalación con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="380be-105">If AllowLockdownPatch is set to "1", nonadministrative users can, in some cases, apply patches to products while running an installation using elevated privileges.</span></span> <span data-ttu-id="380be-106">Con la directiva establecida, la revisión puede instalar [actualizaciones secundarias](minor-upgrades.md) mientras se ejecuta una instalación con privilegios elevados, la revisión no puede instalar las [actualizaciones principales](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="380be-106">With the policy set, the patch can install [minor upgrades](minor-upgrades.md) while running an installation using elevated privileges, the patch cannot install [major upgrades](major-upgrades.md).</span></span> <span data-ttu-id="380be-107">La configuración de esta Directiva también permite a los usuarios no administrativos ejecutar programas en privilegios LocalSystem durante una instalación con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="380be-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="380be-108">Se recomienda la configuración predeterminada para garantizar un entorno seguro.</span><span class="sxs-lookup"><span data-stu-id="380be-108">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="380be-109">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="380be-109">Registry Key</span></span>

<span data-ttu-id="380be-110">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="380be-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="380be-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="380be-111">Data Type</span></span>

<span data-ttu-id="380be-112">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="380be-112">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="380be-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="380be-113">Remarks</span></span>

<span data-ttu-id="380be-114">Cualquier usuario puede aplicar una revisión durante una instalación no elevada.</span><span class="sxs-lookup"><span data-stu-id="380be-114">Any user can apply a patch during a nonelevated installation.</span></span> <span data-ttu-id="380be-115">La configuración de esta [Directiva del sistema](system-policy.md) por equipo en "1" proporciona a los usuarios no administrativos la flexibilidad adicional de aplicar revisiones a cualquier producto durante una instalación con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="380be-115">Setting this per-machine [system policy](system-policy.md) to "1" gives nonadministrative users the additional flexibility of applying patches to any product during an elevated installation.</span></span> <span data-ttu-id="380be-116">Si no se establece esta Directiva, los usuarios no administrativos no podrán aplicar una revisión a las aplicaciones asignadas o publicadas.</span><span class="sxs-lookup"><span data-stu-id="380be-116">If this policy is not set, nonadministrative users cannot apply a patch to assigned or published applications.</span></span>

<span data-ttu-id="380be-117">La configuración de esta Directiva también permite a los usuarios no administrativos ejecutar programas arbitrarios en privilegios LocalSystem si tienen un paquete de revisión Windows Installer que instala o inicia esos programas.</span><span class="sxs-lookup"><span data-stu-id="380be-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer patch package that installs or launches those programs.</span></span>

 

 



