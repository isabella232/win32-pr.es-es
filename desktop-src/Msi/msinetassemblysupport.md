---
description: La propiedad MsiNetAssemblySupport indica si el equipo admite ensamblados de Common Language Runtime en tiempo de ejecución.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: Propiedad MsiNetAssemblySupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653505"
---
# <a name="msinetassemblysupport-property"></a><span data-ttu-id="dfb25-103">Propiedad MsiNetAssemblySupport</span><span class="sxs-lookup"><span data-stu-id="dfb25-103">MsiNetAssemblySupport property</span></span>

<span data-ttu-id="dfb25-104">La propiedad **MsiNetAssemblySupport** indica si el equipo admite ensamblados de Common Language Runtime en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="dfb25-104">The **MsiNetAssemblySupport** property indicates whether the computer supports common language run-time assemblies.</span></span> <span data-ttu-id="dfb25-105">En los sistemas que admiten los ensamblados en tiempo de ejecución de Common Language Runtime, el instalador establece el valor de **MsiNetAssemblySupport** en la versión de archivo de Fusion.dll.</span><span class="sxs-lookup"><span data-stu-id="dfb25-105">On systems that support common language run-time assemblies, the installer sets the value of **MsiNetAssemblySupport** to the file version of Fusion.dll.</span></span> <span data-ttu-id="dfb25-106">El instalador no establece esta propiedad si el sistema operativo no admite ensamblados en tiempo de ejecución de Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="dfb25-106">The installer does not set this property if the operating system does not support common language run-time assemblies.</span></span> <span data-ttu-id="dfb25-107">Cuando se instalan varias versiones de Fusion.dll en paralelo en el equipo del usuario, esta propiedad se establece en la versión más reciente del archivo de Fusion.dll.</span><span class="sxs-lookup"><span data-stu-id="dfb25-107">When multiple versions of Fusion.dll are installed side-by-side on the user's computer, this property is set to the latest version of the Fusion.dll file.</span></span> <span data-ttu-id="dfb25-108">Por ejemplo, si .NET Framework versión 1.0.3705 (Fusion.dll versión 1.0.3705.15) y .NET Framework versión 1.1.4322 (Fusion.dll versión 1.1.4322.314) se instalan en paralelo, la propiedad **MsiNetAssemblySupport** se establece en 1.1.4322.314.</span><span class="sxs-lookup"><span data-stu-id="dfb25-108">For example, if .NET Framework version 1.0.3705 (Fusion.dll version 1.0.3705.15)and .NET Framework version 1.1.4322 (Fusion.dll version 1.1.4322.314) are installed side-by-side, the **MsiNetAssemblySupport** property is set to 1.1.4322.314.</span></span> <span data-ttu-id="dfb25-109">Para obtener más información, vea [ensamblados](assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="dfb25-109">For more information, see [Assemblies](assemblies.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb25-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfb25-110">Requirements</span></span>



| <span data-ttu-id="dfb25-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfb25-111">Requirement</span></span> | <span data-ttu-id="dfb25-112">Value</span><span class="sxs-lookup"><span data-stu-id="dfb25-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb25-113">Versión</span><span class="sxs-lookup"><span data-stu-id="dfb25-113">Version</span></span><br/> | <span data-ttu-id="dfb25-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dfb25-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dfb25-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dfb25-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dfb25-116">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dfb25-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="dfb25-117">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="dfb25-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dfb25-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dfb25-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb25-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dfb25-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




