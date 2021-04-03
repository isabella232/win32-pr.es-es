---
description: Establecer el valor de esta Directiva del sistema por equipo en &\# 0034; 1&\# 0034; permite a los usuarios no administrativos instalar aplicaciones administradas desde orígenes almacenados en medios, como un CD-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914222"
---
# <a name="allowlockdownmedia"></a><span data-ttu-id="094da-103">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="094da-103">AllowLockdownMedia</span></span>

<span data-ttu-id="094da-104">Establecer el valor de esta [Directiva del sistema](system-policy.md) por equipo en "1" permite a los usuarios no administrativos instalar [*aplicaciones administradas*](m-gly.md) desde orígenes almacenados en medios, como un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="094da-104">Setting the value of this per-machine [system policy](system-policy.md) to "1", enables nonadministrative users to install [*managed applications*](m-gly.md) from sources stored on media, such as a CD-ROM.</span></span> <span data-ttu-id="094da-105">Consulte [resistencia del origen](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="094da-105">See [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="094da-106">Por ejemplo, si se establece esta Directiva, un usuario no administrativo puede usar un origen de medios para instalar aplicaciones asignadas o publicadas o aplicaciones que se instalan para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="094da-106">For example, if this policy is set, a nonadministrative user may use a media source to install assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="094da-107">La configuración de esta Directiva también permite a los usuarios no administrativos ejecutar programas en privilegios LocalSystem durante una instalación con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="094da-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="094da-108">El valor predeterminado de esta directiva es 1 solo en los equipos que ejecutan Windows Vista y que no están Unidos a un dominio.</span><span class="sxs-lookup"><span data-stu-id="094da-108">The default value of this policy is 1 only on computers running Windows Vista and that are not joined to a domain.</span></span> <span data-ttu-id="094da-109">El valor predeterminado en otros equipos es que los usuarios no administrativos no pueden instalar aplicaciones administradas desde un origen ubicado en un medio.</span><span class="sxs-lookup"><span data-stu-id="094da-109">The default on other computers is that nonadministrative users cannot install managed applications from a source located on media.</span></span>

<span data-ttu-id="094da-110">Dado que esta directiva permite a los usuarios que no son administradores instalar con privilegios que no tienen de forma predeterminada, antes de establecer esta Directiva debe considerar si proporciona un nivel de seguridad adecuado para el usuario.</span><span class="sxs-lookup"><span data-stu-id="094da-110">Because this policy enables users that are not an administrator to install with privileges they do not have by default, before setting this policy you should consider whether it provides an appropriate level of security for your user.</span></span> <span data-ttu-id="094da-111">Se recomienda la configuración predeterminada para garantizar un entorno seguro.</span><span class="sxs-lookup"><span data-stu-id="094da-111">The default setting is recommended to ensure a secure environment.</span></span>

<span data-ttu-id="094da-112">Para obtener más información acerca de la protección de instalaciones y el uso de certificados digitales, consulte [directrices para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md) y [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md) y [descargar una instalación desde Internet](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="094da-112">For more information about securing installations and using digital certificates see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="094da-113">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="094da-113">Registry Key</span></span>

<span data-ttu-id="094da-114">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="094da-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="094da-115">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="094da-115">Data Type</span></span>

<span data-ttu-id="094da-116">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="094da-116">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="094da-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="094da-117">Remarks</span></span>

<span data-ttu-id="094da-118">La configuración de esta Directiva también permite a los usuarios no administrativos ejecutar programas arbitrarios en privilegios LocalSystem si tienen un paquete de Windows Installer que instala o inicia esos programas.</span><span class="sxs-lookup"><span data-stu-id="094da-118">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="094da-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="094da-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="094da-120">Resistencia de origen</span><span class="sxs-lookup"><span data-stu-id="094da-120">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="094da-121">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="094da-121">AllowLockdownBrowse</span></span>](allowlockdownbrowse.md)
</dt> </dl>

 

 



