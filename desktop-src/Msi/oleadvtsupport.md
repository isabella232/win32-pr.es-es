---
description: El instalador establece la propiedad OLEAdvtSupport en true cuando se ha actualizado el sistema del usuario actual para que funcione con la instalación a petición a través de COM.
ms.assetid: 274d7658-3d33-4c3a-987c-878cbd5bf821
title: Propiedad OLEAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c9bd8f5ecaaa2690654211a2dd7ecdc5e9ef2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653470"
---
# <a name="oleadvtsupport-property"></a><span data-ttu-id="ebb4b-103">Propiedad OLEAdvtSupport</span><span class="sxs-lookup"><span data-stu-id="ebb4b-103">OLEAdvtSupport property</span></span>

<span data-ttu-id="ebb4b-104">El instalador establece la propiedad **OLEAdvtSupport** en true cuando se ha actualizado el sistema del usuario actual para que funcione con la instalación a petición a través de com.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-104">The installer sets the **OLEAdvtSupport** property to true when the current user's system has been upgraded to work with installation-on-demand through COM.</span></span> <span data-ttu-id="ebb4b-105">Tenga en cuenta que para que el instalador registre una clase COM y habilite la instalación a petición, la clase debe aparecer en las tablas [Class](class-table.md) y [ProgID](progid-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ebb4b-105">Note that for the installer to register a COM class and enable installation-on-demand, the class must be listed in the [Class](class-table.md) and [ProgId](progid-table.md) tables.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebb4b-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebb4b-106">Requirements</span></span>



| <span data-ttu-id="ebb4b-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebb4b-107">Requirement</span></span> | <span data-ttu-id="ebb4b-108">Value</span><span class="sxs-lookup"><span data-stu-id="ebb4b-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb4b-109">Versión</span><span class="sxs-lookup"><span data-stu-id="ebb4b-109">Version</span></span><br/> | <span data-ttu-id="ebb4b-110">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-110">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ebb4b-111">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-111">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ebb4b-112">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-112">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ebb4b-113">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ebb4b-113">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebb4b-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ebb4b-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb4b-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ebb4b-115">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ebb4b-116">**Propiedad ShellAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="ebb4b-116">**ShellAdvtSupport Property**</span></span>](shelladvtsupport.md)
</dt> <dt>

[<span data-ttu-id="ebb4b-117">Compatibilidad de la plataforma con el anuncio</span><span class="sxs-lookup"><span data-stu-id="ebb4b-117">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)
</dt> </dl>

 

 




