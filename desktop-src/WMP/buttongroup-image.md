---
title: BUTTONGROUP. Image
description: El atributo Image especifica o recupera el nombre de la imagen que representa los botones de un BUTTONGROUP.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- Media Player BUTTONGROUP. Image de Windows
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa395edc149671ad05a38a5ff7c77053b6e3d82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700191"
---
# <a name="buttongroupimage"></a><span data-ttu-id="6c6ba-104">BUTTONGROUP. Image</span><span class="sxs-lookup"><span data-stu-id="6c6ba-104">BUTTONGROUP.image</span></span>

<span data-ttu-id="6c6ba-105">El atributo **Image** especifica o recupera el nombre de la imagen que representa los botones de un **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="6c6ba-105">The **image** attribute specifies or retrieves the name of the image representing the buttons of a **BUTTONGROUP**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="6c6ba-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="6c6ba-106">Possible Values</span></span>

<span data-ttu-id="6c6ba-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="6c6ba-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c6ba-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c6ba-108">Remarks</span></span>

<span data-ttu-id="6c6ba-109">Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.</span><span class="sxs-lookup"><span data-stu-id="6c6ba-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="6c6ba-110">Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente con los atributos **hueShift** y **saturación** .</span><span class="sxs-lookup"><span data-stu-id="6c6ba-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="6c6ba-111">Si la imagen del control es mayor que la región definida, se recortará la imagen.</span><span class="sxs-lookup"><span data-stu-id="6c6ba-111">If the image of the control is larger than the defined region, the image will be cropped.</span></span>

<span data-ttu-id="6c6ba-112">Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).</span><span class="sxs-lookup"><span data-stu-id="6c6ba-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6ba-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c6ba-113">Requirements</span></span>



| <span data-ttu-id="6c6ba-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c6ba-114">Requirement</span></span> | <span data-ttu-id="6c6ba-115">Value</span><span class="sxs-lookup"><span data-stu-id="6c6ba-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6c6ba-116">Versión</span><span class="sxs-lookup"><span data-stu-id="6c6ba-116">Version</span></span><br/> | <span data-ttu-id="6c6ba-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="6c6ba-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c6ba-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c6ba-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6ba-119">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="6c6ba-119">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="6c6ba-120">**BUTTONGROUP.hueShift**</span><span class="sxs-lookup"><span data-stu-id="6c6ba-120">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="6c6ba-121">**BUTTONGROUP. saturación**</span><span class="sxs-lookup"><span data-stu-id="6c6ba-121">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





