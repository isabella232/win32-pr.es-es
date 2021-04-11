---
description: Si este bit se establece en un control de texto, la aparición del carácter &\# 0034; &&\# 0034; en una cadena de texto se muestra como sí mismo. Si no se establece este bit, el carácter que sigue a &\# 0034; &&\# 0034; en la cadena de texto se muestra como un carácter de subrayado.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: Noprefix (atributo de control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275924"
---
# <a name="noprefix-control-attribute"></a><span data-ttu-id="fb138-104">Noprefix (atributo de control)</span><span class="sxs-lookup"><span data-stu-id="fb138-104">NoPrefix Control Attribute</span></span>

<span data-ttu-id="fb138-105">Si este bit se establece en un control de texto, la aparición del carácter "&" en una cadena de texto se muestra como sí mismo.</span><span class="sxs-lookup"><span data-stu-id="fb138-105">If this bit is set on a text control, the occurrence of the character "&" in a text string is displayed as itself.</span></span> <span data-ttu-id="fb138-106">Si no se establece este bit, el carácter que sigue a "&" en la cadena de texto se muestra como un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="fb138-106">If this bit is not set, then the character following "&" in the text string is displayed as an underscored character.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="fb138-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="fb138-107">Valid Controls</span></span>

[<span data-ttu-id="fb138-108">Texto</span><span class="sxs-lookup"><span data-stu-id="fb138-108">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="fb138-109">Value</span><span class="sxs-lookup"><span data-stu-id="fb138-109">Value</span></span>



| <span data-ttu-id="fb138-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="fb138-110">Decimal</span></span> | <span data-ttu-id="fb138-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="fb138-111">Hexadecimal</span></span> | <span data-ttu-id="fb138-112">Constante</span><span class="sxs-lookup"><span data-stu-id="fb138-112">Constant</span></span>                           |
|---------|-------------|------------------------------------|
| <span data-ttu-id="fb138-113">131 072</span><span class="sxs-lookup"><span data-stu-id="fb138-113">131072</span></span>  | <span data-ttu-id="fb138-114">0x20000</span><span class="sxs-lookup"><span data-stu-id="fb138-114">0x20000</span></span>     | <span data-ttu-id="fb138-115">**msidbControlAttributesNoPrefix**</span><span class="sxs-lookup"><span data-stu-id="fb138-115">**msidbControlAttributesNoPrefix**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fb138-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb138-116">Remarks</span></span>

<span data-ttu-id="fb138-117">Para establecer este atributo en un control, incluya el bit noprefix en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="fb138-117">To set this attribute on a control, include the NoPrefix bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="fb138-118">Vea [controles y](controls.md) [atributos de control](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="fb138-118">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



