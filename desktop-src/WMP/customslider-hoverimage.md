---
title: CUSTOMSLIDER.hoverImage
description: El atributo hoverImage especifica o recupera la imagen que aparece cuando el mouse está encima del control deslizante personalizado.
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- CUSTOMSLIDER. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 361f7d903b6231e92f331ab38a3a9f51bc3ec679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700087"
---
# <a name="customsliderhoverimage"></a><span data-ttu-id="f9c8e-104">CUSTOMSLIDER.hoverImage</span><span class="sxs-lookup"><span data-stu-id="f9c8e-104">CUSTOMSLIDER.hoverImage</span></span>

<span data-ttu-id="f9c8e-105">El atributo **hoverImage** especifica o recupera la imagen que aparece cuando el mouse está encima del control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-105">The **hoverImage** attribute specifies or retrieves the image that appears when the mouse is over the custom slider.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="f9c8e-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="f9c8e-106">Possible Values</span></span>

<span data-ttu-id="f9c8e-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9c8e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9c8e-108">Remarks</span></span>

<span data-ttu-id="f9c8e-109">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-109">This attribute is optional.</span></span> <span data-ttu-id="f9c8e-110">Si no se especifica, se utilizará el archivo especificado en el atributo de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="f9c8e-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="f9c8e-111">**HoverImage** representa el estado de activación del control CUSTOMSLIDER. es decir, el estado que se muestra cuando el cursor del mouse se desplaza sobre él.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-111">The **hoverImage** represents the hover state of the CUSTOMSLIDER control; that is, the state that is shown when the mouse cursor hovers over it.</span></span> <span data-ttu-id="f9c8e-112">Puede ser una sola imagen o una serie de imágenes que representan los distintos Estados del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="f9c8e-113">Si se usan varias imágenes, se organizan de la misma manera que el archivo de **imagen**</span><span class="sxs-lookup"><span data-stu-id="f9c8e-113">If multiple images are used, they are arranged in the same way as the **image** file</span></span>

<span data-ttu-id="f9c8e-114">Los tipos de archivo de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).</span><span class="sxs-lookup"><span data-stu-id="f9c8e-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c8e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9c8e-115">Requirements</span></span>



| <span data-ttu-id="f9c8e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9c8e-116">Requirement</span></span> | <span data-ttu-id="f9c8e-117">Value</span><span class="sxs-lookup"><span data-stu-id="f9c8e-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f9c8e-118">Versión</span><span class="sxs-lookup"><span data-stu-id="f9c8e-118">Version</span></span><br/> | <span data-ttu-id="f9c8e-119">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f9c8e-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9c8e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9c8e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c8e-121">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="f9c8e-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="f9c8e-122">**CUSTOMSLIDER. Image**</span><span class="sxs-lookup"><span data-stu-id="f9c8e-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





