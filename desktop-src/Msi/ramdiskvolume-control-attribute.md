---
description: Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes de disco RAM. Si no se establece este bit, el control muestra los volúmenes en la instalación actual.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Atributo de control RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677767"
---
# <a name="ramdiskvolume-control-attribute"></a><span data-ttu-id="f0aaa-104">Atributo de control RAMDiskVolume</span><span class="sxs-lookup"><span data-stu-id="f0aaa-104">RAMDiskVolume Control Attribute</span></span>

<span data-ttu-id="f0aaa-105">Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes de disco RAM.</span><span class="sxs-lookup"><span data-stu-id="f0aaa-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the RAM disk volumes.</span></span> <span data-ttu-id="f0aaa-106">Si no se establece este bit, el control muestra los volúmenes en la instalación actual.</span><span class="sxs-lookup"><span data-stu-id="f0aaa-106">If this bit is not set the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="f0aaa-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="f0aaa-107">Valid Controls</span></span>

[<span data-ttu-id="f0aaa-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="f0aaa-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="f0aaa-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="f0aaa-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="f0aaa-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="f0aaa-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="f0aaa-111">Value</span><span class="sxs-lookup"><span data-stu-id="f0aaa-111">Value</span></span>



| <span data-ttu-id="f0aaa-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="f0aaa-112">Decimal</span></span> | <span data-ttu-id="f0aaa-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="f0aaa-113">Hexadecimal</span></span> | <span data-ttu-id="f0aaa-114">Constante</span><span class="sxs-lookup"><span data-stu-id="f0aaa-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="f0aaa-115">1048567</span><span class="sxs-lookup"><span data-stu-id="f0aaa-115">1048567</span></span> | <span data-ttu-id="f0aaa-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="f0aaa-116">0x00100000</span></span>  | <span data-ttu-id="f0aaa-117">**msidbControlAttributesRAMDiskVolume**</span><span class="sxs-lookup"><span data-stu-id="f0aaa-117">**msidbControlAttributesRAMDiskVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f0aaa-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0aaa-118">Remarks</span></span>

<span data-ttu-id="f0aaa-119">Para establecer este atributo en un control, incluya el bit RAMDiskVolume en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0aaa-119">To set this attribute on a control, include the RAMDiskVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="f0aaa-120">Vea [controles y](controls.md) [atributos de control](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="f0aaa-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



