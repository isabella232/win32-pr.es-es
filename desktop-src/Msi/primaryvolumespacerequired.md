---
description: El instalador establece el valor de la propiedad PrimaryVolumeSpaceRequired en una cadena que representa el número total de bytes necesarios para todas las características seleccionadas en el volumen al que hace referencia la propiedad PrimaryVolumePath.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: Propiedad PrimaryVolumeSpaceRequired
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654005"
---
# <a name="primaryvolumespacerequired-property"></a><span data-ttu-id="ff8ff-103">Propiedad PrimaryVolumeSpaceRequired</span><span class="sxs-lookup"><span data-stu-id="ff8ff-103">PrimaryVolumeSpaceRequired property</span></span>

<span data-ttu-id="ff8ff-104">El instalador establece el valor de la propiedad **PrimaryVolumeSpaceRequired** en una cadena que representa el número total de bytes necesarios para todas las características seleccionadas en el volumen al que hace referencia la propiedad [**PrimaryVolumePath**](primaryvolumepath.md) .</span><span class="sxs-lookup"><span data-stu-id="ff8ff-104">The installer sets the value of the **PrimaryVolumeSpaceRequired** property to a string representing the total number of bytes required by all selected features on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span> <span data-ttu-id="ff8ff-105">Al igual que con la propiedad [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , este número se expresa en unidades de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="ff8ff-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff8ff-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff8ff-106">Remarks</span></span>

<span data-ttu-id="ff8ff-107">Nota: Si este valor se va a mostrar dentro de un [control de texto](text-control.md)estático, se puede usar el bit [formatable](formatsize-control-attribute.md) para dar formato y etiquetar este número automáticamente en unidades de kilobytes o megabytes según corresponda.</span><span class="sxs-lookup"><span data-stu-id="ff8ff-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff8ff-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff8ff-108">Requirements</span></span>



| <span data-ttu-id="ff8ff-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff8ff-109">Requirement</span></span> | <span data-ttu-id="ff8ff-110">Value</span><span class="sxs-lookup"><span data-stu-id="ff8ff-110">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff8ff-111">Versión</span><span class="sxs-lookup"><span data-stu-id="ff8ff-111">Version</span></span><br/> | <span data-ttu-id="ff8ff-112">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ff8ff-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ff8ff-113">Windows Installer 4,0 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ff8ff-113">Windows Installer 4.0 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ff8ff-114">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ff8ff-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ff8ff-115">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ff8ff-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff8ff-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ff8ff-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff8ff-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff8ff-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




