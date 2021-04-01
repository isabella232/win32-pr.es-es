---
description: Si se establece este bit, los elementos enumerados en el control se muestran en un orden especificado. Si no se establece el bit, los elementos se muestran en orden alfabético.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Atributo de control ordenado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082002"
---
# <a name="sorted-control-attribute"></a><span data-ttu-id="8099e-104">Atributo de control ordenado</span><span class="sxs-lookup"><span data-stu-id="8099e-104">Sorted Control Attribute</span></span>

<span data-ttu-id="8099e-105">Si se establece este bit, los elementos enumerados en el control se muestran en un orden especificado.</span><span class="sxs-lookup"><span data-stu-id="8099e-105">If this bit is set, the items listed in the control are displayed in a specified order.</span></span> <span data-ttu-id="8099e-106">Si no se establece el bit, los elementos se muestran en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="8099e-106">If the bit is not set, items are displayed in alphabetical order.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="8099e-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="8099e-107">Valid Controls</span></span>

[<span data-ttu-id="8099e-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="8099e-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="8099e-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="8099e-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="8099e-110">Control ListView</span><span class="sxs-lookup"><span data-stu-id="8099e-110">ListView Control</span></span>](listview-control.md)

## <a name="value"></a><span data-ttu-id="8099e-111">Value</span><span class="sxs-lookup"><span data-stu-id="8099e-111">Value</span></span>



| <span data-ttu-id="8099e-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="8099e-112">Decimal</span></span> | <span data-ttu-id="8099e-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="8099e-113">Hexadecimal</span></span> | <span data-ttu-id="8099e-114">Constante</span><span class="sxs-lookup"><span data-stu-id="8099e-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="8099e-115">65536</span><span class="sxs-lookup"><span data-stu-id="8099e-115">65536</span></span>   | <span data-ttu-id="8099e-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="8099e-116">0x00010000</span></span>  | <span data-ttu-id="8099e-117">**msidbControlAttributesSorted**</span><span class="sxs-lookup"><span data-stu-id="8099e-117">**msidbControlAttributesSorted**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8099e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8099e-118">Remarks</span></span>

<span data-ttu-id="8099e-119">Para ordenar los elementos de un control [ComboBox](combobox-control.md), incluya el bit ordenado en la columna Attributes de la [tabla de control](control-table.md) y especifique el orden de los elementos en la columna order de la [tabla ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="8099e-119">To sort the items in a [ComboBox](combobox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="8099e-120">Para ordenar los elementos de un [cuadro de lista](listbox-control.md), incluya el bit ordenado en la columna Attributes de la [tabla de control](control-table.md) y especifique el orden de los elementos en la columna order de la [tabla ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="8099e-120">To sort the items in a [ListBox](listbox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="8099e-121">Para ordenar los elementos en un control [ListView](listview-control.md), incluya el bit ordenado en la columna Attributes de la [tabla de control](control-table.md) y especifique el orden de los elementos en la [tabla ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="8099e-121">To sort the items in a [ListView](listview-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the order of items in the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="8099e-122">Vea [controles y](controls.md) [atributos de control](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="8099e-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



