---
description: Si se establece el bit de control Bitmap, el texto del control se sustituye por una imagen de mapa de bits. La columna de texto de la tabla de control es una clave externa de la tabla binaria.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Atributo de control Bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bda78231c1689c4c5faebeab98fbf6566c7e667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909054"
---
# <a name="bitmap-control-attribute"></a><span data-ttu-id="11268-104">Atributo de control Bitmap</span><span class="sxs-lookup"><span data-stu-id="11268-104">Bitmap Control Attribute</span></span>

<span data-ttu-id="11268-105">Si se establece el bit de control Bitmap, el texto del control se sustituye por una imagen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="11268-105">If the Bitmap Control bit is set, the text in the control is replaced by a bitmap image.</span></span> <span data-ttu-id="11268-106">La columna de texto de la [tabla de control](control-table.md) es una clave externa de la [tabla binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="11268-106">The Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="11268-107">Si no se establece este bit, el texto del control se especifica en la columna de texto de la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="11268-107">If this bit is not set, the text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="11268-108">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="11268-108">Valid Controls</span></span>

[<span data-ttu-id="11268-109">CheckBox</span><span class="sxs-lookup"><span data-stu-id="11268-109">CheckBox</span></span>](checkbox-control.md)

 

[<span data-ttu-id="11268-110">Botones</span><span class="sxs-lookup"><span data-stu-id="11268-110">PushButton</span></span>](pushbutton-control.md)

 

[<span data-ttu-id="11268-111">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="11268-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="11268-112">Value</span><span class="sxs-lookup"><span data-stu-id="11268-112">Value</span></span>



| <span data-ttu-id="11268-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="11268-113">Decimal</span></span> | <span data-ttu-id="11268-114">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="11268-114">Hexadecimal</span></span> | <span data-ttu-id="11268-115">Constante</span><span class="sxs-lookup"><span data-stu-id="11268-115">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="11268-116">262 144</span><span class="sxs-lookup"><span data-stu-id="11268-116">262144</span></span>  | <span data-ttu-id="11268-117">0x00040000</span><span class="sxs-lookup"><span data-stu-id="11268-117">0x00040000</span></span>  | <span data-ttu-id="11268-118">**msidbControlAttributesBitmap**</span><span class="sxs-lookup"><span data-stu-id="11268-118">**msidbControlAttributesBitmap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="11268-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11268-119">Remarks</span></span>

<span data-ttu-id="11268-120">Para establecer este atributo en un control, incluya el bit de mapa de bits en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="11268-120">To set this attribute on a control, include the Bitmap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="11268-121">La columna de texto de la tabla de control se usa como clave externa de la [tabla binaria](binary-table.md), por lo que el control no puede contener una imagen de icono y texto.</span><span class="sxs-lookup"><span data-stu-id="11268-121">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="11268-122">No establezca los bits de [icono](icon-control-attribute.md) y de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="11268-122">Do not set both the [Icon](icon-control-attribute.md) and Bitmap bits.</span></span>

<span data-ttu-id="11268-123">Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="11268-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



