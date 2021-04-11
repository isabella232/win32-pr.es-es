---
description: Si este bit se establece en un control de edición, el instalador crea un control de edición de varias líneas con una barra de desplazamiento vertical.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Atributo de control Multiline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276283"
---
# <a name="multiline-control-attribute"></a><span data-ttu-id="11c1f-103">Atributo de control Multiline</span><span class="sxs-lookup"><span data-stu-id="11c1f-103">MultiLine Control Attribute</span></span>

<span data-ttu-id="11c1f-104">Si este bit se establece en un [control de edición](edit-control.md), el instalador crea un control de edición de varias líneas con una barra de desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="11c1f-104">If this bit is set on an [Edit control](edit-control.md), the installer creates a multiple line edit control with a vertical scroll bar.</span></span>

<span data-ttu-id="11c1f-105">Si no se establece este bit, especifica que se muestra un control de edición normal.</span><span class="sxs-lookup"><span data-stu-id="11c1f-105">If this bit is not set, it specifies displaying a normal edit control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="11c1f-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="11c1f-106">Valid Controls</span></span>

<span data-ttu-id="11c1f-107">[Control de edición](edit-control.md).</span><span class="sxs-lookup"><span data-stu-id="11c1f-107">[Edit control](edit-control.md).</span></span>



| <span data-ttu-id="11c1f-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="11c1f-108">Decimal</span></span> | <span data-ttu-id="11c1f-109">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="11c1f-109">Hexadecimal</span></span> | <span data-ttu-id="11c1f-110">Constante</span><span class="sxs-lookup"><span data-stu-id="11c1f-110">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="11c1f-111">65536</span><span class="sxs-lookup"><span data-stu-id="11c1f-111">65536</span></span>   | <span data-ttu-id="11c1f-112">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11c1f-112">0x00010000</span></span>  | <span data-ttu-id="11c1f-113">**msidbControlAttributesMultiline**</span><span class="sxs-lookup"><span data-stu-id="11c1f-113">**msidbControlAttributesMultiline**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="11c1f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11c1f-114">Remarks</span></span>

<span data-ttu-id="11c1f-115">Para establecer este atributo en un control, incluya el bit de varias líneas en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="11c1f-115">To set this attribute on a control, include the MultiLine bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="11c1f-116">Vea [controles y](controls.md) [atributos de control](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="11c1f-116">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



