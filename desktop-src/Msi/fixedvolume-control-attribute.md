---
description: Si se establece el bit de control FixedVolume, el control muestra todos los volúmenes implicados en la instalación actual, además de todas las unidades de disco duro internas fijas.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Atributo de control FixedVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908441"
---
# <a name="fixedvolume-control-attribute"></a><span data-ttu-id="fe5c0-103">Atributo de control FixedVolume</span><span class="sxs-lookup"><span data-stu-id="fe5c0-103">FixedVolume Control Attribute</span></span>

<span data-ttu-id="fe5c0-104">Si se establece el bit de control FixedVolume, el control muestra todos los volúmenes implicados en la instalación actual, además de todas las unidades de disco duro internas fijas.</span><span class="sxs-lookup"><span data-stu-id="fe5c0-104">If the FixedVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the fixed internal hard drives.</span></span>

<span data-ttu-id="fe5c0-105">Si no se establece este bit, el control muestra los volúmenes en la instalación actual.</span><span class="sxs-lookup"><span data-stu-id="fe5c0-105">If this bit is not set, the control lists the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="fe5c0-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="fe5c0-106">Valid Controls</span></span>

[<span data-ttu-id="fe5c0-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="fe5c0-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="fe5c0-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="fe5c0-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="fe5c0-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="fe5c0-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)



| <span data-ttu-id="fe5c0-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="fe5c0-110">Decimal</span></span> | <span data-ttu-id="fe5c0-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="fe5c0-111">Hexadecimal</span></span> | <span data-ttu-id="fe5c0-112">Constante</span><span class="sxs-lookup"><span data-stu-id="fe5c0-112">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="fe5c0-113">131 072</span><span class="sxs-lookup"><span data-stu-id="fe5c0-113">131072</span></span>  | <span data-ttu-id="fe5c0-114">0x00020000</span><span class="sxs-lookup"><span data-stu-id="fe5c0-114">0x00020000</span></span>  | <span data-ttu-id="fe5c0-115">**msidbControlAttributesFixedVolume**</span><span class="sxs-lookup"><span data-stu-id="fe5c0-115">**msidbControlAttributesFixedVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fe5c0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe5c0-116">Remarks</span></span>

<span data-ttu-id="fe5c0-117">Para establecer este atributo en un control, incluya el bit FixedVolume en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="fe5c0-117">To set this attribute on a control, include the FixedVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="fe5c0-118">Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="fe5c0-118">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



