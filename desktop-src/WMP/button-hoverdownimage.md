---
title: BUTTON. hoverDownImage
description: El atributo hoverDownImage especifica o recupera la imagen que se muestra cuando el botón está inactivo y el usuario mantiene el puntero del mouse sobre ella.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- BUTTON. hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc8221875656c38a35eb6539dce25f58133984f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699330"
---
# <a name="buttonhoverdownimage"></a><span data-ttu-id="f26b8-104">BUTTON. hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="f26b8-104">BUTTON.hoverDownImage</span></span>

<span data-ttu-id="f26b8-105">El atributo **hoverDownImage** especifica o recupera la imagen que se muestra cuando el **botón** está inactivo y el usuario mantiene el puntero del mouse sobre ella.</span><span class="sxs-lookup"><span data-stu-id="f26b8-105">The **hoverDownImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the down state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="f26b8-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="f26b8-106">Possible Values</span></span>

<span data-ttu-id="f26b8-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="f26b8-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="f26b8-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f26b8-108">Remarks</span></span>

<span data-ttu-id="f26b8-109">Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.</span><span class="sxs-lookup"><span data-stu-id="f26b8-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="f26b8-110">La imagen predeterminada es la especificada en el atributo **downImage** o su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f26b8-110">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="f26b8-111">Si la imagen de mantener el mouse es mayor que la región definida en el atributo ambiente, se recortará la imagen desplegable.</span><span class="sxs-lookup"><span data-stu-id="f26b8-111">If the hover-down image is larger than the defined region in the ambient attribute, the hover-down image will be cropped.</span></span>

<span data-ttu-id="f26b8-112">Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).</span><span class="sxs-lookup"><span data-stu-id="f26b8-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f26b8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f26b8-113">Requirements</span></span>



| <span data-ttu-id="f26b8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f26b8-114">Requirement</span></span> | <span data-ttu-id="f26b8-115">Value</span><span class="sxs-lookup"><span data-stu-id="f26b8-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f26b8-116">Versión</span><span class="sxs-lookup"><span data-stu-id="f26b8-116">Version</span></span><br/> | <span data-ttu-id="f26b8-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f26b8-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f26b8-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f26b8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f26b8-119">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="f26b8-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="f26b8-120">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="f26b8-120">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





