---
title: Crear controles deslizantes personalizados
description: Crear controles deslizantes personalizados
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- crear máscaras, controles deslizantes
- Reproductor de Windows Media máscaras, controles deslizantes
- máscaras, controles deslizantes
- controles deslizantes en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85a789bbd90003b59e1a9b9dcf8fffcf4a126c38138f7a051c24125780f8c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902335"
---
# <a name="creating-custom-sliders"></a>Crear controles deslizantes personalizados

Puede crear controles deslizantes personalizados en cualquier forma que desee. En este ejemplo, se elige una franja simple, pero la forma real puede ser cualquier cosa. Este es el código del **elemento CUSTOMSLIDER:**


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



Esto configura un valor inicial para el control deslizante. Se presentan dos mapas de bits nuevos. Uno es el mapa de bits de escala de grises (slider.bmp) que define los valores que se usarán al hacer clic en él y el otro (slider.bmp) que determina en qué imagen se mostrará cuando se haga clic en una parte determinada de la escala de grises.

El valor inicial se determina mediante la escucha del volumen con wmpprop y, a continuación, el volumen se puede cambiar cuando el usuario hace clic en una parte del control deslizante que desencadena un cambio en el valor.

Puede ver una máscara de control deslizante de trabajo similar en la sección de ejemplo del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de creación de máscaras**](skin-creation-guide.md)
</dt> </dl>

 

 




