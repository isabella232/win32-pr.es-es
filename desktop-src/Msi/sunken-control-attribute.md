---
description: Si se establece este bit, el control se muestra con un aspecto hundido de tres dimensiones.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Atributo de control hundido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c6852a2f32880a427016e41ce9f68314a4a4ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155120"
---
# <a name="sunken-control-attribute"></a><span data-ttu-id="5e3b3-103">Atributo de control hundido</span><span class="sxs-lookup"><span data-stu-id="5e3b3-103">Sunken Control Attribute</span></span>

<span data-ttu-id="5e3b3-104">Si se establece este bit, el control se muestra con un aspecto hundido de tres dimensiones.</span><span class="sxs-lookup"><span data-stu-id="5e3b3-104">If this bit is set, the control is displayed with a sunken, three dimensional look.</span></span> <span data-ttu-id="5e3b3-105">El efecto de este bit de estilo es diferente en los distintos controles y versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3b3-105">The effect of this style bit is different on different controls and versions of Windows.</span></span> <span data-ttu-id="5e3b3-106">En algunos controles no tiene ningún efecto visible.</span><span class="sxs-lookup"><span data-stu-id="5e3b3-106">On some controls it has no visible effect.</span></span> <span data-ttu-id="5e3b3-107">Si el sistema no admite el atributo de control hundido, el control se muestra en el estilo visual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5e3b3-107">If the system does not support the Sunken control attribute, the control is displayed in the default visual style.</span></span> <span data-ttu-id="5e3b3-108">Si no se establece este bit, el control se muestra con el estilo visual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5e3b3-108">If this bit is not set, the control is displayed with the default visual style.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="5e3b3-109">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="5e3b3-109">Valid Controls</span></span>

<span data-ttu-id="5e3b3-110">Todos los controles.</span><span class="sxs-lookup"><span data-stu-id="5e3b3-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="5e3b3-111">Value</span><span class="sxs-lookup"><span data-stu-id="5e3b3-111">Value</span></span>



| <span data-ttu-id="5e3b3-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="5e3b3-112">Decimal</span></span> | <span data-ttu-id="5e3b3-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="5e3b3-113">Hexadecimal</span></span> | <span data-ttu-id="5e3b3-114">Constante</span><span class="sxs-lookup"><span data-stu-id="5e3b3-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="5e3b3-115">4</span><span class="sxs-lookup"><span data-stu-id="5e3b3-115">4</span></span>       | <span data-ttu-id="5e3b3-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5e3b3-116">0x00000004</span></span>  | <span data-ttu-id="5e3b3-117">**msidbControlAttributesSunken**</span><span class="sxs-lookup"><span data-stu-id="5e3b3-117">**msidbControlAttributesSunken**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5e3b3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e3b3-118">Remarks</span></span>

<span data-ttu-id="5e3b3-119">Para establecer este atributo en un control, incluya el bit hundido en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="5e3b3-119">To set this attribute on a control, include the Sunken bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="5e3b3-120">Vea [controles y](controls.md) [atributos de control](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="5e3b3-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



