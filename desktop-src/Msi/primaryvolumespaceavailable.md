---
description: El instalador establece el valor de la propiedad PrimaryVolumeSpaceAvailable en una cadena que representa el número total de bytes disponibles, en unidades de 512, en el volumen al que hace referencia la propiedad PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Propiedad PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653601"
---
# <a name="primaryvolumespaceavailable-property"></a><span data-ttu-id="f8af3-103">Propiedad PrimaryVolumeSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="f8af3-103">PrimaryVolumeSpaceAvailable property</span></span>

<span data-ttu-id="f8af3-104">El instalador establece el valor de la propiedad **PrimaryVolumeSpaceAvailable** en una cadena que representa el número total de bytes disponibles, en unidades de 512, en el volumen al que hace referencia la propiedad [**PrimaryVolumePath**](primaryvolumepath.md) .</span><span class="sxs-lookup"><span data-stu-id="f8af3-104">The installer sets the value of the **PrimaryVolumeSpaceAvailable** property to a string that represents the total number of bytes available, in units of 512, on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8af3-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8af3-105">Remarks</span></span>

<span data-ttu-id="f8af3-106">Por ejemplo, si [**PrimaryVolumePath**](primaryvolumepath.md) se establece en "D:", y el volumen D: tiene 446.134.272 bytes libres, **PrimaryVolumeSpaceAvailable** se establece en 871356.</span><span class="sxs-lookup"><span data-stu-id="f8af3-106">For example, if [**PrimaryVolumePath**](primaryvolumepath.md) is set to "D:", and volume D: has 446,134,272 bytes free, **PrimaryVolumeSpaceAvailable** is set to 871356.</span></span>

<span data-ttu-id="f8af3-107">Nota: Si este valor se va a mostrar dentro de un [control de texto](text-control.md)estático, se puede usar el bit [formatable](formatsize-control-attribute.md) para dar formato y etiquetar este número automáticamente en unidades de kilobytes o megabytes según corresponda.</span><span class="sxs-lookup"><span data-stu-id="f8af3-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8af3-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8af3-108">Requirements</span></span>



| <span data-ttu-id="f8af3-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8af3-109">Requirement</span></span> | <span data-ttu-id="f8af3-110">Value</span><span class="sxs-lookup"><span data-stu-id="f8af3-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8af3-111">Versión</span><span class="sxs-lookup"><span data-stu-id="f8af3-111">Version</span></span><br/> | <span data-ttu-id="f8af3-112">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f8af3-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f8af3-113">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f8af3-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f8af3-114">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f8af3-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f8af3-115">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f8af3-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8af3-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f8af3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8af3-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f8af3-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




