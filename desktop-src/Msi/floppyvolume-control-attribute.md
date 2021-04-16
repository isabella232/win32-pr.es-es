---
description: Si se establece el bit de control FloppyVolume, el control muestra todos los volúmenes implicados en la instalación actual, además de todos los volúmenes de disquete.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Atributo de control FloppyVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70045ee5d6e16fbe1f679eafd83e6d657c9bf6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544270"
---
# <a name="floppyvolume-control-attribute"></a><span data-ttu-id="ad974-103">Atributo de control FloppyVolume</span><span class="sxs-lookup"><span data-stu-id="ad974-103">FloppyVolume Control Attribute</span></span>

<span data-ttu-id="ad974-104">Si se establece el bit de control FloppyVolume, el control muestra todos los volúmenes implicados en la instalación actual, además de todos los volúmenes de disquete.</span><span class="sxs-lookup"><span data-stu-id="ad974-104">If the FloppyVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the floppy volumes.</span></span>

<span data-ttu-id="ad974-105">Si no se establece este bit, el control muestra los volúmenes en la instalación actual.</span><span class="sxs-lookup"><span data-stu-id="ad974-105">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="ad974-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="ad974-106">Valid Controls</span></span>

[<span data-ttu-id="ad974-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="ad974-107">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="ad974-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="ad974-108">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="ad974-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="ad974-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="ad974-110">Value</span><span class="sxs-lookup"><span data-stu-id="ad974-110">Value</span></span>



| <span data-ttu-id="ad974-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="ad974-111">Decimal</span></span> | <span data-ttu-id="ad974-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="ad974-112">Hexadecimal</span></span> | <span data-ttu-id="ad974-113">Constante</span><span class="sxs-lookup"><span data-stu-id="ad974-113">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="ad974-114">2 097 152</span><span class="sxs-lookup"><span data-stu-id="ad974-114">2097152</span></span> | <span data-ttu-id="ad974-115">0x00200000</span><span class="sxs-lookup"><span data-stu-id="ad974-115">0x00200000</span></span>  | <span data-ttu-id="ad974-116">**msidbControlAttributesFloppyVolume**</span><span class="sxs-lookup"><span data-stu-id="ad974-116">**msidbControlAttributesFloppyVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ad974-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad974-117">Remarks</span></span>

<span data-ttu-id="ad974-118">Para establecer este atributo en un control, incluya el bit FloppyVolume en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ad974-118">To set this attribute on a control, include the FloppyVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="ad974-119">Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="ad974-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



