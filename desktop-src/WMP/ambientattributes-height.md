---
title: AmbientAttributes. Height
description: El atributo height especifica o recupera el alto del control.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- AmbientAttributes. Height Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700064"
---
# <a name="ambientattributesheight"></a><span data-ttu-id="40586-104">AmbientAttributes. Height</span><span class="sxs-lookup"><span data-stu-id="40586-104">AmbientAttributes.height</span></span>

<span data-ttu-id="40586-105">El atributo **height** especifica o recupera el alto del control.</span><span class="sxs-lookup"><span data-stu-id="40586-105">The **height** attribute specifies or retrieves the height of the control.</span></span>

``` syntax
        elementID.height
```

## <a name="possible-values"></a><span data-ttu-id="40586-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="40586-106">Possible Values</span></span>

<span data-ttu-id="40586-107">Este atributo es un **número** de lectura y escritura (**Long**) que representa el alto del control en píxeles.</span><span class="sxs-lookup"><span data-stu-id="40586-107">This attribute is a read/write **Number** (**long**) representing the height of the control in pixels.</span></span> <span data-ttu-id="40586-108">El valor predeterminado es cero o el alto de la imagen especificada en el atributo de **imagen** del control.</span><span class="sxs-lookup"><span data-stu-id="40586-108">The default value is zero or the height of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="40586-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40586-109">Remarks</span></span>

<span data-ttu-id="40586-110">Si el alto especificado es menor que el alto de la imagen proporcionada, se recortará la imagen.</span><span class="sxs-lookup"><span data-stu-id="40586-110">If the height specified is smaller than the height of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="40586-111">Si el alto es mayor que el alto de la imagen, la región de clic irá más allá del límite de la imagen.</span><span class="sxs-lookup"><span data-stu-id="40586-111">If the height is larger than the height of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="40586-112">Independientemente del valor que se proporcione a este atributo, la imagen no puede crecer más allá de la **vista** o la **subvista** primaria.</span><span class="sxs-lookup"><span data-stu-id="40586-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="40586-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40586-113">Requirements</span></span>



| <span data-ttu-id="40586-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="40586-114">Requirement</span></span> | <span data-ttu-id="40586-115">Value</span><span class="sxs-lookup"><span data-stu-id="40586-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="40586-116">Versión</span><span class="sxs-lookup"><span data-stu-id="40586-116">Version</span></span><br/> | <span data-ttu-id="40586-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="40586-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40586-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="40586-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40586-119">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="40586-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





