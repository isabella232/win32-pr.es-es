---
title: BUTTONGROUP.disabledImage
description: El atributo disabledImage especifica o recupera el nombre de la imagen que representa el Estado deshabilitado de los botones en el BUTTONGROUP.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- BUTTONGROUP. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698683"
---
# <a name="buttongroupdisabledimage"></a><span data-ttu-id="147bc-104">BUTTONGROUP.disabledImage</span><span class="sxs-lookup"><span data-stu-id="147bc-104">BUTTONGROUP.disabledImage</span></span>

<span data-ttu-id="147bc-105">El atributo **disabledImage** especifica o recupera el nombre de la imagen que representa el Estado deshabilitado de los botones en el **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="147bc-105">The **disabledImage** attribute specifies or retrieves the name of the image representing the disabled state of the buttons in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="147bc-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="147bc-106">Possible Values</span></span>

<span data-ttu-id="147bc-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="147bc-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="147bc-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="147bc-108">Remarks</span></span>

<span data-ttu-id="147bc-109">Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.</span><span class="sxs-lookup"><span data-stu-id="147bc-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="147bc-110">Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente con los atributos **hueShift** y **saturación** .</span><span class="sxs-lookup"><span data-stu-id="147bc-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="147bc-111">Cuando el atributo **Disabled** de un elemento **BUTTONELEMENT** está establecido en true, se muestra la región correspondiente de **disabledImage** para **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="147bc-111">When the **disabled** attribute of a **BUTTONELEMENT** element is set to true, the corresponding region of the **disabledImage** for the **BUTTONGROUP** is displayed.</span></span> <span data-ttu-id="147bc-112">Si la imagen deshabilitada es mayor que la región definida, se recortará la imagen deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="147bc-112">If the disabled image is larger than the defined region, the disabled image will be cropped.</span></span>

<span data-ttu-id="147bc-113">Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).</span><span class="sxs-lookup"><span data-stu-id="147bc-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="147bc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="147bc-114">Requirements</span></span>



| <span data-ttu-id="147bc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="147bc-115">Requirement</span></span> | <span data-ttu-id="147bc-116">Value</span><span class="sxs-lookup"><span data-stu-id="147bc-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="147bc-117">Versión</span><span class="sxs-lookup"><span data-stu-id="147bc-117">Version</span></span><br/> | <span data-ttu-id="147bc-118">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="147bc-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="147bc-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="147bc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="147bc-120">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="147bc-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="147bc-121">**BUTTONGROUP.hueShift**</span><span class="sxs-lookup"><span data-stu-id="147bc-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="147bc-122">**BUTTONGROUP. saturación**</span><span class="sxs-lookup"><span data-stu-id="147bc-122">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





