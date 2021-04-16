---
title: BUTTON. hoverImage
description: El atributo hoverImage especifica o recupera la imagen que se muestra cuando el botón está en el estado up y el usuario mantiene el puntero del mouse sobre ella.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- BUTTON. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699328"
---
# <a name="buttonhoverimage"></a><span data-ttu-id="46da2-104">BUTTON. hoverImage</span><span class="sxs-lookup"><span data-stu-id="46da2-104">BUTTON.hoverImage</span></span>

<span data-ttu-id="46da2-105">El atributo **hoverImage** especifica o recupera la imagen que se muestra cuando el **botón** está en el estado up y el usuario mantiene el puntero del mouse sobre ella.</span><span class="sxs-lookup"><span data-stu-id="46da2-105">The **hoverImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the up state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="46da2-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="46da2-106">Possible Values</span></span>

<span data-ttu-id="46da2-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="46da2-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="46da2-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46da2-108">Remarks</span></span>

<span data-ttu-id="46da2-109">Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.</span><span class="sxs-lookup"><span data-stu-id="46da2-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="46da2-110">La imagen predeterminada es la especificada en el atributo de **imagen** o su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="46da2-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="46da2-111">Si la imagen de mantener el mouse es mayor que la región definida en el atributo ambiente, se recortará la imagen de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="46da2-111">If the hover image is larger than the defined region in the ambient attribute, the hover image will be cropped.</span></span>

<span data-ttu-id="46da2-112">Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).</span><span class="sxs-lookup"><span data-stu-id="46da2-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="46da2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46da2-113">Requirements</span></span>



| <span data-ttu-id="46da2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="46da2-114">Requirement</span></span> | <span data-ttu-id="46da2-115">Value</span><span class="sxs-lookup"><span data-stu-id="46da2-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="46da2-116">Versión</span><span class="sxs-lookup"><span data-stu-id="46da2-116">Version</span></span><br/> | <span data-ttu-id="46da2-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="46da2-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46da2-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="46da2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46da2-119">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="46da2-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="46da2-120">**BOTÓN. imagen**</span><span class="sxs-lookup"><span data-stu-id="46da2-120">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





