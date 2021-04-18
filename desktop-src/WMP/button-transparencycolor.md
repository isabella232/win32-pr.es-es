---
title: BUTTON. transparencyColor
description: El atributo transparencyColor especifica o recupera el color que será transparente en las imágenes del botón.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- BUTTON. transparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700262"
---
# <a name="buttontransparencycolor"></a><span data-ttu-id="e2b13-104">BUTTON. transparencyColor</span><span class="sxs-lookup"><span data-stu-id="e2b13-104">BUTTON.transparencyColor</span></span>

<span data-ttu-id="e2b13-105">El atributo **transparencyColor** especifica o recupera el color que será transparente en las imágenes del **botón** .</span><span class="sxs-lookup"><span data-stu-id="e2b13-105">The **transparencyColor** attribute specifies or retrieves the color that will be transparent in the **BUTTON** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="e2b13-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="e2b13-106">Possible Values</span></span>

<span data-ttu-id="e2b13-107">Este atributo es una **cadena** de lectura/escritura sin valor predeterminado que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e2b13-107">This attribute is a read/write **String** with no default containing one of the following values.</span></span>



| <span data-ttu-id="e2b13-108">Value</span><span class="sxs-lookup"><span data-stu-id="e2b13-108">Value</span></span>                                    | <span data-ttu-id="e2b13-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2b13-109">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b13-110">Automático</span><span class="sxs-lookup"><span data-stu-id="e2b13-110">Auto</span></span>                                     | <span data-ttu-id="e2b13-111">El color del píxel en la ubicación 0, 0 en la imagen se convierte en el color transparente.</span><span class="sxs-lookup"><span data-stu-id="e2b13-111">The color of the pixel at location 0,0 in the image becomes the transparent color.</span></span>                        |
| <span data-ttu-id="e2b13-112">Cualquier valor de formato de color de Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="e2b13-112">Any Internet Explorer color format value</span></span> | <span data-ttu-id="e2b13-113">Un valor de formato de color de Internet Explorer se convierte en el color transparente (por ejemplo, "red" o " \# FF0000").</span><span class="sxs-lookup"><span data-stu-id="e2b13-113">An Internet Explorer color format value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="e2b13-114">None</span><span class="sxs-lookup"><span data-stu-id="e2b13-114">None</span></span>                                     | <span data-ttu-id="e2b13-115">Sin transparencia.</span><span class="sxs-lookup"><span data-stu-id="e2b13-115">No transparency.</span></span>                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="e2b13-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2b13-116">Remarks</span></span>

<span data-ttu-id="e2b13-117">Un color transparente en una imagen permite que el que está detrás de la imagen se muestre a través de las áreas transparentes.</span><span class="sxs-lookup"><span data-stu-id="e2b13-117">A transparent color in an image allows whatever is behind the image to show through the transparent areas.</span></span> <span data-ttu-id="e2b13-118">El **botón** seguirá recibiendo clics en la región transparente.</span><span class="sxs-lookup"><span data-stu-id="e2b13-118">The **BUTTON** will still receive clicks on the transparent region.</span></span>

<span data-ttu-id="e2b13-119">El color transparente puede ser cualquier valor de color de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e2b13-119">The transparent color can be any Internet Explorer color value.</span></span> <span data-ttu-id="e2b13-120">Si el valor del atributo **transparencyColor** se establece en "auto", se usa el color del píxel en la ubicación 0, 0 en la imagen.</span><span class="sxs-lookup"><span data-stu-id="e2b13-120">If the value of the **transparencyColor** attribute is set to "Auto", the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="e2b13-121">Si el color especificado no es ninguno de los colores de IE válidos, se mantiene el valor anterior.</span><span class="sxs-lookup"><span data-stu-id="e2b13-121">If the color specified is not one of the valid IE colors, the previous value is maintained.</span></span>

<span data-ttu-id="e2b13-122">Dado que los JPGs se pierden y, por lo tanto, están sujetos a cambios de color inesperados, no se recomiendan cuando se usa **transparencyColor** .</span><span class="sxs-lookup"><span data-stu-id="e2b13-122">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b13-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2b13-123">Requirements</span></span>



| <span data-ttu-id="e2b13-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2b13-124">Requirement</span></span> | <span data-ttu-id="e2b13-125">Value</span><span class="sxs-lookup"><span data-stu-id="e2b13-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e2b13-126">Versión</span><span class="sxs-lookup"><span data-stu-id="e2b13-126">Version</span></span><br/> | <span data-ttu-id="e2b13-127">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e2b13-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2b13-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2b13-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b13-129">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="e2b13-129">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="e2b13-130">**BOTÓN. imagen**</span><span class="sxs-lookup"><span data-stu-id="e2b13-130">**BUTTON.image**</span></span>](button-image.md)
</dt> <dt>

[<span data-ttu-id="e2b13-131">**Referencia de color**</span><span class="sxs-lookup"><span data-stu-id="e2b13-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





