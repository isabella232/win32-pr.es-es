---
description: Si esta Directiva del sistema por equipo está establecida en 1, un usuario o un administrador no puede quitar las revisiones del equipo.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908187"
---
# <a name="disablepatchuninstall"></a><span data-ttu-id="591be-103">DisablePatchUninstall</span><span class="sxs-lookup"><span data-stu-id="591be-103">DisablePatchUninstall</span></span>

<span data-ttu-id="591be-104">Si esta [Directiva del sistema](system-policy.md) por equipo está establecida en 1, un usuario o un administrador no puede quitar las revisiones del equipo.</span><span class="sxs-lookup"><span data-stu-id="591be-104">If this per-machine [system policy](system-policy.md) is set to 1, patches cannot be removed from the computer by a user or an administrator.</span></span> <span data-ttu-id="591be-105">El Windows Installer todavía puede quitar una revisión que ya no es aplicable a un producto.</span><span class="sxs-lookup"><span data-stu-id="591be-105">The Windows Installer can still remove a patch that is no longer applicable to a product.</span></span> <span data-ttu-id="591be-106">Si no se establece esta Directiva, un usuario puede quitar una revisión del equipo sólo si se le han concedido privilegios para quitar la revisión.</span><span class="sxs-lookup"><span data-stu-id="591be-106">If this policy is not set, a user can remove a patch from the computer only if the user has been granted privileges to remove the patch.</span></span> <span data-ttu-id="591be-107">Esto puede depender de si el usuario es un administrador, si la configuración de la Directiva de [DisableMsi](disablemsi.md) y [AlwaysInstallElevated](alwaysinstallelevated.md) está establecida, y si la revisión se instaló en un contexto administrado por usuario, no administrado por usuario o por equipo.</span><span class="sxs-lookup"><span data-stu-id="591be-107">This can depend on whether the user is an administrator, whether [DisableMsi](disablemsi.md) and [AlwaysInstallElevated](alwaysinstallelevated.md) policy settings are set, and whether the patch was installed in a per-user managed, per-user unmanaged, or per-machine context.</span></span>

## <a name="registry-key"></a><span data-ttu-id="591be-108">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="591be-108">Registry Key</span></span>

<span data-ttu-id="591be-109">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="591be-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="591be-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="591be-110">Data Type</span></span>

<span data-ttu-id="591be-111">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="591be-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="591be-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="591be-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="591be-113">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="591be-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



