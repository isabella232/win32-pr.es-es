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
# <a name="customsliderpositionimage"></a>CUSTOMSLIDER.positionImage

El atributo **positionImage** especifica o recupera el mapa de imágenes que se usa para determinar la imagen de posición del archivo de imagen que se va a mostrar.

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Observaciones

Este atributo es obligatorio y debe especificarse.

No se muestra **positionImage** . En su lugar, actúa como un mapa que define las regiones en las que se hace clic de la imagen mostrada. La imagen mostrada es una de las subimágenes del archivo de imagen y representa el estado real del control deslizante. **PositionImage** incluye varias regiones de escala de grises iguales al número de estas subimágenes. Las subimágenes deben tener las mismas dimensiones que **positionImage** o el control deslizante personalizado no funcionará correctamente.

No se puede hacer clic en las regiones que no estén en escala de grises. Las regiones en las que se puede hacer clic deben establecerse en valores de color que se ajusten uniformemente por el espectro de la escala de grises de negro a blanco, con la primera región en negro puro y la última región en blanco puro. Los valores de color de cada región sucesiva deben incrementarse en un valor igual a 255 dividido entre el número total de regiones menos uno, y se redondea al número entero más próximo.

Por ejemplo, si hay seis regiones, el incremento sería 51 (255 dividido entre 5) y los seis valores de escala de grises serían 0, 51, 102, 153, 204 y 255. Los valores de color hexadecimal para las seis regiones serían \# 000000, \# 333333, \# 666666, \# 999999, \# CCCCCC y \# FFFFFF.

De esta manera, las regiones tendrán una secuencia dictada por los valores de color de la escala gris y esta secuencia se corresponderá con la secuencia de subimágenes del archivo de imagen. Cuando se hace clic en una de las regiones, se muestra la subimagen correspondiente y el **valor** del control deslizante personalizado se actualiza en consecuencia.

Los tipos de archivo de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).

## <a name="examples"></a>Ejemplos

El siguiente es un ejemplo de un control deslizante personalizado **positionImage**. La imagen correspondiente se muestra en la sección ejemplo de la propiedad **Image** .

![gráfico de positionimage de ejemplo](images/dialmap.png)

En el código siguiente se muestra el uso de los atributos **CUSTOMSLIDER** .


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER. Image**](customslider-image.md)
</dt> </dl>

 

 





