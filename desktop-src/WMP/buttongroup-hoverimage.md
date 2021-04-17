---
title: BUTTONGROUP.hoverImage
description: El atributo hoverImage especifica o recupera el nombre de la imagen que representa el estado de desplazamiento de un botón en el BUTTONGROUP. El estado de desplazamiento se produce cuando el botón está en el estado up y el usuario mantiene el mouse sobre él.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- BUTTONGROUP. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702a7aa73f5800628fdf14deb0dbfe142cd80dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698500"
---
# <a name="buttongrouphoverimage"></a><span data-ttu-id="da8d8-105">BUTTONGROUP.hoverImage</span><span class="sxs-lookup"><span data-stu-id="da8d8-105">BUTTONGROUP.hoverImage</span></span>

<span data-ttu-id="da8d8-106">El atributo **hoverImage** especifica o recupera el nombre de la imagen que representa el estado de desplazamiento de un botón en el **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="da8d8-106">The **hoverImage** attribute specifies or retrieves the name of the image representing the hover state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="da8d8-107">El estado de desplazamiento se produce cuando el botón está en el estado up y el usuario mantiene el mouse sobre él.</span><span class="sxs-lookup"><span data-stu-id="da8d8-107">The hover state occurs when the button is in the up state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="da8d8-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="da8d8-108">Possible Values</span></span>

<span data-ttu-id="da8d8-109">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="da8d8-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="da8d8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da8d8-110">Remarks</span></span>

<span data-ttu-id="da8d8-111">Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.</span><span class="sxs-lookup"><span data-stu-id="da8d8-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="da8d8-112">Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente con los atributos **hueShift** y **saturación** .</span><span class="sxs-lookup"><span data-stu-id="da8d8-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="da8d8-113">La imagen predeterminada es la especificada en el atributo de **imagen** o su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="da8d8-113">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="da8d8-114">Si la imagen de mantener el mouse es mayor que la región definida, se recortará la imagen de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="da8d8-114">If the hover image is larger than the defined region, the hover image will be cropped.</span></span>

<span data-ttu-id="da8d8-115">Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).</span><span class="sxs-lookup"><span data-stu-id="da8d8-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="da8d8-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="da8d8-116">Examples</span></span>

<span data-ttu-id="da8d8-117">Vea *BUTTONELEMENT*. atributo [mappingColor](buttonelement-mappingcolor.md) para un ejemplo que ilustra el uso de este atributo.</span><span class="sxs-lookup"><span data-stu-id="da8d8-117">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="da8d8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da8d8-118">Requirements</span></span>



| <span data-ttu-id="da8d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="da8d8-119">Requirement</span></span> | <span data-ttu-id="da8d8-120">Value</span><span class="sxs-lookup"><span data-stu-id="da8d8-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="da8d8-121">Versión</span><span class="sxs-lookup"><span data-stu-id="da8d8-121">Version</span></span><br/> | <span data-ttu-id="da8d8-122">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="da8d8-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da8d8-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="da8d8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da8d8-124">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="da8d8-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="da8d8-125">**BUTTONGROUP.hueShift**</span><span class="sxs-lookup"><span data-stu-id="da8d8-125">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="da8d8-126">**BUTTONGROUP. Image**</span><span class="sxs-lookup"><span data-stu-id="da8d8-126">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="da8d8-127">**BUTTONGROUP. saturación**</span><span class="sxs-lookup"><span data-stu-id="da8d8-127">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





