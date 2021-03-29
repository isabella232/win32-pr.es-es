---
description: El instalador establece el valor de la propiedad PrimaryVolumeSpaceRemaining en una cadena que representa el número total de bytes restantes en el volumen al que hace referencia la propiedad PrimaryVolumePath, si se instalaron todas las características seleccionadas actualmente.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: Propiedad PrimaryVolumeSpaceRemaining
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654004"
---
# <a name="primaryvolumespaceremaining-property"></a><span data-ttu-id="b234d-103">Propiedad PrimaryVolumeSpaceRemaining</span><span class="sxs-lookup"><span data-stu-id="b234d-103">PrimaryVolumeSpaceRemaining property</span></span>

<span data-ttu-id="b234d-104">El instalador establece el valor de la propiedad **PrimaryVolumeSpaceRemaining** en una cadena que representa el número total de bytes restantes en el volumen al que hace referencia la propiedad [**PrimaryVolumePath**](primaryvolumepath.md) , si se instalaron todas las características seleccionadas actualmente.</span><span class="sxs-lookup"><span data-stu-id="b234d-104">The installer sets the value of the **PrimaryVolumeSpaceRemaining** property to a string representing the total number of bytes remaining on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property, if all currently selected features were installed.</span></span> <span data-ttu-id="b234d-105">Al igual que con la propiedad [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , este número se expresa en unidades de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="b234d-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="b234d-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b234d-106">Remarks</span></span>

<span data-ttu-id="b234d-107">Nota: Si este valor se va a mostrar dentro de un [control de texto](text-control.md)estático, se puede usar el bit [formatable](formatsize-control-attribute.md) para dar formato y etiquetar este número automáticamente en unidades de kilobytes o megabytes según corresponda.</span><span class="sxs-lookup"><span data-stu-id="b234d-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="b234d-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b234d-108">Requirements</span></span>



| <span data-ttu-id="b234d-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="b234d-109">Requirement</span></span> | <span data-ttu-id="b234d-110">Value</span><span class="sxs-lookup"><span data-stu-id="b234d-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b234d-111">Versión</span><span class="sxs-lookup"><span data-stu-id="b234d-111">Version</span></span><br/> | <span data-ttu-id="b234d-112">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b234d-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b234d-113">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b234d-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b234d-114">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="b234d-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b234d-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b234d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b234d-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b234d-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




