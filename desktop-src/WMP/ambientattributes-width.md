---
title: AmbientAttributes. width
description: El atributo width especifica o recupera el ancho del control.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- AmbientAttributes. width Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699342"
---
# <a name="ambientattributeswidth"></a><span data-ttu-id="10526-104">AmbientAttributes. width</span><span class="sxs-lookup"><span data-stu-id="10526-104">AmbientAttributes.width</span></span>

<span data-ttu-id="10526-105">El atributo **width** especifica o recupera el ancho del control.</span><span class="sxs-lookup"><span data-stu-id="10526-105">The **width** attribute specifies or retrieves the width of the control.</span></span>

``` syntax
        elementID.width
```

## <a name="possible-values"></a><span data-ttu-id="10526-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="10526-106">Possible Values</span></span>

<span data-ttu-id="10526-107">Este atributo es un **entero** de 16 bits de lectura/escritura (de 0 a 32.767) que representa el ancho del control en píxeles.</span><span class="sxs-lookup"><span data-stu-id="10526-107">This attribute is a read/write 16-bit **Integer** (0 to 32,767) representing the width of the control in pixels.</span></span> <span data-ttu-id="10526-108">El valor predeterminado es cero o el ancho de la imagen especificada en el atributo de **imagen** del control.</span><span class="sxs-lookup"><span data-stu-id="10526-108">The default value is zero or the width of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="10526-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10526-109">Remarks</span></span>

<span data-ttu-id="10526-110">Si el ancho especificado es más estrecho que el ancho de la imagen proporcionada, se recortará la imagen.</span><span class="sxs-lookup"><span data-stu-id="10526-110">If the width specified is narrower than the width of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="10526-111">Si el ancho es más ancho que el ancho de la imagen, la región de clic irá más allá del límite de la imagen.</span><span class="sxs-lookup"><span data-stu-id="10526-111">If the width is wider than the width of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="10526-112">Independientemente del valor que se proporcione a este atributo, la imagen no puede crecer más allá de la **vista** o la **subvista** primaria.</span><span class="sxs-lookup"><span data-stu-id="10526-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="10526-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10526-113">Requirements</span></span>



| <span data-ttu-id="10526-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="10526-114">Requirement</span></span> | <span data-ttu-id="10526-115">Value</span><span class="sxs-lookup"><span data-stu-id="10526-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="10526-116">Versión</span><span class="sxs-lookup"><span data-stu-id="10526-116">Version</span></span><br/> | <span data-ttu-id="10526-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="10526-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10526-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="10526-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10526-119">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="10526-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





