---
description: Si se establece este bit, el texto del control se muestra en una sola línea. Si el texto se extiende más allá de los márgenes del control, se trunca y un botón de puntos suspensivos (&\# 0034;... &\# 0034;) se inserta al final para indicar el truncamiento. Si no se establece este bit, el texto se ajusta.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: NoWrap (atributo de control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677997"
---
# <a name="nowrap-control-attribute"></a><span data-ttu-id="93ad3-105">NoWrap (atributo de control)</span><span class="sxs-lookup"><span data-stu-id="93ad3-105">NoWrap Control Attribute</span></span>

<span data-ttu-id="93ad3-106">Si se establece este bit, el texto del control se muestra en una sola línea.</span><span class="sxs-lookup"><span data-stu-id="93ad3-106">If this bit is set the text in the control is displayed on a single line.</span></span> <span data-ttu-id="93ad3-107">Si el texto se extiende más allá de los márgenes del control, se trunca y se inserta un botón de puntos suspensivos ("...") al final para indicar el truncamiento.</span><span class="sxs-lookup"><span data-stu-id="93ad3-107">If the text extends beyond the control's margins it is truncated and an ellipsis ("...") is inserted at the end to indicate the truncation.</span></span> <span data-ttu-id="93ad3-108">Si no se establece este bit, el texto se ajusta.</span><span class="sxs-lookup"><span data-stu-id="93ad3-108">If this bit is not set, text wraps.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="93ad3-109">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="93ad3-109">Valid Controls</span></span>

[<span data-ttu-id="93ad3-110">Texto</span><span class="sxs-lookup"><span data-stu-id="93ad3-110">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="93ad3-111">Value</span><span class="sxs-lookup"><span data-stu-id="93ad3-111">Value</span></span>



| <span data-ttu-id="93ad3-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="93ad3-112">Decimal</span></span> | <span data-ttu-id="93ad3-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="93ad3-113">Hexadecimal</span></span> | <span data-ttu-id="93ad3-114">Constante</span><span class="sxs-lookup"><span data-stu-id="93ad3-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="93ad3-115">262 144</span><span class="sxs-lookup"><span data-stu-id="93ad3-115">262144</span></span>  | <span data-ttu-id="93ad3-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="93ad3-116">0x00040000</span></span>  | <span data-ttu-id="93ad3-117">**msidbControlAttributesNoWrap**</span><span class="sxs-lookup"><span data-stu-id="93ad3-117">**msidbControlAttributesNoWrap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="93ad3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93ad3-118">Remarks</span></span>

<span data-ttu-id="93ad3-119">Para establecer este atributo en un control, incluya el bit NoWrap en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="93ad3-119">To set this attribute on a control, include the NoWrap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="93ad3-120">Vea [controles y](controls.md) [atributos de control](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="93ad3-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



