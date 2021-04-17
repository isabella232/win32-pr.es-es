---
description: Si se establece el bit de control CDROMVolume, el control muestra todos los volúmenes de la instalación actual más todos los volúmenes de CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Atributo de control CDROMVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652595"
---
# <a name="cdromvolume-control-attribute"></a><span data-ttu-id="27514-103">Atributo de control CDROMVolume</span><span class="sxs-lookup"><span data-stu-id="27514-103">CDROMVolume Control Attribute</span></span>

<span data-ttu-id="27514-104">Si se establece el bit de control CDROMVolume, el control muestra todos los volúmenes de la instalación actual más todos los volúmenes de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="27514-104">If the CDROMVolume Control bit is set, the control shows all the volumes in the current installation plus all the CD-ROM volumes.</span></span>

<span data-ttu-id="27514-105">Si no se establece este bit, el control muestra todos los volúmenes de la instalación actual.</span><span class="sxs-lookup"><span data-stu-id="27514-105">If this bit is not set, the control shows all the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="27514-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="27514-106">Valid Controls</span></span>

[<span data-ttu-id="27514-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="27514-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="27514-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="27514-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="27514-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="27514-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="27514-110">Value</span><span class="sxs-lookup"><span data-stu-id="27514-110">Value</span></span>



| <span data-ttu-id="27514-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="27514-111">Decimal</span></span> | <span data-ttu-id="27514-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="27514-112">Hexadecimal</span></span> | <span data-ttu-id="27514-113">Constante</span><span class="sxs-lookup"><span data-stu-id="27514-113">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="27514-114">524 288</span><span class="sxs-lookup"><span data-stu-id="27514-114">524288</span></span>  | <span data-ttu-id="27514-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="27514-115">0x00080000</span></span>  | <span data-ttu-id="27514-116">**msidbControlAttributesCDROMVolume**</span><span class="sxs-lookup"><span data-stu-id="27514-116">**msidbControlAttributesCDROMVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="27514-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27514-117">Remarks</span></span>

<span data-ttu-id="27514-118">Para establecer este atributo en un control, incluya el bit CDROMVolume en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="27514-118">To set this attribute on a control, include the CDROMVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="27514-119">Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="27514-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



