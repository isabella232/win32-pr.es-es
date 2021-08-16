---
title: CUSTOMSLIDER.positionImage
description: El atributo positionImage especifica o recupera el mapa de imagen usado para determinar qué imagen de posición del archivo de imagen se va a mostrar.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- CUSTOMSLIDER.positionImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727601ceb7ed078e40a284ab291f2e182a4270682b5f1db104515e31d3dbe2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750001"
---
# <a name="customsliderpositionimage"></a>CUSTOMSLIDER.positionImage

El **atributo positionImage** especifica o recupera el mapa de imagen usado para determinar qué imagen de posición del archivo de imagen se va a mostrar.

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Comentarios

Este atributo es necesario y se debe especificar.

No **se muestra positionImage.** En su lugar, actúa como un mapa que define las regiones en las que se puede hacer clic de la imagen mostrada. La imagen mostrada es una de las sub images del archivo de imagen y representa el estado real del control deslizante. **PositionImage incluye** un número de regiones de escala de grises igual al número de estas subimagenes. Las subimagenes deben tener las mismas dimensiones que **positionImage** o el control deslizante personalizado no funcionará correctamente.

No se podrá hacer clic en ninguna región que no esté en escala de grises. Las regiones en las que se puede hacer clic deben establecerse en valores de color que oscilan uniformemente entre el espectro de escala de grises de negro a blanco, siendo la primera región negra pura y la última región blanca pura. Los valores de color de cada región sucesiva se deben incrementar en un valor igual a 255 dividido entre el número total de regiones menos una, redondeando al número entero más cercano.

Por ejemplo, si hay seis regiones, el incremento sería 51 (255 dividido entre 5) y los seis valores de escala gris serían 0, 51, 102, 153, 204 y 255. Los valores de color hexadecimal de las seis regiones serían \# 000000, \# 333333, \# 666666, \# \# 999999,CCICCC y \# FFFFFF.

De esta manera, las regiones tendrán una secuencia dictada por sus valores de color de escala gris, y esta secuencia se corresponderá con la secuencia de sub images del archivo de imagen. Cuando se hace clic en una de las regiones,  se muestra la sub image correspondiente y el valor del control deslizante personalizado se actualiza en consecuencia.

Los tipos de archivo de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir GIF animados).

## <a name="examples"></a>Ejemplos

A continuación se muestra un ejemplo de un control deslizante **personalizado positionImage**. La imagen correspondiente se muestra en la sección de ejemplo de la **propiedad image.**

![gráfico de imagen de posición de ejemplo](images/dialmap.png)

El código siguiente muestra el uso de **atributos CUSTOMSLIDER.**


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER.image**](customslider-image.md)
</dt> </dl>

 

 





