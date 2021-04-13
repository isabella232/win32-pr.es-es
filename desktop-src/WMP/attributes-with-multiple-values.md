---
title: Atributos con varios valores (SDK de Windows Media Player)
description: Atributos con varios valores
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player, atributos para elementos multimedia
- Modelo de objetos de Windows Media Player, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Windows Media Player Mobile, atributos para elementos multimedia
- Control ActiveX de Windows Media Player, atributos para elementos multimedia
- Control ActiveX móvil de Windows Media Player, atributos para elementos multimedia
- Control ActiveX, atributos para elementos multimedia
- Biblioteca de Media Player de Windows, atributos para elementos multimedia
- Biblioteca, atributos para elementos multimedia
- atributos, varios valores
- varios valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad93c4025d09a234b1834a32e4ca3789bcaa4a35
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421843"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a><span data-ttu-id="6e4f0-114">Atributos con varios valores (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="6e4f0-114">Attributes with Multiple Values (Windows Media Player SDK)</span></span>

<span data-ttu-id="6e4f0-115">Algunos atributos de elemento multimedia pueden tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-115">Some media item attributes can have multiple values.</span></span> <span data-ttu-id="6e4f0-116">Por ejemplo, los atributos **Author**, **WM/Composer** y **WM/Genre** pueden tener más de un valor.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-116">For example, the **Author**, **WM/Composer**, and **WM/Genre** attributes can each have more than one value.</span></span> <span data-ttu-id="6e4f0-117">El tipo de datos de estos atributos es **una cadena multivalor**.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-117">The data type of such attributes is **multi-valued string**.</span></span>

<span data-ttu-id="6e4f0-118">En Windows Media Player, la biblioteca muestra varios valores en un único campo, separando los valores con puntos y comas.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-118">In Windows Media Player, the library displays multiple values in a single field, separating the values with semicolons.</span></span> <span data-ttu-id="6e4f0-119">Sin embargo, cada valor es en realidad un atributo independiente en el elemento de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-119">However, each value is actually a separate attribute in the Windows Media item.</span></span>

<span data-ttu-id="6e4f0-120">Puede escribir código que determine si un atributo determinado tiene varios valores y, a continuación, recupere todos esos valores.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-120">You can write code that will determine whether a given attribute has multiple values and then retrieve all of those values.</span></span> <span data-ttu-id="6e4f0-121">Debe usar *medios*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-121">You must use *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="6e4f0-122">Si utiliza los *medios*. método **getItemInfo** para recuperar un atributo con varios valores, solo se recuperará el primer valor.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-122">If you use the *Media*.**getItemInfo** method to retrieve a multi-valued attribute, you will only retrieve the first value.</span></span>

<span data-ttu-id="6e4f0-123">En el ejemplo final del tema [leer valores de atributo](reading-attribute-values.md) se muestra el uso de los *medios*. **getAttributeCountByType** y *multimedia*. métodos **getItemInfoByType** para recuperar varios valores para un atributo determinado.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-123">The final example in the [Reading Attribute Values](reading-attribute-values.md) topic demonstrates the use of the *Media*.**getAttributeCountByType** and *Media*.**getItemInfoByType** methods to retrieve multiple values for a given attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e4f0-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e4f0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e4f0-125">**Atributos de elemento multimedia**</span><span class="sxs-lookup"><span data-stu-id="6e4f0-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="6e4f0-126">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="6e4f0-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="6e4f0-127">**Leer valores de atributo de un CD o DVD**</span><span class="sxs-lookup"><span data-stu-id="6e4f0-127">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




