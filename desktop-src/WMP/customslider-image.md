---
title: CUSTOMSLIDER. Image
description: El atributo Image especifica o recupera el nombre del archivo que contiene las imágenes correspondientes a los distintos Estados del control deslizante personalizado.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- Media Player CUSTOMSLIDER. Image de Windows
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698472"
---
# <a name="customsliderimage"></a><span data-ttu-id="d84f5-104">CUSTOMSLIDER. Image</span><span class="sxs-lookup"><span data-stu-id="d84f5-104">CUSTOMSLIDER.image</span></span>

<span data-ttu-id="d84f5-105">El atributo **Image** especifica o recupera el nombre del archivo que contiene las imágenes correspondientes a los distintos Estados del control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="d84f5-105">The **image** attribute specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="d84f5-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="d84f5-106">Possible Values</span></span>

<span data-ttu-id="d84f5-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="d84f5-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="d84f5-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d84f5-108">Remarks</span></span>

<span data-ttu-id="d84f5-109">El atributo **Image** es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d84f5-109">The **image** attribute is required.</span></span> <span data-ttu-id="d84f5-110">Especifica un archivo de imagen que consta de una o más subimágenes, organizadas horizontal o verticalmente, que representan los distintos Estados del control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="d84f5-110">It specifies an image file that consists of one or more sub-images, arranged either horizontally or vertically, representing the various states of the custom slider.</span></span> <span data-ttu-id="d84f5-111">Cada subimagen debe tener las mismas dimensiones que **positionImage** o el control deslizante personalizado no funcionará correctamente.</span><span class="sxs-lookup"><span data-stu-id="d84f5-111">Each sub-image must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span> <span data-ttu-id="d84f5-112">El alto o ancho de la imagen global debe ser, por tanto, un múltiplo par del alto o del ancho de **positionImage**.</span><span class="sxs-lookup"><span data-stu-id="d84f5-112">The height or width of the overall image must therefore be an even multiple of the height or width of the **positionImage**.</span></span>

<span data-ttu-id="d84f5-113">Los tipos de archivo de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).</span><span class="sxs-lookup"><span data-stu-id="d84f5-113">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="d84f5-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d84f5-114">Examples</span></span>

<span data-ttu-id="d84f5-115">El siguiente es un ejemplo de una imagen de control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="d84f5-115">The following is an example of a custom slider image.</span></span> <span data-ttu-id="d84f5-116">El **positionImage** correspondiente se muestra en la sección ejemplo de la propiedad **positionImage** .</span><span class="sxs-lookup"><span data-stu-id="d84f5-116">The corresponding **positionImage** is shown in the example section of the **positionImage** property.</span></span>

![imagen de customslider de ejemplo](images/dial.png)

<span data-ttu-id="d84f5-118">El atributo **positionImage** también contiene un ejemplo de código que ilustra cómo se usan los atributos del elemento **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="d84f5-118">The **positionImage** attribute also contains a code sample illustrating how the attributes of the **CUSTOMSLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d84f5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d84f5-119">Requirements</span></span>



| <span data-ttu-id="d84f5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d84f5-120">Requirement</span></span> | <span data-ttu-id="d84f5-121">Value</span><span class="sxs-lookup"><span data-stu-id="d84f5-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d84f5-122">Versión</span><span class="sxs-lookup"><span data-stu-id="d84f5-122">Version</span></span><br/> | <span data-ttu-id="d84f5-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="d84f5-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d84f5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d84f5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d84f5-125">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="d84f5-125">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="d84f5-126">**CUSTOMSLIDER.positionImage**</span><span class="sxs-lookup"><span data-stu-id="d84f5-126">**CUSTOMSLIDER.positionImage**</span></span>](customslider-positionimage.md)
</dt> </dl>

 

 





