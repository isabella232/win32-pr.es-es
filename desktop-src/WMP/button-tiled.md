---
title: BOTÓN. en mosaico
description: El atributo en mosaico especifica o recupera un valor que indica si se va a colocar en mosaico la imagen del botón.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- BOTÓN. Media Player de Windows en mosaico
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700356"
---
# <a name="buttontiled"></a><span data-ttu-id="72f27-104">BOTÓN. en mosaico</span><span class="sxs-lookup"><span data-stu-id="72f27-104">BUTTON.tiled</span></span>

<span data-ttu-id="72f27-105">El atributo en **mosaico** especifica o recupera un valor que indica si se va a colocar en mosaico la imagen del **botón** .</span><span class="sxs-lookup"><span data-stu-id="72f27-105">The **tiled** attribute specifies or retrieves a value indicating whether the **BUTTON** image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="72f27-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="72f27-106">Possible Values</span></span>

<span data-ttu-id="72f27-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="72f27-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="72f27-108">Value</span><span class="sxs-lookup"><span data-stu-id="72f27-108">Value</span></span> | <span data-ttu-id="72f27-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="72f27-109">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="72f27-110">true</span><span class="sxs-lookup"><span data-stu-id="72f27-110">true</span></span>  | <span data-ttu-id="72f27-111">La imagen se mostrará en mosaico.</span><span class="sxs-lookup"><span data-stu-id="72f27-111">Image will be tiled.</span></span>              |
| <span data-ttu-id="72f27-112">false</span><span class="sxs-lookup"><span data-stu-id="72f27-112">false</span></span> | <span data-ttu-id="72f27-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="72f27-113">Default.</span></span> <span data-ttu-id="72f27-114">La imagen no se mostrará en mosaico.</span><span class="sxs-lookup"><span data-stu-id="72f27-114">Image will not be tiled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="72f27-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72f27-115">Remarks</span></span>

<span data-ttu-id="72f27-116">Si la imagen es menor que la región real del control, el mosaico de la imagen se repetirá hasta que se llene toda la región.</span><span class="sxs-lookup"><span data-stu-id="72f27-116">If the image is smaller than the actual region of the control, then tiling the image will repeat it until it fills the entire region.</span></span> <span data-ttu-id="72f27-117">Si no se especifica una imagen o no se puede recuperar, en **mosaico** se establecerá en false.</span><span class="sxs-lookup"><span data-stu-id="72f27-117">If an image is not specified or cannot be retrieved, **tiled** will be set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f27-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72f27-118">Requirements</span></span>



| <span data-ttu-id="72f27-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="72f27-119">Requirement</span></span> | <span data-ttu-id="72f27-120">Value</span><span class="sxs-lookup"><span data-stu-id="72f27-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="72f27-121">Versión</span><span class="sxs-lookup"><span data-stu-id="72f27-121">Version</span></span><br/> | <span data-ttu-id="72f27-122">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="72f27-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72f27-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="72f27-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f27-124">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="72f27-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="72f27-125">**BOTÓN. imagen**</span><span class="sxs-lookup"><span data-stu-id="72f27-125">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





