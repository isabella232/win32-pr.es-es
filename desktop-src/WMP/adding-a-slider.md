---
title: Agregar un control deslizante
description: Agregar un control deslizante
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- crear máscaras, controles deslizantes
- Aspectos de Windows Media Player, controles deslizantes
- máscaras, controles deslizantes
- controles deslizantes en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075976"
---
# <a name="adding-a-slider"></a>Agregar un control deslizante

Puede Agregar un control deslizante para mostrar la posición actual del medio y permitir que el usuario cambie la posición en el archivo multimedia actual.

En primer lugar, debe agregar el elemento **Slider** :


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



Esto establece un valor máximo en función de la duración del archivo multimedia actual. Utiliza un mapa de bits de imagen Thumb pequeño que es simplemente un cuadrado verde de 10 píxeles por 10 píxeles. El fondo del control deslizante será rojo y el primer plano será azul. Cuando el usuario arrastra la imagen Thumb a una nueva posición y permite ir al botón del mouse, el medio cambiará a esa posición.

Pero el control deslizante no se moverá por sí solo a menos que mida la posición actual con el atributo **currentPosition \_ onchange** del elemento **Controls** , que se incrusta en el elemento **Player** .


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



Cuando cambia la posición del elemento multimedia, se desencadena un evento que, a continuación, ejecuta la línea de código que cambia el valor del control deslizante a la posición actual del medio.

Puede ver una máscara de control deslizante de trabajo similar en la sección de ejemplo del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de creación de máscaras**](skin-creation-guide.md)
</dt> </dl>

 

 




