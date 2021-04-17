---
description: Si se establece este bit, el texto se reemplaza por una imagen de icono y la columna de texto de la tabla de control es una clave externa de la tabla binaria.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Atributo de control de icono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60c19674ac26f108109fad04e0836ed8dfeba6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652509"
---
# <a name="icon-control-attribute"></a><span data-ttu-id="48aa5-103">Atributo de control de icono</span><span class="sxs-lookup"><span data-stu-id="48aa5-103">Icon Control Attribute</span></span>

<span data-ttu-id="48aa5-104">Si se establece este bit, el texto se reemplaza por una imagen de icono y la columna de texto de la [tabla de control](control-table.md) es una clave externa de la [tabla binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="48aa5-104">If this bit is set, text is replaced by an icon image and the Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="48aa5-105">Si no se establece este bit, el texto del control se especifica en la columna de texto de la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="48aa5-105">If this bit is not set, text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="48aa5-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="48aa5-106">Valid Controls</span></span>

[<span data-ttu-id="48aa5-107">CheckBox</span><span class="sxs-lookup"><span data-stu-id="48aa5-107">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="48aa5-108">Botones</span><span class="sxs-lookup"><span data-stu-id="48aa5-108">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="48aa5-109">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="48aa5-109">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="48aa5-110">Value</span><span class="sxs-lookup"><span data-stu-id="48aa5-110">Value</span></span>



| <span data-ttu-id="48aa5-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="48aa5-111">Decimal</span></span> | <span data-ttu-id="48aa5-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="48aa5-112">Hexadecimal</span></span> | <span data-ttu-id="48aa5-113">Constante</span><span class="sxs-lookup"><span data-stu-id="48aa5-113">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="48aa5-114">5242288</span><span class="sxs-lookup"><span data-stu-id="48aa5-114">5242288</span></span> | <span data-ttu-id="48aa5-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="48aa5-115">0x00080000</span></span>  | <span data-ttu-id="48aa5-116">**msidbControlAttributesIcon**</span><span class="sxs-lookup"><span data-stu-id="48aa5-116">**msidbControlAttributesIcon**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="48aa5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48aa5-117">Remarks</span></span>

<span data-ttu-id="48aa5-118">Para establecer este atributo en un control, incluya los bits de icono en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="48aa5-118">To set this attribute on a control, include the Icon bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="48aa5-119">La columna de texto de la tabla de control se usa como clave externa de la [tabla binaria](binary-table.md), por lo que el control no puede contener una imagen de icono y texto.</span><span class="sxs-lookup"><span data-stu-id="48aa5-119">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="48aa5-120">No establezca los bits de icono y de [mapa](bitmap-control-attribute.md) de bits.</span><span class="sxs-lookup"><span data-stu-id="48aa5-120">Do not set both the Icon and [Bitmap](bitmap-control-attribute.md) bits.</span></span>

<span data-ttu-id="48aa5-121">Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="48aa5-121">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



