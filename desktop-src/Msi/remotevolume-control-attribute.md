---
description: Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual, además de todos los volúmenes remotos. Si no se establece este bit, el control muestra los volúmenes en la instalación actual.
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: Atributo de control RemoteVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677355"
---
# <a name="remotevolume-control-attribute"></a><span data-ttu-id="35f91-104">Atributo de control RemoteVolume</span><span class="sxs-lookup"><span data-stu-id="35f91-104">RemoteVolume Control Attribute</span></span>

<span data-ttu-id="35f91-105">Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual, además de todos los volúmenes remotos.</span><span class="sxs-lookup"><span data-stu-id="35f91-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the remote volumes.</span></span> <span data-ttu-id="35f91-106">Si no se establece este bit, el control muestra los volúmenes en la instalación actual.</span><span class="sxs-lookup"><span data-stu-id="35f91-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="35f91-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="35f91-107">Valid Controls</span></span>

[<span data-ttu-id="35f91-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="35f91-108">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="35f91-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="35f91-109">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="35f91-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="35f91-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="35f91-111">Value</span><span class="sxs-lookup"><span data-stu-id="35f91-111">Value</span></span>



| <span data-ttu-id="35f91-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="35f91-112">Decimal</span></span> | <span data-ttu-id="35f91-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="35f91-113">Hexadecimal</span></span> | <span data-ttu-id="35f91-114">Constante</span><span class="sxs-lookup"><span data-stu-id="35f91-114">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="35f91-115">262 144</span><span class="sxs-lookup"><span data-stu-id="35f91-115">262144</span></span>  | <span data-ttu-id="35f91-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="35f91-116">0x00040000</span></span>  | <span data-ttu-id="35f91-117">**msidbControlAttributesRemoteVolume**</span><span class="sxs-lookup"><span data-stu-id="35f91-117">**msidbControlAttributesRemoteVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="35f91-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35f91-118">Remarks</span></span>

<span data-ttu-id="35f91-119">Para establecer este atributo en un control, incluya el bit RemoteVolume en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="35f91-119">To set this attribute on a control, include the RemoteVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="35f91-120">Vea [controles y](controls.md) [atributos de control](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="35f91-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



