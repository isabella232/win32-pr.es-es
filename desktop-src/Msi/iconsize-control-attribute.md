---
description: Un archivo de icono puede contener varios tamaños diferentes de la misma imagen de icono.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Atributo de control de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082535"
---
# <a name="iconsize-control-attribute"></a><span data-ttu-id="13e73-103">Atributo de control de iconos</span><span class="sxs-lookup"><span data-stu-id="13e73-103">IconSize Control Attribute</span></span>

<span data-ttu-id="13e73-104">Un archivo de icono puede contener varios tamaños diferentes de la misma imagen de icono.</span><span class="sxs-lookup"><span data-stu-id="13e73-104">An icon file can hold several different sizes of the same icon image.</span></span> <span data-ttu-id="13e73-105">Estos bits especifican el tamaño de la imagen del icono que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="13e73-105">These bits specify which size of the icon image to load.</span></span> <span data-ttu-id="13e73-106">Si no se establece ninguno de los bits, se carga la primera imagen.</span><span class="sxs-lookup"><span data-stu-id="13e73-106">If none of the bits are set, the first image is loaded.</span></span> <span data-ttu-id="13e73-107">Si solo se establece **msidbControlAttributesIconSize16** , se carga la primera imagen 16x16.</span><span class="sxs-lookup"><span data-stu-id="13e73-107">If only **msidbControlAttributesIconSize16** is set, the first 16x16 image is loaded.</span></span> <span data-ttu-id="13e73-108">Si solo se establece **msidbControlAttributesIconSize32** , se carga la primera imagen de 32x32.</span><span class="sxs-lookup"><span data-stu-id="13e73-108">If only the **msidbControlAttributesIconSize32** is set, the first 32x32 image is loaded.</span></span> <span data-ttu-id="13e73-109">Si se establece **msidbControlAttributesIconSize48** , se carga la primera imagen 48x48.</span><span class="sxs-lookup"><span data-stu-id="13e73-109">If **msidbControlAttributesIconSize48** is set, the first 48x48 image is loaded.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="13e73-110">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="13e73-110">Valid Controls</span></span>

[<span data-ttu-id="13e73-111">CheckBox</span><span class="sxs-lookup"><span data-stu-id="13e73-111">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="13e73-112">Icono</span><span class="sxs-lookup"><span data-stu-id="13e73-112">Icon</span></span>](icon-control.md)

[<span data-ttu-id="13e73-113">Botones</span><span class="sxs-lookup"><span data-stu-id="13e73-113">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="13e73-114">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="13e73-114">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="13e73-115">Value</span><span class="sxs-lookup"><span data-stu-id="13e73-115">Value</span></span>



| <span data-ttu-id="13e73-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="13e73-116">Decimal</span></span> | <span data-ttu-id="13e73-117">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="13e73-117">Hexadecimal</span></span> | <span data-ttu-id="13e73-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="13e73-118">Description</span></span>                          |
|---------|-------------|--------------------------------------|
| <span data-ttu-id="13e73-119">2 097 152</span><span class="sxs-lookup"><span data-stu-id="13e73-119">2097152</span></span> | <span data-ttu-id="13e73-120">0x00200000</span><span class="sxs-lookup"><span data-stu-id="13e73-120">0x00200000</span></span>  | <span data-ttu-id="13e73-121">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="13e73-121">**msidbControlAttributesIconSize16**</span></span> |
| <span data-ttu-id="13e73-122">4 194 304</span><span class="sxs-lookup"><span data-stu-id="13e73-122">4194304</span></span> | <span data-ttu-id="13e73-123">0x00400000</span><span class="sxs-lookup"><span data-stu-id="13e73-123">0x00400000</span></span>  | <span data-ttu-id="13e73-124">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="13e73-124">**msidbControlAttributesIconSize32**</span></span> |
| <span data-ttu-id="13e73-125">6291456</span><span class="sxs-lookup"><span data-stu-id="13e73-125">6291456</span></span> | <span data-ttu-id="13e73-126">0x00600000</span><span class="sxs-lookup"><span data-stu-id="13e73-126">0x00600000</span></span>  | <span data-ttu-id="13e73-127">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="13e73-127">**msidbControlAttributesIconSize48**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="13e73-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13e73-128">Remarks</span></span>

<span data-ttu-id="13e73-129">Para establecer este atributo en un control, incluya los bits de los iconos en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="13e73-129">To set this attribute on a control, include the IconSize bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="13e73-130">Si no se establece el bit [FixedSize](fixedsize-control-attribute.md) , la imagen cargada se reduce o se ajusta para ajustarse al control de icono.</span><span class="sxs-lookup"><span data-stu-id="13e73-130">If the [FixedSize](fixedsize-control-attribute.md) bit is not set, the loaded image is shrunk or stretched to fit the icon control.</span></span> <span data-ttu-id="13e73-131">Si se establece el bit [FixedSize](fixedsize-control-attribute.md) y la imagen cargada es más pequeña que el control de icono, la imagen se muestra centrada dentro del control.</span><span class="sxs-lookup"><span data-stu-id="13e73-131">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is smaller than the icon control, the picture is displayed centered inside the control.</span></span> <span data-ttu-id="13e73-132">Si se establece el bit [FixedSize](fixedsize-control-attribute.md) y la imagen cargada es mayor que el control de icono, la imagen se reduce para ajustarse al control.</span><span class="sxs-lookup"><span data-stu-id="13e73-132">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is larger than the icon control, the picture is reduced to fit the control.</span></span>

<span data-ttu-id="13e73-133">Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="13e73-133">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



