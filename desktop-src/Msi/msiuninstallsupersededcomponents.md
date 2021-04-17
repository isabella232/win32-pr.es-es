---
description: Establezca la propiedad MSIUNINSTALLSUPERSEDEDCOMPONENTS en 1 en la tabla de propiedades o en una línea de comandos.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: Propiedad MSIUNINSTALLSUPERSEDEDCOMPONENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680790"
---
# <a name="msiuninstallsupersededcomponents-property"></a><span data-ttu-id="e8698-103">Propiedad MSIUNINSTALLSUPERSEDEDCOMPONENTS</span><span class="sxs-lookup"><span data-stu-id="e8698-103">MSIUNINSTALLSUPERSEDEDCOMPONENTS property</span></span>

<span data-ttu-id="e8698-104">Establezca la propiedad **MSIUNINSTALLSUPERSEDEDCOMPONENTS** en 1 en la [tabla de propiedades](property-table.md) o en una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="e8698-104">Set the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** property to 1 in the [Property table](property-table.md) or on a command line.</span></span> <span data-ttu-id="e8698-105">Cuando esta propiedad se ha establecido en 1, el instalador determina si los componentes de las revisiones reemplazadas se están volviendo redundantes.</span><span class="sxs-lookup"><span data-stu-id="e8698-105">When this property has been set to 1, the installer determines whether the components in any superseded patches are becoming redundant.</span></span> <span data-ttu-id="e8698-106">El instalador puede anular el registro y desinstalar los componentes redundantes para evitar que queden detrás de los componentes huérfanos en el equipo.</span><span class="sxs-lookup"><span data-stu-id="e8698-106">The installer can unregister and uninstall redundant components to prevent leaving behind orphan components on the computer.</span></span>

<span data-ttu-id="e8698-107">El establecimiento de esta propiedad afecta a los componentes de todas las revisiones que se reemplazan.</span><span class="sxs-lookup"><span data-stu-id="e8698-107">Setting this property affects the components in all patches being superseded.</span></span> <span data-ttu-id="e8698-108">Para habilitar esta funcionalidad para componentes individuales, use el atributo **msidbComponentAttributesUninstallOnSupersedence** en la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="e8698-108">To enable this functionality for single components, use the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md).</span></span>

<span data-ttu-id="e8698-109">**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="e8698-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="e8698-110">Las versiones anteriores a Windows Installer 4,5 omiten la propiedad **MSIUNINSTALLSUPERSEDEDCOMPONENTS** .</span><span class="sxs-lookup"><span data-stu-id="e8698-110">Versions earlier than Windows Installer 4.5 ignore the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** Property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8698-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8698-111">Requirements</span></span>



| <span data-ttu-id="e8698-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8698-112">Requirement</span></span> | <span data-ttu-id="e8698-113">Value</span><span class="sxs-lookup"><span data-stu-id="e8698-113">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8698-114">Versión</span><span class="sxs-lookup"><span data-stu-id="e8698-114">Version</span></span><br/> | <span data-ttu-id="e8698-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e8698-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e8698-116">Windows Installer 4,5 o Windows Installer 4,5 en Windows Vista, Windows XP, Windows Server 2003 y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e8698-116">Windows Installer 4.5 or Windows Installer 4.5 on Windows Vista, Windows XP, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="e8698-117">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e8698-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8698-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e8698-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8698-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e8698-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




