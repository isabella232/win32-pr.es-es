---
title: CUSTOMSLIDER.positionImage
description: El atributo positionImage especifica o recupera el mapa de imágenes que se usa para determinar la imagen de posición del archivo de imagen que se va a mostrar.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- CUSTOMSLIDER. positionImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc92a9c263e2b450e64d526ccfc7976fdd6227a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698499"
---
# <a name="customsliderpositionimage"></a><span data-ttu-id="198f4-104">CUSTOMSLIDER.positionImage</span><span class="sxs-lookup"><span data-stu-id="198f4-104">CUSTOMSLIDER.positionImage</span></span>

<span data-ttu-id="198f4-105">El atributo **positionImage** especifica o recupera el mapa de imágenes que se usa para determinar la imagen de posición del archivo de imagen que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="198f4-105">The **positionImage** attribute specifies or retrieves the image map used to determine which position image from the image file to display.</span></span>

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a><span data-ttu-id="198f4-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="198f4-106">Possible Values</span></span>

<span data-ttu-id="198f4-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="198f4-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="198f4-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="198f4-108">Remarks</span></span>

<span data-ttu-id="198f4-109">Este atributo es obligatorio y debe especificarse.</span><span class="sxs-lookup"><span data-stu-id="198f4-109">This attribute is required and must be specified.</span></span>

<span data-ttu-id="198f4-110">No se muestra **positionImage** .</span><span class="sxs-lookup"><span data-stu-id="198f4-110">The **positionImage** is not displayed.</span></span> <span data-ttu-id="198f4-111">En su lugar, actúa como un mapa que define las regiones en las que se hace clic de la imagen mostrada.</span><span class="sxs-lookup"><span data-stu-id="198f4-111">Instead, it serves as a map defining the clickable regions of the displayed image.</span></span> <span data-ttu-id="198f4-112">La imagen mostrada es una de las subimágenes del archivo de imagen y representa el estado real del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="198f4-112">The displayed image is one of the sub-images of the image file and represents the actual state of the slider.</span></span> <span data-ttu-id="198f4-113">**PositionImage** incluye varias regiones de escala de grises iguales al número de estas subimágenes.</span><span class="sxs-lookup"><span data-stu-id="198f4-113">The **positionImage** includes a number of gray scale regions equal to the number of these sub-images.</span></span> <span data-ttu-id="198f4-114">Las subimágenes deben tener las mismas dimensiones que **positionImage** o el control deslizante personalizado no funcionará correctamente.</span><span class="sxs-lookup"><span data-stu-id="198f4-114">The sub-images must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span>

<span data-ttu-id="198f4-115">No se puede hacer clic en las regiones que no estén en escala de grises.</span><span class="sxs-lookup"><span data-stu-id="198f4-115">Any region that is not in gray scale will not be clickable.</span></span> <span data-ttu-id="198f4-116">Las regiones en las que se puede hacer clic deben establecerse en valores de color que se ajusten uniformemente por el espectro de la escala de grises de negro a blanco, con la primera región en negro puro y la última región en blanco puro.</span><span class="sxs-lookup"><span data-stu-id="198f4-116">The clickable regions should be set to color values that range evenly across the gray scale spectrum from black to white, with the first region being pure black and the last region being pure white.</span></span> <span data-ttu-id="198f4-117">Los valores de color de cada región sucesiva deben incrementarse en un valor igual a 255 dividido entre el número total de regiones menos uno, y se redondea al número entero más próximo.</span><span class="sxs-lookup"><span data-stu-id="198f4-117">The color values of each successive region should be incremented by a value equal to 255 divided by the total number of regions minus one, rounding to the nearest whole number.</span></span>

<span data-ttu-id="198f4-118">Por ejemplo, si hay seis regiones, el incremento sería 51 (255 dividido entre 5) y los seis valores de escala de grises serían 0, 51, 102, 153, 204 y 255.</span><span class="sxs-lookup"><span data-stu-id="198f4-118">For example, if there are six regions, the increment would be 51 (255 divided by 5), and the six gray scale values would be 0, 51, 102, 153, 204, and 255.</span></span> <span data-ttu-id="198f4-119">Los valores de color hexadecimal para las seis regiones serían \# 000000, \# 333333, \# 666666, \# 999999, \# CCCCCC y \# FFFFFF.</span><span class="sxs-lookup"><span data-stu-id="198f4-119">The hexadecimal color values for the six regions would then be \#000000, \#333333, \#666666, \#999999, \#CCCCCC, and \#FFFFFF.</span></span>

<span data-ttu-id="198f4-120">De esta manera, las regiones tendrán una secuencia dictada por los valores de color de la escala gris y esta secuencia se corresponderá con la secuencia de subimágenes del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="198f4-120">In this way, the regions will have a sequence dictated by their gray scale color values, and this sequence will correspond to the sequence of sub-images in the image file.</span></span> <span data-ttu-id="198f4-121">Cuando se hace clic en una de las regiones, se muestra la subimagen correspondiente y el **valor** del control deslizante personalizado se actualiza en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="198f4-121">When one of the regions is clicked, the corresponding sub-image is shown and the **value** of the custom slider is updated accordingly.</span></span>

<span data-ttu-id="198f4-122">Los tipos de archivo de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).</span><span class="sxs-lookup"><span data-stu-id="198f4-122">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="198f4-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="198f4-123">Examples</span></span>

<span data-ttu-id="198f4-124">El siguiente es un ejemplo de un control deslizante personalizado **positionImage**.</span><span class="sxs-lookup"><span data-stu-id="198f4-124">The following is an example of a custom slider **positionImage**.</span></span> <span data-ttu-id="198f4-125">La imagen correspondiente se muestra en la sección ejemplo de la propiedad **Image** .</span><span class="sxs-lookup"><span data-stu-id="198f4-125">The corresponding image is shown in the example section of the **image** property.</span></span>

![gráfico de positionimage de ejemplo](images/dialmap.png)

<span data-ttu-id="198f4-127">En el código siguiente se muestra el uso de los atributos **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="198f4-127">The following code illustrates the use of **CUSTOMSLIDER** attributes.</span></span>


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

    <SLIDER
      id = "myslider"
      min = "0"
      max = "wmpprop:player.currentMedia.duration"
      onmouseup = "player.controls.currentPosition = myslider.value; "
      tooltip = "current position"
      height = "10"
      width = "180"
      top = "150"
      left = "88"
      backgroundColor = "red"
      foregroundColor = "blue"
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
    />

    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    > 

      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />

      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />

    </BUTTONGROUP>

  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="198f4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="198f4-128">Requirements</span></span>



| <span data-ttu-id="198f4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="198f4-129">Requirement</span></span> | <span data-ttu-id="198f4-130">Value</span><span class="sxs-lookup"><span data-stu-id="198f4-130">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="198f4-131">Versión</span><span class="sxs-lookup"><span data-stu-id="198f4-131">Version</span></span><br/> | <span data-ttu-id="198f4-132">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="198f4-132">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="198f4-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="198f4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="198f4-134">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="198f4-134">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="198f4-135">**CUSTOMSLIDER. Image**</span><span class="sxs-lookup"><span data-stu-id="198f4-135">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





