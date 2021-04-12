---
title: Elemento de la subvista
description: Elemento de la subvista
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Aspectos de Windows Media Player, elemento de subvista
- máscaras, elemento de subvista
- Elemento de la subvista
- referencia de máscaras, elemento de subvista
- elementos, subvistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357568"
---
# <a name="subview-element"></a><span data-ttu-id="f656c-108">Elemento de la subvista</span><span class="sxs-lookup"><span data-stu-id="f656c-108">SUBVIEW Element</span></span>

<span data-ttu-id="f656c-109">El elemento de la **subvista** proporciona una manera de manipular una parte de una máscara, por ejemplo, para proporcionar un panel de control que se puede ocultar cuando no se está utilizando.</span><span class="sxs-lookup"><span data-stu-id="f656c-109">The **SUBVIEW** element provides a way to manipulate a portion of a skin, for example, to provide a control panel that can be hidden when it is not being used.</span></span> <span data-ttu-id="f656c-110">Los elementos de la **vista** secundaria siempre son elementos secundarios de los elementos de la **vista** primaria y pueden contener otros elementos de máscara, excepto **Ver**, **tema** y **otros elementos de la vista secundaria** .</span><span class="sxs-lookup"><span data-stu-id="f656c-110">**SUBVIEW** elements are always children of parent **VIEW** elements, and can contain other skin element except for **VIEW**, **THEME**, and other **SUBVIEW** elements.</span></span>

<span data-ttu-id="f656c-111">El elemento de la **subvista** admite los atributos siguientes, que se definen bajo el elemento de **vista** .</span><span class="sxs-lookup"><span data-stu-id="f656c-111">The **SUBVIEW** element supports the following attributes, which are defined under the **VIEW** element.</span></span>



| <span data-ttu-id="f656c-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="f656c-112">Attribute</span></span>                                                       | <span data-ttu-id="f656c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f656c-113">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f656c-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f656c-114">backgroundColor</span></span>](view-backgroundcolor.md)                     | <span data-ttu-id="f656c-115">Especifica o recupera el color de fondo del control de la **subvista** .</span><span class="sxs-lookup"><span data-stu-id="f656c-115">Specifies or retrieves the background color of the **SUBVIEW** control.</span></span> <span data-ttu-id="f656c-116">El valor predeterminado es "none".</span><span class="sxs-lookup"><span data-stu-id="f656c-116">The default value is "none".</span></span>        |
| [<span data-ttu-id="f656c-117">backgroundImage</span><span class="sxs-lookup"><span data-stu-id="f656c-117">backgroundImage</span></span>](view-backgroundimage.md)                     | <span data-ttu-id="f656c-118">Especifica o recupera la imagen de fondo del control de **subvista** .</span><span class="sxs-lookup"><span data-stu-id="f656c-118">Specifies or retrieves the background image of the **SUBVIEW** control.</span></span>                                     |
| [<span data-ttu-id="f656c-119">backgroundImageHueShift</span><span class="sxs-lookup"><span data-stu-id="f656c-119">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="f656c-120">Especifica o recupera la cantidad por la que se desplaza el matiz de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="f656c-120">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                      |
| [<span data-ttu-id="f656c-121">backgroundImageSaturation</span><span class="sxs-lookup"><span data-stu-id="f656c-121">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="f656c-122">Especifica o recupera el valor de saturación de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="f656c-122">Specifies or retrieves the saturation value of the background image.</span></span>                                        |
| [<span data-ttu-id="f656c-123">backgroundTiled</span><span class="sxs-lookup"><span data-stu-id="f656c-123">backgroundTiled</span></span>](view-backgroundtiled.md)                     | <span data-ttu-id="f656c-124">Especifica o recupera un valor que indica si la imagen de fondo del control de **subvista** está en mosaico.</span><span class="sxs-lookup"><span data-stu-id="f656c-124">Specifies or retrieves a value indicating whether the background image of the **SUBVIEW** control is tiled.</span></span> |
| [<span data-ttu-id="f656c-125">resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="f656c-125">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="f656c-126">Especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="f656c-126">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                      |
| [<span data-ttu-id="f656c-127">Property</span><span class="sxs-lookup"><span data-stu-id="f656c-127">transparencyColor</span></span>](view-transparencycolor.md)                 | <span data-ttu-id="f656c-128">Especifica o recupera el color de transparencia de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="f656c-128">Specifies or retrieves the transparency color of the background image.</span></span>                                      |



 

<span data-ttu-id="f656c-129">El elemento de la **subvista** admite los atributos de ambiente, excepto donde se indique.</span><span class="sxs-lookup"><span data-stu-id="f656c-129">The **SUBVIEW** element supports the ambient attributes, except where noted.</span></span> <span data-ttu-id="f656c-130">Para obtener más información, consulte [atributos de ambiente](ambient-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="f656c-130">For more information, see [Ambient Attributes](ambient-attributes.md).</span></span>

<span data-ttu-id="f656c-131">El elemento de la **subvista** puede implementar los controladores de eventos ambiente siguientes: [onendmove](onendmove.md) y [OnResize](onresize.md).</span><span class="sxs-lookup"><span data-stu-id="f656c-131">The **SUBVIEW** element can implement the following ambient event handlers: [onendmove](onendmove.md) and [onresize](onresize.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f656c-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f656c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f656c-133">**Referencia de programación de máscara**</span><span class="sxs-lookup"><span data-stu-id="f656c-133">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="f656c-134">**Elemento de vista**</span><span class="sxs-lookup"><span data-stu-id="f656c-134">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 




