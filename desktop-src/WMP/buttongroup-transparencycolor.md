---
title: BUTTONGROUP. transparencyColor
description: El atributo transparencyColor especifica o recupera el color transparente de las imágenes BUTTONGROUP.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- BUTTONGROUP. transparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699516"
---
# <a name="buttongrouptransparencycolor"></a><span data-ttu-id="bc984-104">BUTTONGROUP. transparencyColor</span><span class="sxs-lookup"><span data-stu-id="bc984-104">BUTTONGROUP.transparencyColor</span></span>

<span data-ttu-id="bc984-105">El atributo **transparencyColor** especifica o recupera el color transparente de las imágenes **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="bc984-105">The **transparencyColor** attribute specifies or retrieves the transparent color of the **BUTTONGROUP** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="bc984-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="bc984-106">Possible Values</span></span>

<span data-ttu-id="bc984-107">Este atributo es una **cadena** de lectura y escritura sin valores predeterminados, que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bc984-107">This attribute is a read/write **String** with no default, containing one of the following values.</span></span>



| <span data-ttu-id="bc984-108">Value</span><span class="sxs-lookup"><span data-stu-id="bc984-108">Value</span></span>                                       | <span data-ttu-id="bc984-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc984-109">Description</span></span>                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc984-110">Automático</span><span class="sxs-lookup"><span data-stu-id="bc984-110">Auto</span></span>                                        | <span data-ttu-id="bc984-111">El píxel de la ubicación 0, 0 en la imagen se convierte en el color transparente.</span><span class="sxs-lookup"><span data-stu-id="bc984-111">The pixel at location 0,0 in the image becomes the transparent color.</span></span>                              |
| <span data-ttu-id="bc984-112">cualquier valor de color de Microsoft Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="bc984-112">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="bc984-113">Un valor de color de Internet Explorer se convierte en el color transparente (por ejemplo, "red" o " \# FF0000").</span><span class="sxs-lookup"><span data-stu-id="bc984-113">An Internet Explorer color value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="bc984-114">None</span><span class="sxs-lookup"><span data-stu-id="bc984-114">None</span></span>                                        | <span data-ttu-id="bc984-115">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bc984-115">Default.</span></span> <span data-ttu-id="bc984-116">Sin transparencia.</span><span class="sxs-lookup"><span data-stu-id="bc984-116">No transparency.</span></span>                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="bc984-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc984-117">Remarks</span></span>

<span data-ttu-id="bc984-118">Un color transparente en una imagen permitirá todo lo que haya detrás de la imagen para que se muestre a través de las áreas de transparencia.</span><span class="sxs-lookup"><span data-stu-id="bc984-118">A transparent color in an image will allow whatever is behind the image to show through the areas of transparency.</span></span> <span data-ttu-id="bc984-119">La región transparente es seleccionable a menos que se recorte por la etiqueta **clippingImage** .</span><span class="sxs-lookup"><span data-stu-id="bc984-119">The transparent region is clickable unless clipped by the **clippingImage** tag.</span></span>

<span data-ttu-id="bc984-120">El color puede ser cualquier valor de color de Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bc984-120">The color can be any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="bc984-121">Si el valor es auto, se usa el color del píxel de la ubicación 0, 0 de la imagen.</span><span class="sxs-lookup"><span data-stu-id="bc984-121">If the value is Auto, then the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="bc984-122">Si el color especificado no es uno de los colores válidos de Internet Explorer, se devuelve una advertencia y se mantiene el valor anterior.</span><span class="sxs-lookup"><span data-stu-id="bc984-122">If the color specified is not one of the valid Internet Explorer colors, a warning is returned and the previous value is maintained.</span></span>

<span data-ttu-id="bc984-123">Dado que los JPGs se pierden y, por lo tanto, están sujetos a cambios de color inesperados, no se recomiendan cuando se usa **transparencyColor** .</span><span class="sxs-lookup"><span data-stu-id="bc984-123">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc984-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc984-124">Requirements</span></span>



| <span data-ttu-id="bc984-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc984-125">Requirement</span></span> | <span data-ttu-id="bc984-126">Value</span><span class="sxs-lookup"><span data-stu-id="bc984-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bc984-127">Versión</span><span class="sxs-lookup"><span data-stu-id="bc984-127">Version</span></span><br/> | <span data-ttu-id="bc984-128">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="bc984-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc984-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc984-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc984-130">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="bc984-130">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="bc984-131">**Referencia de color**</span><span class="sxs-lookup"><span data-stu-id="bc984-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





