---
title: AmbientAttributes.clippingColor
description: El atributo clippingColor especifica o recupera el color que se va a recortar del mapa de bits clippingImage.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- AmbientAttributes. clippingColor Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700067"
---
# <a name="ambientattributesclippingcolor"></a><span data-ttu-id="25925-104">AmbientAttributes.clippingColor</span><span class="sxs-lookup"><span data-stu-id="25925-104">AmbientAttributes.clippingColor</span></span>

<span data-ttu-id="25925-105">El atributo **clippingColor** especifica o recupera el color que se va a recortar del mapa de bits **clippingImage** .</span><span class="sxs-lookup"><span data-stu-id="25925-105">The **clippingColor** attribute specifies or retrieves the color to clip out from the **clippingImage** bitmap.</span></span>

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a><span data-ttu-id="25925-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="25925-106">Possible Values</span></span>

<span data-ttu-id="25925-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="25925-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="25925-108">Value</span><span class="sxs-lookup"><span data-stu-id="25925-108">Value</span></span>                                       | <span data-ttu-id="25925-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="25925-109">Description</span></span>                                       |
|---------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="25925-110">Automático</span><span class="sxs-lookup"><span data-stu-id="25925-110">Auto</span></span>                                        | <span data-ttu-id="25925-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="25925-111">Default.</span></span> <span data-ttu-id="25925-112">Se utiliza el color en la ubicación de píxel 0, 0.</span><span class="sxs-lookup"><span data-stu-id="25925-112">The color at pixel location 0,0 is used.</span></span> |
| <span data-ttu-id="25925-113">cualquier valor de color de Microsoft Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="25925-113">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="25925-114">Se utiliza el color especificado de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="25925-114">The specified Internet Explorer color is used.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="25925-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25925-115">Remarks</span></span>

<span data-ttu-id="25925-116">El color de recorte indica las regiones del **clippingImage** (o la **BackgroundImage** para la **vista** o la **subvista**) que corresponden a partes transparentes y no en las que se pueda hacer clic en el control.</span><span class="sxs-lookup"><span data-stu-id="25925-116">The clipping color indicates the regions of the **clippingImage** (or **backgroundImage** for **VIEW** or **SUBVIEW**) that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="25925-117">El color de recorte puede indicar varias regiones que se van a recortar. Se emite una advertencia si el **clippingImage** es un jpg para advertir de la pérdida de color en jpgs.</span><span class="sxs-lookup"><span data-stu-id="25925-117">The clipping color can indicate multiple regions to be clipped out. A warning is issued if the **clippingImage** is a JPG to warn of loss of color in JPGs.</span></span>

<span data-ttu-id="25925-118">El elemento de **lista de reproducción** no admite el atributo **clippingColor** .</span><span class="sxs-lookup"><span data-stu-id="25925-118">The **clippingColor** attribute is not supported by the **PLAYLIST** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="25925-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25925-119">Requirements</span></span>



| <span data-ttu-id="25925-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="25925-120">Requirement</span></span> | <span data-ttu-id="25925-121">Value</span><span class="sxs-lookup"><span data-stu-id="25925-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="25925-122">Versión</span><span class="sxs-lookup"><span data-stu-id="25925-122">Version</span></span><br/> | <span data-ttu-id="25925-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="25925-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25925-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="25925-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25925-125">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="25925-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="25925-126">**AmbientAttributes.clippingImage**</span><span class="sxs-lookup"><span data-stu-id="25925-126">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> <dt>

[<span data-ttu-id="25925-127">**Referencia de color**</span><span class="sxs-lookup"><span data-stu-id="25925-127">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





