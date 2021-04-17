---
title: CUSTOMSLIDER.downImage
description: El atributo downImage especifica o recupera la imagen de estado hacia abajo del control deslizante personalizado.
ms.assetid: e1efe703-df0a-4ef9-92a9-c9cfb991ee37
keywords:
- CUSTOMSLIDER. downImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8365043654bc3cca9fbf79162302cf804155956d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700124"
---
# <a name="customsliderdownimage"></a><span data-ttu-id="7314d-104">CUSTOMSLIDER.downImage</span><span class="sxs-lookup"><span data-stu-id="7314d-104">CUSTOMSLIDER.downImage</span></span>

<span data-ttu-id="7314d-105">El atributo **downImage** especifica o recupera la imagen de estado hacia abajo del control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="7314d-105">The **downImage** attribute specifies or retrieves the down state image of the custom slider.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="7314d-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="7314d-106">Possible Values</span></span>

<span data-ttu-id="7314d-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="7314d-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="7314d-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7314d-108">Remarks</span></span>

<span data-ttu-id="7314d-109">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="7314d-109">This attribute is optional.</span></span> <span data-ttu-id="7314d-110">Si no se especifica, se utilizará el archivo especificado en el atributo de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="7314d-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="7314d-111">**DownImage** representa el estado inactivo del control **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="7314d-111">The **downImage** represents the down state of the **CUSTOMSLIDER** control.</span></span> <span data-ttu-id="7314d-112">Puede ser una sola imagen o una serie de imágenes que representan los distintos Estados del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="7314d-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="7314d-113">Si se usan varias imágenes, se organizan de la misma manera que el archivo de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="7314d-113">If multiple images are used, they are arranged in the same way as the **image** file.</span></span>

<span data-ttu-id="7314d-114">Los tipos de archivo de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).</span><span class="sxs-lookup"><span data-stu-id="7314d-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="7314d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7314d-115">Requirements</span></span>



| <span data-ttu-id="7314d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7314d-116">Requirement</span></span> | <span data-ttu-id="7314d-117">Value</span><span class="sxs-lookup"><span data-stu-id="7314d-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7314d-118">Versión</span><span class="sxs-lookup"><span data-stu-id="7314d-118">Version</span></span><br/> | <span data-ttu-id="7314d-119">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7314d-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7314d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7314d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7314d-121">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="7314d-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="7314d-122">**CUSTOMSLIDER. Image**</span><span class="sxs-lookup"><span data-stu-id="7314d-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





