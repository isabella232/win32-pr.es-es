---
description: Si se establece el bit de control FixedSize, la imagen se recorta o se centra en el control sin cambiar su forma o tamaño.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Atributo de control FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809506"
---
# <a name="fixedsize-control-attribute"></a><span data-ttu-id="eef94-103">Atributo de control FixedSize</span><span class="sxs-lookup"><span data-stu-id="eef94-103">FixedSize Control Attribute</span></span>

<span data-ttu-id="eef94-104">Si se establece el bit de control FixedSize, la imagen se recorta o se centra en el control sin cambiar su forma o tamaño.</span><span class="sxs-lookup"><span data-stu-id="eef94-104">If the FixedSize Control bit is set, the picture is cropped or centered in the control without changing its shape or size.</span></span>

<span data-ttu-id="eef94-105">Si no se establece este bit, la imagen se ajusta para ajustarse al control.</span><span class="sxs-lookup"><span data-stu-id="eef94-105">If this bit is not set the picture is stretched to fit the control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="eef94-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="eef94-106">Valid Controls</span></span>

[<span data-ttu-id="eef94-107">Bitmap</span><span class="sxs-lookup"><span data-stu-id="eef94-107">Bitmap</span></span>](bitmap-control.md)

[<span data-ttu-id="eef94-108">CheckBox</span><span class="sxs-lookup"><span data-stu-id="eef94-108">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="eef94-109">Icono</span><span class="sxs-lookup"><span data-stu-id="eef94-109">Icon</span></span>](icon-control.md)

[<span data-ttu-id="eef94-110">Botones</span><span class="sxs-lookup"><span data-stu-id="eef94-110">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="eef94-111">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="eef94-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="eef94-112">Value</span><span class="sxs-lookup"><span data-stu-id="eef94-112">Value</span></span>



| <span data-ttu-id="eef94-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="eef94-113">Decimal</span></span> | <span data-ttu-id="eef94-114">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="eef94-114">Hexadecimal</span></span> | <span data-ttu-id="eef94-115">Constante</span><span class="sxs-lookup"><span data-stu-id="eef94-115">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="eef94-116">1 048 576</span><span class="sxs-lookup"><span data-stu-id="eef94-116">1048576</span></span> | <span data-ttu-id="eef94-117">0x00100000</span><span class="sxs-lookup"><span data-stu-id="eef94-117">0x00100000</span></span>  | <span data-ttu-id="eef94-118">**msidbControlAttributesFixedSize**</span><span class="sxs-lookup"><span data-stu-id="eef94-118">**msidbControlAttributesFixedSize**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="eef94-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eef94-119">Remarks</span></span>

<span data-ttu-id="eef94-120">Para establecer este atributo en un control, incluya el bit FixedSize en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="eef94-120">To set this attribute on a control, include the FixedSize bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="eef94-121">Establecer el bit FixedSize no tiene ningún efecto en [CheckBox](checkbox-control.md), [Pushbutton](pushbutton-control.md)o [RadioButtonGroup](radiobuttongroup-control.md) si no se ha establecido el [mapa](bitmap-control-attribute.md) de bits o el [icono](icon-control-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="eef94-121">Setting the FixedSize bit has no effect on a [CheckBox](checkbox-control.md), [PushButton](pushbutton-control.md), or [RadioButtonGroup](radiobuttongroup-control.md) if neither the [Bitmap](bitmap-control-attribute.md) or the [Icon](icon-control-attribute.md) have been set.</span></span>

<span data-ttu-id="eef94-122">Establecer el bit FixedSize no tiene ningún efecto en un control de icono o un botón de opción asociado a un icono si no se establece el valor de los [iconos](iconsize-control-attribute.md) de los bits.</span><span class="sxs-lookup"><span data-stu-id="eef94-122">Setting the FixedSize bit has no effect on an Icon control, or a PushButton associated with an icon, if the [IconSize](iconsize-control-attribute.md) bits is not set.</span></span>

<span data-ttu-id="eef94-123">Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="eef94-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



