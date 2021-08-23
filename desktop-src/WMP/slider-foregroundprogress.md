---
title: SLIDER.foregroundProgress
description: El atributo foregroundProgress especifica o recupera la posición actual de la barra de progreso de primer plano como porcentaje del área deslizante.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- SLIDER.foregroundProgress Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48819a2b3245fc8a72d29e9a30135cc37702417ca498c88b8be01578b74988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646345"
---
# <a name="sliderforegroundprogress"></a>SLIDER.foregroundProgress

El **atributo foregroundProgress** especifica o recupera la posición actual de la barra de progreso de primer plano como porcentaje del área deslizante.

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** **(float)** que va de 0 a 100.

## <a name="remarks"></a>Comentarios

Este atributo se usa principalmente para realizar un seguimiento del progreso de descarga de un archivo multimedia mientras se realiza el seguimiento simultáneo de la posición de reproducción actual del archivo mediante el **atributo value.** La posición del control deslizante está restringida al área del progreso de primer plano. Esto permite que la búsqueda interactiva solo se lleve a cabo dentro de la parte disponible de un archivo de descarga.

Para usar esta funcionalidad, el **atributo useForegroundProgress** debe establecerse en true.

## <a name="examples"></a>Ejemplos


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.min**](slider-min.md)
</dt> <dt>

[**SLIDER.max**](slider-max.md)
</dt> <dt>

[**SLIDER.useForegroundProgress**](slider-useforegroundprogress.md)
</dt> <dt>

[**SLIDER.value**](slider-value.md)
</dt> </dl>

 

 





