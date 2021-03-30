---
description: Al establecer la Directiva TransformsSecure en 1 se informa al instalador de que las transformaciones se almacenan en caché localmente en el equipo del usuario en una ubicación en la que el usuario no tiene acceso de escritura.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: Directiva TransformsSecure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907617"
---
# <a name="transformssecure-policy"></a><span data-ttu-id="8b6e8-103">Directiva TransformsSecure</span><span class="sxs-lookup"><span data-stu-id="8b6e8-103">TransformsSecure Policy</span></span>

<span data-ttu-id="8b6e8-104">Al establecer la Directiva TransformsSecure en 1 se informa al instalador de que las transformaciones se almacenan en caché localmente en el equipo del usuario en una ubicación en la que el usuario no tiene acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-104">Setting the TransformsSecure policy to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="8b6e8-105">Establecer esta directiva es igual que establecer la [propiedad TRANSFORMSSECURE](transformssecure.md) , excepto que el ámbito es diferente.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-105">Setting this policy is the same as setting the [TRANSFORMSSECURE property](transformssecure.md) except the scope is different.</span></span> <span data-ttu-id="8b6e8-106">La configuración de la Directiva TransformsSecure se aplica a todos los paquetes instalados en un equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-106">Setting TransformsSecure policy applies to all packages installed to a given computer.</span></span> <span data-ttu-id="8b6e8-107">El establecimiento de la propiedad TRANSFORMSSECURE se aplica al paquete independientemente del equipo.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-107">Setting the TRANSFORMSSECURE property applies to the package regardless of the computer.</span></span>

<span data-ttu-id="8b6e8-108">La finalidad de esta directiva es proporcionar almacenamiento de transformación seguro con usuarios móviles de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-108">The purpose of this policy is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="8b6e8-109">A partir de Windows Server 2003, el valor predeterminado de esta directiva es 1.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-109">Beginning with Windows Server 2003, the default value of this policy is 1.</span></span>

<span data-ttu-id="8b6e8-110">Cuando se establece esta Directiva, una [instalación de mantenimiento](maintenance-installation.md) solo puede utilizar la transformación de la caché protegida.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-110">When this policy is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the secured cache.</span></span> <span data-ttu-id="8b6e8-111">En caso de que el instalador encuentre que falta la transformación en el equipo local, el instalador intenta restaurar la transformación.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-111">In the event that the installer finds that the transform is missing on the local computer, the installer attempts to restore the transform.</span></span> <span data-ttu-id="8b6e8-112">Para que el instalador restaure la transformación, la transformación segura debe residir en un origen autorizado en la lista de origen del paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-112">In order for the installer to restore the transform, the secure transform must reside at an authorized source in the installation package's source list.</span></span> <span data-ttu-id="8b6e8-113">Para obtener más información, consulte [resistencia del origen](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="8b6e8-113">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="8b6e8-114">Se produce un error en la instalación de mantenimiento si la transformación no está disponible o no se puede cargar.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-114">The maintenance installation fails if the transform is unavailable or cannot be loaded.</span></span>

<span data-ttu-id="8b6e8-115">En Windows Server 2003, si no se establece esta Directiva, el comportamiento predeterminado es almacenar las transformaciones en una ubicación segura.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-115">On Windows Server 2003, if this policy is not set, the default behavior is to store the transforms in a secure location.</span></span> <span data-ttu-id="8b6e8-116">En todas las versiones anteriores a Windows Server 2003, si no se establece la Directiva, el comportamiento predeterminado es almacenar las transformaciones en el perfil de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-116">On all versions prior to Windows Server 2003, if the policy is not set, the default behavior is to store the transforms in the users profile.</span></span>

<span data-ttu-id="8b6e8-117">Vea también [transformaciones protegidas](secured-transforms.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-117">See also [Secured Transforms](secured-transforms.md) for more information.</span></span>

<span data-ttu-id="8b6e8-118">Windows Installer interpreta que la [Directiva TransformsAtSource](transformsatsource-policy.md) es la misma que la Directiva TransformsSecure.</span><span class="sxs-lookup"><span data-stu-id="8b6e8-118">Windows Installer interprets the [TransformsAtSource policy](transformsatsource-policy.md) to be the same as the TransformsSecure policy.</span></span>

## <a name="registry-key"></a><span data-ttu-id="8b6e8-119">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="8b6e8-119">Registry Key</span></span>

<span data-ttu-id="8b6e8-120">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="8b6e8-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="8b6e8-121">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8b6e8-121">Data Type</span></span>

<span data-ttu-id="8b6e8-122">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="8b6e8-122">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b6e8-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b6e8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b6e8-124">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="8b6e8-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



