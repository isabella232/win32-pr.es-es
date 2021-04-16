---
title: TEXT. foregroundColor
description: El atributo foregroundColor especifica o recupera el color del texto del control de texto.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- Media Player de Windows TEXT. foregroundColor
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699360"
---
# <a name="textforegroundcolor"></a><span data-ttu-id="868d7-104">TEXT. foregroundColor</span><span class="sxs-lookup"><span data-stu-id="868d7-104">TEXT.foregroundColor</span></span>

<span data-ttu-id="868d7-105">El atributo **foregroundColor** especifica o recupera el color del texto del control de texto.</span><span class="sxs-lookup"><span data-stu-id="868d7-105">The **foregroundColor** attribute specifies or retrieves the text color for the Text control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="868d7-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="868d7-106">Possible Values</span></span>

<span data-ttu-id="868d7-107">Este atributo es una **cadena** de lectura/escritura que contiene cualquier valor de color de Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="868d7-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="868d7-108">El valor predeterminado es "Black".</span><span class="sxs-lookup"><span data-stu-id="868d7-108">The default value is "black".</span></span>

<span data-ttu-id="868d7-109">Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="868d7-109">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

<span data-ttu-id="868d7-110">Cuando se usa **alphaBlend** o **alphaBlendTo** con un elemento de **texto** que no tiene el parámetro **BackgroundColor** especificado, se usará un color de fondo negro.</span><span class="sxs-lookup"><span data-stu-id="868d7-110">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="868d7-111">Si el color de primer plano también es negro (que es el valor predeterminado para el atributo **foregroundColor** ), es posible que el texto sea ilegible.</span><span class="sxs-lookup"><span data-stu-id="868d7-111">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="868d7-112">Para evitarlo, especifique siempre el atributo **BackgroundColor** o establezca **foregroundColor** en un color distinto de Black.</span><span class="sxs-lookup"><span data-stu-id="868d7-112">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

## <a name="requirements"></a><span data-ttu-id="868d7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="868d7-113">Requirements</span></span>



| <span data-ttu-id="868d7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="868d7-114">Requirement</span></span> | <span data-ttu-id="868d7-115">Value</span><span class="sxs-lookup"><span data-stu-id="868d7-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="868d7-116">Versión</span><span class="sxs-lookup"><span data-stu-id="868d7-116">Version</span></span><br/> | <span data-ttu-id="868d7-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="868d7-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="868d7-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="868d7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868d7-119">**AmbientAttributes.alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="868d7-119">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="868d7-120">**AmbientAttributes.alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="868d7-120">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="868d7-121">**Referencia de color**</span><span class="sxs-lookup"><span data-stu-id="868d7-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="868d7-122">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="868d7-122">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="868d7-123">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="868d7-123">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> </dl>

 

 





