---
description: Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual, además de todos los volúmenes extraíbles. Si no se establece este bit, el control muestra los volúmenes en la instalación actual.
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: Atributo de control RemovableVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a91a464eb55ee965f12eae9885849eb2080996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809494"
---
# <a name="removablevolume-control-attribute"></a><span data-ttu-id="94e7c-104">Atributo de control RemovableVolume</span><span class="sxs-lookup"><span data-stu-id="94e7c-104">RemovableVolume Control Attribute</span></span>

<span data-ttu-id="94e7c-105">Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual, además de todos los volúmenes extraíbles.</span><span class="sxs-lookup"><span data-stu-id="94e7c-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the removable volumes.</span></span> <span data-ttu-id="94e7c-106">Si no se establece este bit, el control muestra los volúmenes en la instalación actual.</span><span class="sxs-lookup"><span data-stu-id="94e7c-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="94e7c-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="94e7c-107">Valid Controls</span></span>

[<span data-ttu-id="94e7c-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="94e7c-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="94e7c-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="94e7c-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="94e7c-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="94e7c-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="94e7c-111">Value</span><span class="sxs-lookup"><span data-stu-id="94e7c-111">Value</span></span>



| <span data-ttu-id="94e7c-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="94e7c-112">Decimal</span></span> | <span data-ttu-id="94e7c-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="94e7c-113">Hexadecimal</span></span> | <span data-ttu-id="94e7c-114">Constante</span><span class="sxs-lookup"><span data-stu-id="94e7c-114">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="94e7c-115">65536</span><span class="sxs-lookup"><span data-stu-id="94e7c-115">65536</span></span>   | <span data-ttu-id="94e7c-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="94e7c-116">0x00010000</span></span>  | <span data-ttu-id="94e7c-117">**msidbControlAttributesRemovableVolume**</span><span class="sxs-lookup"><span data-stu-id="94e7c-117">**msidbControlAttributesRemovableVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="94e7c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94e7c-118">Remarks</span></span>

<span data-ttu-id="94e7c-119">Para establecer este atributo en un control, incluya el bit RemovableVolume en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="94e7c-119">To set this attribute on a control, include the RemovableVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="94e7c-120">Vea [controles y](controls.md) [atributos de control](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="94e7c-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



