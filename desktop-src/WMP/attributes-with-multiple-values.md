---
title: Atributos con varios valores (Reproductor de Windows Media SDK)
description: Obtenga información sobre los atributos con varios valores en Reproductor de Windows Media SDK. Algunos atributos de elementos multimedia pueden tener varios valores.
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Reproductor de Windows Media,atributos para elementos multimedia
- Reproductor de Windows Media modelo de objetos, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Reproductor de Windows Media Mobile,attributes for media items
- Reproductor de Windows Media control ActiveX, atributos para elementos multimedia
- Reproductor de Windows Media control ActiveX móvil, atributos para elementos multimedia
- Control ActiveX, atributos para elementos multimedia
- Reproductor de Windows Media biblioteca, atributos para elementos multimedia
- library,attributes para elementos multimedia
- attributes,multiple values
- varios valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16baf4bab47dc972ec7b043980dccb0f2aadd57
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262607"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a><span data-ttu-id="48bf9-115">Atributos con varios valores (Reproductor de Windows Media SDK)</span><span class="sxs-lookup"><span data-stu-id="48bf9-115">Attributes with Multiple Values (Windows Media Player SDK)</span></span>

<span data-ttu-id="48bf9-116">Algunos atributos de elementos multimedia pueden tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="48bf9-116">Some media item attributes can have multiple values.</span></span> <span data-ttu-id="48bf9-117">Por ejemplo, los **atributos Author**, **WM/Composer** y **WM/Genre** pueden tener más de un valor.</span><span class="sxs-lookup"><span data-stu-id="48bf9-117">For example, the **Author**, **WM/Composer**, and **WM/Genre** attributes can each have more than one value.</span></span> <span data-ttu-id="48bf9-118">El tipo de datos de estos atributos es **una cadena de varios valores.**</span><span class="sxs-lookup"><span data-stu-id="48bf9-118">The data type of such attributes is **multi-valued string**.</span></span>

<span data-ttu-id="48bf9-119">En Reproductor de Windows Media, la biblioteca muestra varios valores en un solo campo, separando los valores con punto y coma.</span><span class="sxs-lookup"><span data-stu-id="48bf9-119">In Windows Media Player, the library displays multiple values in a single field, separating the values with semicolons.</span></span> <span data-ttu-id="48bf9-120">Sin embargo, cada valor es realmente un atributo independiente en el elemento de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="48bf9-120">However, each value is actually a separate attribute in the Windows Media item.</span></span>

<span data-ttu-id="48bf9-121">Puede escribir código que determine si un atributo determinado tiene varios valores y, a continuación, recuperar todos esos valores.</span><span class="sxs-lookup"><span data-stu-id="48bf9-121">You can write code that will determine whether a given attribute has multiple values and then retrieve all of those values.</span></span> <span data-ttu-id="48bf9-122">Debe usar *Media*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="48bf9-122">You must use *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="48bf9-123">Si usa media *.* **Método getItemInfo** para recuperar un atributo de varios valores; solo recuperará el primer valor.</span><span class="sxs-lookup"><span data-stu-id="48bf9-123">If you use the *Media*.**getItemInfo** method to retrieve a multi-valued attribute, you will only retrieve the first value.</span></span>

<span data-ttu-id="48bf9-124">En el ejemplo final del tema [Leer valores de atributo](reading-attribute-values.md) se muestra el uso de *media*. **getAttributeCountByType** y *Media*. **Métodos getItemInfoByType** para recuperar varios valores para un atributo determinado.</span><span class="sxs-lookup"><span data-stu-id="48bf9-124">The final example in the [Reading Attribute Values](reading-attribute-values.md) topic demonstrates the use of the *Media*.**getAttributeCountByType** and *Media*.**getItemInfoByType** methods to retrieve multiple values for a given attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48bf9-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="48bf9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48bf9-126">**Atributos de elementos multimedia**</span><span class="sxs-lookup"><span data-stu-id="48bf9-126">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="48bf9-127">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="48bf9-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="48bf9-128">**Lectura de valores de atributo desde un CD o DVD**</span><span class="sxs-lookup"><span data-stu-id="48bf9-128">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




