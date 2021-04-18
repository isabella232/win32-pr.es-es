---
title: BUTTON. downImage
description: El atributo downImage especifica o recupera la imagen que representa el estado inactivo del botón.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- BUTTON. downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698614"
---
# <a name="buttondownimage"></a><span data-ttu-id="4d5ef-104">BUTTON. downImage</span><span class="sxs-lookup"><span data-stu-id="4d5ef-104">BUTTON.downImage</span></span>

<span data-ttu-id="4d5ef-105">El atributo **downImage** especifica o recupera la imagen que representa el estado inactivo del **botón**.</span><span class="sxs-lookup"><span data-stu-id="4d5ef-105">The **downImage** attribute specifies or retrieves the image representing the down state of the **BUTTON**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="4d5ef-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="4d5ef-106">Possible Values</span></span>

<span data-ttu-id="4d5ef-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="4d5ef-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d5ef-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d5ef-108">Remarks</span></span>

<span data-ttu-id="4d5ef-109">Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.</span><span class="sxs-lookup"><span data-stu-id="4d5ef-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="4d5ef-110">La imagen predeterminada es la especificada en el atributo de **imagen** o su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4d5ef-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="4d5ef-111">Si la imagen hacia abajo es mayor que la región definida en el atributo ambiente, se recortará la imagen hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="4d5ef-111">If the down image is larger than the defined region in the ambient attribute, the down image will be cropped.</span></span>

<span data-ttu-id="4d5ef-112">Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).</span><span class="sxs-lookup"><span data-stu-id="4d5ef-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d5ef-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d5ef-113">Requirements</span></span>



| <span data-ttu-id="4d5ef-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d5ef-114">Requirement</span></span> | <span data-ttu-id="4d5ef-115">Value</span><span class="sxs-lookup"><span data-stu-id="4d5ef-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4d5ef-116">Versión</span><span class="sxs-lookup"><span data-stu-id="4d5ef-116">Version</span></span><br/> | <span data-ttu-id="4d5ef-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4d5ef-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d5ef-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d5ef-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d5ef-119">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="4d5ef-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="4d5ef-120">**BOTÓN. abajo**</span><span class="sxs-lookup"><span data-stu-id="4d5ef-120">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="4d5ef-121">**BOTÓN. imagen**</span><span class="sxs-lookup"><span data-stu-id="4d5ef-121">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





