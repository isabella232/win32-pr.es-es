---
title: BUTTONGROUP.downImage
description: El atributo downImage especifica o recupera el nombre de la imagen que representa el estado de inactividad de BUTTONGROUP.
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- BUTTONGROUP. downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b8a1d5bc2f4c68894a3bba1ad8ce9f2b3aa28a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699621"
---
# <a name="buttongroupdownimage"></a><span data-ttu-id="8781e-104">BUTTONGROUP.downImage</span><span class="sxs-lookup"><span data-stu-id="8781e-104">BUTTONGROUP.downImage</span></span>

<span data-ttu-id="8781e-105">El atributo **downImage** especifica o recupera el nombre de la imagen que representa el estado de inactividad de **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="8781e-105">The **downImage** attribute specifies or retrieves the name of the image representing the down state of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="8781e-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="8781e-106">Possible Values</span></span>

<span data-ttu-id="8781e-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="8781e-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8781e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8781e-108">Remarks</span></span>

<span data-ttu-id="8781e-109">Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.</span><span class="sxs-lookup"><span data-stu-id="8781e-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="8781e-110">Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente con los atributos **hueShift** y **saturación** .</span><span class="sxs-lookup"><span data-stu-id="8781e-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="8781e-111">La imagen predeterminada es la especificada en el atributo de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="8781e-111">The default image is the one specified in the **image** attribute.</span></span>

<span data-ttu-id="8781e-112">Si la imagen hacia abajo es mayor que la región definida, se recortará la imagen hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="8781e-112">If the down image is larger than the defined region, the down image will be cropped.</span></span>

<span data-ttu-id="8781e-113">Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).</span><span class="sxs-lookup"><span data-stu-id="8781e-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8781e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8781e-114">Requirements</span></span>



| <span data-ttu-id="8781e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8781e-115">Requirement</span></span> | <span data-ttu-id="8781e-116">Value</span><span class="sxs-lookup"><span data-stu-id="8781e-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8781e-117">Versión</span><span class="sxs-lookup"><span data-stu-id="8781e-117">Version</span></span><br/> | <span data-ttu-id="8781e-118">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8781e-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8781e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="8781e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8781e-120">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="8781e-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="8781e-121">**BUTTONGROUP.hueShift**</span><span class="sxs-lookup"><span data-stu-id="8781e-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="8781e-122">**BUTTONGROUP. Image**</span><span class="sxs-lookup"><span data-stu-id="8781e-122">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="8781e-123">**BUTTONGROUP. saturación**</span><span class="sxs-lookup"><span data-stu-id="8781e-123">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





