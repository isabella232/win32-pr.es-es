---
description: Establecer el valor de esta Directiva del sistema por equipo en &\# 0034; 1&\# 0034; permite a los usuarios no administrativos usar un cuadro de diálogo examinar para buscar orígenes de aplicaciones administradas.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909117"
---
# <a name="allowlockdownbrowse"></a><span data-ttu-id="7594b-103">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="7594b-103">AllowLockdownBrowse</span></span>

<span data-ttu-id="7594b-104">Establecer el valor de esta [Directiva del sistema](system-policy.md) por equipo en "1" permite a los usuarios no administrativos usar un [cuadro de diálogo examinar](browse-dialog.md) para buscar orígenes de [*aplicaciones administradas*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7594b-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" enables nonadministrative users to use a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md).</span></span> <span data-ttu-id="7594b-105">Los orígenes pueden incluir medios, como CD-ROM, direcciones URL y ubicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="7594b-105">Sources may include media, such as CD-ROM, URLs, and network locations.</span></span> <span data-ttu-id="7594b-106">Para obtener más información, consulte [resistencia del origen](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="7594b-106">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="7594b-107">El valor predeterminado en Windows Installer es que los usuarios no administrativos no pueden buscar nuevos orígenes de aplicaciones administradas.</span><span class="sxs-lookup"><span data-stu-id="7594b-107">The default on Windows Installer is that nonadministrative users cannot browse for new sources of managed applications.</span></span> <span data-ttu-id="7594b-108">Los únicos orígenes disponibles son aquellos que ya están registrados en la lista de origen del producto.</span><span class="sxs-lookup"><span data-stu-id="7594b-108">The only sources available are those that are already registered in the source list of the product.</span></span> <span data-ttu-id="7594b-109">Si se establece esta Directiva, un usuario no administrativo puede buscar nuevos orígenes de aplicaciones asignadas o publicadas o aplicaciones instaladas para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7594b-109">If this policy is set, a nonadministrative user may browse for new sources of assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="7594b-110">La configuración de AllowLockdownBrowse también permite a los usuarios no administrativos ejecutar programas en privilegios LocalSystem durante una instalación con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="7594b-110">Setting AllowLockdownBrowse also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="7594b-111">Se recomienda la configuración predeterminada para garantizar un entorno seguro.</span><span class="sxs-lookup"><span data-stu-id="7594b-111">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="7594b-112">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="7594b-112">Registry Key</span></span>

<span data-ttu-id="7594b-113">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="7594b-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="7594b-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7594b-114">Data Type</span></span>

<span data-ttu-id="7594b-115">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="7594b-115">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="7594b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7594b-116">Remarks</span></span>

<span data-ttu-id="7594b-117">La configuración de esta Directiva también permite a los usuarios no administrativos ejecutar programas arbitrarios en privilegios LocalSystem si tienen un paquete de Windows Installer que instala o inicia esos programas.</span><span class="sxs-lookup"><span data-stu-id="7594b-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

<span data-ttu-id="7594b-118">[DisableBrowse](disablebrowse.md) invalida AllowLockdownBrowse y evita que se examine incluso si AllowLockdownBrowse está establecido.</span><span class="sxs-lookup"><span data-stu-id="7594b-118">[DisableBrowse](disablebrowse.md) overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

<span data-ttu-id="7594b-119">Para obtener información sobre la interacción de esta directiva con los orígenes de instalación, consulte [Administración de orígenes de instalación](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="7594b-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7594b-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7594b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7594b-121">Resistencia de origen</span><span class="sxs-lookup"><span data-stu-id="7594b-121">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="7594b-122">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="7594b-122">AllowLockdownMedia</span></span>](allowlockdownmedia.md)
</dt> </dl>

 

 



