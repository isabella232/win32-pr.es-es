---
title: TEXT. backgroundColor
description: El atributo backgroundColor especifica o recupera el color de fondo del control de texto.
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- TEXT. backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718676"
---
# <a name="textbackgroundcolor"></a><span data-ttu-id="e7cc2-104">TEXT. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="e7cc2-104">TEXT.backgroundColor</span></span>

<span data-ttu-id="e7cc2-105">El atributo **BackgroundColor** especifica o recupera el color de fondo del control de texto.</span><span class="sxs-lookup"><span data-stu-id="e7cc2-105">The **backgroundColor** attribute specifies or retrieves the background color for the Text control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="e7cc2-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="e7cc2-106">Possible Values</span></span>

<span data-ttu-id="e7cc2-107">Este atributo es una **cadena** de lectura/escritura que contiene cualquier valor de color de Microsoft Internet Explorer o el valor "none".</span><span class="sxs-lookup"><span data-stu-id="e7cc2-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value or the value "none".</span></span> <span data-ttu-id="e7cc2-108">Tiene un valor predeterminado de "none", lo que significa que el fondo es transparente.</span><span class="sxs-lookup"><span data-stu-id="e7cc2-108">It has a default value of "none", which means the background is transparent.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7cc2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7cc2-109">Remarks</span></span>

<span data-ttu-id="e7cc2-110">El color de fondo se establece para el alto y ancho del control.</span><span class="sxs-lookup"><span data-stu-id="e7cc2-110">The background color is set for the height and width of the control.</span></span> <span data-ttu-id="e7cc2-111">Si no se establece el alto y el ancho, el color de fondo se establece en el alto y ancho del texto.</span><span class="sxs-lookup"><span data-stu-id="e7cc2-111">If height and width are not set, the background color is set to the height and width of the text.</span></span>

<span data-ttu-id="e7cc2-112">Cuando se usa **alphaBlend** o **alphaBlendTo** con un elemento de **texto** que no tiene el parámetro **BackgroundColor** especificado, se usará un color de fondo negro.</span><span class="sxs-lookup"><span data-stu-id="e7cc2-112">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="e7cc2-113">Si el color de primer plano también es negro (que es el valor predeterminado para el atributo **foregroundColor** ), es posible que el texto sea ilegible.</span><span class="sxs-lookup"><span data-stu-id="e7cc2-113">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="e7cc2-114">Para evitarlo, especifique siempre el atributo **BackgroundColor** o establezca **foregroundColor** en un color distinto de Black.</span><span class="sxs-lookup"><span data-stu-id="e7cc2-114">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

<span data-ttu-id="e7cc2-115">Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="e7cc2-115">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7cc2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7cc2-116">Requirements</span></span>



| <span data-ttu-id="e7cc2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7cc2-117">Requirement</span></span> | <span data-ttu-id="e7cc2-118">Value</span><span class="sxs-lookup"><span data-stu-id="e7cc2-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e7cc2-119">Versión</span><span class="sxs-lookup"><span data-stu-id="e7cc2-119">Version</span></span><br/> | <span data-ttu-id="e7cc2-120">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e7cc2-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7cc2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7cc2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7cc2-122">**AmbientAttributes.alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="e7cc2-122">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="e7cc2-123">**AmbientAttributes.alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="e7cc2-123">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="e7cc2-124">**Referencia de color**</span><span class="sxs-lookup"><span data-stu-id="e7cc2-124">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="e7cc2-125">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="e7cc2-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="e7cc2-126">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="e7cc2-126">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





