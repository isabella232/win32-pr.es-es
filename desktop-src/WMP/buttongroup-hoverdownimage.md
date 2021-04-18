---
title: BUTTONGROUP.hoverDownImage
description: El atributo hoverDownImage especifica o recupera el nombre de la imagen que representa el estado de desactivación de un botón en el BUTTONGROUP. El estado de desactivación se produce cuando el botón está en estado inactivo y el usuario mantiene el mouse sobre él.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- BUTTONGROUP. hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698501"
---
# <a name="buttongrouphoverdownimage"></a><span data-ttu-id="207b1-105">BUTTONGROUP.hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="207b1-105">BUTTONGROUP.hoverDownImage</span></span>

<span data-ttu-id="207b1-106">El atributo **hoverDownImage** especifica o recupera el nombre de la imagen que representa el estado de desactivación de un botón en el **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="207b1-106">The **hoverDownImage** attribute specifies or retrieves the name of the image representing the hover-down state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="207b1-107">El estado de desactivación se produce cuando el botón está en estado inactivo y el usuario mantiene el mouse sobre él.</span><span class="sxs-lookup"><span data-stu-id="207b1-107">The hover-down state occurs when the button is in the down state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="207b1-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="207b1-108">Possible Values</span></span>

<span data-ttu-id="207b1-109">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="207b1-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="207b1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="207b1-110">Remarks</span></span>

<span data-ttu-id="207b1-111">Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.</span><span class="sxs-lookup"><span data-stu-id="207b1-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="207b1-112">Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente con los atributos **hueShift** y **saturación** .</span><span class="sxs-lookup"><span data-stu-id="207b1-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="207b1-113">La imagen predeterminada es la especificada en el atributo **downImage** o su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="207b1-113">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="207b1-114">Si la imagen desplegable es más grande que la región definida, se recortará la imagen de la que se mantiene el puntero.</span><span class="sxs-lookup"><span data-stu-id="207b1-114">If the hover-down image is larger than the defined region, the hover-down image will be cropped.</span></span>

<span data-ttu-id="207b1-115">Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).</span><span class="sxs-lookup"><span data-stu-id="207b1-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="207b1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="207b1-116">Requirements</span></span>



| <span data-ttu-id="207b1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="207b1-117">Requirement</span></span> | <span data-ttu-id="207b1-118">Value</span><span class="sxs-lookup"><span data-stu-id="207b1-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="207b1-119">Versión</span><span class="sxs-lookup"><span data-stu-id="207b1-119">Version</span></span><br/> | <span data-ttu-id="207b1-120">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="207b1-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="207b1-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="207b1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="207b1-122">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="207b1-122">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="207b1-123">**BUTTONGROUP.downImage**</span><span class="sxs-lookup"><span data-stu-id="207b1-123">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> <dt>

[<span data-ttu-id="207b1-124">**BUTTONGROUP.hueShift**</span><span class="sxs-lookup"><span data-stu-id="207b1-124">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="207b1-125">**BUTTONGROUP. saturación**</span><span class="sxs-lookup"><span data-stu-id="207b1-125">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





