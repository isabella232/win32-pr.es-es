---
description: Se trata de una combinación del orden de lectura de derecha a izquierda RTLRO, los atributos RightAligned y LeftScroll.
ms.assetid: 4eaec16f-ee1c-437b-8b76-7ebbdc4e2f71
title: Atributo de control BiDi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556195c1b3170983083473598f69acb99cdcfaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652603"
---
# <a name="bidi-control-attribute"></a><span data-ttu-id="da40d-103">Atributo de control BiDi</span><span class="sxs-lookup"><span data-stu-id="da40d-103">BiDi Control Attribute</span></span>

<span data-ttu-id="da40d-104">Se trata de una combinación del orden de lectura de derecha a izquierda [RTLRO](rtlro-control-attribute.md), los atributos [RightAligned](rightaligned-control-attribute.md)y [LeftScroll](leftscroll-control-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="da40d-104">This is a combination of the right-to-left reading order [RTLRO](rtlro-control-attribute.md), the [RightAligned](rightaligned-control-attribute.md), and [LeftScroll](leftscroll-control-attribute.md) attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="da40d-105">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="da40d-105">Valid Controls</span></span>

[<span data-ttu-id="da40d-106">ScrollableText</span><span class="sxs-lookup"><span data-stu-id="da40d-106">ScrollableText</span></span>](scrollabletext-control.md)

 

[<span data-ttu-id="da40d-107">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="da40d-107">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="da40d-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="da40d-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="da40d-109">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="da40d-109">DirectoryList</span></span>](directorylist-control.md)

 

[<span data-ttu-id="da40d-110">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="da40d-110">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="da40d-111">Editar</span><span class="sxs-lookup"><span data-stu-id="da40d-111">Edit</span></span>](edit-control.md)

 

[<span data-ttu-id="da40d-112">ListBox</span><span class="sxs-lookup"><span data-stu-id="da40d-112">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="da40d-113">ListView</span><span class="sxs-lookup"><span data-stu-id="da40d-113">ListView</span></span>](listview-control.md)

 

[<span data-ttu-id="da40d-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="da40d-114">SelectionTree</span></span>](selectiontree-control.md)

 

[<span data-ttu-id="da40d-115">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="da40d-115">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="da40d-116">Value</span><span class="sxs-lookup"><span data-stu-id="da40d-116">Value</span></span>



| <span data-ttu-id="da40d-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="da40d-117">Decimal</span></span> | <span data-ttu-id="da40d-118">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="da40d-118">Hexadecimal</span></span> | <span data-ttu-id="da40d-119">Constante</span><span class="sxs-lookup"><span data-stu-id="da40d-119">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="da40d-120">224</span><span class="sxs-lookup"><span data-stu-id="da40d-120">224</span></span>     | <span data-ttu-id="da40d-121">0x000000E0</span><span class="sxs-lookup"><span data-stu-id="da40d-121">0x000000E0</span></span>  | <span data-ttu-id="da40d-122">**msidbControlAttributesBiDi**</span><span class="sxs-lookup"><span data-stu-id="da40d-122">**msidbControlAttributesBiDi**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="da40d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da40d-123">Remarks</span></span>

<span data-ttu-id="da40d-124">Para establecer este atributo en un control, incluya el bit BiDi en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="da40d-124">To set this attribute on a control, include the BiDi bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="da40d-125">Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="da40d-125">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



