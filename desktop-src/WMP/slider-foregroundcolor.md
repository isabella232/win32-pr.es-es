---
title: SLIDEr. foregroundColor
description: El atributo foregroundColor especifica o recupera el color de primer plano del control deslizante.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- CONTROL SLIDEr. foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661193"
---
# <a name="sliderforegroundcolor"></a><span data-ttu-id="0beca-104">SLIDEr. foregroundColor</span><span class="sxs-lookup"><span data-stu-id="0beca-104">SLIDER.foregroundColor</span></span>

<span data-ttu-id="0beca-105">El atributo **foregroundColor** especifica o recupera el color de primer plano del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="0beca-105">The **foregroundColor** attribute specifies or retrieves the foreground color of the slider control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="0beca-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="0beca-106">Possible Values</span></span>

<span data-ttu-id="0beca-107">Este atributo es una **cadena** de lectura/escritura que contiene cualquier valor de color de Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0beca-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="0beca-108">El valor predeterminado es "blanco".</span><span class="sxs-lookup"><span data-stu-id="0beca-108">The default value is "white".</span></span>

## <a name="remarks"></a><span data-ttu-id="0beca-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0beca-109">Remarks</span></span>

<span data-ttu-id="0beca-110">Un control deslizante básico se puede construir especificando uno de los dos pares de atributos: **BackgroundColor** y **foregroundColor**, o el argumento **BackgroundImage** y **foregroundImage**.</span><span class="sxs-lookup"><span data-stu-id="0beca-110">A basic slider control can be constructed by specifying one of two pairs of attributes: the **backgroundColor** and **foregroundColor**, or the **backgroundImage** and **foregroundImage**.</span></span>

<span data-ttu-id="0beca-111">Cuando se construye un control deslizante con los atributos de color, las dimensiones del control deslizante definen el área rellenada por el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="0beca-111">When you construct a slider control using the color attributes, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="0beca-112">El color de primer plano cubre el color de fondo a medida que aumenta la posición del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="0beca-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="0beca-113">Para hacer un relleno de degradado en el área ocupada por el color de fondo o de primer plano, especifique los atributos **backgroundEndColor** o **foregroundEndColor** .</span><span class="sxs-lookup"><span data-stu-id="0beca-113">To make a gradient fill in the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="0beca-114">Vea *CUSTOMSLIDER*. atributo [positionImage](customslider-positionimage.md) para un ejemplo que muestra cómo se utilizan los atributos del elemento **Slider** .</span><span class="sxs-lookup"><span data-stu-id="0beca-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0beca-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0beca-115">Requirements</span></span>



| <span data-ttu-id="0beca-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0beca-116">Requirement</span></span> | <span data-ttu-id="0beca-117">Value</span><span class="sxs-lookup"><span data-stu-id="0beca-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0beca-118">Versión</span><span class="sxs-lookup"><span data-stu-id="0beca-118">Version</span></span><br/> | <span data-ttu-id="0beca-119">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0beca-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0beca-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0beca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0beca-121">**Referencia de color**</span><span class="sxs-lookup"><span data-stu-id="0beca-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="0beca-122">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="0beca-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="0beca-123">**Control deslizante. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="0beca-123">**SLIDER.backgroundColor**</span></span>](slider-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="0beca-124">**SLIDEr. backgroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="0beca-124">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="0beca-125">**SLIDEr. foregroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="0beca-125">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="0beca-126">**SLIDEr. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="0beca-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





