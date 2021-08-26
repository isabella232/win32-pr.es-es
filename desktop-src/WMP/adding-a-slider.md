---
title: Agregar un control deslizante
description: Agregar un control deslizante
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- crear máscaras, controles deslizantes
- Reproductor de Windows Media máscaras, controles deslizantes
- máscaras, controles deslizantes
- controles deslizantes en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c3644e1b243188664295bbc00101a74377cbef17632217ff0a81dac0d377a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004385"
---
# <a name="adding-a-slider"></a>Agregar un control deslizante

Puede agregar un control deslizante para mostrar la posición actual del medio y también permitir que el usuario cambie la posición en el archivo multimedia actual.

En primer lugar, debe agregar el **elemento SLIDER:**


```C++
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
  thumbImage = "thumb.bmp"/>

```



Esto establece un valor máximo en función de la duración del archivo multimedia actual. Esto usa un mapa de bits de imagen de miniatura diminuta que es solo un cuadrado verde de 10 píxeles por 10 píxeles. El fondo del control deslizante será rojo y el primer plano será azul. Cuando el usuario arrastra la imagen de posición a una nueva posición y suelta el botón del mouse, el medio cambia a esa posición.

Pero el control deslizante no se moverá por sí solo a menos que mida la posición actual con el atributo **currentPosition \_ onchange** del elemento **CONTROLS,** que se incrusta en el **elemento PLAYER.**


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



Cuando cambia la posición del medio, se produce un evento que ejecuta la línea de código que cambia el valor del control deslizante a la posición actual del medio.

Puede ver una máscara de control deslizante de trabajo similar en la sección de ejemplo del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de creación de máscaras**](skin-creation-guide.md)
</dt> </dl>

 

 




